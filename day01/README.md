# Java_Network_Front_End

## Day 01  HTML

[TOC]

### 1. HTML 简介

> ​		`HTML(HyperText Mark-up Language)`即 **超文本标记语言**，是目前网络上应用最为广泛的语言，**也是构成网页文档的主要语言**。`HTML文本`是由`HTML命令(标签)`组成的描述性文本，`HTML命令`可以说明文字、图 形、动画、声音、表格、链接等。`HTML`的结构包括`头部（Head）`、`主体（Body）`两大部分，其中头部描述浏览器所需的信息，而主体则包含所要说明的具体内容。



#### 1.1 互联网三大基石

> ​		`HTML语言`被称为 **互联网的三大基石之一** (其余两大基石分别为：`HTTP协议`、`URL`)。它解决了如何以丰富的效果展示数据内容的问题。互联网中，数据是在服务器和浏览器之间互相传送和执行。三大基石分别解决了如下问题：
>
> - `HTTP协议`：解决了服务器和浏览器之间数据如何传送、传送格式的问题！实现了分布式的信息共享。
> - `URL协议`：解决了众多服务器中资源定位问题。从而让浏览器可以访问不同的服务器资源，实现了全球信息的精确定位。
> - `HTML语言`：解决了数据在浏览器中如何丰富多彩的展示，及如何合理标示信息的问题。



#### 1.2 HTML 基本规范

>基本概念总结：
>
>- `HTML` 指的是`超文本标记语言 (Hyper Text Markup Language)`
>- **HTML 不是一种编程语言，而是一种标记语言 (markup language)**
>- 标记语言是一套`标记标签 (markup tag)`
>- HTML 使用标记标签来描述网页
>- **HTML语言不区分大小写！**
>
>HTML标记标签通常被称为 `HTML 标签 (HTML tag)`。



------



### 2. HTML 标签



#### 2.1 常用标签

- `<head>`

> <head> 元素是所有头部元素的容器。
>
> <head> 元素必须包含文档的标题（title），可以包含脚本、样式、meta 信息 以及其他更多的信息。
>
> 以下列出的元素能被用在 <head> 元素内部：
>
> 1. `<title>`  (在头部中，这个元素是必需的)。
> 2. `<style>`
> 3. `<base>` 等。
>
> 
>
> - 测试代码
>
> ```html
> <head>
> <--!-->1. 在标题栏上显示。 2.告诉搜索引擎本文档的主题。一般不要超过28个字符.
> <title>典型的head</title> 
>     
> <meta http-equiv="Content-Type" content="text/html; charset=gb2312" />
> <meta name="author" content="zhangsan">
>     
> <--!-->浏览器差异的问题</--!-->
> <meta http-equiv="pragma" content="no-cache">
> <meta http-equiv="cache-control" content="no-cache">
>     
> <meta http-equiv="expires" content="0">
> <meta http-equiv="expires" content="0">
> <meta name="keywords" content=“JAVA,学习,培训 ">
> <meta name="description " content=“关于北京地区java培训的介绍">
>     
> <--!-->5秒后跳转到163.com  如果只写5，表示每5秒刷新一次。
> <meta http-equiv="refresh" content="5;URL=http://www.163.com">
> <link rel="stylesheet" type="text/css" href="css/pagination.css" />
> <script type="text/javascript" src="js/search.js"></script>
> </head>
> ```



- `<hx>` 标题标记

> ​		`<h1>、<h2>、<h3>、<h4>、<h5>、<h6>`,作为标题使用，并且依据重要性递减。`<h1>`是最高的等级。例如: 
>
> ```html
> <h1>文档标题</h1> 
> 
> <h2>次级标题</h2>
> 
> <--!搜索引擎比较重视<hx>标记中的内容。-->
> ```
>
> 

- `<b> <i> <u> <del>` 文本标记

> ```html
> <b>粗体显示
> 
> <i>斜体显示
> 
> <u>下划线显示
> 
> <del>中划线显示(删除效果)
> ```

- `<pre> `预格式文本 

> ```html
> hc+o<sub>2</sub> = co<sub>2</sub>
> 
> x<sup>2</sup> + y<sup>2</sup> = z<sup>2</sup>
> ```



#### 2.2 要掌握的标签



##### 2.2.1 	`<font>` 字体标签

> `<font>` 规定文本的字体、字体尺寸、字体颜色。比如：
>
> ```html
> <font size = "3" color="red"> hi </font>
> <font face="verdana" color="green"> hi2 </font>
> ```



##### 2.2.2 	`<br> 或者 <br/>`  换行

