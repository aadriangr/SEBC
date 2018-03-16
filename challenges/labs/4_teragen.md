I did not use the -Ddfs.replication=1 because the challenge didn't specify it. If i want to benchmark disk i must use it.

```
[hilary@ip-10-0-0-7 centos]$ time /opt/cloudera/parcels/CDH/bin/hadoop jar \
>     /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen \
>     -Ddfs.block.size=67108864 \
> -Dmapreduce.job.maps=16 \
>     -Dmapreduce.map.memory.mb=768 \
>     -Dmapreduce.map.java.opts.max.heap=614 \
>     65536000 tgen
18/03/16 10:57:19 INFO client.RMProxy: Connecting to ResourceManager at ip-10-0-0-33.eu-west-1.compute.internal/10.0.0.33:8032
18/03/16 10:57:19 INFO terasort.TeraGen: Generating 65536000 using 16
18/03/16 10:57:19 INFO mapreduce.JobSubmitter: number of splits:16
18/03/16 10:57:19 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
18/03/16 10:57:20 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1521195459536_0003
18/03/16 10:57:20 INFO impl.YarnClientImpl: Submitted application application_1521195459536_0003
18/03/16 10:57:20 INFO mapreduce.Job: The url to track the job: http://ip-10-0-0-33.eu-west-1.compute.internal:8088/proxy/application_1521195459536_0003/
18/03/16 10:57:20 INFO mapreduce.Job: Running job: job_1521195459536_0003
18/03/16 10:57:26 INFO mapreduce.Job: Job job_1521195459536_0003 running in uber mode : false
18/03/16 10:57:26 INFO mapreduce.Job:  map 0% reduce 0%
18/03/16 10:57:44 INFO mapreduce.Job:  map 21% reduce 0%
18/03/16 10:57:46 INFO mapreduce.Job:  map 28% reduce 0%
18/03/16 10:57:47 INFO mapreduce.Job:  map 33% reduce 0%
18/03/16 10:57:49 INFO mapreduce.Job:  map 35% reduce 0%
18/03/16 10:57:52 INFO mapreduce.Job:  map 40% reduce 0%
18/03/16 10:57:53 INFO mapreduce.Job:  map 44% reduce 0%
18/03/16 10:58:01 INFO mapreduce.Job:  map 50% reduce 0%
18/03/16 10:58:02 INFO mapreduce.Job:  map 56% reduce 0%
18/03/16 10:58:04 INFO mapreduce.Job:  map 63% reduce 0%
18/03/16 10:58:10 INFO mapreduce.Job:  map 67% reduce 0%
18/03/16 10:58:12 INFO mapreduce.Job:  map 77% reduce 0%
18/03/16 10:58:14 INFO mapreduce.Job:  map 79% reduce 0%
18/03/16 10:58:15 INFO mapreduce.Job:  map 85% reduce 0%
18/03/16 10:58:18 INFO mapreduce.Job:  map 95% reduce 0%
18/03/16 10:58:20 INFO mapreduce.Job:  map 98% reduce 0%
18/03/16 10:58:29 INFO mapreduce.Job:  map 100% reduce 0%
18/03/16 10:58:30 INFO mapreduce.Job: Job job_1521195459536_0003 completed successfully
18/03/16 10:58:30 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=2368502
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=1368
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=64
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=32
        Job Counters
                Launched map tasks=16
                Other local map tasks=16
                Total time spent by all maps in occupied slots (ms)=333286
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=333286
                Total vcore-milliseconds taken by all map tasks=333286
                Total megabyte-milliseconds taken by all map tasks=341284864
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=1368
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=2806
                CPU time spent (ms)=150420
                Physical memory (bytes) snapshot=4812210176
                Virtual memory (bytes) snapshot=21631127552
                Total committed heap usage (bytes)=5602017280
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000

real    1m13.482s
user    0m5.657s
sys     0m0.282s
```

```
[hilary@ip-10-0-0-7 centos]$ hdfs dfs -ls /user/hilary/tgen
Found 17 items
-rw-r--r--   3 hilary supergroup          0 2018-03-16 10:58 /user/hilary/tgen/_SUCCESS
-rw-r--r--   3 hilary supergroup  409600000 2018-03-16 10:57 /user/hilary/tgen/part-m-00000
-rw-r--r--   3 hilary supergroup  409600000 2018-03-16 10:57 /user/hilary/tgen/part-m-00001
-rw-r--r--   3 hilary supergroup  409600000 2018-03-16 10:57 /user/hilary/tgen/part-m-00002
-rw-r--r--   3 hilary supergroup  409600000 2018-03-16 10:57 /user/hilary/tgen/part-m-00003
-rw-r--r--   3 hilary supergroup  409600000 2018-03-16 10:57 /user/hilary/tgen/part-m-00004
-rw-r--r--   3 hilary supergroup  409600000 2018-03-16 10:57 /user/hilary/tgen/part-m-00005
-rw-r--r--   3 hilary supergroup  409600000 2018-03-16 10:57 /user/hilary/tgen/part-m-00006
-rw-r--r--   3 hilary supergroup  409600000 2018-03-16 10:57 /user/hilary/tgen/part-m-00007
-rw-r--r--   3 hilary supergroup  409600000 2018-03-16 10:58 /user/hilary/tgen/part-m-00008
-rw-r--r--   3 hilary supergroup  409600000 2018-03-16 10:58 /user/hilary/tgen/part-m-00009
-rw-r--r--   3 hilary supergroup  409600000 2018-03-16 10:58 /user/hilary/tgen/part-m-00010
-rw-r--r--   3 hilary supergroup  409600000 2018-03-16 10:58 /user/hilary/tgen/part-m-00011
-rw-r--r--   3 hilary supergroup  409600000 2018-03-16 10:58 /user/hilary/tgen/part-m-00012
-rw-r--r--   3 hilary supergroup  409600000 2018-03-16 10:58 /user/hilary/tgen/part-m-00013
-rw-r--r--   3 hilary supergroup  409600000 2018-03-16 10:58 /user/hilary/tgen/part-m-00014
-rw-r--r--   3 hilary supergroup  409600000 2018-03-16 10:58 /user/hilary/tgen/part-m-00015
```

```
[hilary@ip-10-0-0-7 centos]$ hadoop fsck -blocks /user/hilary
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-10-0-0-7.eu-west-1.compute.internal:50070/fsck?ugi=hilary&blocks=1&path=%2Fuser%2Fhilary
FSCK started by hilary (auth:SIMPLE) from /10.0.0.7 for path /user/hilary at Fri Mar 16 11:01:38 UTC 2018
..................................Status: HEALTHY
 Total size:    8091893838 B (Total open files size: 3154116608 B)
 Total dirs:    32
 Total files:   34
 Total symlinks:                0 (Files currently being written: 12)
 Total blocks (validated):      151 (avg. block size 53588700 B) (Total open file blocks (not validated): 48)
 Minimally replicated blocks:   151 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Fri Mar 16 11:01:38 UTC 2018 in 21 milliseconds


The filesystem under path '/user/hilary' is HEALTHY
```
