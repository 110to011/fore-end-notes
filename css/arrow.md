
# 绘制箭头

```html
<span class="caret"></span>
```

```css
.caret {
	position: relative;
	display: inline-block;
	width: 10px;
	height: 20px;
}
.caret:before {
	content: "";
	position: absolute;
	top: 0;
	left: 0;
	width: 0;
	height: 0;
	line-height: 0;
	border: 10px solid transparent;
	border-right-width: 0;
	border-left-color: #ccc;
}
.caret:after {
	content: "";
	position: absolute;
	top: 3px;
	left: 0px;
	width: 0;
	height: 0;
	line-height: 0;
	border: 7px solid transparent;
	border-right-width: 0;
	border-left-color: #f00;
}
```
