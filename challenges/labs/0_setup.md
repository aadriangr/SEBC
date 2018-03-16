Cloud provider: AWS

Instances IPs
```
ec2-34-251-104-209.eu-west-1.compute.amazonaws.com 34.251.104.209 ip-10-0-0-45.eu-west-1.compute.internal 10.0.0.45
ec2-34-244-106-222.eu-west-1.compute.amazonaws.com 34.244.106.222 ip-10-0-0-100.eu-west-1.compute.internal 10.0.0.100
ec2-34-244-137-79.eu-west-1.compute.amazonaws.com 34.244.137.79 ip-10-0-0-140.eu-west-1.compute.internal 10.0.0.140
ec2-34-245-231-141.eu-west-1.compute.amazonaws.com 34.245.231.141 ip-10-0-0-236.eu-west-1.compute.internal  10.0.0.236
ec2-34-244-83-63.eu-west-1.compute.amazonaws.com 34.244.83.63 ip-10-0-0-246.eu-west-1.compute.internal 10.0.0.246
```
OS: Centos 7.4

First node file system capacity: 50GB
```
[centos@ip-10-0-0-45 ~]$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       50G  2.2G   48G   5% /
devtmpfs        7.8G     0  7.8G   0% /dev
tmpfs           7.8G     0  7.8G   0% /dev/shm
tmpfs           7.8G   17M  7.8G   1% /run
tmpfs           7.8G     0  7.8G   0% /sys/fs/cgroup
tmpfs           1.6G     0  1.6G   0% /run/user/1000
```

Yum repositories
```
[centos@ip-10-0-0-45 ~]$ yum repolist enabled
Loaded plugins: fastestmirror
Determining fastest mirrors
 * base: ftp.heanet.ie
 * extras: mirrors.coreix.net
 * updates: mirrors.coreix.net
repo id                                          repo name                                          status
!base/7/x86_64                                   CentOS-7 - Base                                    9,591
!extras/7/x86_64                                 CentOS-7 - Extras                                    436
!updates/7/x86_64                                CentOS-7 - Updates                                 2,407
repolist: 12,434
```

/etc/passwd
```
hilary:x:2800:2800::/home/hilary:/bin/bash
anupam:x:2900:2900::/home/anupam:/bin/bash
```

/etc/group
```
analytics:x:1001:hilary
datasci:x:1002:anupam
hilary:x:2800:
anupam:x:2900:
```