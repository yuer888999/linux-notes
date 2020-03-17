# 1，最大有效权限mask

:point_right:mask是用来指定最大有效权限的。如果我给用户赋予了ACL权限，是需要和mask的权限“相与”才能得到用户的正在权限

# 修改最大有效权限

[root@localhost /]#setfacl -m m:rx 文件名

#设定mask权限为r-x。使用“m:权限”格式

# 2，删除ACL权限

[root@localhost /]# setfacl -x u:用户名 文件名

#删除指定用户的ACL权限

[root@localhost /]# setfacl -x g:组名  文件名

#删除指定用户组的ACL权限

[root@localhost /]# setfacl -b 文件名

#会删除文件的所有的ACL权限

