# 二列宽度自适应

```css
.clearfix:before,
.clearfix:after {
	content: "";
	display: block;
	width: 0;
	height: 0;
	line-height: 0;
}
.clearfix:after {
	clear: both;
}
.left {
	background-color: #f90;
	border: 2px solid #333;
	width: 20%;
	height: 500px;
	float: left;
}
.right {
	background-color: #0ff;
	border: 2px solid #333;
	width: 70%;
	height: 500px;
	float: left;
	/*margin-left: 20%;*/
}
```

```html
<div class="wrap clearfix">
	<div class="left"></div>
	<div class="right"></div>
</div>
```
> 元素在有border等的情况下设定宽度时不能使左右两边的元素宽度之和为100%。

> left设置左浮动，right可以设置左浮动或不设置，右侧不设置浮动时可以通过margin-left的值为左侧宽度达到同样效果
