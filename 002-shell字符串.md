##  shell字符串

### 一。shell单引号字符串

```shell
str1='this single quote mark str'
```

单引号的字符串限制：

- 单引号里的任何字符都会原样输出，单引号字符串中的变量是无效的；
- 单引号字串中不能出现单独一个的单引号（对单引号使用转义符后也不行），但可成对出现，作为字符串拼接使用。

### 二。shell双引号字符串

```shell
str2="this double quote mark str"
your_name='runoob'
str="Hello, I know you are \"${your_name}\"! \n"
echo -e $str
```

输出结果为：

```shell
Hello, I know you are "runoob"! 
```

双引号字符的优点：

- 双引号里可以有变量
- 双引号里可以出现转义字符

###  三。字符串拼接

```shell
your_name="runoob"
# 使用双引号拼接
greeting="hello, "$your_name" !"
greeting_1="hello, ${your_name} !"
echo $greeting  $greeting_1
# 使用单引号拼接
greeting_2='hello, '$your_name' !'
greeting_3='hello, ${your_name} !'
echo $greeting_2  $greeting_3
```

输出结果：

```shell
hello, runoob ! hello, runoob !
hello, runoob ! hello, ${your_name} 
```

可以看到双引号的无需加""也可以正确地拼接变量的值，

单引号必须加''包裹住变量才行

优先使用单引号

### 四。获取字符串长度

shell提供了获取字符串长度的方法

```shell
string="abcd"
echo ${#string} #输出 4
```

### 五。提取子字符串

shell提取子字符串的写法，

```shell
string="runoob is a great site"
echo ${string:1:4} # 输出 unoo
```

上面的表示从string的第2个字符取4个字符出来

### 六。查找子字符串的位置

```shell
string="runoob is a great site"
echo `expr index "$string" io`  # 输出 4
```

上面语句是在string中找字符'i'或者'o'的位置，哪个在前就输出哪个的位置。