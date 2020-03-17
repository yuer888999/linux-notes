# 1，修改用户信息usermod

[root@localhost ~]#usermod [选项] 用户名

选项：

​        -u    UID：              修改用户的UID号

​        -c     用户说明：     修改用户的说明信息

​        -G    组名:                修改用户的附加组

​        -L :                            临时锁定用户（Lock)

​        -U :                            解锁用户锁定（Unlock）

:point_right:[root@localhost ~]# usermod -c “test user” lion  #修改用户的说明

:point_right:[root@localhost ~]# usermod -G root lion  #把lion用户加入root组

:point_right:[root@localhost ~]# usermod -L lion  #锁定用户

:point_right:[root@localhost ~]# usermod -U lion  #解锁用户

# 2,修改用户密码状态chage

[root@localhost ~]#chage [选项] 用户名

选项：

​       -l :                    列出用户的详细密码状态

​       -d 日期：        修改密码最后一次更改日期（shadow3字段）

​       -m 天数 ：      两次密码修改间隔（4字段）

​       -M 天数：       密码有效期（5字段）

​       -W 天数 ：      密码过期前警告天数（6字段）

​       -I   天数：        密码过后宽限天数（7字段）

​       -E  日期：         账号失效时间（8字段）

:point_right:[root@localhost ~]# chage -d lion

#这个命令其实是把密码修改日期归0了（shadow第3字段)

#这样用户一登陆就要修改密码