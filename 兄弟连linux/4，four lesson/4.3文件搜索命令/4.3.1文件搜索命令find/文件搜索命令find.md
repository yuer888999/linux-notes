#  文件搜索命令：find

### 命令名称：find

### 命令所在路径：/bin/find

### 执行权限：所有用户

### 语法：find [搜索范围] [匹配条件]

### 功能描述：文件搜索

$ find /etc -name init

在目录/etc中查找文件init

==-iname不区分大小写==

$ find / -size +204800

在根目录下查找大于100MB的文件

+n 对于  -n小于  n等于

$ find /home -user laiyuer 

在根目录下查找所有者为laiyuer的文件

-group根据所属组查找

$ find /etc -cmim -5

在/etc下查找5分钟内被修改过属性的文件和目录

==-amin 访问时间 access==

==-cmin 文件属性 change==

==-mmin 文件内容 modify==

$ find /etc -size +163840 -a -size -204800

在/etc下查找大于80MB小于100MB的文件

-a 两个条件同时满足

-o 两个条件满足任意一个即可

$ find /etc -name inittab -exec ls -l {}\;

在/etc下查找inittab文件并显示其详细信息

-exec/-ok 命令{}\;对搜索结果执行操作

-type 根据文件类型查找

​    f 文件   d 目录   l软连接文件

-inum 根据 i 节点查找

