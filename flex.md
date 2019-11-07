### Flex

##### Flex常规操作

注意：设为 Flex 布局以后，子元素的float、clear和vertical-align属性将失效

容器的属性：
* flex-direction
* flex-wrap
* flex-flow
* justify-content
* align-items
* align-content

项目的属性：
* order
* flex-grow
* flex-shrink
* flex-basis
* flex
* align-self

——————————————————————————————————

flex-direction:
	->  row | column | row-reverse(右 -> 左) | column-reverse(下 -> 上)

flex-wrap:
	-> nowrap | wrap | wrap-reverse (不折行、折行、反向折行)

复合属性:
	 1. flex-flow = flex-drection + flex-wrap
	 	-> flex-flow: row nowrap;

	2. flex = flex-grow + flex-shrink + flex-basis
		-> 简写
            * flex: 1 = flex: 1 1 0%
            * flex: 2 = flex: 2 1 0%
            * flex: auto = flex: 1 1 auto;
            * flex: none = flex: 0 0 auto; // 常用于固定尺寸 不伸缩

		 -> flex:1 (flex-basis:0)和 flex:auto (flex-basis:auto)的区别
            * flex-basis是指定初始尺寸，当设置为0时（绝对弹性元素），
            * 此时flex-grow和flex-shrink在伸缩的时候不需要考虑它的尺寸；
            * 相反当设置为auto时（相对弹性元素），此时则需要在伸缩时将元素尺寸纳入考虑。

弹性伸缩应对:
	flex-wrap: nowrap;
        		1. flex-shrink：缩小比例（容器宽度<元素总宽度时如何收缩）
		   -> flex-shrink 默认为1，也就是当不够分配时，元素都将等比例缩小，占满整个宽度
		  -> 容器宽度有剩余时也是不会生效

		2. flex-grow：放大比例（容器宽度>元素总宽度时如何伸展）
		    -> 无多余宽度时，flex-grow无效

flex-basis：
	1. flex-basis: 0; -	> 根据内容撑开宽度
	2. width: 50px; flex-basis: 50px; 
		-> 数值相同时两者等效
		->  同时设置，flex-basis优先级高
	3. flex-basis: auto;
		-> 设置了width则元素尺寸由width决定
		-> 没有设置则由内容决定
	4. flex-direction: column
	   -> 	将主轴方向改为：上→下
	   -> 此时主轴上的尺寸是元素的height
           -> flex-basis == height

容器内容对齐：
	1. 主轴上的对齐方式: justify-content
        * Flex-start：左 -> 右
        * Flex-end：右 -> 左
        * Center：居中
        * Space-between：两端对齐，项目之间的间隔都相等
        * Space-around：每个项目两侧的间隔相等

	2. 交叉轴上的对齐方式：align-items
		!= stretch : 在交叉轴方向上的尺寸将由内容或自身尺寸（宽高）决定
        * stretch(默认)：如果元素未设置高度或auto,将占满整个容器高度
        * Flex-start: 沿交叉轴起点对齐
        * Flex-end: 沿交叉轴终点对齐
        * Center：沿交叉轴中间点对齐
        * baseline：沿第一行文字的基线对齐

	3. align-content(只对多行元素有效，容器必须开启换行)
        * Flex-start：左 -> 右
        * Flex-end：右 -> 左
        * Center：居中
        * Space-between：左右贴边，两端分布
        * Space-around：居中，两端分布
        * Stretch:

order：更优雅地调整元素顺序
	     可设置元素之间的排列顺序
        1. 数值越小，越靠前，默认为0
        2. 值相同时，以dom中元素排列为准

<div>
	<div>1</div>
	<div>2</div>
	<div>3</div>
	<div>4</div>
</div>
#container > div:first-child {
  order: 2;
}
#container > div:nth-child(2) {
  order: 4;
}
#container > div:nth-child(3) {
  order: 1;
}
#container > div:nth-child(4) {
  order: 3;
}

// 显示结果为： 3， 1， 4， 2

Error:
  1. 内容换行问题，左右布局，row, 使用flex：1
      -> 可能嵌套太多层，无法识别，改为手动设置宽度