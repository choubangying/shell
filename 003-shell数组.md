## shell数组

### 一。shell数组定义

```
array_name=(value1 ... valuen)
```

shell中的数组用()括起来，每个成员用空格隔开；也可以使用下标直接赋值来定义

示例：

```shell
#! /bin/bash
# 定义数组方式1
num_arr=(1 2 3 4)

# 定义数组方式2
char_arr[0]=a
char_arr[1]=b
char_arr[2]=c
```

### 二。获取数组元素

```shell
#! /bin/bash
# 定义数组方式1
num_arr=(1 2 3 4)

# 定义数组方式2
char_arr[0]=a
char_arr[1]=b
char_arr[2]=c

# 获取数组成员
echo "num_arr的第一个元素为  : ${num_arr[0]}"
echo "char_arr的第一个元素为 : ${char_arr[0]}"
```

输出：

```shell
num_arr的第一个元素为  : 1
char_arr的第一个元素为 : a
```

shell获取数组元素很方便，和C类似，使用数组名[index]的方式

### 三。获取数组中所有元素

shell可以指定数组下标为*或者@来获取所有元素：

```shell
#! /bin/bash
# 定义数组方式1
num_arr=(1 2 3 4)

# 定义数组方式2
char_arr[0]=a
char_arr[1]=b
char_arr[2]=c

# 获取数组成员
echo "num_arr为  : ${num_arr[*]}"
echo "char_arr为 : ${char_arr[@]}"
```

输出：

```shell
num_arr为  : 1 2 3 4
char_arr为 : a b c
```

### 四。获取数组长度

```shell
#! /bin/bash

# 定义数组方式1
num_arr=(1 2 3 4)

# 定义数组方式2
char_arr[0]=a
char_arr[1]=b
char_arr[2]=c

# 获取数组长度
echo "num_arr len 为  : ${#num_arr[*]}"
echo "char_arr len 为 : ${#char_arr[@]}"
```

输出：

```
num_arr len 为  : 4
char_arr len 为 : 3
```

