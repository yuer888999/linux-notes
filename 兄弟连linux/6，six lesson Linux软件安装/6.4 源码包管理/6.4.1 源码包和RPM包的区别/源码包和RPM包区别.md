# 1，区别

:point_right:安装之前的区别：概念上的区别

:point_right:安装之后的区别：安装位置不同

# 2，RPM包安装位置

:point_right:是安装在默认位置中

| RPM包默认安装路径 | RPM包默认安装路径          |
| :---------------- | :------------------------- |
| /etc/             | 配置文件安装目录           |
| /usr/bin/         | 可执行的命令安装目录       |
| /usr/lib/         | 程序所使用的函数库保存位置 |
| /usr/share/doc/   | 基本的软件使用手册保存位置 |
| /usr/share/dman/  | 帮助文件保存位置           |

# 3，源码包安装位置

:point_right:安装在指定位置当中，一般是 /usr/local/软件名/

# 4，安装位置不同带来的影响

:point_right:RPM包安装的服务可以使用系统服务管理命令（service）来管理，例如RPM包安装的apache的启动方法是：

:point_right:/etc/rc.d/init.d/httpd start

:point_right:service httpd start

:point_right:而源码包安装的服务则不能被服务管理命令管理，因为没有安装到默认路径中。所以只能用绝对路径进行服务的管理，如：

:point_right:/usr/local/apach2/bin/apachectl start

==网页保存位置==   var/www/html