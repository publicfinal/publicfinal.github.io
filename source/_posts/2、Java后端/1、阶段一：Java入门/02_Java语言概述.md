---
title: 02-Java语言概述
categories: 
	- Ⅱ、Java后端
	- 1、阶段一：Java入门
	- 02-Java语言概述
tags: ["java历史"]
---

```
作者: 左岸小镇_梦归
企鹅: 2427419219
邮箱: publicfinal@163.com
博客: https://publicfinal.top/
备用: https://publicfinal.gitee.io/
```



## 第一章 Java语言的历史发展

<!-- more -->

```
硬件的发展 -- 廉价的单片式微控制器 -- 用于智能化家居

1991年成立Green小组(詹姆斯·高斯林任组长),专攻计算机在家电领域的嵌入式应用
1992年夏Oak开发功能(根据C++语言改造),Oak开发成功之后需要硬件厂家支持,但是硬件厂家没同意(因为Oak没人用)Oak直接凉了
1995年互联网蓬勃发展,那时候需要一种语言可以在网络上传输,并且给页面增加动态效果,Green小组成员发现Oak可以完成这样的要求,并且当初设计的时候这门语言也比较小适合在网络上传输,所以对Oak语言一顿修改,重命名为Java,并且在Sun World大会上亮相被认可(IBM,微软,HP..)
1996年1月 Sun公司发布了Java的第一个开发工具包（JDK1.0）
1997年2月 JDK1.1
1999年6月 JDK1.2
	J2ME（Java2 Micro Edition Java2平台的微型版）应用于嵌入式、无线领域
	J2SE（Java2 Standard Edition Java2平台的标准版）应用于桌面环境,现在已经被Android应用和IOS应用取代
	J2EE（Java 2Enterprise Edition Java 2平台的企业版）应用于基于Java的应用服务器,以后的学习方向
2000年5月 JDK1.3、JDK1.4
2004年9月 JDK5(从原来的1.x版本编程了x版本) 里程碑版本,增加了很多实用功能
2005年6月 JDK6
2009年    甲骨文(Oracle)公司宣布收购Sun
2011年    JDK7
2014年    JDK8(JDK8版本开始部分收费 JDK8u211及以上版本开始收费,以下版本依然免费) 当前国内使用的版本
2017年9月 JDK9 收费
2018年3月 JDK10 收费
...
当前(2021年) JDK16 收费
...
当前(2021年) JDK17 免费
```

## 第二章 Java语言的优势

### 第1节 Java语言应用

```
Java语言的职业方向
1. Android系统应用早期是用Java语言开发的,当然现在也可以使用,不过现在有替代语言Kotlin
2. 很多大数据相关框架都是使用Java语言开发的,比如hadoop，Hbase，Elasticsearch等
3. 在应用领域很多软件的后台服务都是基于Java开发
	3.1 电商领域(淘宝、京东...)
	3.2 金融领域(支付宝、银行...)
	3.3 软件工具(Eclipse...)
	3.4 国内的各个领域(政府、金融、保险、医疗、教育...)Java占着举足轻重的地位

打开我们的手机,里面的APP软件大部分后台都是Java语言编写的.
```

### 第2节 Java语言特点

```
1. 简单性
2. 面向对象
3. 分布性
4. 健壮性
5. 安全性
6. 跨平台
...
```

## 第三章 Java语言的环境搭建

```
Java官方提供了Java语言的开发工具包叫JDK,所以我们只需要去官网下载官方提供的JDK开发工具集即可进行Java语言开发

JDK(Java Development Kit)Java开发工具包,工具包中包含了开发Java语言的各种工具以及运行Java软件的环境等
```

<img width="450" align="center" src="https://note.youdao.com/yws/api/personal/file/WEBdaa9087635d58b139be4d6b7a2dfeaf9?method=download&shareKey=73a434c86ec63645b819d2efc01ae39c">

* 下载地址

```
https://www.oracle.com/java/technologies/downloads/
```

* 安装

```
傻瓜式安装
注意: 安装路径不能有中文,不能有空格,不需要额外安装jre(Java运行时环境)
```

* 安装目录介绍

<img width="600" alitn="center" src="https://note.youdao.com/yws/api/personal/file/WEB46e65b155fd784526a889d04673cf545?method=download&shareKey=9c57ce9c71cabbbfb0ad318b8d164027">

* 环境变量配置

```
1. 设置变量 JAVA_HOME=JDK安装路径,精确到bin目录的上一级
2. 将JAVA_HOME添加到Path路径下 %JAVA_HOME%\bin;

注意:
1. JAVA_HOME 必须全部大写
2. JAVA_HOME 两个单词中间是下划线而非减号
3. %XXX% 百分号是windows系统中取变量值的一种语法 
```

* 测试

```
在DOS命令行窗口中执行 java -version 命令. 如果打印出jdk的版本,说明安装成功.
```

## 第四章 第一个Java软件

* 软件开发工具介绍

```
Windows自带的文本文档
notepad++ (后改名为 notepad-plus)
Eclipse
IntelliJ IDEA
...
```

* 编写第一个Java软件的注意事项

```
1. 创建一个文本文件,文件的格式以.java结尾
2. 文件的名字理论上可以随意命名,但是这里强调不能使用中文,只能使用 0-9、a-z、A-Z、_、$ 不能使用其他
3. 文件名字不能以数字开头
4. 在起文件名字时,英文单词的首字母必须大写,多英文单词的时候首字母也一定要大写 eg: XxxYyyZzz
```

* 代码编写

```java
public class HelloWorld{
	public static void main(String[] args){
		System.out.println("HelloWorld");
	}
}
```

## 第五章 Java软件的运行流程

```
1. 首先Java语言是高级语言,高级语言编写的代码是不能直接被计算机解析和运行的(计算机只认识0和1)
2. 所以首先就是对我们编写的代码进行处理(编译),处理成可以被计算机认识的形式
3. 编译 javac XxxYyyZzz.java 将.java的源文件编译成XxxYyyZzz.class字节码文件
4. 运行 java XxxYyyZzz  -- 将其加载到JVM虚拟机的内存中由CPU解析和运行
```

<img width="700" align="center" src="https://note.youdao.com/yws/api/personal/file/WEB4cf28e123fcaf24959991d947af085f6?method=download&shareKey=9a37def37a7dbd7751c14799b6abd74c">



## 第六章 Java的注释

```
//单行注释
/* 
 * 多行注释
 */
/**
 * 文档型注释/多行注释/Java语言独有的
 */
jdk提供了对文档注释的操作使用javadoc命令可以生成java文档
eg: 
javadoc  -d C:\Users\Administrator\Desktop\d  -encoding utf-8  HelloWorld.java
```

## 第七章 软件的运行流程

* 计算机软件的运行流程

```
比如在你的D盘安装了一个QQ
鼠标双击QQ运行这个QQ软件 -- 将硬盘里面的QQ软件加载到内存中
加到到内存之后CPU开始读取内存中QQ软件的每一行代码
```

* Java软件的运行流程

```
以HelloWorld.java为例

使用java命令运行.class字节码文件时
使用java命令执行.class字节码文件  --  将字节码文件通过JVM加载到内存中
加载到内存中之后CPU开始一行行进行Java代码的解析

这就是Java软件运行的流程,其实所有的计算机软件运行流程都是一样的...
```

<img width="600" align="center" src="https://note.youdao.com/yws/api/personal/file/WEB83ebdb444e5faa547b63fed8e4082a4c?method=download&shareKey=259472074d1ff521df8cf13fe510fc6c"> 
