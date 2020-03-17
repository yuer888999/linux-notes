# 1，sudo权限

:point_right: root 把本来只能超级用户执行的命令赋予普通用户执行。

:point_right: sudo 的操作对象是系统命令

# 2，sudo使用

[root@localhost ~] # visudo

#实际修改的是/etc/sudoers文件

root     ALL=(ALL)     ALL

#用户名 被管理主机的地址 =  （可使用的身份）   授权命令（绝对路径）

\# %wheel     ALL=(ALL)     ALL

#%组名   被管理主机的地址=（可使用的身份）   授权命令（绝对路径）

# 3，授权sc用户可以重启服务器

[root@localhost ~] # visudo

sc   ALL=/sbin/shutdown -r now