#                                sed命令

:point_right: sed是一种几乎所有UNIX平台（包括Linux）的轻量级编辑器。sed主要是用来将数据进行选取，替换，删除，新增的命令。

### [root@localhost ~]# sed [选项] ‘[动作]’ 文件名

选项：

​     -n :           一般sed命令会把所有数据输出到屏幕，如果加入此选择，则只会把经过sed命令处理的行输出到屏幕。

​     -e :           允许对输入数据应用多条sed命令编辑

​     -i :             用sed的修改结果直接修改读取数据的文件，而不是由屏幕输出

动作：

​     a\:            追加，在当前行后添加一行或多行。添加多行时，除最后一行外，每行末尾需要用 “\” 代表数据末完结

​     c\:             行替换，用c后面的字符串替换原数据行，替换多行，除最后一行外，每行末尾需要用 “\” 代表数据未完结。

​     i\ :             插入，当前行前插入一行或多行。插入多行时，除最后一行外，每行末尾需要用 “\” 代表数据末完结。

​     d:              删除，删除指定的行。

​     p:              打印，输出指定的行。

​     s：            字符替换，用一个字符替换另外一个字符串。格式为“行规围s/旧字符/新字符/g（和vim中的替换格式类似）

###              行数据操作

[root@localhost ~]# sed ‘2p’student,txt

#查看文件的第二行

[root@localhost ~]# sed -n ‘2p’student,txt

---------------------------------------------------------------------------------------------------------------------------------------------------

[root@localhost ~]# sed ‘2,4d’student,txt

#删除第二行到第四行的数据，但不修改文件本身

[root@localhost ~]# sed ‘2a hello’student,txt

#在第二行后追加hello

[root@localhost ~]# sed ‘2i hello \ world’ student,txt

#在第二行前插入两行数据

[root@localhost ~]# sed ‘2c No such person’ student,txt

#数据替换

#####                    字符串替换

[root@localhost ~]# sed ‘s/旧字串/新字串/g’ 文件名

[root@localhost ~]# sed ‘3s/74/99/g’ student,txt

#在第三行中，把74换成99

[root@localhost ~]# sed -i ‘3s/74/99/g’ student,txt

#sed操作的数据直接写入文件

[root@localhost ~]# sed -e ‘sLiming//g;sGao//g’ student,txt

\#同时把“Liming”和“Gao”替换为空

