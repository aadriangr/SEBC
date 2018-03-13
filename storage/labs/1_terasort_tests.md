# Create an end-user Linux account named with your GitHub handle
Create linux user
```
[root@ip-10-0-0-148 centos]# useradd jconca
[root@ip-10-0-0-148 centos]# passwd jconca
```

Create HDFS user folder
```
Changing password for user jconca.
New password:
Retype new password:
passwd: all authentication tokens updated successfully.
[centos@ip-10-0-0-148 ~]$ sudo su hdfs
[hdfs@ip-10-0-0-148 centos]$ hdfs dfs -mkdir /user/jconca
[hdfs@ip-10-0-0-148 centos]$ hdfs dfs -chown jconca /user/jconca
```

# Create a 10 GB file using teragen
Teragen
```
[jconca@ip-10-0-0-148 centos]$ time yarn jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen \
> -Ddfs.replication=1 \
> -Dmapreduce.job.maps=4 \
> -Ddfs.blocksize=33554432 \
> 107374180 teragen
18/03/13 12:48:41 INFO client.RMProxy: Connecting to ResourceManager at ip-10-0-0-166.eu-west-1.compute.internal/10.0.0.166:8032
18/03/13 12:48:42 INFO terasort.TeraSort: Generating 107374180 using 4
18/03/13 12:48:42 INFO mapreduce.JobSubmitter: number of splits:4
18/03/13 12:48:42 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1520933211815_0016
18/03/13 12:48:42 INFO impl.YarnClientImpl: Submitted application application_1520933211815_0016
18/03/13 12:48:42 INFO mapreduce.Job: The url to track the job: http://ip-10-0-0-166.eu-west-1.compute.internal:8088/proxy/application_1520933211815_0016/
18/03/13 12:48:42 INFO mapreduce.Job: Running job: job_1520933211815_0016
18/03/13 12:48:47 INFO mapreduce.Job: Job job_1520933211815_0016 running in uber mode : false
18/03/13 12:48:47 INFO mapreduce.Job:  map 0% reduce 0%
18/03/13 12:48:59 INFO mapreduce.Job:  map 13% reduce 0%
18/03/13 12:49:02 INFO mapreduce.Job:  map 22% reduce 0%
18/03/13 12:49:05 INFO mapreduce.Job:  map 31% reduce 0%
18/03/13 12:49:08 INFO mapreduce.Job:  map 41% reduce 0%
18/03/13 12:49:11 INFO mapreduce.Job:  map 50% reduce 0%
18/03/13 12:49:14 INFO mapreduce.Job:  map 60% reduce 0%
18/03/13 12:49:17 INFO mapreduce.Job:  map 69% reduce 0%
18/03/13 12:49:20 INFO mapreduce.Job:  map 79% reduce 0%
18/03/13 12:49:24 INFO mapreduce.Job:  map 87% reduce 0%
18/03/13 12:49:27 INFO mapreduce.Job:  map 90% reduce 0%
18/03/13 12:49:30 INFO mapreduce.Job:  map 93% reduce 0%
18/03/13 12:49:32 INFO mapreduce.Job:  map 94% reduce 0%
18/03/13 12:49:33 INFO mapreduce.Job:  map 95% reduce 0%
18/03/13 12:49:36 INFO mapreduce.Job:  map 98% reduce 0%
18/03/13 12:49:41 INFO mapreduce.Job:  map 99% reduce 0%
18/03/13 12:49:42 INFO mapreduce.Job:  map 100% reduce 0%
18/03/13 12:49:43 INFO mapreduce.Job: Job job_1520933211815_0016 completed successfully
18/03/13 12:49:43 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=494320
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10737418000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=194641
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=194641
                Total vcore-seconds taken by all map tasks=194641
                Total megabyte-seconds taken by all map tasks=199312384
        Map-Reduce Framework
                Map input records=107374180
                Map output records=107374180
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1157
                CPU time spent (ms)=162680
                Physical memory (bytes) snapshot=885784576
                Virtual memory (bytes) snapshot=6282969088
                Total committed heap usage (bytes)=935854080
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=230593858507236407
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10737418000

real    1m4.090s
user    0m5.483s
sys     0m0.286s

```
Terasort
```
[jconca@ip-10-0-0-148 centos]$ time yarn jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort \
> teragen terasort
18/03/13 12:50:36 INFO terasort.TeraSort: starting
18/03/13 12:50:38 INFO input.FileInputFormat: Total input paths to process : 4
Spent 204ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 209ms
Sampling 10 splits of 320
Making 6 from 100000 sampled records
Computing parititions took 684ms
Spent 896ms computing partitions.
18/03/13 12:50:38 INFO client.RMProxy: Connecting to ResourceManager at ip-10-0-0-166.eu-west-1.compute.internal/10.0.0.166:8032
18/03/13 12:50:39 INFO mapreduce.JobSubmitter: number of splits:320
18/03/13 12:50:39 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1520933211815_0017
18/03/13 12:50:39 INFO impl.YarnClientImpl: Submitted application application_1520933211815_0017
18/03/13 12:50:39 INFO mapreduce.Job: The url to track the job: http://ip-10-0-0-166.eu-west-1.compute.internal:8088/proxy/application_1520933211815_0017/
18/03/13 12:50:39 INFO mapreduce.Job: Running job: job_1520933211815_0017
18/03/13 12:50:45 INFO mapreduce.Job: Job job_1520933211815_0017 running in uber mode : false
18/03/13 12:50:45 INFO mapreduce.Job:  map 0% reduce 0%
18/03/13 12:56:31 INFO mapreduce.Job:  map 99% reduce 27%
18/03/13 12:57:29 INFO mapreduce.Job:  map 100% reduce 100%
18/03/13 12:57:30 INFO mapreduce.Job: Job job_1520933211815_0017 completed successfully
18/03/13 12:57:30 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=4784918797
                FILE: Number of bytes written=9488440185
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10737466000
                HDFS: Number of bytes written=10737418000
                HDFS: Number of read operations=978
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Launched map tasks=320
                Launched reduce tasks=6
                Data-local map tasks=200
                Rack-local map tasks=120
                Total time spent by all maps in occupied slots (ms)=3034557
                Total time spent by all reduces in occupied slots (ms)=707517
                Total time spent by all map tasks (ms)=3034557
                Total time spent by all reduce tasks (ms)=707517
                Total vcore-seconds taken by all map tasks=3034557
                Total vcore-seconds taken by all reduce tasks=707517
                Total megabyte-seconds taken by all map tasks=3107386368
                Total megabyte-seconds taken by all reduce tasks=724497408
        Map-Reduce Framework
                Map input records=107374180
                Map output records=107374180
                Map output bytes=10952166360
                Map output materialized bytes=4662755930
                Input split bytes=48000
                Combine input records=0
                Combine output records=0
                Reduce input groups=107374180
                Reduce shuffle bytes=4662755930
                Reduce input records=107374180
                Reduce output records=107374180
                Spilled Records=214748360
                Shuffled Maps =1920
                Failed Shuffles=0
                Merged Map outputs=1920
                GC time elapsed (ms)=35199
                CPU time spent (ms)=1497190
                Physical memory (bytes) snapshot=154427514880
                Virtual memory (bytes) snapshot=513863675904
                Total committed heap usage (bytes)=191040061440
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10737418000
        File Output Format Counters
                Bytes Written=10737418000
18/03/13 12:57:30 INFO terasort.TeraSort: done

real    6m54.580s
user    0m8.538s
sys     0m0.428s

```