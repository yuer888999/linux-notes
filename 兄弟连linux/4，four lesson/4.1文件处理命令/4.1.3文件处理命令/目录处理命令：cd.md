

# 文件处理命令：touch

### 命令名称：touch

### 命令英文原意：touch

### 命令所在路径：/bin/touch

### 执行权限：所有用户

### 语法：touch[文件名]

### 功能描述：创建空文件

范例：$ touch laiyuer.list

# 文件处理命令：cat

### 命令名称：cat

### 命令所在路径：/bin/cat

### 执行权限：所有用户

### 语法：cat[文件名]

### 功能描述：显示文件内容

### -n   显示行号

范例：$ cat /etc/issue

​            $ cat -n/etc/services

# 文件处理命令：tac

### 命令名称：tac

### 命令所在路径：usr/bin/tac

### 执行权限：所有用户

### 语法：tac[文件名]

### 功能描述：显示文件内容(反向列示)

范例：$ tac /etc/issue

# 文件处理命令：more

### 命令名称：more

### 命令所在路径：/bin/more

### 执行权限：所有用户

### 语法：more[文件名]

### （ 空格）或f       翻页

### （Enter）换行

### q或Q 退出

### 功能描述：分页显示文件内容

范例：$ more /etc/services

# 文件处理命令：less

### 命令名称：less

### 命令所在路径：usr/bin/less

### 执行权限：所有用户

### 语法：less[文件名]

### 功能描述：分页显示文件内容（可向上翻页）

范例：$ less /etc/issue

按 /+搜索词      按n可以往下翻

# 文件处理命令：head

### 命令名称：head

### 命令所在路径：usr/bin/head

### 执行权限：所有用户

### 语法：head[文件名]

### 功能描述：显示文件前面几行

### -n  指定行数

范例：$ head -n 20 /etc/services

# 文件处理命令：tail

### 命令名称：tail

### 命令所在路径：usr/bin/tail

### 执行权限：所有用户

### 语法：tail[文件名]

### 功能描述：显示文件后面几行

### -n  指定行数

### -f   动态显示文件末尾内容

范例：$ tail -n 20 /etc/services

