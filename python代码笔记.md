# python代码笔记

#### 列表拷贝

```python
# [26] 删除排序数组中的重复项
#
# @lc code=start
class Solution:
    def removeDuplicates(self, nums: List[int]) -> int:
        nums[:] = sorted(list(set(nums))) #用nums = sorted(list(set(nums)))为浅拷贝
        return len(nums)
```

深copy：

`A=[1,2,3,4]  or  A=A[:]`

浅copy

`B=A`

浅copy在后面对B操作以后就会影响到A，A的值也会随之改变 

#### 列表逆序切片

`A[start:end:-1] 如A[-1:3:-1]为正确的逆序切片表达，start为开始切片的位置，end为终止位置`

#### 单词一个个分开

`s=123413`

`digits = list(str(s)) `

#### 动态插入

```python
first = 'yifan'
last = 'xu'
# situation 1
msg = first + ' ['+last+'] is a coder.'
#sitution 2
msg = f'{first} [{last}] is a coder.'
```

#### mosh python 笔记

Python title() 方法返回"标题化"的字符串,就是说所有单词都是以大写开始，其余字母均为小写。

#### Numpy运算

```python
m = np.array([[1,2,3],[4,5,6]])
n = m * 0.25

#  m*n 结果等于 np.multiply(m,n) 
#  均为点乘，维度要一致
```

```python
#矩阵相乘方法一： 不能用*代替np.matmul()
np.matmul(a,b)
#矩阵相乘方法二： 
a.dot(b)
##矩阵相乘方法三：
a@b
```

#### 返回字典中频次最大的key值

```python
max(dic,key=lambda x:dic[x])
max(dic,key=dic.get)
```

#### rand和randn区别

```python
np.random.rand() # 返回均匀分布的伪随机数.数值均匀分布在[0.1)间
np.random.randn() # 返回标准正态分布的伪随机数.均值为0,方差为1
```

#### python函数注释规范

我选择使用Google的python命名规范

```python
def add(a, b):
    """
    Calculate the sum of a and b
    
    :param a: a number
    :param b: a number
    :return: the sum
    """
```

