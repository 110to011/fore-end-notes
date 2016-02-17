#### 元素垂直居中的方法

1. 利用table和table-cell

```html
<div class="outer">
	<div class="inner">我是内层</div>
</div>
```
```css
.outer {
  display: table;
  height: 200px;
  width: 200px;
}
.inner {
  display: table-cell;
  vertical-align: middle;
}
2. 利用绝对定位


.outer {
	position: relative;
	width: 400px;
	height: 400px;
	background-color: #cfc;
}
.inner {
	position: absolute;
	top: 50%;
	margin-top: -100px;
	width: 200px;
	height: 200px;
	background-color: #ccc;
}
```
