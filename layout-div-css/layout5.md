# 三列浮动中间列宽度自适应

```css
body {
	font-family: Arial,"宋体";
	font-size: 14px;
	color: #e6e6e6;
	margin: 0px;
	background: #7c7c7c;
}
.left {
	background-color: #f90;
	border: 2px solid #333;
	width: 100px;
	height: 500px;
	position: absolute;
	top: 0;
	left: 0;
}
.center {
	background-color: #0ff;
	border: 2px solid #333;
	margin: 0 104px;
	height: 500px;
}
.right {
	background-color: #f90;
	border: 2px solid #333;
	width: 100px;
	height: 500px;
	position: absolute;
	top: 0;
	right: 0;
}
```

```html
<div class="left"></div>
<div class="center"></div>
<div class="right"></div>
```
