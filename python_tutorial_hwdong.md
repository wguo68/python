
### list
 任意对象的有序集合（顺序集合）。用方括号[]定义，元素之间以逗号隔开：
 ```python
     L1 = [20,3,45,68]
     L1 = [20,3,45.78,'A',"string"]
     L1 = [20,3,45.78,'A',"string",["abc","xyz","uvw"]]
 ```
 
 通过下标访问（读写）每个数据元素，下标从0开始。
 ```python
   # 下标： 0   1   2     3      4
   # 下标：-5  -4  -3     -2    -1
     L1 = [20, 3, 45.78, 'A', "string"]
     L1[2]
     L1[-1]
```
通过下标范围访问（读写）一个子列表（list）。
  
 ```python
   # 格式： 列表名[起始位置：结束位置] ，返回一个列表，但不包括最后位置的元素。
   # 下标： 0   1   2     3      4
   # 下标：-5  -4  -3     -2    -1
     L1 = [20, 3, 45.78, 'A', "string"]
     L1[0:3]
     L1[:4]
     L1[-3:-1]
     L1[:]
```