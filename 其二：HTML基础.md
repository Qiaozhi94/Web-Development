
## 初识HTML

### 1. HTML概述
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

## HTML结构详解

### 1. 快速生成HTML页面

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

### 2. HTML骨架标签

HTML标签通常是成对出现的（**双边标记**），比如 `<div>` 和 `</div>`；也有少部分单标签（**单边标记**），如：`<br />`、`<hr />`和`<img src="images/1.jpg" />`等

属性与标记之间、各属性之间需要以空格隔开。属性值以双引号括起来

|标签名|定义|说明|
|-------|----------|--------|
|```<html></html>```|HTML标签|页面中最大的标签，称其为根标签|
|```<head></head>```|文档的头部|注意在head标签中必须要设置的标签为title|
|```<title></title>```|文档的标题|让页面拥有一个属于自己的网页标题|
|```<body></body>```|文档的主体|元素包含文档的所有内容，页面内容基本都是放在```<body>```标签里面|

### 3. 文档声明头

在此前快速生成的HTML代码中可以看到第一行代码为```<!DOCTYPE html>```，这就是文档声明头，即DocType Declaration，简称DTD

任何一个标准的HTML页面，第一行一定有文档声明头，即以以```<!DOCTYPE ....>```为开头的语句。**文档声明头可以告知浏览器文档使用哪种HTML或XHTML规范**

 **XHTML：Extensible Hypertext Markup Language**，可扩展超文本标注语言。 XHTML的主要目的是为了**取代HTML**，也可以理解为HTML的升级版。 HTML的标记书写很不规范，会造成其它的设备(ipad、手机、电视等)无法正常显示。 XHTML与HTML4.0的标记基本上一样。 XHTML是**严格的、纯净的**HTML。目前普遍使用了HTML5的规范，就没有了XHTML了，所以文档声明头就是```<!DOCTYPE html>```

 ### 3. 页面语言 lang
 
```html
<html lang="en">
```
上面这一行标签是用于指定页面的语言类型的。最常见的语言类型有两种：
* en：定义页面语言为英语
* zh-CN：定义页面语言为中文


### 4. 头标签 head

HTML的比较完整的骨架：
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="Content-Type" content="text/html;charset=UTF-8">
	<meta name="Author" content="">
    <meta name="Keywords" content="厉害很厉害" />
    <meta name="Description" content="网易是中国领先的互联网技术公司，为用户提供免费邮箱、游戏、搜索引擎服务，开设新闻、娱乐、体育等30多个内容频道，及博客、视频、论坛等互动交流，网聚人的力量。" />
    <title>Document</title>
</head>
<body>

