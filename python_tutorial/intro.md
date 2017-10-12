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




[Using Python as a Calculator](https://docs.python.org/3/tutorial/introduction.html#using-python-as-a-calculator)
