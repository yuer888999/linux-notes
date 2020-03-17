# 1，查看ACL命令

[root@localhost ~]# getfacle 文件名

#查看ACL权限

# 2，设定ACL权限的命令

[root@localhost ~]# setfacl  选项 文件名

选项：

​       -m       设定ACL权限

​       -x         删除指定的ACL权限

​       -b         删除所有的ACL权限

​       -d         设定默认ACL权限

​       -k          删除默认ACL权限

​       -R         递归设定ACL权限

# 3，给用户设定ACL权限

*![1557496684514](C:\Users\laiyuer\AppData\Roaming\Typora\typora-user-images\1557496684514.png)*

[root@localhost ~]# useradd spectator

[root@localhost ~]# useradd duck

[root@localhost ~]# useradd chick

[root@localhost ~]# groupadd spectator

[root@localhost ~]# mkdir /project

[root@localhost ~]# chown root:spectator /project

[root@localhost ~]# chmod 770 /project

[root@localhost ~]# setfacl -m u:spectator:rx /project

#给用户spectator赋予r-x权限，使用 ”u:用户名:权限“ 格式

# 4，给用户组设定ACL权限

[root@localhost /]# groupadd spectator

[root@localhost /]#  setfacl -m g:spectator:rx project

#为组spectator分配ACL权限。使用 “g：组名：权限” 格式