# Check vm.swappiness on all your nodes
Modify swappiness for this boot
<code>sudo sysctl -w vm.swappiness=1</code>

Modify swappiness for future boots
<code>sudo vi /etc/sysctl.conf</code>
<code>  vm.swappiness=1</code>
![Swappiness](../png/swappiness.png)

# Show the mount attributes of your volume(s)
I create a couple of volumes extra for my datanades to store hdfs data.
10.0.0.148 is going to be my edge node, so it has only one partition
![Mount Points](../png/mount_points.png)

# If you have ext-based volumes, list the reserve space setting
<code>sudo tune2fs -m 0 /dev/xvdb1</code>
<code>sudo tune2fs -l /dev/xvdb1 | grep 'Reserved block count'</code>
![File System Reserved](../png/file_system_reserved.png)

