
#绘制简单菱形的方法

>在绘制三角形的基础上绘制菱形

```html
<div class="single"></div>
```

```css
.single {
	position: absolute;
	top: 80px;
	left: 0;
	width: 40px;
	height: 40px;
	overflow: hidden;
}
.single:before {
	position: absolute;
	top: 0;
	left: 0;

	width: 0;
	height: 0;
	content: "";

	border: 20px solid transparent;
	border-left-width: 0;
	border-right-color: #f90;
}
.single:after {
	position: absolute;
	top: 0;
	left: 20px;

	width: 0;
	height: 0;
	content: "";

	border: 20px solid transparent;
	border-right-width: 0;
	border-left-color: #f90;
}
```

#复杂菱形的绘制方法

```html
<div class="diamond">
	<div class="left"></div>
	<div class="right"></div>
</div>
```

```css
.diamond {
	position: relative;
	width: 40px;
	height: 40px;
}
.left {
	position: absolute;
	top: 0;
	left: 0;
	width: 20px;
	height: 40px;
	overflow: hidden;
}
.right {
	position: absolute;
	top: 0;
	left: 20px;
	width: 20px;
	height: 40px;
	overflow: hidden;
}
.left:before {
	position: absolute;
	top: 0;
	left: 0;

	width: 0;
	height: 0;
	content: "";

	border: 20px solid transparent;
	border-left-width: 0;
	border-right-color: #f90; 
}
.left:after {
	position: absolute;
	top: 0;
	left: 5px;

	width: 0;
	height: 0;
	content: "";

	border: 20px solid transparent;
	border-left-width: 0;
	border-right-color: #0f0; 
}
.right:before {
	position: absolute;
	top: 0;
	left: 0;

	width: 0;
	height: 0;
	content: "";

	border: 20px solid transparent;
	border-right-width: 0;
	border-left-color: #f90; 
}
.right:after {
	position: absolute;
	top: 0;
	left: -5px;

	width: 0;
	height: 0;
	content: "";

	border: 20px solid transparent;
	border-right-width: 0;
	border-left-color: #0f0; 
}
```
