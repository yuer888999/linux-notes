# 1，递归ACL权限

:point_right:递归是父目录在设定ACL权限时，所有的子文件和子目录也会拥有相同的ACL权限

:point_right:setfacl -m u:用户名：权限 -R 文件名

# 2，默认ACL权限

:point_right:默认ACL权限的作用是如果给父目录设定了默认ACL权限，那么父目录中所有新建的子文件都会继承父目录的ACL权限

:point_right:setfacl -m d:u:用户名：权限文件名

