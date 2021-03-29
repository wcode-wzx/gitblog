<!--
author: thyme
date: 2019-12-23
title: 通过JDBC连接Hive 
tags:  
category: hadoop
status: publish   
summary:  通过JDBC连接Hive 
-->

- 1、启动hiveserver2服务

  - 1.1、启动hiveserver2服务

    在master服务器上启动hadoop集群，启动mysqld服务，并启动hive的hiveserver2服务，JDBC连接的关键服务hiveserver2，默认端口是10000

    参考命令：

    启动hadoop集群

    ```
cd /usr/local/zhitu/hadoop-2.7.3
    
    bin/hdfs namenode -format
    
    sbin/./start-all.sh
    ```
    
    启动mysqld服务

    ```
systemctl start mysqld
    ```
    
    启动hiveserver2：

    参考命令：

    ```
hive --service hiveserver2 &
    ```
    
    

- 2、开发java程序连接hive

  - 2.1、创建Maven项目

    在develop-pc服务器上，打开eclipse创建maven项目。

    参考步骤如下：

    ![1](http://www.thyme.org.cn/gitblog/blog/img/1.png)

    点击菜单栏的File，依次File->New->Project:

    ![1](http://www.thyme.org.cn/gitblog/blog/img/2.png)

    点击Project,弹出如下，选择maven项目，点击next：

    ![1](http://www.thyme.org.cn/gitblog/blog/img/3.png)

    勾选标记处创建简单项目,点击next：

    ![1](http://www.thyme.org.cn/gitblog/blog/img/4.png)

    写入group id:com.yundaxue,artifact id: jdbc_hive_demo_01,点击finish：

     ![1](http://www.thyme.org.cn/gitblog/blog/img/5.png)

    项目新建完成后，结构如下，打开pom.xml文件：

     ![1](http://www.thyme.org.cn/gitblog/blog/img/6.png)

    编辑pom.xml文件，配置开发是需要依赖的jar包。

    参考内容如下：

    ```xml
  <project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
  
  <modelVersion>4.0.0</modelVersion>
  
  <groupId>com.yundaxue</groupId>
  
  <artifactId>jdbc_hive_demo_01</artifactId>
  
  <version>0.0.1-SNAPSHOT</version>
  
  <dependencies>
  
  <dependency>
  
  <groupId>org.apache.hive</groupId>
  
  <artifactId>hive-jdbc</artifactId>
  
  <version>2.1.0</version>
  
  </dependency>
  
  <dependency>
  
  <groupId>org.apache.hive</groupId>
  
  <artifactId>hive-service</artifactId>
  
  <version>2.1.0</version>
  
  </dependency>
  
  <dependency>
  
  <groupId>org.apache.hive</groupId>
  
  <artifactId>hive-exec</artifactId>
  
  <version>2.1.0</version>
  
  </dependency>
  
    <dependency>
  
    <groupId>org.apache.hive</groupId>
  
    <artifactId>hive-metastore</artifactId>
  
    <version>2.1.0</version>
  
    </dependency>
  
    <dependency>
  
    <groupId>org.apache.thrift</groupId>
  
    <artifactId>libfb303</artifactId>
  
    <version>0.9.3</version>
  
    </dependency>
  
    <dependency>
  
    <groupId>commons-logging</groupId>
  
    <artifactId>commons-logging</artifactId>
  
    <version>1.2</version>
  
    </dependency>
  
    <dependency>
  
    <groupId>commons-codec</groupId>
  
    <artifactId>commons-codec</artifactId>
  
    <version>1.6</version>
  
    </dependency>
  
    <dependency>
  
    <groupId>org.apache.hadoop</groupId>
  
    <artifactId>hadoop-common</artifactId>
  
    <version>2.6.5</version>
  
    </dependency>
  
    <dependency>
  
    <groupId>org.apache.httpcomponents</groupId>
  
    <artifactId>httpclient</artifactId>
  
    <version>4.3.4</version>
  
    </dependency>
  
    <dependency>
  
    <groupId>org.apache.httpcomponents</groupId>
  
    <artifactId>httpcore</artifactId>
  
    <version>4.3.2</version>
  
    </dependency>
  
    <dependency>
  
    <groupId>log4j</groupId>
  
    <artifactId>log4j</artifactId>
  
    <version>1.2.17</version>
  
    </dependency>
  
    <dependency>
  
    <groupId>org.slf4j</groupId>
  
    <artifactId>slf4j-log4j12</artifactId>
  
    <version>1.7.5</version>
  
    </dependency>
  
    <dependency>
  
    <groupId>org.slf4j</groupId>
  
    <artifactId>slf4j-api</artifactId>
  
    <version>1.7.7</version>
  
    </dependency>
  
    <dependency>
  
    <groupId>jdk.tools</groupId>
  
    <artifactId>jdk.tools</artifactId>
  
    <version>1.8</version>
  
    <scope>system</scope>
  
    <systemPath>${JAVA_HOME}/lib/tools.jar</systemPath>
  
    </dependency>
  
    </dependencies>
  
    </project>
    ```
  
    
  
  - 2.2、开发java代码操作hive
  
    服务器上已有数据集：/usr/local/zhitu/sample/sample1.txt，开发java代码，实现功能：
  
    1 创建表：sample_data，结构与sample1.txt一致
  
    2 导入/usr/local/zhitu/sample/sample1.txt文件内容到表sample_daeta中。
  
    3 获取表sample_data中的数据。
  
    4 显示hive默认数据库下的所有表
  
    参考代码（注意：请将jdbc连接字符串改为自己三台服务器中主服务器的IP，例如  jdbc:hive2://172.20.6.38:10000/default）：
  
    
  
    ```java
    package com.yundaxue; 
    import java.sql.Connection;
    import java.sql.DriverManager;
    import java.sql.ResultSet;
    import java.sql.Statement; 
    public class HiveDemo01 {   
        public static void main(String[] args) {    
            createTable();    
            showTables();    
            loadData();    
            getData();  }   /**   * 查看所有表名   */  
        public static void showTables() {    
            try {      
                Class.forName("org.apache.hive.jdbc.HiveDriver");     //创建连接，并执行显示表命令，数据库连接url为：jdbc:hive2://ip地址:10000/default      
                Connection con = DriverManager.getConnection("jdbc:hive2://172.20.6.38:10000/default", "root", "");      Statement stmt = con.createStatement();      
                String querySQL = "show tables";      
                ResultSet res = stmt.executeQuery(querySQL);      System.out.println("show tables:");      
                while (res.next()) {        
                    System.out.println(res.getString(1));      
                }    
            } catch (Exception e) {      
                e.printStackTrace();    
            }  
        }   /**   * 创建表   */  
        public static void createTable() {    
            try {     
                //与上一步类似，建立连接，执行hiveQL语句      
                Class.forName("org.apache.hive.jdbc.HiveDriver");      
                Connection con = DriverManager.getConnection("jdbc:hive2://172.20.6.38:10000/default", "root", "");      Statement stmt = con.createStatement();      
                String sql = "create table if not exists sample_data(name string) stored as textfile";      
                stmt.execute(sql);      
                System.out.println("sample_data is created!!!");    
            } catch (Exception e) {      
                e.printStackTrace();    
            }  
        }   /**   * 载入数据   */  
        public static void loadData() {    
            try {      
                Class.forName("org.apache.hive.jdbc.HiveDriver");      
                Connection con = DriverManager.getConnection("jdbc:hive2://172.20.6.38:10000/default", "root", "");      Statement stmt = con.createStatement();      
                String sql = "load data local inpath '/usr/local/zhitu/sample/sample1.txt' into table sample_data";      
                stmt.execute(sql);      
                System.out.println("sample_data load data success!!!");    
            } catch (Exception e) {      
                e.printStackTrace();    
            }  
        }   /**   * 查询数据   */  
        public static void getData() {    
            try {      
                Class.forName("org.apache.hive.jdbc.HiveDriver");      
                Connection con = DriverManager.getConnection("jdbc:hive2://172.20.6.38:10000/default", "root", "");      Statement stmt = con.createStatement();      
                String querySQL = "select * from sample_data limit 10";      
                ResultSet res = stmt.executeQuery(querySQL);      System.out.println("show 10 data begin---------");      
                while (res.next()) {        
                    System.out.println(res.getString(1));      
                }      
                System.out.println("show 10 data end---------");        
            } catch (Exception e) {      
                e.printStackTrace();    
            }  
        }
    }
    ```
  
    
  
    
  
  - 2.3、运行java程序
  
    右击pom.xml，选择run as，然后选择maven install：
  
      ![1](http://www.thyme.org.cn/gitblog/blog/img/7.png)
  
    出现BUILD SUCCESS字样即编译完成：
  
      ![1](http://www.thyme.org.cn/gitblog/blog/img/8.png)
  
    右击HiveDemo01.java文件，选择Run As -> Java Application:
  
     ![1](http://www.thyme.org.cn/gitblog/blog/img/9.png)
  
    执行结果如下：
  
     ![1](http://www.thyme.org.cn/gitblog/blog/img/10.png)