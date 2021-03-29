<!--
author: thyme
date: 2019-12-17
title: HiveQL
tags:  
category: hadoop
status: publish   
summary: 
-->

 通过HiveQL查询处理数据 

- 1.1、启动hadoop

  在master服务器上，进入到/usr/local/zhitu/hadoop-2.7.3目录下启动hadoop服务。

  参考命令：

  ```
cd /usr/local/zhitu/hadoop-2.7.3
  bin/hdfs namenode -format
  sbin/./start-all.sh
  ```
- 1.2、启动mysqld服务

本实验中hive使用mysql数据库作为元数据库，需要启动mysqld服务。maste主机上已经安装好mysql，只用启动mysqld服务即可。

```
参考命令：systemctl start mysqld
```
- 1.3、启动hive

  在主服务器上开启hive的metastore服务。

  参考命令：

```
hive --service metastore &
```


开启hive的命令行

直接在命令行中输入命令：hive



```
  create database IF NOT EXISTS demo;
```

  

```
  use demo;

  create table stock_data(Datel string, Open float, High float, Lowfloat, Close float, Volume int, AdjClose float)row format delimited fieldsterminated by ',' stored as textfile;

   load data local inpath '/usr/local/zhitu/sample/sample1.txt' into table stock_data; 
 
   select * from stock_data where datel = "2016-9-29"; 
  
   select * from stock_data where  volume>1500000 limit 3; 
```




  3.1、创建表

  创建两张表Post_data_uk和Post_data_us，Post_data_uk表示英国的邮政数据，Post_data_us表示美国的邮政数据。

  两张表有相同的字段：

  用户的firstname，lastname，公司名称，地址，城市，国家，邮编，电话1，电话2，电子邮箱，web地址。

  参考sql:

```mysql
create table Post_data_uk(First_name string,Last_name string,Company_name string,Address string,City string,Country string,Postal string,Phonel string,Phone2 string,Email string,Web string) row format delimited fields terminated by ',' stored as textfile;
```

```mysql
create table Post_data_us(First_name string,Last_name string,Company_name string,Address string,City string,Country string,Postal string,Phonel string,Phone2 string,Email string,Web string) row format delimited fields terminated by ',' stored as textfile;
```

3.2、导入数据

将本地目录/usr/local/zhitu/sample/ 下的uk_data.txt和us_data.txt两个文件中的数据分别导入到表：Post_data_uk和Post_data_us中。

```shell
load data local inpath '/usr/local/zhitu/sample/uk_data.txt' into table Post_data_uk; 


load data local inpath '/usr/local/zhitu/sample/us_data.txt' into table Post_data_us; 
```
3.3、关联查询

1.使用一条HiveQL语句查询两个国家具有相同first_name的人，显示出这些相同的first_name；

2.查询两国都有的人名以及只有英国有的人名；

3.查询两国都有的人名以及只有美国有的人名。

参考sql:


```mysql
  select uk.first_name from Post_data_uk uk join Post_data_us us on(uk.first_name=us.first_name);

  select uk.first_name from Post_data_uk uk left outer join Post_data_us us on (uk.first_name=us.first_name);

  select uk.first_name from Post_data_uk uk right outer join Post_data_us us on (uk.first_name=us.first_name);
  
```

3.4、创建分区表

创建表名为：Post_data的分区表，包含字段：

用户的firstname，lastname，公司名称，地址，城市，国家，邮编，电话1，电话2，电子邮箱，web地址。

分区字段为：country。

并将本地目录/usr/local/zhitu/sample/ 下的uk_data.txt和us_data.txt两个文件中的数据分别导入到表Post_data的分区country='uk'和country='us'中。

再查看分区country='uk'中的数据。

参考sql:

```mysql
create table Post_data (first_name string, last_name string,company_name string,address string,city string, state string,postal string,phonel string,phone2 string,email string,web string) partitioned by(country string) row format delimited fields terminated by ',' stored as textfile;
```

```mysql
load data local inpath '/usr/local/zhitu/sample/uk_data.txt' overwrite into table Post_data partition(country='uk');
```

```mysql
load data local inpath '/usr/local/zhitu/sample/us_data.txt' overwrite into table Post_data partition(country='us');
```

```mysql
select * from Post_data where country='uk';
```

