## 控制语句（control_flow）

### if条件语句
 当关键字**if**后面的表达式为真（非0、非空），就执行其条件语句块。 *注意*： 按照python语法，条件语句块要缩进
```python   
    if 条件真
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
