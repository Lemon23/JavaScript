#绘图实现
		为了学习绘图功能，我阅读了很多书籍和网上教程，希望通过练习可以更好的掌握。
		这里我运用了两种绘图方式来实现绘图功能：
－	[SVG](http://baike.baidu.com/link?url=r1q72s9Mzh20NhSWE_hDhjjm_fzQq_ohCSUeyty74NIH77sgcUFH559CiAPGkSLPM9Jwib8eWJTEHlLmBVTpivNCdh6t7udQBEHm-PHVGR7)

－	[canvas元素](http://www.w3school.com.cn/html5/html5_canvas.asp)
		一开始，我对两个方法做了一个简单的[基础绘图示例](https://github.com/Lemon23/JavaScript/blob/master/Draw/基础绘图示例.html)
		打开这个示例文件，我直观的发现了`SVG`和`canvas元素`的一个重要区别。
		通过之后的学习和探索，我明白了为什么会出现这种差异，这更引来了我对绘图的好奇心和求知欲。。。

###SVG
>		首先，`SVG`———— 可缩放矢量图形，使用XML格式定义图形，图像再放大或改变尺寸的情况下其图形质量不会有亏损。
>		SVG这种语法比较庞大并且有一定的复杂度，它不仅可以用于简单的基本图形绘制，还支持任意曲线、文本及动画的绘制。
>		SVG图形甚至能够整合JavaScript脚本和CSS样式表来添加行为和展示信息。
>		我将练习使用客户端JavaScript利用SVG动态绘制图形。
>####NO.1  [使用SVG绘制饼状图](https://github.com/Lemon23/JavaScript/blob/master/Draw/使用SVG绘制饼状图.html)
>####效果：![](https://github.com/Lemon23/JavaScript/raw/master/Draw/pic/D-1.jpeg)
>>		该例使用XML语法来处理SVG，使用SVG命名空间以及`createElementNS()`这样的DOM方法而不是`createElement()`。
>>		每一个饼楔都是用`<svg:path>`元素来表示，最难的是`d`属性，该属性使用简洁语法通过字符和数字来指定坐标、角度和其他值。
具体参数需要参阅 [标准文档](https://www.w3.org/TR/SVG/) 。

>####NO.2 [使用SVG绘制时钟](https://github.com/Lemon23/JavaScript/blob/master/Draw/使用SVG绘制时钟.html)
>####效果：![](https://github.com/Lemon23/JavaScript/raw/master/Draw/pic/D-2.jpeg)
>>		该例使用SVG来绘制一个动态模拟时钟，包含三个SVG`<line>元素`来分别表示分针、时针和秒针，随后通过JavaScript设置没个`<line>元素`的`transform属性`让它们旋转一定角度来现实正确的时间。
>>		其中用到了SVG滤镜效果，用来向形状和文本添加特殊的滤镜效果。
>####滤镜效果代码：![](https://github.com/Lemon23/JavaScript/raw/master/Draw/pic/D-2-1.jpeg)
>>		`<filter>`标签用来定义SVG滤镜，其中`id`属性为`shadow`表示声明定义为阴影滤镜。`<filter>`标签必须嵌套在`<defs>`标签内。
>> 		滤镜效果通过`<feGaussianBlur>`标签定义，其中的`stdDeviation`属性可定义模糊的程度。
>>		`<feOffset>`标签，表示相对于图形的当前位置来移动图像。
>>		`in="SourceGraphic"`属性定义了由整个图像创建效果
>>		通过设置`setTimeout`属性来定义时钟每1秒钟更新一次时间，这样秒针就动起来了。

		参考自《JavaScript权威指南》