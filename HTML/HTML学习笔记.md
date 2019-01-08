
# HTML学习
####  HTML基础
1.HTML标题 是通过`<h1>-<h6>`来定义的
    
2.HTML段落 是通过标签`<p>`来定义的
    
3.HTML连接 是通过标签`<a>`来定义的 
```html
<a href="连接地址">说明</a> 
```
* HTML图像 是通过标签`<img>`来定义的 `<img src=""/>`
*  **href和src的区别**
    (1) href 是hypertext reference的缩写,表示超文本引用,用来建立当前元素与文档之间的联系；常用的有：link，a;
    列如:
    ```html
    <link href="reset.css" rel=”stylesheet“/>
    ```
   浏览器会识别该文档为 css 文档，并行下载该文档，并且不会停止对当前文档的处理。这也是建议使用 link，而不采用 @import 加载 css 的原因。
   (2)  src 是 source 的缩写，src 的内容是页面必不可少的一部分，是引入。src 指向的内容会嵌入到文档中当前标签所在的位置。常用的有：img、script、iframe。
   例如:
   ```html
    <script src="script.js"></script>
   ```
   浏览器解析到该元素时，会暂停浏览器的渲染，直到该资源加载完毕。这也是将js脚本放在底部而不是头部得原因。
   简而言之，src 用于替换当前元素；href 用于在当前文档和引用资源之间建立联系。

* **html与jpg在相同或者不同目录下的处理**

   >1、*.html 文件跟 *.jpg 文件(f盘)在不同目录下：
        ` <img src="file:///f:/*.jpg" width="300" height="120"/>`     
   
   >2、*.html 文件跟 *.jpg 图片在相同目录下：
       `<img src="*.jpg" width="300" height="120"/>`
    
  > 3、*.html 文件跟 *.jpg 图片在不同目录下：
    *  图片 *.jpg 在 image 文件夹中，*.html 跟 image 在同一目录下：
       `<img src="image/*.jpg/"width="300" height="120"/>`
    * 图片 *.jpg 在 image 文件夹中，*.html 在 connage 文件夹中，image 跟 connage 在同一目录下：
      `<img src="../image/*.jpg/"width="300" height="120"/>`

  >4、如果图片来源于网络，那么写绝对路径：
     `<img src="http://static.runoob.com/images/runoob-logo.png" width="300" height="120"/>`

* 如何定义图片带超级链接
 ```html
<a href="http://www.baidu.com"> 
<img src="http://static.runoob.com/images/runoob-logo.png" width ="300" height="120"> 
</a>
```
 
##### HTML元素
***
|开始标签|元素内容|结束标签|
|---|---|---|
|`<p>`|这是一个段落|</p>|
|`<a>`|这是一个链接|</a>|
| `<br> `|换行||

开始标签被称为**起始标签**,结束标签被称为**闭合标签**
###### HTML语法
* HTML 元素以开始标签起始
* HTML 元素以结束
* 标签终止元素的内容是开始标签与结束标签之间的内容
* 某些 HTML 元素具有空内容（empty content）
* 空元素在开始标签中进行关闭（以开始标签的结束而结束）
* 大多数 HTML 元素可拥有属性

##### HTML属性
***
* HTML 元素可以设置**属性**
* 属性可以在元素中添加**附加信息**
* 属性一般描述于**开始标签**
* 属性总是以名称/值对的形式出现，比如：name="value"。

###### HTML 属性常用引用属性值

属性值应该始终被包括在引号内。
双引号是最常用的，不过使用单引号也没有问题。
![info](info.gif "提示图标")
提示:&nbsp;在某些个别的情况下，比如属性值本身就含有双引号，那么您必须使用单引号，例如：`name='John "ShotGun" Nelson'`

###### HTML属性参考

|属性|描述|
|---|---|
|class|为html元素定义一个或多个类名（classname）(类名从样式文件引入)|
|id|定义元素的唯一id|
|style|规定元素的行内样式（inline style）|
|title|描述了元素的额外信息 (作为工具条使用)|

