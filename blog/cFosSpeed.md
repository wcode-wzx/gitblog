<!--
author: thyme
date: 2020-03-31
title: cFosSpeed
tags:  
category: 软件分享
status: publish   
summary: 
-->


## 给大家分享一款软件：cFosSpeed



我们先看一下[百度百科](https://baike.baidu.com/item/cfosspeed/5913606?fr=aladdin)：cFosSpeed 软件是Windows操作系统下的一款重要的网络工具软件，其特别的通信流量调整功能可以保证网络在上传下载工作时均保持满速高速的运行状态，可对已有网络带宽的利用发挥到极致。

cFosSpeed是使用者真正能感觉到网速提升的软件，它可以真正做到自动调节网速，让你的网络达到最大值，并且详细的设置使cFosSpeed更具自定义性。特别是对于喜欢使用P2P之类软件，如电驴、迅雷、bt、pps网络电视等大量占用带宽程序的用户，安装使用该软件后，同时浏览网页、聊天、玩游戏等一般都能流畅顺利地进行。因此原因而经常掉线的，使用该软件后也一般不掉线了。 

###### 首先这个软件在第一次使用的时候是需要手动配置的，找到设置。

![12 (1)](http://www.thyme.org.cn\blog\img\121.png)

###### 弹出网页后，左侧目录选择“适配器信息”，会看到Calibration Done 是 10%(Poor)，所以接下来我们得自己配置一下，让Calibration Done接近 100%

![12 (4)](http://www.thyme.org.cn\blog\img\124.png)





#### cFosSpeed配置

------

- cFosSpeed开启后，任务栏里的 cfosspeed 图标右键--"流量调整"--"线路校准"

  ![213](http://www.thyme.org.cn\blog\img\213.png)

- 接着开始宽带测速，测出并记下最大上传速度，平均上传速度，最大下载速度和平均下载速度，如下图：
  ![12 (2)](http://www.thyme.org.cn\blog\img\122.png)

  

  速度截图

  

- 任务栏里的 cfosspeed 图标右键--"流量调整"--"打开cfosspeed控制台"，接着输入命令`spd speed`：可以查看具体各项配置情况，如下图，可以看到现在 calibrated 为 10 ，我们要配置使得它接近 100：


  ![12 (5)](http://www.thyme.org.cn\blog\img\125.png)

  控制台

  

- 配置下面5项的值：

  ```python
  maxtxraw： 最大上传总值，峰值
  maxtxacked：最大上传速度的ACK字元，接近上传速度稳定值
  maxrx：最大下载速度，峰值
  txspeed：上传速度，稳定值
  tx_bounce_cnt：tx的弹射连接项，这里设置为 5
  以我为例，根据上面测出的速度，可以这样配置：
  spd set maxtxraw 27000k
  spd set maxtxacked 26624k
  spd set maxrx 69632k
  spd set txspeed 26624k
  spd set tx_bounce_cnt 5
  ```

  ![12 (6)](http://www.thyme.org.cn\blog\img\126.png)

  

  我们再看任务栏的图标右键 “选项”--“配置”，选择“适配器信息”可以看到Calibration Done接近 100%，说明配置成功：

  ![235](http://www.thyme.org.cn\blog\img\235.png)

  适配器信息



### 在官网我们可以看到售价为15.90欧元

![324](http://www.thyme.org.cn\blog\img\324.png)

### 但是我们可以注意一下这个条款，没错在2020年4月13日之前，我们可以免费获得cForSpeed的终身授权。

![36](http://www.thyme.org.cn\blog\img\36.png)



赶紧试试吧！

> 注：Calibration会稍稍波动，正常，只要接近100即可。
>
> 软件下载链接：https://www.cfos.de/en/index.htm 