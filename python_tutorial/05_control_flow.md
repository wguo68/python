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
