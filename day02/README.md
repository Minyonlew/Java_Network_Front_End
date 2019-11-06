# Java_Network_Front_End

## Day 02  CSS

[TOC]

### 1. `CSS`



#### 1.1 `CSS` 简介

>  		`CSS`是**层叠样式表（Cascading Style Sheets）的缩写**，它用于定义`HTML元素`的显示形式，是一种格式化网页内容的技术。`CSS`现在已经被大多数浏览器所支持，成为网页设计者必须掌握的技术之一。



#### 1.2  `css`的作用

>1. 专注于显示。使显示和数据本身分离。
>
>2. 优势：
>
>a)      `CSS`将从基础开始建设直到全面替代传统Web设计方法。`W3C组织`创建的`CSS`技术将替代`HTML`中用于表现的`HTML元素`。
>
>b)      提高页面浏览速度。使用`CSS`，比传统的Web设计方法至少节约50%以上的文件尺寸。 
>
>c)      缩短改版时间，降低维护费用。只要简单修改几个`CSS`文件就可以重新设计一个有成百上千页面的站点。
>
>d)      强大的字体控制和排版能力。有了`CSS`，我们不再需要用`font`标记或者透明的`1 px GIF图片`来控制标题，改变字体颜色、字体样式等等。
>
>e)     ` CSS`非常容易编写。我们可以象写`HTML`代码一样轻松地编写`CSS`。
>
>f)        可以一次设计，随处发布。你的设计不仅仅用于Web浏览器，也可以发布在其他设备上。
>
>g)      更好的控制页面布局。结合`CSS`和`div元素`，可以比传统的使用`table`元素更好地控制页面布局。
>
>h)      **实现表现和结构、内容相分离**。将网页的表现形式部分剥离出来放在一个独立样式文件中，可以减少未来网页无效的可能。
>
>i)        更方便搜索引擎的搜索。用只包含结构化内容的`HTML`代替嵌套的标签，搜索引擎将更有效地搜索到网页的内容，并可能给网页一个较高的评价。



#### 1.3  `css` 的声明规则

> - `CSS`声明学习:
>   				 1、在`head`标签中使用`style`标签声明：
>   				 		作用：此声明一般声明当前网页的公共样式或者给某个标签的单独样式
>   				 2、在标签上使用`style`属性进行声明：
>   				 		作用：此声明会将`css`样式直接作用于当前标签。
>   				 3、在`head`标签中使用`link`标签引入外部声明好的`css`文件
>   						作用：此声明相当于调用,解决了不同网页间样式重复使用的问题
>   							一次声明，随处使用(常用)
>   			**问题：**
>   				不同的声明给同一个标签操作了同一个样式，会使用谁的？
>
>   ​			**答：**
>
>   ​				**如果`Css`的声明全部在head标签中，则遵循就近原则，谁离标签近，谁就会被显示。**

