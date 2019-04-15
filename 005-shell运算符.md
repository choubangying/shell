## shell运算符

### 一。算数运算符

常用算数运算符：

| 运算符 | 说明 | 举例             |
| ------ | ---- | ---------------- |
| +      | 加法 | `expr $a + $b`   |
| -      | 减法 | `expr $a - $b`   |
| *      | 乘法 | `expr $a \* $b ` |
| /      | 除法 | `expr $a / $b`   |
| %      | 取余 | `expr $a % $b`   |
| =      | 赋值 | a=$b             |

bash本身不支持算数运算需借助其它命令来实现，如expr

运算符和操作数之间要加空格，$a+$b是错误的，需写成$a + $b

示例：

```shell
#! /bin/bash

a=10
b=100

echo `expr $a + $b`
echo `expr $a - $b`
echo `expr $a \* $b`
echo `expr $a / $b`
echo `expr $a % $b`

a=$b
echo "$a"
```

输出：

```shell
110
-90
1000
0
10
100
```



### 二。逻辑运算符

逻辑运算符只支持数字，不支持字符串，除非字符串的值是数字。

shell常用逻辑运算符：

| 运算符 | 说明                                                  | 举例                                |
| ------ | ----------------------------------------------------- | ----------------------------------- |
| ==     | 相等。用于比较两个数字，相同则返回 true。             | [ $a == $b ]，相等返回true          |
| !=     | 不相等。用于比较两个数字，不相同则返回 true。         | [ $a != $b ]，不相等返回true        |
| -eq    | 检测两个数是否相等，相等返回 true。                   | [ $a -eq $b ]，相等返回true         |
| -nq    | 检测两个数是否不相等，不相等返回true。                | [ $a -nq $b ]，不相等返回true       |
| -gt    | 检测左边的数是否大于右边的，如果是，则返回 true。     | [ $a -gt $b ]，左大于右返回true     |
| -lt    | 检测左边的数是否小于右边的，如果是，则返回 true。     | [ $a -lt $b ]，左小于右返回true     |
| -ge    | 检测左边的数是否大于等于右边的，如果是，则返回 true。 | [ $a -ge $b ]，左大于等于右返回true |
| -le    | 检测左边的数是否小于等于右边的，如果是，则返回 true。 | [ $a -le $b ]，左小于等于右返回true |

示例：

```shell
#! /bin/bash

a=10
b=100
a=$b
#检测a是不是等于b
if [ $a == $b ]
then
    echo "a equals b"
fi
#检测a是不是不等于b
if [ $a != $b ]
then
    echo "a not equals b"
fi
#检测a是不是等于b
if [ $a -eq $b ]
then
    echo "a eq b"
fi
#检测a是不是不等于b
if [ $a -ne $b ]
then
    echo "a nq b"
fi
#检测a是不是大于b
if [ $a -gt $b ]
then
    echo "a gt b"
fi
#检测a是不是小于b
if [ $a -lt $b ]
then
    echo "a lt b"
fi
#检测a是不是大于等于b
if [ $a -ge $b ]
then
    echo "a ge b"
fi
#检测a是不是小于等于b
if [ $a -le $b ]
then
    echo "a le b"
fi
```

输出：

```shell
a equals b
a eq b
a ge b
a le b
```



### 三。布尔运算符

shell布尔运算符：

| 运算符 | 说明                                                | 举例 |
| ------ | --------------------------------------------------- | ---- |
| !      | 非运算，表达式为 true 则返回 false，否则返回 true。 |      |
| -o     | 或运算，有一个表达式为 true 则返回 true。           |      |
| -a     | 与运算，两个表达式都为 true 才返回 true。           |      |



### 五。逻辑运算符



### 六。字符串运算符



### 七。文件测试运算符

