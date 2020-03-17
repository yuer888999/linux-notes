# 1，下载NTFS-3G插件

<https://www.tuxera.com/blog/community/open-source-ntfs-3g-download>

# 2，安装NTFS-3G

[root@localhost ~]# tar-zxvf ntfs-3g_ntfsprogs-2013.1.13.tgz

#解压

[root@localhost ~]#  cd ntfs-3_ntfsprogs-2013.1.13

#进入解压目录

[root@localhost ntfs-3_ntfsprogs-2013.1.13]# /confgure

#编译器准备。没有指定安装目录，安装到默认位置中

[root@localhost ntfs-3_ntfsprogs-2013.1.13]# make

#编译

[root@localhost ntfs-3_ntfsprogs-2013.1.13]#make install

#编译安装

# 3，使用

[root@localhost  ~]#mount -t ntfs-3g 分区设备文件名 挂载点

 