> ```css
> //1.外部样式表（常用）
> //不需要style标签
> <link rel=“stylesheet” href=“” />
> 
> //2.嵌入式样式表
> <style  type=“text/css”>
> p{}
> </style>
> 
> //3.内联样式（少用）
> 属性名为style
> 举例:<p style=“”></p>
> 
> ```
>
> - 演示引入外部声明好的`css`文件的例子：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title>css的声明学习</title>
> 		<!--引入外部声明好的css文件-->
> 		<link rel="stylesheet" type="text/css" href="css/my.css"/>
> 		<!--声明css代码域-->
> 		<style type="text/css">
> 			hr{
> 				width: 50%;
> 				height: 20px;
> 				color: red;
> 				background-color: red;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<h3>css的声明学习</h3>
> 		<hr style="background-color: blue;height:50px;"/>
> 		<hr/>
> 	</body>
> </html>
> ```



### 2.  `css` 选择器学习



#### 2.1  `css`的选择器学习：

> - 标签选择器：
>   - 标签名{样式名1：样式值1;……
>   - 作用：会将当前网页内的所有该标签增加相同的样式
> - id选择器:
>   - #标签的id属性值{样式名1：样式值1;……}
>   - **作用：**给某个指定的标签添加指定的样式
> - 类选择器：
>   - . 类选择器名{样式名1：样式值1;……}
>   - **作用：**给不同的标签添加相同的样式
> - 全部选择选择器
>   - *{样式名1：样式值1;……}
>   - 作用：选择所有的HTML标签，并添加相同的样式
>
> - 组合选择器：
>
>   - 选择器1,选择器2,……{样式名1：样式值1;……}
>   - 作用：解决不同的选择器之间重复样式的问题
>
> - 子标签选择器
>
>   - 选择器1 子标签选择器{样式名1：样式值1;……}
>
> - 属性选择器：
>
>   - 标签名[属性名=属性值]{样式名1：样式值1;……}
>
>   - 作用：选择某标签指定具备某属性并且属性值为某属性值的标签
>
>     



### 3. `css`的各种属性设置：

#### 3.1 常用属性

> **1、声明`css`代码域。**
> **2、使用选择器选择要添加样式的标签。**
>
> - 根据需求来:
>   - 使用*选择器来给整个页面添加基础样式
>   - 使用类选择器给不同的标签添加基础样式
>   - 使用标签选择器给某类标签添加基础样式
>   - 使用id、属性选择器、style属性声明方式给某个标签添加个性化样式。
>
> **3、书写样式单**
>
> - **边框设置:**
> `border:solid 1px;`
> - **字体设置:**
> `font-size:10px;`           设置字体大小
> 	`font-family:`          		"黑体";(设置字体的格式)
> 	`font-weight：bold;` 	 设置字体加粗
> - **字体颜色设置:**
> `color:`  颜色;
> - **背景颜色设置:**
> `background-color:`  颜色;
> - **背景图片设置:**
> 	`background-img:`		`url`(图片的相对路径);
> `background-repeate:no-repeate;`  设置图片不重复
> `bacground-size:cover;`    图片平铺整个页面
> - 高和宽设置
>     浮动设置
> `float:left|right`
> 	行高设置
> `line-height:10;`
>
> 
>
> 4. **鼠标样式**
>
> - **伪类选择器**  (使用伪类给标签添加样式)
>   - `a:hover{}` 
>
> - **常规，非访问超链接**
>   - `a:link{}`
> - **访问过的超链接**
>   - `a:visited{}`
> - **鼠标点击时的超链接**
>   - `a:active{}`
>
> ```html
> <style>
>     /* 未访问的链接 */
>     a:link {
>         color:red
>     }
>     /* 已访问的链接 */
>     a:visited {
>         color: green;
>     }
>     /* 鼠标移动到链接上 */
>     a:hover {
>         color: yellow;
>     }
> 
>     /* 选定的链接 */
>     a:active {
>         color: skyblue;
>     }
> 
>     /*使用伪类给标签添加样式*/
>     img:hover{
>     /*设置图片旋转角度和大小变化*/
>     transform: rotate(-10deg) scale(1.2);
>     /*设置显示优先级别*/
>     z-index: 1;
>     /*设置显示加载时间*/
>     transition:1.0s;
> 
>     }
> 	</style>
> ```



#### 3.2 布局属性

> - 浮动的框可以向左或向右移动，直到它的外边缘碰到包含框或另一个浮动框的边框为止。
>
> - 浮动特点：
>
>   1.失去文档流功能。
>
>   2.块级标签变成了行内标签。
>
>   | **属性名** | **说明**         | **常用参数**                       |
>   | ---------- | ---------------- | ---------------------------------- |
>   | float      | **漂浮**         | **none \| left   \|right**         |
>   | clear      | **是否允许漂浮** | **none \| left   \|right \| both** |
>   | display    | **能否显示**     | **none \|block\|inline**           |
>   | visibility | **可见性**       | **inherit \| visible   \| hidden** |
>
> - **注意：**
>
>   - **`float` 是魔鬼，会影响其他相邻元素；但是clear是小白，其只会影响自身，不会对其他相邻元素造成影响！**
>   - `Display`:为`None`时，其他元素可以占据该元素的位置。
>   - `Display`:为  `inline`时，将块级标签变成行内标签。



### 4. 盒子模型学习



> ​		**网页设计**中常听的属性名：`内容(content)`、`内边距(padding)`、`边框(border)`、`外边距(margin)`， `CSS盒子模型`都具备这些属性。这些属性我们可以用日常生活中的常见事物——盒**子作一个比喻来理解，所以叫它盒子模型。**`CSS盒子模型`就是在网页设计中经常用到的`CSS技术`所使用的一种思维模型。**所有HTML元素可以看作盒子。**

#### 4.1 盒子模型

> **1 .`css`的盒子模型学习：**
>
> - **div标签：**
>- **块级标签**，主要是用来进行网页布局的，会将其中的子元素内容作为一个独立的整体存在。
>   - **特点：**
>     - 默认宽度是页面的宽度，但是可以设置。
>     - 高度默认是没有的，但是可以设置。(可以顶开)
>     - 如果子元素设置了百分比的高或者宽，占据的是div的百分比，不是页面的
>   
>- **盒子模型：**
> 
>  - `外边距:margin`
> 
>    - 作用：用来设置元素和元素之间的间隔。
>     - 居中设置: `margin:0px auto;`     上下间隔是 `0px`  水平居中。
>     - 可以根据需求单独的设置上下左右的外边距。
> 
>  - `边框：border`
> 
>    - 作用：用来设置元素的边框大小
>     - 可以单独设置上下左右
> 
>  - `内边距：padding`
> 
>    - 作用：设置内容和边框之间的距离
>     - 注意：内边距不会改变内容区域的大小
>     - 可以单独的设置上下左右的内边距
> 
>  - `内容区域：`
> 
>    - 作用：改变内容区域的大小。
>     - 设置宽和高即可改变内容区域的大小。
> 
> 
>    
>- **测试代码**
> 
>```HTML
> <html>
> 	<head>
> 		<title>css的盒子模型学习</title>
> 		<meta charset="UTF-8"/>
> 		<style type="text/css">
> 			img{
> 				width: 49.53%;
> 				height: 150px;
> 			}
> 			#showdiv{
> 				border: solid 5px;
> 				width: 410px;
> 				height: 200px;
> 				/*margin-bottom: 100px;*/
> 				/*如果margin设置了auto，且加上了对应的值，则其上下左右都是同一个值*/
> 				margin: 100px auto;
> 				/*div内部内容大小*/
> 				padding: 20px;
> 			}
> 			#div01{
> 				border: dashed 3px orange;
> 				width: 40%;
> 				height: 200px;
> 				margin-left: 100px;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<div id="showdiv">
> 			<img src="imgs/01.jpg"/>
> 			<img src="imgs/02.jpg"/>
> 		</div>	
>      
>    		<div id="div01">	
> 		</div>
> 	</body>
> </html>
> ```



#### 4.2 盒子模型简单布局

> - `div `中含有 `div` 。
> - **测试代码**
>
> ```html
> <html>
> 	<head>
> 		<title>盒子模型简单的布局</title>
> 		<meta charset="UTF-8"/>
> 		<style type="text/css">
> 		/*设置div的基础样式*/
> 			div{
> 				width: 300px;
> 				height: 300px;
> 			}
> 		/*设置header和footer的样式*/
> 			#header,#footer{
> 				width: 650px;
> 				margin: auto;
> 				margin-top: 20px;
> 			}
> 		/*设置子div的样式*/
> 			#div01{
> 				border: solid 1px orange;
> 				float: left;
> 				margin-right: 20px;
> 			}
> 			#div02{
> 				border: solid 1px blueviolet;
> 				float: left;
> 			}
> 			#div03{
> 				border: solid 1px #4791FF;
> 				float: left;
> 				margin-right: 20px;
> 			}
> 			#div04{
> 				border: solid 1px coral;
> 				float: left;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<div id="header">
> 				<div id="div01">
> 					我是div01
> 				</div>
> 				<div id="div02">
> 					我是div02
> 				</div>
> 		</div>
> 		
> 		<div id="footer">
> 			<div id="div03">
> 				我是div03
> 			</div>
> 			<div id="div04">
> 				我是div04
> 			</div>
> 		</div>
> 		
> 	</body>
> </html>
> ```



#### 4.3 定位属性

> - **文档流：元素在文档中占有的原始位置**。
>
> - `position`:
>
>   - 相对定位:`relative`
>     - 作用：相对元素原有位置移动指定的距离**(相对的自己的原有位置)**
>     - 可以使用`top,left,right,bottom`来进行设置。
>     - 注意：
>       - 其他元素的位置是不改变的。
>   - 绝对定位:`absolute`
>     - 作用：可以使用元素参照界面或者相对父元素来进行移动 	
>     - 注意：
>       - 如果父级元素成为参照元素，必须使用相对定位属性
>       - 默认情况下是以界面为基准进行移动的。
>   - 固定定位:`fixed`
>     - 作用：将元素固定现在页面的指定位置，不会随着滚动条的移动而改变位置。
>
> - 以上定位都可以使用`top,left,right,bottom`来进行移动。
>
> - **`z-index:`此属性是用来声明元素的显示级别的。**
>
>   
>
> - **测试代码**
>
> ```html
> <html>
> 	<head>
> 		<title>css的定位</title>
> 		<meta charset="UTF-8"/>
> 		<!--声明css代码域-->
> 		<style type="text/css">
> 		/*给div01添加样式*/
> 			#div01{
> 				border: solid 2px orange;
> 				height: 200px;
> 				width: 800px;
> 				margin-bottom: 10px;
> 				margin-top: 50px;
> 				position: relative;/*给div01添加相对定位成为其子元素绝对定位的参照元素*/
> 			}
> 			/*给showdiv添加样式*/
> 			#showdiv{
> 				border: solid 3px;
> 				height: 50px;
> 				width: 50px;
> 				position: absolute;
> 				top:10px;
> 			}
> 		/*给div02添加样式*/
> 			#div02{
> 				border: dashed 2px coral;
> 				height:200px;
> 				width: 800px;
> 				margin-bottom: 10px;
> 				position: relative;/*使用相对定位*/
> 				left:50px;
> 				top:100px;
> 				background-color: coral;
> 				z-index: 3;    /*层数*/
> 			}
> 		/*给div03添加样式*/
> 			#div03{
> 				border: solid 2px #FF7F50;
> 				height: 200px;
> 				width: 800px;
> 				background-color: gray;
> 				position: relative;
> 				z-index: 4;
> 			}
> 		/*给div04添加样式*/
> 			#div04{
> 				border: solid 3px blue;
> 				height: 50px;
> 				width: 50px;
> 				position: fixed;/*所固定的对象是可视窗口而并非是body或是父级元素。*/
> 				top:270px;
> 				right: 10px;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<div id="div01">
> 				<div id="showdiv">
> 					
> 				</div>
> 		</div>
> 		<div id="div02">我是div02</div>
> 		<div id="div03"></div>
> 		<div id="div04">
> 			
> 		</div>
> 		<br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br />
> 	</body>
> </html>
> ```
>
> 



### 5. 图片墙 百度首页模拟练习

- **测试代码：`CSSNote`**

