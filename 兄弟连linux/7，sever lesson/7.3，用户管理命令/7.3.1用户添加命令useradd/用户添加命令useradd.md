# 1,useradd命令格式

[root@locathost ~ ]# useradd [选项] 用户名

选项：

​         -u UID ：手工指定用户的UID号

​         -d  家目录：   手工指定用户的家目录

​         -c   用户说明：   手工指定用户的说明

​         -g   组名：    手工指定用户的初始组

​         -G   组名：    指定用户的附加组

​         -s     shell:      手工指定用户的登录shell。默认是/bin/bash

# 2,添加默认用户

:abc:[root@localhost ~]#useradd xiaolai

:point_right:[root@localhost ~]# useradd xiaolai

:point_right:[root@localhost ~]# grep xiaolai /etc/passwd

:point_right:[root@localhost ~]# grep xiaolai /etc/shadow

:point_right:[root@localhost ~]# grep xiaolai /etc/group

:point_right:[root@localhost ~]# grep xiaolai /etc/gshadow

:point_right:[root@localhost ~]# ll -d /home/lamp

:point_right:[root@localhost ~]# ll /var/spool/mail/lamp

# 3,指定选项添加用户

:point_right:useradd -u 666 -G root,bin -d/home/lamp1 -c “text user” -s /bin/bash xiaolai

#  4,用户默认值文件

:abc: /etc/default/useradd

:point_right:GROUNP=100      #用户默认组

:point_right:HOME=/home      #用户家目录

:point_right:INACTIVE = -1        #密码过期宽限天数（shadow文件7字段）

:point_right:EXPIRE =                 #密码失效时间（8）

:point_right:SHELL = /bin/bash     #默认shell

:point_right:SKEL =/etc/skel        #模板目录

:point_right:CREATE _ MALL _ SPOOL = yes       #是否建立邮箱​

:abc: /etc/login.defs

:point_right:PASS_MAX_DAYS 99999​                  #密码有效期（5）

:point_right:PASS_MIN_DAYS 0​                            #密码修改间隔（4） 

:point_right:PASS_NIN_LEN    5                            #密码最小5（PAM）

:point_right:PASS_WARN_AGE 7​                           #密码到期警告（6）

:point_right:UID_MIN​           500                            #最小和最大UID范围

:point_right:GID_MAN         60000​

:point_right:ENCRYPT-METHOD     SHA512​         #加密模式

