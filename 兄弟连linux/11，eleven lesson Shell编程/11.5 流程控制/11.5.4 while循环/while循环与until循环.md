# 			1，while循环

:point_right: while循环是不定循环，也称作条件循环。只要条件判断式成立，循环就会一直继续，直到条件判断式不成立，循环才会停止。这就和for的固定循环不太一样了。

while	[	条件判断式	]

​	do

​		程序

​	done

# 例子

#!/bin/bash

#从1加到100

\#	Author :  shenchao	( E-mail :  shenchao@lampbrother.net)

i=1

s=0

while [ $i -le 100]

\# 如果变量i的值小于等于100， 则执行循环

​	do

​			s=$(( $s+$i ))

​			i=$(( $i+1 ))

​	done

echo “The sum is: $s”

# 			2，until循环

:point_right: until循环，和while循环相反，until循环时只要条件判断式不成立则进行循环，并执行循环程序。一旦循环条件成立，则终止循环。

until	[	条件判断式	]

​	do

​		程序

​	done

# 例子

#!/bin/bash

#从1加到100

\#	Author :  shenchao	( E-mail :  shenchao@lampbrother.net)

i=1

s=0

until [ $i -le 100]

\# 循环直到变量i的值大于100，就停止循环

​	do

​			s=$(( $s+$i ))

​			i=$(( $i+1 ))

​	done

echo “The sum is: $s”