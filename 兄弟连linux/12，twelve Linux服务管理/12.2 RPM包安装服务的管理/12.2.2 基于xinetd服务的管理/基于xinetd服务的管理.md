# 			1，安装xinetd与telnet

[root@penguin ~]# yum -y install xinetd

[root@penguin ~]# yum -y install telnet-server

# 			2，xinetd服务的启动

[root@penguin ~]# vi /etc/xinetd.d/telnet

service telnet									<--服务的名称为telnet

{

​	flags			REUSE						<--标志为REUSE，设定TCP/IP socket可重用

​	socket_type		=stream			<--使用TCP协议数据包

​	wait			=no							<--允许多个连接同时连接

​	user			=root						<--启动服务的用户为root

​	server		=/usr/sbin/in.telnetd			<--服务的启动程序

​	log_on failure +=USERID						<--登入失败后，记录用户的ID

​	disable		=no										<--服务不启动

}

##### 重启xinetd服务

[root@penguin ~]# service xinetd restart

# 			3，xinetd服务的自启动

[root@penguin ~]# chkconfig telnet on

ntsysv	==-->redhat专有==

