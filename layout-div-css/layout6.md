# 高度自适应

> 子级高度自适应生效的前提是其父级元素也要设置高度自适应

```css
html,body {
	font-family: Arial,"宋体";
	font-size: 14px;
	color: #e6e6e6;
	margin: 0;
	height: 100%;
	background: #7c7c7c;
}
.left {
	background-color: #f90;
	border: 2px solid #333;
	width: 300px;
	height: 100%;
}
```

```html
<div class="left"></div>
```
