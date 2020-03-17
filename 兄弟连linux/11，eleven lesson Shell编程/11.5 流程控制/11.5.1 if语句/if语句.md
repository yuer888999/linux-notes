# 1，单分支if条件语句

if [ 条件判断式 ]；then

程序

fi

==或者==

if [ 条件判断式 ]

​	then

​		程序

fi

# 单分支条件语句需要注意几个点

:point_right: if语句使用fi结尾，和一般语言使用大括号结尾不同

:point_right: [ 条件判断式 ]就是使用test命令判断，使用中括号和条件判断式之间必须有空格

:point_right: then后面跟符合条件之后执行的程序，可以放在[]之后，用 ” ；“分割。也可以换行写入，就不需要 ”；“ 了

# 例子：判断分区使用率

#!/bin/bash

#统计根分区使用率

\# Author :  shengchao   (E-mail: shengchao@lampbrother.net)

rate=$(df -h | grep “/dev/sda3” | awk ‘{print $5}” | cut -d  ‘“%”  -f1’)

#把根分区使用率作为变量赋予变量rate

if [ $rate -ge 80 ]

​	then 

​			echo “Warning! /dev/sda3 is full”

​	fi

# 2，双分支if条件语句

if	[ 条件判断式 ]

​	then

​			条件成立时，执行的程序

​	else

​			条件不成立，执行的另一个程序

fi

# 例子1：备份mysql数据库

#!/bin/bash

#备份mysql数据库

\# Author :  shenchao  (E-mail :  shenchao@lampbrother.net)

ntpdate asia.pool.ntp.org &> /dev/null

#同步系统时间

date=$(date +%y%m%d)

#把当前系统时间按照 “年月日” 格式赋予变量date

size=$(du -sh /var/lib/mysql)

#统计mysql数据库的大小，并把大小赋予size变量

*![1566906783340](C:\Users\laiyuer\AppData\Roaming\Typora\typora-user-images\1566906783340.png)*

# 例子2：判断apache是否启动

*![1566907271250](C:\Users\laiyuer\AppData\Roaming\Typora\typora-user-images\1566907271250.png)*

# 3，多分支if条件语句

if	[	条件判断式1	]

​	then

​			当条件判断式1成立时，执行程序1

​	elif	[	条件判断式2	]

​		then

​			当条件判断式2成立，执行程序2

。。。省略更多条件

else

​		当所有条件都不成立时，最后执行此程序

fi

# 例子

#!/bin/bash

#判断用户输入的是什么文件

\# Author :  shengchao   (E-mail: shengchao@lampbrother.net)

read -d “Please input a filename: ”file

#接收键盘的输入，并赋予变量file

if	[	-z  “$file”	]

#判断file变量是否为空

​	then

​			echo “Error,please input a filename”

​			exit 1

elif	[	! -e “$file”	]

\# 判断file的值是否存在

​	then

​			echo “Your input is not a file!”

​			exit 2

elif	[	-f “$file”	]

\# 判断file的值是否为普通文件

​	then

​			echo “$file is a regulare file!”

  elif	[	-d “$file”	]

\# 判断file的值是否为目录文件

​	then

​			echo “$file is a directory!”

​	else

​			echo “$file is a other file!”

fi

  