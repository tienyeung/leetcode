# python内建函数及技巧

# 1.内建函数

1. 最大公约数：

   `from fractions import gcd`

   `gcd(param1,param2)`求二者的最大公约数

2. reduce：

   e.g `reduce(gcd, vals)`,表示对于迭代器`vals`中的元素，用`gcd`先对头两个元素求解，再把求得的解与下一个元素同样用`gcd`求解，以此类推。

3. collections：

   计数：`dict=collections.Counter(iter)`

   异常字典：`dict=collections.defaultdict(err)`参数中 的err表示当找不到字典中的某个key时，默认返回这个err所代表的异常，err可以是`int`表示默认返回0

4. 分组：

   `from itertools import groupby`

   `groupby(iter)`是将一个列表中相同的元素归为一组，返回的是两个值：（组别名，组中元素）
   
5. 排序：

   `sorted([elem,,,],key=lambda x:())`

   这个x就是代指elem，即当前需要排序的元素，排序的规则基于x后面的()，里面的优先权是从左至右的，比如(len(x),x)表示的是先按长度排序再按elem，如果是str的话，按照字母表顺序排序。

6. 分割：

   `Str.split(" ",number)`按照“”内的元素分割，关键是后面的数字，-1默认表示全部分隔开，假如是1表示从左至右只分割一次即止。

7. 排列：

   `itertools.permutations(a1，a2)`从数组a1中选取a2个数，返回这a2个数组成的全排列(与顺序相关)。
   
   `itertools.combinations(a1，a2)`从数组a1中选取a2个数，返回这a2个数组成的组合(与顺序无关)。
   
8. 最小堆：

   `from heapq import heapify, heappush, heappop`

   分别对应建立最小堆，插入，取出
   
9. 缺省字典：

   `collections.defaultdict(list)`参数代表的是字典中若不存在当前key，则新建一个键值对，默认的值为list
   
10. OrderedDict:

    有序字典:`from collections import OrderedDict`

    方法：`move_to_end`: 指定一个key，把对应的key-value移到最后

    ​			`pop`: 获取指定key的value，并在字典中删除

    ​			popitem`: 按照后进先出原则，删除最后加入的元素，返回key-value;popitem(last = False)则删除最开始的元素。

# 2. 模板

1. [算法模板](https://github.com/Alex660/Algorithms-and-data-structures/blob/master/theoreticalKnowledge/AlgorithmTemplate算法模板.md)
2. [二分法](https://tienyeung.github.io/post/er-fen-cha-zhao/)

