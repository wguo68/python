## 控制语句（control_flow）

### 1. if条件语句
 当关键字**if**后面的表达式为真（非0、非空），就执行其条件语句块，否则，就跳过条件语句块，继续执行if语句后面的语句。
 
 *注意*： 1） 按照python语法，条件语句块要缩进 2） 条件表达式后要跟一个冒号':' 。
```python   
    if 条件真：
        条件语句块
    ...
```    
    ![](https://www.tutorialspoint.com/python/images/decision_making.jpg)
    
    还有其他一些变种，如：
```python   
    if 条件真：       #如果条件真，执行“条件语句块”
        条件语句块    
    else             #否则，执行“条件语句块2“
        条件语句块2
    ...
```  
```python   
    if 条件1：             #如果条件1为真，执行“条件1语句块”
        条件1语句块    
    elif 条件2             #否则如果条件2为真，执行“条件2语句块”
        条件2语句块
    elif 条件3             #否则如果条件3为真，执行“条件3语句块”
        条件3语句块
        ... 
    else                    #否则(其他情况)，执行“其他情况语句块”
        其他情况语句块
    ...
```  
例如下面的程序：
```python
>>> x = int(input("Please enter an integer: "))
Please enter an integer: 42
>>> if x < 0:
...     x = 0
...     print('Negative changed to zero')
... elif x == 0:
...     print('Zero')
... elif x == 1:
...     print('Single')
... else:
...     print('More')
...
More
```

当然，if语句里可以嵌套if语句，例如：
```python
var = 100
if var < 200:
   print "Expression value is less than 200"
   if var == 150:
      print "Which is 150"
   elif var == 100:
      print "Which is 100"
   elif var == 50:
      print "Which is 50"
elif var < 50:
   print "Expression value is less than 50"
else:
   print "Could not find true expression"

print "Good bye!"
```
当执行上述代码后，将输出：
```python
Expression value is less than 200
Which is 100
Good bye!
```
### 2. while条件语句
当关键字**while**后面的表达式为真（非0、非空），就执行while循环体里的语句块
 ```python   
    while 条件真：
        语句块
    ...
```   
![](https://www.tutorialspoint.com/python/images/python_while_loop.jpg)

例如：
```python
count = 0
while (count < ):
   print 'The count is:', count
   count = count + 1
```
执行后，输出：
```python
The count is: 0
The count is: 1
The count is: 2
The count is: 3
```
