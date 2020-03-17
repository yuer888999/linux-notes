# 1，删除用户userdel

[root@localhost ~]# userdel [-r] 用户名

选项：

​        -r       删除用户的同时删除用户家目录

## 手工删除用户

:point_right:[root@localhost ~]# vi /etc/passwd

:point_right:[root@localhost ~]# vi /etc/shadow

:point_right:[root@localhost ~]# vi /etc/group

:point_right:[root@localhost ~]# vi /etc/gshadow

:point_right:[root@localhost ~]# rm -rf /var/spool/mail/lion

:point_right:[root@localhost ~]# rm -rf /home/lion

# 2,查看用户ID

[root@localhost ~]# id 用户名

# 3，切换用户身份su

[root@localhost ~]# su [选项] 用户名

选项：

​         - ：         选项只使用 “-” 代表连带用户的环境变量一起切换

​         -c 命令： 仅执行一次命令，而不切换用户身份 

:point_right:[lion@localhost ~]$ su - root    

  #切换成root

:point_right:[lion@localhost ~]$ su -root -c “useradd user3”   

#不切换成root，但是执行useradd命令添加user1用户

