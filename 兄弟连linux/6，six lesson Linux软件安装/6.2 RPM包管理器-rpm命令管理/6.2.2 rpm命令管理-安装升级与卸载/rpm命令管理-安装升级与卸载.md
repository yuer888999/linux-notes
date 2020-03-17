# 1，包全名与包名

:point_right:包全名：操作的包是没有安装的软件包时，使用包全名。而且要注意路径

:point_right:包名：操作已经安装的软件包时，使用包名。是搜索/var/lib/rpm/中的数据库

# 2，RPM安装

rpm -ivh 包名

选项：

​		-i（install）					安装

​		-v（verbose)					显示详细信息

​		-h（hash)						显示进度

​		--nodeps						不检测依赖性

# 3，RPM包升级

rpm -Uvh			包全名

选项：

​		-U（upgrade)			升级

# 4，卸载

rpm -e 包名

选项：

​		-e（erase）					卸载

​		--nodeps						不检查依赖性