> ```html
> <--使用  <br/> 更通用!-->
> ```



##### 2.2.3 	`<hr>` 水平线

> ```html
> <hr> <--!标签在 HTML 页面中创建一条水平线。-->
> <--!如果是百分比，会随着窗口的变化，宽度也发生变化。像素值的话，窗口大小发生变化，水平线宽度也不发生变化。----></--!如果是百分比，会随着窗口的变化，宽度也发生变化。像素值的话，窗口大小发生变化，水平线宽度也不发生变化。---->
> <hr width="50%" color = "red"> 
>  
> ```



##### 2.2.4  	字符实体 `&nbsp`  `&lt` 等

| **显示结果** | **描述**       | **实体名**   | **实体号** |
| ------------ | -------------- | ------------ | ---------- |
|              | 不可拆分的空格 | &nbsp;       | &#160;     |
| **<**        | 小于           | &lt;         | &#60;      |
| **>**        | 大于           | &gt;         | &#62;      |
| **&**        | **and符号**    | **&amp;**    | **&#38;**  |
| **"**        | **引号**       | **&quot;**   | **&#34;**  |
| **£**        | **英镑**       | **&pounds;** | **&#163;** |



##### 2.2.5  	`<a>` 超链接

> ```html
> <--!-->超链接</--!-->
> <a href="http://www.baidu.com/">百度</a>
> 
> <--!>图片作为超链接</--!>
> <a href="http://www.baidu.com/">
> 	<img border ="0" src=".\images\next.gif">
> </a>
> 
> <--!-->target 属性（定义从什么地方打开链接地址）
>     	_blank 重新打开一个窗口 打开链接
>         _self  从当前的页面打开
> </--!>
> <a href=:"http://www.163.com/" target="_blank">163!</a>
> 
> <--!-->锚标签和name属性,命名一个锚点：</--!-->
> <a name="label">头部</a>
> 
> <--!-->链接到锚点：</--!-->
> <a href=”#label”>回到头部</a>
> 
> ```



##### 2.2.6	`<img>` 图像标签

> 1. `src`:源文件地址.    2. `width`:宽度.   3. `height`: 高度   4. `alt` :说明文字
> 2. **注意：**
>    - 一般建议都增加`alt属性`，这样有利于搜索引擎的搜索。
>    - 虽然可以使用`width、height`调整图像的大小，但是实际编程时，最好还是通过后台程序将图片进行缩放处理。



##### 2.2.7	`<embed>` 内嵌   `<video>`  `<iframe>`

> - `<embed>标记`用于在页面中嵌入多媒体文件，但是用户计算机上需要事先安装相应的处理程序。
>
> - 常用嵌入式文档的格式：`mp3, mid, wma, asf, swf, flv, rm, ra, ram, avi`.
>
> 
>
> - `autostart`:是否自动播放嵌入的文件。
>
>   `loop`:是否循环播放。也可以取数字，表明循环多少次。
>
>   `hidden`:是否显示播放器。
>
> ```html
> <embed src="ee.wmv" autostart="true" loop='true' 
>        hidden='false' width="100px" height="100px"/>
> ```
>
> - **播放器**
>
> ```html
> <!--html5  中使用video标签-->
> <video src="../video/aa.mp4" controls="controls"></video>
> ```
>
> ```html
> <iframe height=498 width=510 
> 	src='http://player.youku.com/embed/XNDI1ODU2MDI4MA==' 
>     frameborder=0 'allowfullscreen'>
> </iframe>
> ```



##### 2.2.8 	`<ul><li><ol>` 列表标签

> - `<ul> 标签定义无序列表。ul标签内部一般只存放li标签`
>
> ```html
> <ul>
>   <li>Coffee</li>
>   <li>Tea</li>
>   <li>Milk</li>
> </ul>
> ```
>
> - `<ol> 标签定义有序列表。`
>
> ```html
> <ol>
>   <li>Coffee</li>
>   <li>Tea</li>
>   <li>Milk</li>
> </ol>
> ```
>
> - **注：列表标签经常跟`CSS`结合，制作菜单导航！**



##### 2.2.9 	`<table><tr><td><th> 表格标签`

