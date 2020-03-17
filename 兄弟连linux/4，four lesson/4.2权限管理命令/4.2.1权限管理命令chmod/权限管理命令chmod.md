# 权限管理命令：chmod

### 命令名称：chmod

### 命令英文原意：==ch==ange the permissions ==mod==e of a file

### 命令所在路径：/bin/chmod

### 执行权限：所有用户

### 语法：chmod [{ugoa}{+-=}{rwx}] [文件或目录] [mode=421] [文件或目录] -R 递归修改

### 功能描述：改变文件或目录权限

### 权限的数字表示   r ---- 4   w ---- 2    x ---- 1

### rwxrw-r--      

###  7   6   4

范例： $ chmod g+w testfile

​             赋予文件testfile所属组写权限

​             $ chmod -R 777 testfile

​             修改目录testfile及其目录下文件为所有用户具有全部权限

# <center>文件目录权限总结</center>

| 代表字符 |   权限   |               对文件的含义               |                    对目录的含义                    |
| :------: | :------: | :--------------------------------------: | :------------------------------------------------: |
|    r     |  读权限  | 可以查看文件内容 cat/more/head/tail/less |             可以列出目录中的内容    ls             |
|    w     |  写权限  |        可以修改文件内容   vi/vim         | 可以在目录中创建，删除文件    touch/mkdir/rmdir/rm |
|    x     | 执行权限 |       可以执行文件  script/command       |                 可以进入目录   cd                  |

