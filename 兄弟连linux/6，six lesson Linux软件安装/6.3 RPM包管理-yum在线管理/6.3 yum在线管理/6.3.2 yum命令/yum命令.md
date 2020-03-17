# 1，常用yum命令

### 1）查询

[root@localhost yum.repos.d]# yum list

#查询所有可用软件包列表

[root@localhost yum.repos.d]# yum search 关键字

#搜索服务器上所有和关键字相关的包

### 2）安装[root@localhost yum.repos.d]# yum -y install 包名

选项：

​		install					安装

​		-y							自动回答yes

### 3）升级

[root@localhost yum.repos.d]# yum -y update包名

选项：

​		update			升级

​		-y					自动回答yes

### 4）卸载

[root@localhost yum.repos.d]# yum -y remove 包名

选项：

​		remove			卸载

​		-y						自动回答yes

# 2，yum软件组管理命令

[root@localhost  ~]# yum grouplist

#列出所有可用的软件组列表

[root@localhost  ~]# yum groupinstall 软件组名

#安装指定软件组，组名可用由grouplist查询出来

[root@localhost  ~]# yum groupremove 软件组名

#卸载指定软件组