更对属性参考:[html全局属性参考手册](http://www.runoob.com/tags/ref-standardattributes.html)

###### HTML发送邮件
``` html
<p>这是一个电子邮件链接：<a href="mailto:someone@example.com?Subject=Hello%20again" target="_top">发送邮件</a></p><p> <b>注意:</b>  单词之间空格使用 %20 代替，以确保浏览器可以正常显示文本。</p>
```

##### HTML <head> 元素
  **<head> 元素**包含了所有的头部标签元素。
  在 **<head>元素**中你可以插入**脚本（scripts） , 样式文件（CSS）**，及各种meta信息。
  可以添加在头部区域的元素标签为: **<title>**, **<style>**, **<meta>**, **<link>**, **<script>**, **<noscript>**, and **<base>**
  
  
| 标签 |  描述 |
| --- | --- |
| `<head>`|  定义了文档的信息 |
| `<title>` |  定义了文档的标题 |
| `<base>`|定义了页面链接标签的默认链接地址|
| `<link>`|定义了一个文档和外部资源之间的关系|
| `<meta>`|定义了HTML文档中的元数据|
| `<script>`|定义了客户端的脚本文件|
|`<style>`|定义了HTML文档的样式文件|
  
###### HTML `<title>` 元素
 <title> 标签定义了不同文档的标题。
 <title> 在 HTML/XHTML 文档中是必须的。
 <title> 元素:
 * 定义了浏览器工具栏的标题
 * 当网页添加到收藏夹时，显示在收藏夹中的标题
 * 显示在搜索引擎结果页面的标题
 
 ###### HTML `<base>` 元素
 <base> 标签描述了基本的链接地址/链接目标，该标签作为HTML文档中所有的链接标签的默认链接:
```html
 <head><base href="http://www.runoob.com/images/" target="_blank"></head>
 ```

 ##### HTML `<link>` 元素
 <link> 标签定义了文档与外部资源之间的关系。
 <link> 标签通常用于链接到样式表:
 ```html
 <head><link rel="stylesheet" type="text/css" href="mystyle.css"></head>
 ```
 ##### HTML `<style>` 元素
 <style> 标签定义了HTML文档的样式文件引用地址.在<style> 元素中你也可以直接添加样式来渲染 HTML 文档:
 ```html
<head><style type="text/css">
body {background-color:yellow}
p {color:blue}</style></head>
```

##### HTML `<meta>` 元素
 meta标签描述了一些基本的元数据。
 `<meta>` 标签提供了元数据.元数据也不显示在页面上，但会被浏览器解析。
 META 元素通常用于指定网页的描述，关键词，文件的最后修改时间，作者，和其他元数据。元数据可以使用于浏览器（如何显示内容或重新加载页面），搜索引擎（关键词），或其他Web服务。
 `<meta>` 一般放置于 `<head>` 区域
 ###### <meta> 标签- 使用实例
* 为搜索引擎定义关键词:
 ```html
<meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript">
```
* 为网页定义描述内容:
 ```html
<meta name="description" content="免费 Web & 编程 教程">
```
* 定义网页作者:
 ```html
<meta name="author" content="Runoob">
```
* 每30秒钟刷新当前页面:
 ```html
<meta http-equiv="refresh" content="30">
```

##### HTML样式-CSS

1.如何使用CSS

CSS 是在 HTML 4 开始使用的,是为了更好的渲染HTML元素而引入的.
CSS 可以通过以下方式添加到HTML中:
* 内联样式- 在HTML元素中使用"style" 属性
* 内部样式表 -在HTML文档头部 <head> 区域使用<style> 元素 来包含CSS外部引用 - 使用
* 外部 CSS 文件最好的方式是通过外部引用CSS文件.

2.内联样式
当特殊的样式需要应用到个别元素时，就可以使用内联样式。 使用内联样式的方法是在相关的标签中使用样式属性。样式属性可以包含任何 CSS 属性。以下实例显示出如何改变段落的颜色和左外边距。
```html
<p style="color:blue;margin-left:20px;">This is a paragraph.</p>
```
* 实例
   背景色属性定义一个元素的背景颜色
```html
<body style="background-color:yellow;"> <h2 style="background-color:red;">这是一个标题</h2> <p style="background-color:green;">这是一个段落。</p> </body>
```
3.外部样式
  当样式需要被应用到很多页面的时候，外部样式表将是理想的选择。使用外部样式表，你就可以通过更改一个文件来改变整个站点的外观。
  ```html
<head><link rel="stylesheet" type="text/css" href="mystyle.css"></head>
```
##### HTML样式-图像

###### HTML图像标签（`<img>`）和源属性（Src）
在 HTML 中，图像由`<img>` 标签定义。`<img>` 是空标签，意思是说，它只包含属性，并且没有闭合标签。要在页面上显示图像，你需要使用源属性（src）。src 指 "source"。源属性的值是图像的 URL 地址。定义图像的语法是：
```html
<img src="url" alt="some_text">
```
###### HTML 图像- Alt属性
alt 属性用来为图像定义一串预备的可替换的文本。替换文本属性的值是用户定义的。
```html
<img src="boat.gif" alt="Big Boat">
```
在浏览器无法载入图像时，替换文本属性告诉读者她们失去的信息。此时，浏览器将显示这个替代性的文本而不是图像。

###### HTML 图像- 设置图像的高度与宽度
height（高度） 与 width（宽度）属性用于设置图像的高度与宽度。属性值默认单位为像素:
```html
<img src="pulpit.jpg" alt="Pulpit rock" width="304" height="228">
```
提示: 指定图像的高度和宽度是一个很好的习惯。如果图像指定了高度宽度，页面加载时就会保留指定的尺寸。如果没有指定图片的大小，加载页面时有可能会破坏HTML页面的整体布局。

###### HTML `<area>` 标签的 coords 属性

* **定义和用法**
coords 属性规定区域的 x 和 y 坐标。coords 属性与 shape 属性配合使用，来规定区域的尺寸、形状和位置。图像左上角的坐标是 "0,0"。
* **详细解释：**
`<area>` 标签的 coords 属性定义了客户端图像映射中对鼠标敏感的区域的坐标。坐标的数字及其含义取决于 shape 属性中决定的区域形状。可以将客户端图像映射中的超链接区域定义为矩形、圆形或多边形等。
*下面列出了每种形状的适当值：*

**圆形：shape="circle"，coords="x,y,z"**
这里的 x 和 y 定义了圆心的位置（"0,0" 是图像左上角的坐标），r 是以像素为单位的圆形半径。

**多边形:shape="polygon",coords="x1,y1,x2,y2,x3,y3,..."**
每一对 "x,y" 坐标都定义了多边形的一个顶点（"0,0" 是图像左上角的坐标）。定义三角形至少需要三组坐标；高纬多边形则需要更多数量的顶点。多边形会自动封闭，因此在列表的结尾不需要重复第一个坐标来闭合整个区域。

**矩形：shape="rectangle"，coords="x1,y1,x2,y2"**

第一个坐标是矩形的一个角的顶点坐标，另一对坐标是对角的顶点坐标，"0,0" 是图像左上角的坐标。请注意，定义矩形实际上是定义带有四个顶点的多边形的一种简化方法。例如，下面的 XHTML 片段在一个 100x100 像素图像的右下方四分之一处，定义了一个对鼠标敏感的区域，并在图像的正中间定义了一个圆形区域。
```html
<map name="map">
  <area shape="rect" coords="75,75,99,99" nohref="nohref">
  <area shape="circ" coords="50,50,25" nohref="nohref">
</map>
```
