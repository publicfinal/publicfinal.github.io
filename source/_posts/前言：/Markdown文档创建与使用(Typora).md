---
title: Markdown文档创建与使用(Typora)
categories: 
	- 前言
	- Markdown文档创建与使用(Typora)
tags: ["Markdown","Typora"]

---

```
作者: 左岸小镇_梦归
企鹅: 2427419219
邮箱: publicfinal@163.com
博客: https://publicfinal.top/
备用: https://publicfinal.gitee.io/
```

# Markdown文档创建与使用(Typora)

[TOC]

<!-- more -->

## 前言

​		作为一个程序员，Markdown就像是情人一样。world文本虽美依旧敌不过情人的魅力。Markdown文档格式为.md文件。Markdown也是一种标记语言。该类型文件可使用普通编辑器打开或者编辑，例如：[记事本](https://notepad-plus-plus.org/)，[EditPlus](https://so.csdn.net/so/search?q=EditPlus&spm=1001.2101.3001.7020)，[sublime](http://www.sublimetext.com/)等等，当然了，也有更专业的编辑器，例如我现在正在使用的——Typora。

[Typora](https://typoraio.cn) https://typoraio.cn/

## md文件的书写格式

### 标题 

> #一级标题
>
> ##二级标题
>
> ###三级标题
>
> ####四级标题
>
> #####五级标题
>
> ######六级标题

快捷键：Ctrl+1~6

### 列表

* 有序列表

> 1. 有序列表
> 2. 有序列表

输入“1.+空格”  后面输入内容换行

* 无序列表

```
* 无序列表
+ 无序列表
- 无序列表
```

* 无序列表
+ 无序列表

- 无序列表

### 引用

```
> +空格
```

>这是引用文本段

换行后 shift+tab 可以快速退出引用。

### 分割线

```
***
---
___ 三个连续的* 或- 或_

```

***

---

___

### 链接

```
[url描述](url)
```

[记事本](https://notepad-plus-plus.org/)

### 图片

```
![](图片url)
```

![](../../imgae/Markdown文档创建与使用(Typora)/image-20220730130917194.png)

### 代码框

~~~apl
​~~~+换行    #表示代码框，可以在换行前声明代码语言 
```+换行
~~~

```java

```

### 强调作用

```
**字体加粗**
__字体加粗__
*倾斜*
_倾斜_
~~删除~~
```

**字体加粗**
__字体加粗__
*倾斜*
_倾斜_
~~删除~~

### 表格

```
插入两行两列的表格
|      |      |
| ---- | ---- |
|      |      |
建议使用Typora右键插入
```



|      |      |
| ---: | :--: |
|      |      |

### 公式

```
$$
999+iiii
$$
```


$$
999999+iiii
$$

### 复选框

```
- [] +空格 
```

- [ ] 

- [x] 

### 目录

```
[TOC] #自动生成文档目录
```

### 语义化标签(md支持使用html标签)

```
<h1> 标题1</h1>
<h2> 标题2</h2>
<h3> 标题3</h3>
<h4> 标题4</h4>
<h5> 标题5</h5>
<h6> 标题6</h6>
```

<h1> 标题1</h1>
<h2> 标题2</h2>
<h3> 标题3</h3>
<h4> 标题4</h4>
<h5> 标题5</h5>
<h6> 标题6</h6>

| 序号 | 标签      | 名字 | 描述                                               |
| ---- | --------- | ---- | -------------------------------------------------- |
| 1    | <h1>-<h6> | 标题 | 通常用来划分或标注内容中的文本段落                 |
| 2    | <header>  | 页眉 | 一般是有导航，logo等元素组成                       |
| 3    | <footer>  | 页脚 | 一般是由友情链接，联系方式，备案号，版权等纤细组成 |
| 4    | <nav>     | 导航 | 导航通常是由一个或者多个链接标签<a>标签组成        |
| 5    | <main>    | 主体 | 展示页面主体内容，建议一个页面只出现一次           |
| 6    | <article> | 文档 | 本义是文档，实际上可以充当其他内容的容器           |
| 7    | <aside>   | 边栏 | 与主体无关的信息（广告位，相关推荐，阅读排行等）   |
| 8    | <section> | 区块 | 文档或主体中的通用小组件                           |
| 9    | <div>     | 容器 | 本身无任何语义，通过它的属性来描述用途             |



<!DOCTYPE>
<html lang="en">
<head>
<meat chatset="UTF-8" />
<meat name="viewport"  />
<!--标题内容-->
<title>第一次作业</title>
<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  width: 100vw;
  height: 100vh;
  display: grid;
  grid-template-rows: 60px 1fr 60px;
  gap: 10px;
}
header,
footer {
  height: 80px;
  background-color: lightgreen;
  text-align: center;
}
.container {
  display: grid;
  grid-template-columns: 200px 1fr;
  gap: 10px;
  padding: 10px;
  background-color: lightskyblue;
}
.container > aside {
  background-color: lightcyan;
  text-align: center;
}
.container > main {
  display: grid;
  grid-template-rows: 1fr 200px;
  background-color: wheat;
  text-align: center;
  padding: 10px;
}
.container > main > div {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px;
}
main div section {
  background-color: violet;
}
</style>
</head>
<body>
<!--页眉-->
<header>
<h4>&lt这里面输入你想要的页眉即可&gt（&lt是左括号<；&gt是右括号>）</h4>
</header>
<!--边栏-->
<aside>
<h3>&lt这里面输入你的边栏内容即可&gt</h3>
</aside>
<!--主体-->
<main>
<h2>&lt这里面输入你的主体内容即可&gt</h2>
</main>
<!--区块-->
<div>
<section>
<h2>区块1</h2>
</section>
<section>
<h2>区块2</h2>
</section>
</div>
<!--页脚-->
<footer>
<h2>这里面输入你的页脚内容即可，一般是友情链接或ICP备案号等</h2>
</footer>
</body>
</html>







