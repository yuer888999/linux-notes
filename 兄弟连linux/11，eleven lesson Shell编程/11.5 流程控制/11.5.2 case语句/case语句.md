# 多分支case条件语句

:point_right: case语句和if...elif...else语句一样是多分支条件语句，不过和if多分支语句不同的是，case语句只能判断一种关系，而if语句可以判断多种条件关系。

case	$变量名 in	

​	“值1”）

​			如果变量的值等于值1，则执行程序1

​			；；

​	“值2”）

​			如果变量的值等于值2，则执行程序2

 			；；

​	。。。省略其他分支。。。

​	*）

​			如果变量的值都不是以上的值，则执行此程序

​			；；

esac

# 例子

#!/bin/bash

#判断用户输入

\# Author :  shenchao   (E-mail: shenchao@lampbrother.net)

read -p “Please choose yes/no: ” -t 30 cho

case $cho in

​				“yes”)

​							echo “Your choose is yes!”

​							: :

​				“no”)

​							echo “Your choose is no!”

​							: :

​				*)

​							echo “Your choose is error!”

​							: :

esac

