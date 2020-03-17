# 光盘yum源搭建步骤

1）挂载光盘

[root@localhost  ~]# mount /dev/sr0 /mnt/cdrom

2）让网络yum源文件失效

[root@localhost  ~]# cd /etc/yum.repos.d/

[root@localhost  yum.repos.d]#mv CentOS-Base.repos.d \ CentOS-Base.repo.bak

[root@localhost  yum.repos.d]#mv CentOS-Debuginfo.repo \ CentOS-Debuginfo.repo.bak

[root@localhost  yum.repos.d]#mv CentOS-Vault.repo \ CentOS-Vault.repo.bak

3）修改光盘yum源文件

[root@localhost  yum.repos.d]#vim CentOS-Media.repo

[c6-media]

name=CentOS-$releasever - Media

baseurl=file:///mnt/cdrom

#地址为你自己的光盘挂载地址

\#		file:///media/cdrom

\#		file:///media/cdrecorder

\#注释这恋歌不存在的地址

gpgcheck=1

enabled=1

\#把enabled=0改为enable=1,让这个yum源配置文件生效

gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6

# 2，yum软件组管理命令

[root@localhost  ~]# yum grouplist

#列出所有可用的软件组列表

[root@localhost  ~]# yum groupinstall 软件组名

#安装指定软件组，组名可用由grouplist查询出来

[root@localhost  ~]# yum groupremove 软件组名

#卸载指定软件组