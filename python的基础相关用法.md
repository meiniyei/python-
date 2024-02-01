# python的基础相关用法

## 一、函数

### 1，匿名函数

lambda将函数转换为另一种写法

1,定义函数：

def add(a,b=1);

​	return a+b

print(add(10,20))

print(add(10))

转换为lambda函数：

add lambda=lambda a,b=1:a+b     //lambda函数中冒号前的是该函数的参数，冒号后的是执行的内容

2,if条件语句

利用lambda式将其进行转换

get_odd_even=lambda x:'even'if x%2==0 else 'odd' //如果x%2==0则返回even,否则为'odd'

3,无参表达式

import random

ran_lambda=lambda:random.random()

print(ran_lambda())//该函数为无参表达式，所以lambda与引号之间的位置并没有相关的参数，random()为随机生成函数，无需相关的参数即可执行

4,map内置函数的转换

def add(x);

​	return x**2

mobj=map(add,[1,2,3,4])     //map内置函数起到一个遍历的作用，将1到4全部进行遍历，之后传参给add函数

print(list(mobj))  //最后的结果为 1，4，9，16

使用lambda代码：
mobj=map(lambda x:x**2,[1,2,3,4] )   //以map内置函数为整体然后进行嵌套将def自定义的函数转换成相关的lambda代码即可

print(list(mobj))
