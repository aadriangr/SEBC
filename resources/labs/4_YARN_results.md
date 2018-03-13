I test first with small data 1GB

My cluster has 9 cores for YARN, terasort is not memory intensive so i don't change its value.
The worst times are 
<li>with few mappers for teragen and few reducers for terasort. Cluster mostly stale
<li>with a lot of mappers and a lot of reducers. With small data the overhead for more task has a great impact

```
Testing loop started on Tue Mar 13 16:10:00 UTC 2018
Mappers 8 Reducers 4 Memory 512

real    0m22.788s
user    0m5.265s
sys     0m0.291s

real    0m38.570s
user    0m7.322s
sys     0m0.317s
Deleted tg-10GB-8-4-512
Deleted ts-10GB-8-4-512

Mappers 16 Reducers 16 Memory 512

real    0m30.847s
user    0m5.272s
sys     0m0.281s

real    0m56.660s
user    0m8.306s
sys     0m0.365s
Deleted tg-10GB-16-16-512
Deleted ts-10GB-16-16-512
Testing loop ended on Tue Mar 13 16:21:20 UTC 2018
```

Then I generate 10GB datasets and test with 8-16 mappers and 4-8 resources. With more data the task overhead has not so impact. Nevermind times are comparable.
```
Testing loop started on Tue Mar 13 16:34:40 UTC 2018
Mappers 8 Reducers 4 Memory 512

real    2m0.717s
user    0m5.725s
sys     0m0.332s

real    3m27.737s
user    0m8.412s
sys     0m0.384s
Deleted tg-10GB-8-4-512
Deleted ts-10GB-8-4-512
Mappers 16 Reducers 8 Memory 512

real    1m59.311s
user    0m5.607s
sys     0m0.270s

real    3m20.394s
user    0m7.928s
sys     0m0.356s
Deleted tg-10GB-16-8-512
Deleted ts-10GB-16-8-512
Testing loop ended on Tue Mar 13 16:56:26 UTC 2018
```
