<!--
author: thyme
date: 2020-03-12
title: 蓝桥杯 [基础训练6-10] 
tags:  
category: python
status:    
summary:  
-->



| BASIC-6 | [杨辉三角形](http://lx.lanqiao.cn/problem.page?gpid=T10) |
| ------- | -------------------------------------------------------- |
|         | 基础练习 二维数组                                        |

```python
def triangle():
    line = [1]         # 第一行就一个元素1
    while True:
        yield line
        # 生成下一行，表达式为 : [1] + 上一行的两个元素之和 + [1]
        line = [1] + [line[i] + line[i + 1] for i in range(len(line) - 1)] + [1]

m = int(input())
n = 0     # 控制输出行数
for item in triangle():
    print(*item)
    n += 1
    if n % m == 0:
        break
```

| BASIC-7 | [特殊的数字](http://lx.lanqiao.cn/problem.page?gpid=T46) |
| ------- | -------------------------------------------------------- |
|         | 循环 判断 数位                                           |

```python
for i in range(1,10):
    for j in range(0,10):
        for k in range(0,10):
            if i*100+j*10+k == i**3+j**3+k**3:
                print(i*100+j*10+k)

```

| BASIC-8 | [回文数](http://lx.lanqiao.cn/problem.page?gpid=T47) |
| ------- | ---------------------------------------------------- |
|         | 循环 判断 回文数                                     |

```python
for i in range(1000,10000):
    i = str(i)
    if i[0]==i[3] and i[1]==i[2]:
        print(i)
```

| BASIC-9 | [特殊回文数](http://lx.lanqiao.cn/problem.page?gpid=T48) |
| ------- | -------------------------------------------------------- |
|         | 回文数 循环 条件语句                                     |

```python
n = int(input())
m = []
for i in range(1,10):
    for j in range(0,10):
        for k in range(0,10):
            if n == 2*i+2*j+k:
                x=i*10000+j*1000+k*100+j*10+i
                m.append(x)
            if n == 2*i+2*j+2*k:
                x=i*100000+j*10000+k*1000+k*100+j*10+i
                m.append(x)
m.sort()
for v in m:
    print(v)
```

| BASIC-10 | [十进制转十六进制](http://lx.lanqiao.cn/problem.page?gpid=T49) |
| -------- | ------------------------------------------------------------ |
|          | 循环 整除 求余 判断                                          |

```python
n = int(input())
m = str(hex(n))
m = m.upper()
print(m[2::])
```

