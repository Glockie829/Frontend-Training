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


Day6(2025.6.14):
	后代选择器：ul li { color : red}  所有ul中的li标签都会生效，包括嵌套其他的标签里的li标签.
	子代选择器：ul>li { color : red}  只有ul子代里的li才生效
	相邻兄弟选择器：ul+li{ color : red} 只有和ul相邻的第一个li才会生效,只能向下选择.
	通用兄弟选择器：ul~li{ color : red} 和ul相邻的所有li都会生效，向下选择.
	[index1.html - index6.html]

	Box Model(盒子模型):
		所有的html元素都可看作盒子，CSS盒模型本质上是一个盒子，封装周围的html元素，包括：外边距(margin)，边框(border),内边距(padding),和实际内容(content)
		e.g.
		<style>
			div{
				color: red;
				padding: 50px;
				padding: 20px 50px;
				/*20px:上下 50px:左右*/
				/*padding可分为上下左右, e.g. padding-left : 50px;*/
			}
		</style>

	Flex box(弹性盒模型):
		弹性盒是一种当页面需要适应不同的屏幕大小以及设备类型时确保元素拥有恰当行为的布局方式.
		弹性盒子由弹性容器(Flex container)和弹性子元素(Flex item)构成,通过设置display属性的值为flex将其定义为弹性容器.
		默认弹性盒里的内容横向摆放.
		display: flex;
		flex-direction: column;
		justify-content: flex-start;/*内容属性应用在弹性容器上，把弹性项沿着弹性容器的主轴线对齐*/
		align-items: flex-start | flex-end | center /*设置或检索弹性盒子在侧轴方向上的对齐方式*/
		子元素上的属性：flex-grow/flex. 权重占比：e.g.
		.box1{
			flex:3;
		}
		.box2{
			flex:1;
		}
		.box3{
			flex:1;
		}

Day6(2025.6.18):
	浮动: 
			(1)浮动以后使元素脱离了文档流.
			(2)浮动只有左右浮动,没有上下浮动.
		float: left

		浮动副作用:
			(1)浮动元素会造成父元素高度塌陷
			(2)后续元素会受到影响

		清除浮动:
			(1)父元素设置高度: height: 10px
			(2)受影响的元素增加clear属性: clear: both -> 左浮动或者右浮动
			(3)overflow清除浮动: overflow: hidden; clear: both
			(4)伪对象方式:		
				.container::after{
					content: "";
					display: block;
					clear: both;
				}

	定位:
			position属性指定了元素的定位类型.
			relative: 相对定位(index4.html)
			absolute: 绝对定位(index5.html)
			fixed: 固定定位
			其中，绝对定位和固定定位会脱离文档流(有压盖的问题存在)
			设置定位之后，可以使用四个方向值进行调整位置: left, top, right, bottom
		*设置定位之后，相对定位和绝对定位是相对于具有定位的父级元素进行位置调整，如果父级元素没有定位，则继续向上寻找，直到顶层文档*
	Z-index
		z-index属性设置元素的堆叠顺序，拥有更高堆叠顺序的元素总是会处于堆叠顺序较低的元素的前面
		.box1{
			z-index:100
		}
		.box2{
			z-index:50
		}
		box1的元素覆盖box2的元素