
## 初识HTML

#### 1. HTML概述
HTML全称为HyperText Markup Language，译为**超文本标记语言**

* 超文本包括图片、音频、视频等内容，不仅仅为纯文本内容
* 超文本还包括链接，即从一个文件跳转到另外一个文件，与世界各地主机的文件进行连接

HTML不是一种编程语言，而是一种描述性的标记语言

* 标记语言是一套标记标签。例如：标签```<a>```表示超链接、标签```<img>```表示图片、标签```<h1>```表示一级标题等等，它们都属于典型的HTML标签
* 编译语言是有编译过程的，如C++或Python等，而标记语言是没有编译过程的，HTML标签是直接由浏览器解析执行

HTML是负责描述文档语义的语言

* HTML格式的文件是一个纯文本文件，用一些标签来描述语义，这些标签在浏览器页面上无法直接看到的，故而称为**超文本标记语言**
* HTML中的标签对的作用是给文本增加不同的语义，如```<h1>```标签是给文本增加主标题的语义

## HTML的历史

**XHTML介绍：** XHTML：Extensible Hypertext Markup Language，可扩展超文本标注语言。 XHTML的主要目的是为了**取代HTML**，也可以理解为HTML的升级版。 HTML的标记书写很不规范，会造成其它的设备(ipad、手机、电视等)无法正常显示。 XHTML与HTML4.0的标记基本上一样。 XHTML是**严格的、纯净的**HTML。


## HTML的专有名词

-   网页 ：由各种标记组成的一个页面就叫网页。
-   主页(首页) : 一个网站的起始页面或者导航页面。
-   标记： 比如`<p>`称为开始标记 ，`</p>`称为结束标记，也叫标签。每个标签都规定好了特殊的含义。
-   元素：比如`<p>内容</p>`称为元素.
-   属性：给每一个标签所做的辅助信息。
-   XHTML：符合XML语法标准的HTML。
-   DHTML：dynamic，动态的。`javascript + css + html`合起来的页面就是一个 DHTML。
-   HTTP：超文本传输协议。用来规定客户端浏览器和服务端交互时数据的一个格式。SMTP：邮件传输协议，FTP：文件传输协议。

## 第一个HTML页面

#### 1. 在VS code中快速生成html的骨架



## HTML结构详解

#### 1. 快速生成HTML页面

在VS code中新建一个html文件，然后输入```！```，选择第一个选项后则自动生成如下html代码：
```html
<!DOCTYPE html>

<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>
</head>
<body>

</body>
</html>
```
在此基础上稍作修改后即可输出第一个HTML页面，使用chrome浏览器可以查看该文件

#### 2. HTML骨架标签

HTML标签通常是成对出现的（**双边标记**），比如 `<div>` 和 `</div>`；也有少部分单标签（**单边标记**），如：`<br />`、`<hr />`和`<img src="images/1.jpg" />`等

属性与标记之间、各属性之间需要以空格隔开。属性值以双引号括起来

|标签名|定义|说明|
|-------|----------|--------|
|```<html></html>```|HTML标签|页面中最大的标签，称其为根标签|
|```<head></head>```|文档的头部|注意在head标签中必须要设置的标签为title|
|```<title></title>```|文档的标题|让页面拥有一个属于自己的网页标题|
|```<body></body>```|文档的主体|元素包含文档的所有内容，页面内容基本都是放在```<body>```标签里面|

#### 3. 文档声明头

在此前快速生成的HTML代码中可以看到第一行代码为```<!DOCTYPE html>```，这就是文档声明头，即DocType Declaration，简称DTD

任何一个标准的HTML页面，第一行一定有文档声明头，即以以```<!DOCTYPE ....>```为开头的语句。**文档声明头可以告知浏览器文档使用哪种HTML或XHTML规范**

 在早期的
