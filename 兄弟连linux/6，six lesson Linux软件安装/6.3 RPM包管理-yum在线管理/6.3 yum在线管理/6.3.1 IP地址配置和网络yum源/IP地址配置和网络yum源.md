# 1，IP地址配置

[root@localhost ~]# setup

#使用setup工具

[root@localhost ~]#vi /etc/sysconfig/network-scripts/ifcfg-eth0

把ONBOOT=“no”改为ONBOOT=“yes”

#启动网卡

[root@localhost ~]#service network restart

#重启网络服务

# 2，网络yum源

[root@localhost yum.repos.d]# vi /etc/yum.repos.d/CentOS-Base.repo

:point_right:[base]					容器名称，一定要发在[]中

:point_right:name					容器说明，可以自己随便写

:point_right:mirrorlist				镜像站点，这个可以注稀掉

:point_right:baseurl					我们的yum源服务器地址。默认是CentOS官方的yum源服务器，是可以使用的，如果你觉得慢可以改成你喜欢的yum源地址

:point_right:enabled				此容器是否生效，如果不写或写成enable=1都是生效，写成enable=0就不生效

:point_right:gpgcheck				如果是1是指RPM的数字证书生效，如果是0则不生效

:point_right:gpgkey					数字证书的公钥文件保存位置。不用修改