> - `<table>标签定义 HTML 表格.`
> - 简单的 `HTML 表格`由 `table` 元素以及一个或多个 `tr、th 或 td` 元素组成。
> - **`tr 元素`定义表格行，`th 元素`定义表头，`td 元素`定义表格单元。**
>
> ```html
> <!--表格练习-->
> <！-->
> 	border 边框
>     align  表格在页面中居中
>     cellspacing=0 不要内框
>     bgcolor 表格背景颜色
> </！-->
> <table border="1" align="center" cellspacing="0" bgcolor="#7fffd4">
> <tr>
>     <td colspan="2">第一行第一列</td> <td>第一行第三列</td> <td>第一行第四列</td>
> </tr>
> <tr>
>      <td>第二行第一列</td>  <td>第二行第二列</td> 
>      <td>第二行第三列</td>  <td>第二行第四列</td>
> </tr>
> <tr>
>     <td rowspan="2">第三行第一列</td> <td>第三行第二列</td> 
>     <td colspan="2" rowspan="2">第三行第三列</td>
> </tr>
> <tr>
>     <td>第四行第二列</td>
> </tr>
> </table>
> ```



##### 2.2.10 `<div>` 块元素

>- `<div>`可定义文档中的分区或节，域标签（division/section）。
>- `<div>`标签可以把文档分割为独立的、不同的部分。它可以用作严格的组织工具，并且不使用任何格式与其关联。
>- `<div> `是一个块级元素。这意味着它的内容自动地开始一个新行。
>- 如果与 CSS 一同使用，<div> 元素可用于对大的内容块设置样式属性。
>- `<div> `元素的另一个常见的用途是文档布局。它取代了使用表格定义布局的老式方法。使用 `<table> 元素`进行文档布局不是表格的正确用法。`<table> `元素的作用是显示表格化的数据。
>
>
>
>- **块级标签：不管内容长度多少，都会占满一行。**
>  - 比如：` <b>, <h1>, <p>, <ul>, <table>`



##### 2.2.11 `<span>` 行内（内联）元素

> - **`HTML <span> 元素`是内联元素，可用作文本的容器。`<span>` 元素也没有特定的含义**



##### 2.2.12 `<frameset><frame><iframe>`框架标签

> - `frameset 元素`可定义一个框架集。它被用来组织多个窗口（框架）。每个框架存有独立的文档。在其最简单的应用中，`frameset 元素`仅仅会规定在框架集中存在多少列或多少行。必须使用 `cols 或 rows 属性`。
>
> - **注意：**  使用`frameset` 不能添加 `body标签 `。
>
> ```html
> <frameset rows="20%,60%,20%">      <--!-->各文件占用页面的比例</--!-->
>         <frame src="head.html" />  <--!-->引用别的html文件</--!-->
>         <frame src="body.html" />
>         <frame src="foot.html" />
> </frameset>
> ```



##### 2.2.13 表单标签（重点）`<form>`

> - `action 属性` : 定义在提交表单时执行的动作。向服务器提交表单的通常做法是使用提交按钮。
>   - 通常，表单会被提交到`web` 服务器上的网页。
> - `method 属性`规定在提交表单时所用的`HTTP 方法（GET 或 POST）`.

- 测试代码

> - 文本框
> - 密码框
> - 单选框
> - 多选框
> - 复选框
> - 下拉列表
> - 多行文本
> - 重置按钮 提交按钮
>
> ```html
> <!DOCTYPE html>
> <html lang="en">
> <head>
>     <meta charset="UTF-8">
>     <title>注册</title>
> </head>
> <body>
>     <form action="../../0A2第二阶段课堂视频代码/day01-最终版/案例/firstProject11.4/test1.html" method="get">
>     <--!-->文本框</--!-->
>     账号：<input type="text" value="请输入账号" name="username"><br>    
>         
>     <--!-->密码框</--!-->    
>     密码：<input type="password" name="password"><br>    
>         
>     <--!-->单选框</--!-->    
>     性别：<input type="radio" name="gender" value="1" id="nan" checked>                 <label for="nan">男 </label>
>           <input type="radio" name="gender" value="0" id="nv">
>           <label for="nv">女 </label><br>  
>         
>     <--!-->复选框</--!-->     
>     爱好：<input type="checkbox" name="favorite" checked> Java
>           <input type="checkbox" name="favorite"> PHP
>           <input type="checkbox" name="favorite"> C#  <br>
>     
>     <--!-->下拉列表</--!-->     
>     地区：<select name="city" >
>             <option selected>广东</option>
>             <option value="2">广西</option>
>             <option value="3">北京</option>
>          </select><br>
>      
>      <--!-->多行文本</--!-->    
>      个人简介：<textarea name="persontext" rows="2" cols="20"></textarea><br>
>      
>      <--!-->重置按钮  提交按钮</--!-->    
>      <input type="reset" name="reset">
>      <input type="submit" name="submit" value="注册">
>      <input type="button" name="button1" title="按钮">
>     </form>
> </body>
> </html>
> ```





