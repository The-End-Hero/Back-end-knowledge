Python3

list

Python内置的一种数据类型是列表：list。list是一种有序的集合，可以随时添加和删除其中的元素。

```python
classmates = ['Michael', 'Bob', 'Tracy']
classmates

len(classmates) # len()获取list元素的个数

# 当索引超出了范围时，Python会报一个IndexError错误，所以，要确保索引不要越界，记得最后一个元素的索引是len(classmates) - 1。 

classmates[-1] # 直接获取最后一个元素

classmates.append('Adam') # append往list末尾追加元素

classmates.insert(1, 'Jack') # insert插入到指定位置，比如索引为1的位置

classmates.pop() # pop从list末尾删除一个元素

classmates.pop(1) # pop(i)表示指定删除的索引

```



tuple

另一种有序列表叫元组：tuple。tuple和list非常类似，但是tuple一旦初始化就不能修改。

```python
t = (1) # 1

t = (1,) # Python在显示只有1个元素的tuple时，也会加一个逗号,，以免你误解成数学计算意义上的括号。

t = ('a', 'b', ['A', 'B'])
t[2][0] = 'X'
t[2][1] = 'Y'
# ('a', 'b', ['X', 'Y']) tuple所谓的不可变实际是指向不可变，但是指向为数组的时候，改变这个数组，并不会影响这个指向。
```



if条件判断简写

```python
if x:
    print('True')
# 只要x是非零数值，非空字符串，非空list等，就判断为True，否则为False
```



range()函数

```python
list((range(5)) # [0,1,2,3,4] renge()函数，生成整数序列，再通过list()转换成list
```



break 提前结束循环



continue 跳出当前循环，直接开始下一次循环



### dict

请务必注意，dict内部存放的顺序和key放入的顺序是没有关系的。

和list比较，dict有以下几个特点：

1. 查找和插入的速度极快，不会随着key的增加而变慢；
2. 需要占用大量的内存，内存浪费多。

而list相反：

1. 查找和插入的时间随着元素的增加而增加；
2. 占用空间小，浪费内存很少。

所以，dict是用空间来换取时间的一种方法。

```python
d = {'Michael': 95, 'Bob': 75, 'Tracy': 85}
d['Michael'] # 95
d['Adam'] = 67
d['Adam'] # 67
d['Thomas'] # 不存在，即报错    in判断key是否存在，或 dict的get()方法
d.get('Thomas') # 不存在返回None
d.get('Thomas', -1) # 不存在返回自己指定的value

```

dict可以用在需要高速查找的很多地方，在Python代码中几乎无处不在，正确使用dict非常重要，需要牢记的第一条就是dict的key必须是**不可变对象**。

这是因为dict根据key来计算value的存储位置，如果每次计算相同的key得出的结果不同，那dict内部就完全混乱了。这个通过key计算位置的算法称为哈希算法（Hash）。

要保证hash的正确性，作为key的对象就不能变。在Python中，字符串、整数等都是不可变的，因此，可以放心地作为key。而list是可变的，就不能作为key



set

set和dict类似，也是一组key的集合，但不存储value。由于key不能重复，所以，在set中，没有重复的key。

```python
s = set([1, 1, 2, 2, 3, 3])
s # {1, 2, 3}
s.add(4)
s.add(4)
s # {1, 2, 3, 4}
s.remove(4)
s # {1, 2, 3}

# set可以看成数学意义上的无序和无重复元素的集合，因此，两个set可以做数学意义上的交集、并集等操作
s1 = set([1, 2, 3])
s2 = set([2, 3, 4])
s1 & s2 # {2,3}
s1 | s2 # {1,2,3,4}
```

set和dict的唯一区别仅在于没有存储对应的value，但是，set的原理和dict一样，所以，同样不可以放入可变对象，因为无法判断两个可变对象是否相等，也就无法保证set内部“不会有重复元素”。



def

定义函数时，需要确定函数名和参数个数；

如果有必要，可以先对参数的数据类型做检查；

函数体内部可以用`return`随时返回函数结果；

函数执行完毕也没有`return`语句时，自动`return None`。

函数可以同时返回多个值，但其实就是一个tuple。