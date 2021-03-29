<!--
author: thyme
date: 2020-03-10
title: 蓝桥杯 [基础训练1-5] 
tags:  
category: python
status:    
summary:  
-->



| BASIC-1 | [闰年判断](http://lx.lanqiao.cn/problem.page?gpid=T5) |
| ------- | ----------------------------------------------------- |
|         | 条件判断                                              |

```python
n = int(input())
if n % 4 == 0 or n % 100 ==0 and n % 400 != 0:
    print("yes")
else:
    print("no")
```

| BASIC-2 | [01字串](http://lx.lanqiao.cn/problem.page?gpid=T6) |
| ------- | --------------------------------------------------- |
|         | 循环                                                |

```python
for i in range(0,32):
    numb = bin(i) #转换成二进制
    munb = str(numb) #转换成字符串
    m = munb[2:7:1] #为了省去0x
    m = int(m)
    print('%05d'%m)
```

| BASIC-3 | [字母图形](http://lx.lanqiao.cn/problem.page?gpid=T7) |
| ------- | ----------------------------------------------------- |
|         | 循环 字符串                                           |

```python
m,n = map(int, input().split())
for i in range(0,m):
    for j in range(0,n):
        print("%c"%(65+abs(i-j)),end="")
    print("")

```



| BASIC-4 | [数列特征](http://lx.lanqiao.cn/problem.page?gpid=T8) |
| ------- | ----------------------------------------------------- |
|         | 循环 最大值 最小值 累加                               |
```python
while True:
    try:
        n = int(input())
        A = list(map(int,input().split()))

        print(max(A))
        print(min(A))
        print(sum(A))
    except:
        break
```
| BASIC-5 | [查找整数](http://lx.lanqiao.cn/problem.page?gpid=T9) |
| ------- | ----------------------------------------------------- |
|         | 循环 判断                                             |
```python
n = int(input())
A = list(map(int,input().split()))
m = int(input())
for i in range(0,n):
            if A[i] == m:
                print(i+1)
                break
            if m not in A:
                print(-1)
            else:
                pass
```