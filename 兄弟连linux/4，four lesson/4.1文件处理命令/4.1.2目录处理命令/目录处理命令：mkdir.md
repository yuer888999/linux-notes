# 目录处理命令：mkdir

### 命令名称：mkdir

### 命令英文原意：make directories

### 命令所在路径：/bin/mkdir

### 执行权限：所有用户

### 语法：mkdir -p 【目录名】

### 功能描述：创建新目录

### -p   递归创建

##### 范例：$mkdir -p /tmp/xiaolai/yuer/xiaolainiu

# 目录处理命令：cd

### 命令名称：cd

### 命令英文原意：change directory

### 命令所在路径：shell内置命令

### 执行权限：所有用户

### 语法：cd【目录】

### 功能描述：切换目录

##### 示范：$cd /tmp/xiaolai/yuer/xiaolainiu  切换到指定目录

##### $cd ..             回到上一级目录

# 目录处理命令：pwd

### 命令名称：pwd

### 命令英文原意：print working directory

### 命令所在路径：/bin/pwd

### 执行权限：所有用户

### 语法：pwd 

### 功能描述：显示当前目录

### 范例：$pwd

# 文件处理命令：rmdir

### 命令名称：rmdir

### 命令英文原意：remove empty directories

### 命令所在路径：/bin/rmdir

### 执行权限：所有用户

### 语法：rmdir【目录名】

##### 范例：$rmdir/tmp/xiaolai/yuer

# 目录处理命令：cp

### 命令名称：cp

### 命令英文原意：copy

### 命令所在路径：/bin/cp

### 执行权限：所有用户              

### 语法：cp -rp 【原文件或目录】【目标目录】

### -r     复制目录 

### -p    保留文件属性

### 功能描述：复制文件或目录   可以改名

范例：$ cp -r /tmp/xiaolai/yuer /root

​           将目录/tmp/xiaolai/yuer复制到目录/root下

​          $ cp -rp /tmp/xiaolai/yuer /tmp/xiaolai/xiaolainiu /root下

​           将/tmp/xiaolai目录下的yuer和xiaolainiu目录复制到/root下，保     留目录属性

# 目录处理命令：mv

### 命令名称：mv

### 命令英文原意：move

### 命令所在路径：/bin/mv

### 执行权限：所有用户

### 语法：mv【原文件或目录】【目标目录】

### 功能描述：剪切文件，改名

# 目录处理命令：rm

### 命令名称：rm

### 命令英文原意：remove

### 命令所在路径：/bin/rm

### 执行权限：所有用户

### 语法：rm -rf【文件或目录】

### -r   删除目录

### -f   强制执行

### 功能描述：删除文件

范例：$ rm /tmp/yum.log

​            删除文件/tmp/yum.log

​            $ rm -rf /tmp/xiaolai/yuer

​            删除目录 /tmp/xiaolai/yuer