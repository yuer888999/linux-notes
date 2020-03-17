# 语法一

for 变量 in 值1 值2 值3 ...

​	do

​		程序

​	done

# 例子1

#!/bin/bash

#打印时间

\# Author :  shenchao	(E-mail :	shenchao@lampbrother.net)

for time in morning noon afternoon evening

​		do

​					echo	“This time is $time!”

​		done

# 例子2

#!/bin/bash

#批量解压缩脚本

\# Author : shenchao	(E-mail :	shenchao@lampbrother.net)

cd /lamp

ls *.tar.gz>ls.log

for i in $(cat ls.log)

​	do

​			tar -zxf $i &>/dev/null

​	done

rm -rf /lamp/ls.log

# 语法二

for(( 初始值；循环控制条件；变量变化 ))

​	do

​		程序

​	done

# 例子

#!/bin/bash

#从1加到100

\# Author : shenchao	(E-mail :	shenchao@lampbrother.net)

s=0

for (( i=1;i<=100;i=i+1 ))

​	do 

​		s=$(( $s+$i))

​	done

echo “The sum of 1+2+...+100 is : $s”

#例子2

#!/bin/bash

#批量添加指定数量的用户

\# Author : shenchao	(E-mail :	shenchao@lampbrother.net)

read -p “Please input user name:” -t 20 num

read -p “Please input the number of users :” -t 30 num

read -p “Please input the password of users:” -t 30 pass

if [ ! -z “$name” -a ! -z “$num” -a ! -z “$pass”]

​	then

​	y=$(echo $num | sed’s/[0-9]//g’)

​		if[ -z “$y”]

​			then

​			for((i=1;i<=$num;i=i+1))

​				do

​					/usr/sbin/useradd$name$i &> /dev/null

​						echo $pass | /usr/bin/passwd --stdin $name$i &> /dev/null

​				done

​	fi

fi