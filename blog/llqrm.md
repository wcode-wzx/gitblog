<!--
author: thyme
date: 2020-02-27
title: 蓝桥杯 [入门训练] 
tags:  
category: python
status:    
summary:  
-->



| BEGIN-1 | [A+B问题](http://lx.lanqiao.cn/problem.page?gpid=T1) |
| ------- | ---------------------------------------------------- |
|         |                                                      |

```python
while True:
    try:
        #把输入的数用map转化为一个存整数类型的列表
        caption = list(map(int, input().split()))
        ans = 0
        for i in caption:
            ans += i
        print(ans)
    except EOFError:
        break
```

| BEGIN-2 | [序列求和](http://lx.lanqiao.cn/problem.page?gpid=T2) |
| ------- | ----------------------------------------------------- |
|         |                                                       |

```python
n = int(input())
num = 0
sum = 0
for i in range(1,n+2):
    sum += num
    num += 1
print(sum)

//很容易想到的暴力求解 运行超时
```

```python
n = int(input())
sum = n+(n*(n-1))/2
num=int(sum)
print(num)

// 利用前n项和公式 AC
```

| BEGIN-3 | [圆的面积](http://lx.lanqiao.cn/problem.page?gpid=T3) |
| ------- | ----------------------------------------------------- |
|         |                                                       |

说明：在本题中，输入是一个整数，但是输出是一个实数。

对于实数输出的问题，请一定看清楚实数输出的要求，比如本题中要求保留小数点后7位，则你的程序必须**严格的**输出7位小数，输出过多或者过少的小数位数都是不行的，都会被认为错误。

实数输出的问题如果没有特别说明，舍入都是按四舍五入进行。

```python
PI=3.14159265358979323
r = int(input())
f = PI*r**2
print('%.7f' % f)
```

| BEGIN-4 | [Fibonacci数列](http://lx.lanqiao.cn/problem.page?gpid=T4) |
| ------- | ---------------------------------------------------------- |
|         |                                                            |

```python
def fibonacci(n):
    f0, f1, f2 = 0, 1, 0
    if n == 0:
        return 0
    if n == 1:
        return 1
    i = 2
    while i <= n:
        f2 = f0 + f1
        f0 = f1
        f1 = f2
        i += 1
    return f2
n = int(input())
print(fibonacci(n)%10007)
// 超时
```

改进  f2 = (f0 + f1)%10007 

对每一斐波那契数列进行取余相加 ，直接计算余数往往比先算出原数再取余简单。 

```python
def fibonacci(n):
    f0, f1, f2 = 0, 1, 0
    if n == 0:
        return 0
    if n == 1:
        return 1
    i = 2
    while i <= n:
        f2 = (f0 + f1)%10007
        f0 = f1
        f1 = f2
        i += 1
    return f2
n = int(input())
print(fibonacci(n))

```