</body>
</html>
```


头标签内部常见标签有以下几种：
* title：指定整个网页的标题，在浏览器的最上方显示
* base：为页面上的所有链接规定默认地址或默认目标
* meta：提供有关页面的基本信息。常见的几种meta标签如下：
	* 字符集 charset：```<meta charset="UTF-8">```
		charset即为character set的缩写，意为字符集，即网站的编码方式，绝大多数中文网站都是用utf-8的编码方式
	* 视口 viewport：```<meta name="viewport" content="width=device-width, initial-scale=1.0">```
		`width=device-width` ：表示视口宽度等于屏幕宽度。
	* 关键词 Keywords：```<meta name="Keywords" content="厉害很厉害" />```
		关键词是告诉搜索引擎该网页的功能，提高搜索的命中率
	* 页面描述 Description：```<meta name="Description" content="网易是中国领先的互联网技术公司，为用户提供免费邮箱、游戏、搜索引擎服务，开设新闻、娱乐、体育等30多个内容频道，及博客、视频、论坛等互动交流，网聚人的力量。" />```
		页面描述主要的目的是优化搜索引擎的使用效率，能更准确呈现出来想要的网页，此技术称为SEO（search engine optimization，搜索引擎优化）
	* 页面标题 title：```<title>Document</title>```
		title标签也是有助于SEO搜索引擎优化的。
	* Base标签：```<base href="/">```
		base 标签用于指定基础的路径。指定之后，所有的 a 链接都是以这个路径为基准。
* body：用于定义HTML文档所要显示的内容，称为主体内容。大部分的网站代码必须放置在此标签下。body标签的常用属性如下：
	* `bgcolor`：设置整个网页的背景颜色。
	-   `background`：设置整个网页的背景图片。
	-   `text`：设置网页中的文本颜色。
	-   `leftmargin`：网页的左边距。IE浏览器默认是8个像素。
	-   `topmargin`：网页的上边距。
	-   `rightmargin`：网页的右边距。
	-   `bottommargin`：网页的下边距。

* link：定义文档与外部资源的关系


### 5. HTML的规范
-   HTML不区分大小写，但HTML的标签名、类名、标签属性、大部分属性值建议统一用小写。
-   HTML页面的后缀名是html或者htm(有一些系统不支持后缀名长度超过3个字符，比如dos系统)

#### 1. 编写XHTML的规范：

1. 所有标记元素都要正确的嵌套，不能交叉嵌套。正确写法举例：`<h1><font></font></h1>`
2. 所有的标记都必须小写。
3. 所有的标签都必须闭合。
	-   双标签：`<span></span>`
	-   单标签：`<br>` 建议写成 `<br />` `<hr>` 建议转成 `<hr />`，还有`<img src=“URL” />`

4. 所有的属性值必须加引号。`<font color="red"></font>`
5. 所有的属性必须有值。`<hr noshade="noshade">`、`<input type="radio" checked="checked" />`
6. XHTML文档开头必须要有DTD文档类型定义。

#### 2. HTML的基本语法特性

1. HTML对换行不敏感，对tab不敏感

HTML只在乎标签的嵌套结构，嵌套的关系。谁嵌套了谁，谁被谁嵌套了，和换行、tab无关。换不换行、tab不tab，都不影响页面的结构。
也就是说，HTML不是依靠缩进来表示嵌套的，而是看标签的嵌套关系。但是，为了代码更加易读，还是尽可能要使用缩进标签。

2.  空白折叠现象
HTML中所有的**文字之间**，如果有空格、换行、tab都将被折叠为一个空格显示。

3. 标签一定要严格左右封闭


## HTML标签

### 1. 排版标签
#### 1. 标题标签 h1

标题使用`<h1>`至`<h6>`标签进行定义。`<h1>`定义最大的标题，`<h6>`定义最小的标题。具有align属性，属性值包括：left、center、right。代码为：`<h1>H1：千古壹号，永不止步</h1>`

#### 2. 段落标签 p

段落标签`<p>`可以把 HTML 文档分割为若干段落。在网页中如果要把文字有条理地显示出
来，离不开段落标签。就如同我们平常写文章一样，整个网页也可以分为若干个段落。代码为：`<p align="属性值">这是一段文字</p>`，其中属性值可以是left center right来表示段落对齐方式。

**注意**：HTML标签是分等级的，HTML将所有的标签分为两种：
-   **文本级标签**：p、span、a、b、i、u、em。文本级标签里只能放**文字、图片、表单元素**。（不能放诸如标题等元素，其中a标签里不能放a和input）
-   **容器级标签**：div、h系列、li、dt、dd。容器级标签里可以放置任何东西。

#### 3. 水平线标签 hr /

水平分隔线（horizontal rule）可以在视觉上将文档分隔成各个部分。在网页中常常看到一些水平线将段落与段落之间隔开，使得文档结构清晰，层次分明。属性值如下：
-   `align="属性值"`：设定线条置放位置。属性值可选择：left right center。
-   `size="2"`：设定线条粗细。以像素为单位，内定为2。
-   `width="500"`或`width="70%"`：设定线条长度。可以是绝对值（单位是像素）或相对值。如果设置为相对值的话，内定为100%。
-   `color="#0000FF"`：设置线条颜色。
-   `noshade`：不要阴影，即设定线条为平面显示。若没有这个属性则表明线条具阴影或立体。


#### 4. 换行标签 br /

如果希望某段文本强制换行显示，就需要使用换行标签。代码为：`这是 <br/> 一段<br/>文字`

#### 5. 分割标签 div

`<div>`标签可以把标签中的内容分割为独立的区块。**必须单独占据一行。** 代码为：
```html
<div class="header">
	<div class="logo"></div>
	<div class="nav"></div>
</div>
<div class="content">
	<div class="guanggao"></div>
	<div class="dongxi"></div>
</div>
<div class="footer"></div>
```
可以通过`align="属性值"`来设置块的位置。属性值可选择：left、right、 center。
**注意**：div在浏览器中，默认是不会增加任何的效果的，但是语义变了，div中的所有元素是一个小区域。 div标签是一个**容器级**标签，里面什么都能放，甚至可以放div自己。
一般采用div+css来实现网页的各种样式，其中div负责布局，结构与分块，css负责样式。

#### 6. 分隔标签 span

`<span>`标签与`<div>`标签的作用一致，**只是不需要换行。** 代码为：
```html
<p>
	简介简介简介简介简介简介简介简介
	<span>
		<a href="">详细信息</a>
		<a href="">购买</a>
	</span>
</p>
```
**注意**：span也是表达“小区域、小跨度”的标签，但只是一个**文本级**的标签。 就是说，span里面只能放置文字、图片、表单元素。 span里面不能放p、h、ul、dl、ol、div。

#### 7. 内容居中标签 center

`<center>`可以代表一个内容居中的标签，只是在HTML5中不建议这样使用，建议使用css布局来实现居中效果。

#### 8. 预定义（预格式化）标签 pre
`<pre>`标签指的是将保留标签内部所有的空白字符(空格、换行符)，原封不动地输出结果（告诉浏览器不要忽略空格和空行）。但是在实际使用中基本不会用到该标签，取而代之的是使用css来实现更加复杂的布局要求。

#### 9. 注释格式

HTML的注释格式为：```<!-- 我是 html 注释  -->```


### 2. 字体标签和超链接





### 3. 图片标签
