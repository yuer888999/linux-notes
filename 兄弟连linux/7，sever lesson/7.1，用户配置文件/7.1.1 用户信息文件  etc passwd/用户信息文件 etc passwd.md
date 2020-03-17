# 1，用户管理界面

:point_right:所以越是对服务器安全性要求高的服务器，越需要建立合理的用户权限等级制度和服务器操作规范。

:point_right:在Linux中主要是通过用户配置文件来查看和修改用户信息

#  2，/etc/passwd

:aquarius::第1字段：用户名称

:aquarius::第2字段：密码标志

:aquarius::第3字段：UID（用户ID）

:point_right:0:                    超级用户

:point_right:1-499:             系统用户（伪用户）

:point_right: 500-65535:    普通用户

:aquarius:第四字段：GID（用户初始组ID)

:aquarius:第五字段：用户说明

:aquarius:第六字段：家目录

:point_right:普通用户：/home/用户名/

:point_right:超级用户：/root/

:aquarius:第七字段：登入之后的Shell

# 3,初始组和附加组

:point_right:初始组：就是用户一登录就立刻拥有这个用户组的相关权限，每个用户的初始组只能有一个，一般就是和这个用户的用户名相同的组名作为这个用户的初始组

:point_right:附加组：指用户可以加入多个其它的用户组，并拥有这些组的权限，附加组可以有多个。

# 4，Shell是什么

:point_right:Shell就是Linux的命令解释器

:point_right:在/etc/passwd当中，除了标准Shell是/bin/bash之外，还可以写如/sbin/nologin。

