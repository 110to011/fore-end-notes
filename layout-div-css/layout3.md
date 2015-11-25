# 两列右列宽度自适应

```css
body {
	font-family: Arial,"宋体";
	font-size: 14px;
	color: #e6e6e6;
	margin: 0px;
	padding-bottom: 60px;
	background: #7c7c7c;
}
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
	width: 100px;
	height: 500px;
	float: left;
}
.right {
	background-color: #0ff;
	border: 2px solid #333;
	height: 500px;
}
```

```html
<div class="wrap clearfix">
	<div class="left"></div>
	<div class="right"></div>
</div>
```
