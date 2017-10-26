## 控制语句（control_flow）

### if条件语句
 当关键字**if**后面的表达式为真（非0、非空），就执行其条件语句块，否则，就跳过条件语句块，继续执行if语句后面的语句。
 
 *注意*： 1） 按照python语法，条件语句块要缩进 2） 条件表达式后要跟一个冒号':' 。
```python   
    if 条件真：
        条件语句块
    ...
```    
    ![](https://www.tutorialspoint.com/python/images/decision_making.jpg)
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
