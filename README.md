# Frontend-Training


Day1(2025.5.27): 

	html内部属性


Day2(2025.5.28): 
	
	html所有知识


Day3(2025.5.30): 

	CSS的样式：内部，内联，外部


Day4(2025.5.31): 

	CSS的选择器: 全局选择器*，类选择器class，元素选择器:标签名称，id选择器#. id -> #, class -> . id选择器的只能针对某一个特定的标签来使用，只能使用一次。

	元素选择器的权重为1
	class选择器的权重为10
	id选择器的权重为100
	内联样式的权重为1000
	优先级： 行内样式1000 > id选择器100 > 类选择器10 > 元素选择器1
	同级下面覆盖上面

	color:
	color: black
	color: #00000f
	color:rgb(0,0,255)
	color:rgba(0,0,0,0.5)

	font-size:
	## chorme浏览器最小字体为12px

	font-weight:
	bold -> 粗体字符
	bolder -> 更粗
	lighter -> 更细字符
	100-900 -> 由细到粗 400等同默认 700等同于bold

	font-style:
	normal -> 默认
	italic -> 定义斜体

	font-family:
	定义字体

Day5(2025.6.1):

	背景属性(index1.html)：
			background-image: url("images/Niko.jpg");

			background-color: aqua

			background-repeat: no-repeat; 
			//不平铺，水平/垂直平铺

			background-size: cover;  
			//第一个值宽度第二个值高度，如果设置第一个，第二个为auto（length->宽度高度，percentage->百分比，cover->保持图片纵横比并将图片缩放成完全覆盖背景区域的最小大小，contain->保持图片纵横比并将图片缩放成适合背景定位区域的最大大小）

			background-position: left center; 
			//起始位置，默认值为 0% 0%


	文本属性(index2.html)：
			text-align: left;  // left,right,center

			text-decoration: underline;	//underline, overline, line-through

			text-transform: captialize; //uppercase, lowercase

			text-indent: 50px

	表格属性(index3.html)
			border: 1px, red, solid;

			border-collapse: collapse; // 折叠：折叠成单表格.

			水平对齐: td{text-align: center}
			垂直对齐: td{height: 50px, vertical-align: bottom;} // top, middle, bottom
			文本和表格之间填充: padding: 20px
			字体颜色和表格内颜色：			
			background-color: blue;  // 表格内颜色
			color: azure;	// 字体颜色