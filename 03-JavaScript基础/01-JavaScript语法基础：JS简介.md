

> 本文最初发表于[博客园](https://www.cnblogs.com/smyhvae/p/8303507.html)，并在[GitHub](https://github.com/smyhvae/Web)上持续更新**前端的系列文章**。欢迎在GitHub上关注我，一起入门和进阶前端。

> 以下是正文。

## JavaScript简介

Web前端有三层：

- HTML：从语义的角度，描述页面**结构**

- CSS：从审美的角度，描述**样式**（美化页面）

- JavaScript：从交互的角度，描述**行为**（提升用户体验）

JavaScript是世界上用的最多的**脚本语言**。

### 发展历史

JavaScript诞生于**1995年**。布兰登 • 艾奇（Brendan Eich，1961年～），1995年在网景公司，发明的JavaScript。

JavaScript是由**网景**公司发明，起初命名为LiveScript，后来由于SUN公司的介入更名为了JavaScript

> 备注：由于当时Java这个语言特别火，所以为了傍大牌，就改名为JavaScript。如同“北大”和“北大青鸟”的关系。“北大青鸟”就是傍“北大”大牌。

同时期还有其他的网页语言，比如VBScript、JScript等等，但是后来都被JavaScript打败了，所以现在的浏览器中，只运行一种脚本语言就是JavaScript。

### JavaScript和ECMAScript的关系

ECMAScript是一种由Ecma国际（前身为欧洲计算机制造商协会,英文名称是European Computer Manufacturers Association）制定和发布的脚本语言规范。

JavaScript是由公司开发而成的，问题是不便于其他的公司拓展和使用。所以欧洲的这个ECMA的组织，牵头制定JavaScript的标准，取名为ECMAScript。

简单来说，**ECMAScript不是一门语言，而是一个标准**。符合这个标准的比较常见的有：JavaScript、Action Script（Flash中用的语言）。就是说，你JavaScript学完了，Flash中的程序也就轻而易举了。

ECMAScript在2015年6月，发布了ECMAScript 6版本，语言的能力更强（也包含了很多新特性）。但是，浏览器的厂商不能那么快去追上这个标准。

### JavaScript的发展：蒸蒸日上

2003年之前，JavaScript被认为“牛皮鲜”，用来制作页面上的广告，弹窗、漂浮的广告。什么东西让人烦，什么东西就是JavaScript开发的。所以浏览器就推出了屏蔽广告功能。

2004年，JavaScript命运开始改变，那一年，**谷歌公司开始带头使用Ajax技术**，Ajax技术就是JavaScript的一个应用。并且，那时候人们逐渐开始提升用户体验了。Ajax有一些应用场景。比如，当我们在百度搜索框搜文字时，输入框下方的智能提示，可以通过Ajax实现。比如，当我们注册网易邮箱时，能够及时发现用户名是否被占用，而不用调到另外一个页面。

2007年乔布斯发布了第一款iPhone，这一年开始，用户就多了上网的途径，就是用移动设备上网。
**JavaScript在移动页面中，也是不可或缺的**。并且这一年，互联网开始标准化，按照W3C规则三层分离，JavaScript越来越被重视。

2010年，人们更加了解**HTML5技术**，**HTML5推出了一个东西叫做Canvas**（画布），工程师可以在Canvas上进行游戏制作，利用的就是JavaScript。

2011年，**Node.js诞生**，使JavaScript能够开发服务器程序了。

如今，**WebApp**已经非常流行，就是用**网页技术开发手机应用**。手机系统有iOS、安卓。比如公司要开发一个“携程网”App，就需要招聘三队人马，比如iOS工程师10人，安卓工程师10人，前端工程师10人。共30人，开发成本大；而且如果要改版，要改3个版本。现在，假设公司都用web技术，用html+css+javascript技术就可以开发App。也易于迭代（网页一改变，所有的终端都变了）。

虽然目前WebApp在功能和性能上的体验远不如Native App，但是“WebApp慢慢取代Native App”很有可能是未来的趋势。


## JavaScript编程相关

### JavaScript入门易学性

- JavaScript对初学者比较友好。

- JavaScript是有界面效果的（比如C语言只有白底黑字）。

- JavaScript是**弱变量类型**的语言，变量只需要用var来声明。而Java中变量的声明，要根据变量的类型来定义。

比如Java中需要定义如下变量：

```java
	int a;
	float a;
	double a;
	String a;
	boolean a;
```

而JavaScript中，只用定义一个变量：

```JavaScript
	var a;
```

- JavaScript不用关心其他的一些事情（比如内存的释放、指针等），更关心自己的业务。

### 浏览器工作原理

![](http://img.smyhvae.com/20180124_1700.png)

1、User Interface  用户界面，我们所看到的浏览器

2、Browser engine  浏览器引擎，用来查询和操作渲染引擎

3、Rendering engine 用来显示请求的内容，负责解析HTML、CSS

4、Networking   网络，负责发送网络请求

5、JavaScript Interpreter(解析者)   JavaScript解析器，负责执行JavaScript的代码

6、UI Backend   UI后端，用来绘制类似组合框和弹出窗口

7、Data Persistence(持久化)  数据持久化，数据存储  cookie、HTML5中的sessionStorage

参考链接：<https://www.2cto.com/kf/201202/118111.html>

### JavaScript是前台语言

JavaScript是前台语言，而不是后台语言。

JavaScript运行在用户的终端网页上，而不是服务器上，所以我们称为“**前台语言**”。就是服务于页面的交互效果、美化，不能操作数据库。

**后台语言**是运行在服务器上的，比如PHP、ASP、JSP等等，这些语言都能够操作数据库，都能够对数据库进行“增删改查”操作。Node.js除外。

### JavaScript的组成

JavaScript基础分为三个部分：

- ECMAScript：JavaScript的语法标准。包括变量、表达式、运算符、函数、if语句、for语句等。

- **DOM**：文档对象模型，操作**网页上的元素**的API。比如让盒子移动、变色、轮播图等。

- **BOM**：浏览器对象模型，操作**浏览器部分功能**的API。比如让浏览器自动滚动。

PS：JS机械重复性的劳动几乎为0，基本都是创造性的劳动。而不像HTML、CSS中margin、padding都是机械重复劳动。

### JavaScript的特点

（1）简单易用：可以使用任何文本编辑工具编写，只需要浏览器就可以执行程序。

（2）**解释型语言**：事先不需要被编译为机器码再执行，逐行执行、无需进行严格的变量声明。

> 由于少了编译这一步骤，所以解释型语言开发起来尤为轻松，但是解释型语言运行较慢也是它的劣势。不过解释型语言中使用了JIT技术，使得运行速度得以改善。

（3）基于对象：内置大量现成对象，编写少量程序可以完成目标

### 编程语言的分类

- 解释型语言：**边解析边执行**，不需要事先编译。例如：JavaScript、php。

- 编译型语言：事先把所有的代码翻译成计算机能够执行的指令，然后整体执行。例如：c、c++。

## 开始写第一行JavaScript代码

### JavaScript代码的书写位置

（1）内嵌的方式：

页面中，我们可以在`<body>`标签里放入`<script type=”text/javascript”></script>`标签对儿，并在`<script>`里书写JavaScript程序：

```
		<script type="text/javascript">

		</script>
```

text表示纯文本，因为JavaScript也是一个纯文本的语言。

PS：在Sublime Text里，输入`<sc`后，按tab键，可以自动补齐。

（2）外链式：引入外部JavaScript文件（放到body标签里，可以和内嵌的js代码并列）

```
	<script src="tool.js"></script>
```

### alert语句

我们要学习的第一个语句，就是alert语句。

```
		<script type="text/javascript">
			alert("生命壹号");
		</script>
```

**alert**（英文翻译为“警报”）的用途：**弹出“警告框”**。

`alert("")`警告框的效果如下：

![](http://img.smyhvae.com/20180116_1735.gif)

这个警告框，在IE浏览器中长这样：

![](http://img.smyhvae.com/20180116_1906.png)

上面的代码中，如果写了两个alert()语句的话，网页的效果是：弹出第一个警告框，点击确定后，继续弹出第二个警告框。

### 语法规则

学习程序，是有规律可循的，就是程序是有相同的部分，这些部分就是一种规定，不能更改，我们成为：语法。

（1）JavaScript对换行、缩进、空格不敏感。每一条语句以分号结尾。

也就是说：

代码一：

```
		<script type="text/javascript">
			alert("今天蓝天白云");
			alert("我很高兴");
		</script>
```

等价于代码二：

```
		<script type="text/javascript">
			alert("今天蓝天白云");alert("我很高兴");
		</script>
```

备注：每一条语句末尾要加上分号，虽然分号不是必须加的，如果不写分号，浏览器会自动添加，但是会消耗一些系统资源。

（2）所有的符号，都是英语的。比如**括号**、引号、分号。

如果你用的是搜狗拼音，**建议不要用shift切换中英文**（可以在搜狗软件里进行设置），不然很容易输入中文的分号；建议用ctrl+space切换中英文输入法。

（3）严格区分大小写

### 注释

我们不要把html、CSS、JavaScript三者的注释格式搞混淆了。

（1）**html的注释：**

```html
<!-- 我是注释  -->
```

（2）**CSS的注释：**

```html
<style type="text/css">

	/*
		我是注释
	*/

	p{
		font-weight: bold;
		font-style: italic;
		color: red;
	}

</style>
```

注意：CSS只有`/*  */`这种注释，没有`//`这种注释。而且注释要写在`<style>`标签里面才算生效哦。

（3）**JavaScript的注释：**

单行注释：

```
// 我是注释
```

多行注释：

```
/*
	多行注释1
	多行注释2
*/
```

备注：sublime中，单行注释的快捷键是`ctrl+/`，多行注释的快捷键是`ctrl+shift+/`。

## Javascript 网页中输出信息的写法

### 弹出警告框：alert("")

我们在上一段讲到了alert语句，这里不再赘述。

### 控制台输出：console.log("")

`console.log("")`表示在控制台中输出。console表示“控制台”，log表示“输出”。

控制台在Chrome浏览器的F12中。控制台是工程师、程序员调试程序的地方。程序员经常使用这条语句输出一些东西，来测试程序是否正确。

`console.log("")`效果如下：

![](http://img.smyhvae.com/20180116_2008.gif)

普通人是不会在意控制台的，但是有些网站另藏玄机。有个很有意思的地方是，百度首页的控制台，悄悄地放了一段招聘信息：

![](http://img.smyhvae.com/20180116_2010.png)

毕竟做前端的人是经常使用控制台的。

接下来，我们开始学习JavaScript语法。

### 用户输入：prompt()语句

`prompt()`就是专门用来弹出能够让用户输入的对话框。用得少，测试的时候可能会用。

JS代码如下：

```javascript
			var a = prompt("请随便输入点什么东西吧");
			console.log(a);
```

上方代码中，用户输入的内容，将被传递到变量 a 里面。

效果如下：

![](http://img.smyhvae.com/20180116_2230.gif)

**prompt()语句中，用户不管输入什么内容，都是字符串。**

**alert和prompt的区别：**

```javascript
	alert("从前有座山");                //直接使用，不需要变量
	var a = prompt("请输入一个数字");   // 必须用一个变量，来接收用户输入的值
```

## 我的公众号

想学习<font color=#0000ff>**代码之外的软技能**</font>？不妨关注我的微信公众号：**生命团队**（id：`vitateam`）。

扫一扫，你将发现另一个全新的世界，而这将是一场美丽的意外：

![](http://img.smyhvae.com/2016040102.jpg)

