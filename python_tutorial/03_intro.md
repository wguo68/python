## hello world 程序
print("hello world\n")

## python作为一个计算器

```python
>>> (50 - 5*6) / 4
5.0

>>> 17 / 3  # 实数除法
5.666666666666667
>>>
>>> 17 // 3  # 整数除法
5
>>> 17 % 3  # the % 取模
2
>>> 2 ** 7  #  指数
128
```
用等于符号 (=) 可以给一个值起一个名字，叫做变量
```python
>>> pi = 3.1415926
>>> r= 2.5
>>> area = pi*r*r/2
>>> r = "hello"  #变量可以表示不同类型的量，现在r表示了一个字符串。变量类型根据它指向的值的类型而变化，称之为“动态类型"。
                 # 因此，python称为动态语言
```

python 是一个动态（dynamic）语言，在源代码里不需要对变量、参数、函数和方法进行任何类型声明（type declarations）。变量的类型由其指向的数据的类型决定。比如上面的r开始是一个实数类型（指向2.5）,后来变成了一个字符串(string)类型（指向字符串“hello”）。即变量的类型是可以动态变化的（而其他编程语言，一旦定义变量，其类型就不能改变）。


### 字符串string
 可以用首尾单引号‘ ’ 或首尾2个双引号 来表字符串
```
'hello'
"world"
```
单引号表示的字符串中可以包含 ```"``` ，双引号表示的字符串中可以包含 ```‘``` 。

```python
'hello ”world“'
"'hello' world"
```
如果字符串本身既包含双引号 ```"``` ，又包含单引号 ```‘``` 。就需要用转义字符```\```来进行转义，以能表示单或双引号。
如要表示字符串 Bob said "I'm OK"。
```python
  'Bob said \"I\'m OK\".'  
```
常用的转义字符还有：
```
\n  表示换行
\t  表示一个制表符
\\  表示 \ 字符本身
```
也可以在字符串表示前加r,表示raw字符串，可以避免使用转义字符如"\t","\n"等，但单引号和双引号仍然需要用转义字符。如
```
r'\(~_~)/ \(~_~)/'
```
Unicode字符串:为了支持两个字节表示的Unicode国际编码，以便表示中文、日文等文字，可以在包含中文等字符串前加一个字母u。如：
```
  print u'中文'
