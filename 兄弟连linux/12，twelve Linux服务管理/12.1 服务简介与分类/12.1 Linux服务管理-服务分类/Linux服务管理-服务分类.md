# 			1，服务的分类

*![1566983058493](C:\Users\laiyuer\AppData\Roaming\Typora\typora-user-images\1566983058493.png)*

# 			启动与自启动

:point_right: 服务启动：就是在当前系统中让服务运行，并提供功能。

:point_right: 服务自启动：自启动是指服务在系统开机或重启动之后，随着系统的启动而自动启动服务。

# 			查询已安装的服务

:point_right: RPM包安装的服务

​	:point_right: chkconfig --list

​	#查看服务自启动状态，可以看到所有RPM包安装的服务

:point_right: 源码包安装的服务

​	:point_right: 查看服务安装位置，一般是/usr/local/下

##### 		RPM安装服务和源码包安装服务的区别

:point_right: RPM安装服务和源码包安装服务的区别就是安装位置的不同

​	:point_right: 源码包安装在指定位置，一般是/usr/local/

​	:point_right: RPM包安装在默认位置中

