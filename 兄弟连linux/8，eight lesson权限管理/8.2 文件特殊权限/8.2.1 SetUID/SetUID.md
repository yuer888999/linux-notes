# 1，SetUID的功能

:point_right:只有可以执行的二进制程序才能设定SUID权限

:point_right:命令执行者要对该程序拥有X（执行）权限

:point_right:命令执行者在执行该程序时获得该程序文件属主的身份（在执行程序的过程中灵魂附体为文件的属主）

:point_right:SetUID权限只在该程序执行过程中有效，也就是说身份改变只在程序执行过程中有效

:point_right:passwd命令拥有SetUID权限，所有普通可以修改自己的密码

[root@localhost ~]# ll /usr/bin/passwd

-rw==s==r-xr-x. 1 root root 25980 2月 22 2012 /usr/bin/passwd

:point_right:cat命令没有SetUID权限，所有普通用户不能查看/etr/shadow文件

[root@localhost ~]# ll /bin/cat

-rwxr-xr-x 1 root root 47976 6月 22 2012 /bin/cat

*![1557748149786](C:\Users\laiyuer\AppData\Roaming\Typora\typora-user-images\1557748149786.png)*

# 2，设定SetUID的方法

:point_right: 4代表SUID

​    :arrow_forward: chmod 4755文件名

​    :arrow_forward: chmod u+s 文件名

# 3，取消SetUID的方法

   :arrow_forward: 755 文件名

   :arrow_forward: chmod u-s 文件名

# 4，危险的SetUID

:point_right: 关键目录应严格控制写权限。比如 ”/“ ， ”/usr“ 等

:point_right: 用户的密码设置要严格遵守密码三原则

:point_right: 对系统中默认应该具有SetUID权限的文件作一列表，定时检查有没有这之外的文件被设置了SetUID权限

   

