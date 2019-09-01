HTML5基础知识、核心技术和前沿案例笔记



## 第一章

1、transform 属性设置translateY的值，使container在Y轴方向上移动



```css
#container {
	width: 100%;
	text-align: center;
	position: absolute;
	top: 50%;
	transform: translateY(-50%);
	-ms-transform: translateY(-50%); /* IE 9*/
	-moz-transform: translateY(-50%); /* Firefox */
	-webkit-transform: translateY(-50%); /* Safari Chrome */
	-o-transform: translateY(-50%); /* Opera */
}
```

2、
```css
a {
	font-size: 18px;
	color: #fff;
	border: 1px solid #fff;
	border-radius: 3px;
	padding: 10px 100px;
	text-decoration: none;
}
```
![image.png](https://upload-images.jianshu.io/upload_images/7572791-44b59218f77f2d99.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

3、script 最好的做法是将其置于body底部，以尽可能提高加载速度，并且避免JavaScript代码的提前解析执行。


## 第二章
### 2.1 HTML代码基础
1、常见的非内容标签包括<meta>、<img>、<br>、<hr>、<input>、<link>、<embed>等
2、manifest 离线页面缓存。Mainfest的特点是一旦设置后，浏览器便会将需要缓存的文件保存在本地。
3、base元素被用于标记文档的基础URL地址。
![image.png](https://upload-images.jianshu.io/upload_images/7572791-f16a979df7b21878.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

4、div元素是使用频率非常高的元素，我们也可以将其视为一种分组内容元素。由于div自身不带有任何意义，在HTML5强烈要求代码语义化的大背景下，div被视作一种“最后的解决方案”， 也就是优先使用header、section、article、aside、footer等语义化区块元素，在这些元素都不适用的情形下再使用div。

5、
```HTML
		<ul>
			<li>I Walk the line</li>
			<li>Out among the stars</li>
			<li>Rock and roll shoes</li>
		</ul>
		<ol type="a">
			<li>I Walk the line</li>
			<li>Out among the stars</li>
			<li>Rock and roll shoes</li>
		</ol>
		<dl>
			<dt>名称</dt>
				<dd>蒲坝站</dd>
			<dt>级别</dt>
				<dd>四等车站</dd>
			<dt>业务</dt>
				<dd>办理旅客乘降</dd>
				<dd>办理行李、包裹托运</dd>				
```
6、
```HTML
		<figure>
			<img src="tower.png" alt="埃菲尔铁塔">
			<figcaption>巴黎最高的建筑物:埃菲尔铁塔</figcaption>
		</figure>
```
由于HTML5对于代码语义的强调，因此img元素中的alt属性的重要性较高。alt属性指定了替代文本，当图像无法显示或者用户禁用图像显示时，能够代替图像在浏览器中的显示，因此它也是提升页面可访问性的重要因素
8、main
```HTML
		<main>
			<article>
				<h1>自行车越野</h1>
				<p>自行车越野简称BMX...</p>
			</article>
		</main>
```
### 2.2 HTML常用元素

1、a元素有趣的地方在于它实际上是一种类似包裹的东西，不仅能包裹文字，还能包裹图片、段落、列表、表格等，甚至包裹整个section
```HTML
		<a href="html5.html" target="_blank">
			<section>
				<h1>HTML5的革新</h1>
				<p>了解超链接中的诸多新特性</p>
			</section>
		</a>
```
![image.png](https://upload-images.jianshu.io/upload_images/7572791-cd2f1d41827f012d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
2、span元素是另一种常见的文本元素，它常常被用来组合文本，以便于有针对性地设置相应的样式。在span的运用中往往结合了class或者id属性。例如，当我们希望对一段话中的个别文字专门设置某种颜色时，就需要将文字用span加以标记，并标注对应了某种颜色的CSS 样式。
```HTML
<p>这段文字有<span class="red">红</span><span class="green">绿</span><span class="blue">蓝</span></p>
```
如果不对span设置样式，则span中的文本和其他的文本看上去不会有任何差异。
3、在HTML5中两种表示强调的文本元素，分别为em和strong。其中em元素更多代表语义、语气的加强，而strong则更加强调页面文本重要性、紧急程度等
```HTML
		<p><em>北京</em>获得2022年冬奥会主办权</p>
		<p><strong>北京</strong>获得2022年冬奥会主办权</p>
```
![image.png](https://upload-images.jianshu.io/upload_images/7572791-9110ff3a4e6e287a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

4、big small
```HTML
		<p>当前热门促销活动: </p>
		<p><big>特价！啤酒节满199-100元</big></p>
		<p><small>任何媒体、网站或个人未经协议授权不得转载本页面信息</small></p>
```
5、当文本中需要插入引用时，有q和cite两类元素可供使用。当需要插入某句被引用的话，或者某段文字摘录时，可以使用q元素，而当需要插入文献的标题、作者、链接时，可以使用cite元素。
```HTML
		<p>《图书馆的故事》作者<cite>勒纳</cite>写道：<q>公元前48年，凯撒发动亚历山大战争时，意外的火灾摧毁了图书馆......烧毁
		四十万卷图书。</q></p>
```
![image.png](https://upload-images.jianshu.io/upload_images/7572791-4158c21524b3e097.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
6、ps：p 元素会自动在其前后创建一些空白。浏览器会自动添加这些空间，您也可以在样式表中规定。
```HTML
		<form method="post" action="server.php">
			<p><label>姓名：<input name="username" type="text" placeholder="请输入您的姓名"></label></p>
			<p>
				<label for="sex">性别：</label>
				<input type="radio" name="sex" value="male" checked>男
				<input type="radio" name="sex" value="female">女	
			</p>
			<p><label>电话：<input name="tel" type="tel"></label></p>
			<p><label>邮箱：<input name="email" type="email"></label></p>
			<p><label>时间：<input name="date" type="date" pattern="\d{1,2}/\d{1,2}/\d{4}"></label></p>
			<p>
				<label for="equipment">请选择预约的仪器</label>
				<select name="equipment">
					<option value="1">分光光度仪</option>
					<option value="2">气相色谱仪</option>
					<option value="3">低速离心机</option>
					<option value="4">电子天平</option>
				</select>
			</p>
			<p>
				<label><input type="checkbox" name="rule">遵守实验仪器使用规范</label>
			</p>
			<p><button>提交表单</button></p>
		</form>
```
![image.png](https://upload-images.jianshu.io/upload_images/7572791-2b439d662d0f2ab5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
7、
```HTML
		<fieldset>
			<legend>性别：</legend>
			<p><label><input type="radio" name="sex" value="male" checked>男</label></p>
			<p><label><input type="radio" name="sex" value="female">女</label></p>
		</fieldset>
```
![image.png](https://upload-images.jianshu.io/upload_images/7572791-0c56dc85cba93235.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 第三章 CSS新手详解
### 3.1 CSS代码基础
1、在CSS中，每一条声明都由属性和属性的值两部分组成。当属性的值为多项时，可以用空格来分隔各项参数。如article碳元素定义宽度为1像素、样式为实心、颜色为黑色的边框时，需要为border属性设置三个参数，代码如下：
```CSS
article {
	border: 1px solid #000;
}
```
在设置属性时，要牢记以顺时针的方向来设置参数，即“上、右、下、左”
:smile:经验
`百分比是一个例外，当数值为百分之零时，在CSS中一定要写成0%而非0。`

#### 3.1.2 继承

```HTML
<!doctype html>
<html>
	<meta charset="UTF-8">
	<title>Untitled Document</title>
	<style type="text/css">
		body{
			color: #808080
		}
		
		#first{
			color: #1ABC9C;
		}
		
		#second{
			color: #2ECC71;
		}
		
		#third{
			color: #F1C40F;
		}
		
		#fourth{
			color: #E67E22;
		}
	</style>
	<body>
		<div id='first'>
			<p>Nothing seek, nothing find.</p>
			<div id='second'>
				<p>Cease to struggle and you cease to live.</p>
			<div id='third'>
				<p>Man errs as long as he strives.</p>
				<div id='fourth'>
					<p>Energy and persistence conquer all things.</p>
				</div>
			</div>
			</div>
		</div>
	</body>
</html>
```

:smile:经验

`为了避免浏览器默认设置产生的影响，我们常常使用专门的CSS重设文件，如reset.css来清理所有默认样式（虽然现在逐渐有质疑的声音反对这一做法）,这样的CSS文件可以通过在页面中使用link标签导入，也可以在CSS文件中使用@import语法来导入。`

#### 3.1.3 选择器

CSS中存在三种类型的选择器，分别是标签选择器、类选择器、和id选择器

除三种主要类型的选择器外，在CSS中还有一些附加的选择器，包括伪类选择器和伪元素选择器。伪类选择器是在之前的选择器基础之上，加上一些用于指定元素状态的关键字，如鼠标位置、浏览历史、内容状态等。伪类选择器的标志是在选择器与关键字之间以英文冒号“：”j间隔。

```CSS
a:hover{
	background: #FF0;
}
a:visited{
    color:#FF);
}
```

伪元素选择器的功能是在选择某元素的基础上，在文档中再增加一些额外的元素。伪元素选择器的标志是在选择器与关键字之间以两个英文冒号“：”间隔。例如，我们要为一段英文文字开头添加两个单词，段落代码如下：

```HTML
<p>everything happens for a reason.</p>
```

```CSS
p::before{
    content: "He said";
}
```

​	在以上代码中，before选择器将在段落之前插入content属性中的文字内容。因此在页面中以上段落文本将显示为"He said everything happens for a reason. "

​	虽然带有一个“伪”字，但在选择器中这并非贬义词。`伪类选择器和伪元素选择器都是HTML5开发的好帮手，`

其使用的频率相当高，一些新奇的效果可以巧妙地借助这些选择器加以制作。

### 3.2 CSS3常用属性

####3.2.1文本和字体

![1543934089851](C:\Users\ATITUI~1\AppData\Local\Temp\1543934089851.png)

行高的另一个重要功能是设置内容的垂直居中

```CSS 
		h1{
			color:#F00;
			background: #ECF0F1;
			height: 60px;
		}
```

增加高度后，文字位于左上角，也就是垂直方向上为顶对齐方式

![1543934714116](C:\Users\ATITUI~1\AppData\Local\Temp\1543934714116.png)

加上line-height属性，使得行高等于高度，即可实现垂直居中

```CSS
		h1{
			color:#F00;
			background: #ECF0F1;
			height: 60px;
			line-height: 60px;
		
		}
```

![1543934902070](C:\Users\ATITUI~1\AppData\Local\Temp\1543934902070.png) 

CSS3还为字体爱好者提供 @font-face 来声明一种自定义字体

#### 3.2.2 边框和背景



```CSS3
		.block{
			border: 5px dotted #F00;
			border-radius: 50%;
			width:200px; 
			height:200px;
		}
		img {
			border: 10px solid #F00;
			border-radius:50%;
		}
```

border-radius 数值为50%时，边框将显示圆形

![1544108503894](C:\Users\ATITUI~1\AppData\Local\Temp\1544108503894.png)

```CSS
		h1{
			color:#F00;
			background: #ECF0F1;
			height: 60px;
			line-height: 60px;
			border-bottom: 2px solid rgba(0, 0, 0, .15);
			padding-bottom: 10px;
		
		}
```

rgba(0, 0, 0, .15)是另一种颜色的表示方式，它的优点是能够设置半透明的颜色。括号里的四个参数分别是R、G、B及透明值。最后一位的取值范围是0至1，0为完全透明，1为完全不透明