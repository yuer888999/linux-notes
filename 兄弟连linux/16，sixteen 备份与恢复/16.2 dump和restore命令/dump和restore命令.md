# 			1，dump命令

[root@penguin ~]#  dump [选项] 备份之后的文件名 原文件或目录

选项：

​	-level :			就是我们说的0-9十个级别

​	-f文件名：		指定备份之后的文件名

​	-u:					备份成功之后，把备份时间记录在/etc/dumpdates文件

​	-v:					显示备份过程中更多的输出信息

​	-j:					调用bzlibz库压缩备份文件，其实就是备份文件压缩为.bz2格式

​	-w:					显示允许被dump的分区的备份等级及备份时间

# 			备份分区

dump -0uj -f /root/boot.bak.bz /boot

#备份命令。先执行一次完全备份，并压缩和更新备份时间

cat /etc/dumpdates

#先查看备份时间文件

cp install.log /boot/

#复制日志文件到/boot分区

dump -1uj -f /root/boot.bak1.bz2 /boot/

#增量备份/boot分区，并压缩

dump -W

#查询分区的备份时间及备份级别的

# 			备份文件或目录

dump -0j -f /root/etc.dump.bz2 /etc/

#完全备份/etc/目录，只能使用0级别进行完全备份，而不再支持增量备份

# 			2，restore命令

[root@penguin ~]# restore [模式选项] [选项]

模式选项：restore命令常用的模式有以下四种，这四个模式不能混用。

​	-C：	比较备份数据和实际数据的变化

​	-i:		进入交互模式，手工选择需要恢复的文件

​	-t:		查看模式，用于查看备份文件中拥有那些数据。

​	-r:		还原模式，用于数据还原。

选项：

​	-f:		指定备份文件的文件名

# 			比较备份数据和实际数据的变化

mv /boot/vmlinuz-2.6.32-279.el6.i686 /boot/vmlinz-2.6.32-279.el6.i686.bak

\#把/boot目录中内核镜像文件改个名字

restore -C -f /root/boot.bak.bz2

\#restore发现内核镜像文件丢失

# 			查看模式

restore -t -f boot.bak.bz2

# 			还原模式

#还原boot.bak.bz2分区备份

#先还原完全备份的数据

mkdir boot.test

cd boot.test/

restore -r -f /root/boot.bak.bz2

#解压缩

restore -r -f /root/boot.bak1.bz2

#恢复增量备份数据

#还原/etc/目录的备份etc.dump.bz2

restore -r -f etc.dump.bz2

#还原etc.dump.bz2备份