```
三引号```"""```用于表示多行字符串
```
   >>>str = """\
         Usage: thingy [OPTIONS]
         -h                        Display this usage message
         -H hostname               Hostname to connect to
       """
 print (str)
```

字符串可以用加号+进拼接，用乘号* 复制。如：
```python
   >>>3 * 'un' + 'ium'
   'unununium'
```
字符串可以用下标进行访问：
```python
>>> word = 'Python'
>>> word[0]  # character in position 0
'P'
>>> word[5]  # character in position 5
'n'
>>> word[-1]  # last character
'n'
>>> word[-2]  # second-last character
'o'
>>> word[-6]
'P'
```
第一个字符下标是0，最后一个字符下标是-1 或（长度-1）。如图：
```
 +---+---+---+---+---+---+
 | P | y | t | h | o | n |
 +---+---+---+---+---+---+
 0   1   2   3   4   5   6
-6  -5  -4  -3  -2  -1
```
切片(slicing)可通过给出起始下标得到一个原字符串的”子串“。如：
```python
>>> word[0:2]  # characters from position 0 (included) to 2 (excluded)
'Py'
>>> word[2:5]  # characters from position 2 (included) to 5 (excluded)
'tho'
>>> word[:2]   # character from the beginning to position 2 (excluded)
'Py'
>>> word[4:]   # characters from position 4 (included) to the end
'on'
>>> word[-2:]  # characters from the second-last (included) to the end
'on'
```

访问单个字符时下标不能越界，如：
```python
>>> word[42]  # the word only has 6 characters
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: string index out of range
```
但切片可以越界，如：
```python
>>> word[4:42]
'on'
>>> word[42:]
''
```

##  python编程：
  
  可以用python左一些复杂的事情，比如计算Fibonacci序列：
```
>>> # Fibonacci series:
... # the sum of two elements defines the next
... a, b = 0, 1
>>> while b < 10:
...     print(b)
...     a, b = b, a+b
...
1
1
2
3
5
8
```
说明：

* 其中第一行语句“a, b = 0, 1”是一个“多赋值语句（multiple assignment:）”，变量a,b同时用右边的表达式进行赋值。
* while循环一直执行，只要其中的条件表达式“b<10”为真（即非0或非空值）。“b<10”是一个简单的比较测试，标准的*比较运算符*有： < (小于), > (大于), == (等于), <= (小于等于), >= (大于等于) and != (不等于)
* 循环体中的所有语句是缩进对齐（indented）的，表示它们属于一个程序块。
* print() 用于输出信息，可以跟多个参数，如字符串、浮点数等。比如：
```
>>> i = 256*256
>>> print('The value of i is', i)
The value of i is 65536
```
print()可以跟一个关键字参数**end**以避免输出的换行或者输出一个不同的字符串，比如:
```
>>> a, b = 0, 1
>>> while b < 1000:
...     print(b, end=',')
...     a, b = b, a+b
...
1,1,2,3,5,8,13,21,34,55,89,144,233,377,610,987,
```

类似于python自带的print函数，我们也可以用关键字**def**定义自己的函数。将一些使用的程序块用函数封装起来，提供给我们自己或其他人的程序使用。

```
# 定义一个带有2个参数的 "repeat" 函数.
def repeat(s, exclaim):
    """
    返回字符串's'的3次重复 .
    如果exclaim为真，追加3个感叹号.
    """

    result = s + s + s  # 也可以使用更快的乘法运算符*, "s * 3" 
    if exclaim:
        result = result + '!!!'
    return result
    
print repeat('Yay', False)      ## 输出结果将是：YayYayYay
print repeat('Woo Hoo', True)   ## 输出结果将是：Woo HooWoo HooWoo Hoo!!!   
```
这个程序中，我们定义了一个repeat函数，之后执行了2次函数调用语句，分别传递了相应的参数。*注意*：函数必须在其调用前先定义。
```
# 定义一个带有2个参数的 "repeat" 函数.
def repeat(s, exclaim):
    """
    返回字符串's'的3次重复 .
    如果exclaim为真，追加3个感叹号.
    """

    result = s + s + s  # 也可以使用更快的乘法运算符*, "s * 3" 
    if exclaim:
        result = result + '!!!'
    return result

# 又定义了叫做main的函数，其中2次调用了repeat函数
def main():
    print repeat('Yay', False)      ## YayYayYay
    print repeat('Woo Hoo', True)   ## Woo HooWoo HooWoo Hoo!!!

# 如果变量名__name__等于 '__main__'就执行main函数
if __name__ == '__main__':
    main()

```

一个python模块既可以直接执行，如"python hello.py"，也可以被其他模块调用执行。 当它被直接执行时，有一个特殊的变量名 "__name__" 被设置成 "__main__"，反之当它被其他模块调用执行时，"__name__" 被设置成它自身的文件名。因此，上面的程序只有被直接执行时，才会执行main函数。

### 模块和名字空间
   
### 总结
   python程序由一些模块组成，模块就是一个扩展名为".py"脚本文件。模块会被分类组成在各种包中，包就是一个包含模块文件的文件夹。其中必须有一个叫做init.py的特殊脚本文件（通常是一个内容空的文件。）。而一个模块中是一些函数定义和python命令（其中包括了函数调用命令、控制语句命令），模块的命令被一句一句地执行。

[Using Python as a Calculator](https://docs.python.org/3/tutorial/introduction.html#using-python-as-a-calculator)
