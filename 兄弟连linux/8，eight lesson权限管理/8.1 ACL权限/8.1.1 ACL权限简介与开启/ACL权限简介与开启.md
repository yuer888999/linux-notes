*![1557401517991](C:\Users\laiyuer\AppData\Roaming\Typora\typora-user-images\1557401517991.png)*

# 2，查看分区ACL权限是否开启

[root@localhost ~] # dumpe2fs -h /dev/sda3

#dumpe2fs 命令是查询指定分区详细文件系统信息的命令

详细：

​        -h     仅显示超级块中信息，而不显示磁盘块组的详细信息

# 3，临时开启分区ACL权限

[root@localhost ~]# mount -o remount,acl/

#重新挂载根分区，并挂载加入acl权限

# 4，永久开启分区ACL权限

[root@localhost ~] # vi /etc/fstab

UUID=76cc5d4c-819d-43cb-a8ce-fcc74eac1061 /boot                   xfs     defaults
0 0

#加入acl

[root@localhost ~]# mount -o remount /

#重新挂载文件系统或重启系统，使修改生效