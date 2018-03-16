Cloud provider: AWS

Instances IPs
```
54.246.244.232   ip-10-0-0-7.eu-west-1.compute.internal
52.208.110.143   ip-10-0-0-33.eu-west-1.compute.internal
34.245.118.219   ip-10-0-0-51.eu-west-1.compute.internal
34.245.162.29    ip-10-0-0-77.eu-west-1.compute.internal
34.242.245.121   ip-10-0-0-212.eu-west-1.compute.internal
```
OS: Centos 7.4

First node file system capacity: 50GB
```
[centos@ip-10-0-0-7 ~]$ df -h
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
[centos@ip-10-0-0-7 ~]$ yum repolist enabled
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