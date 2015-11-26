# 简单的滑动条的实现

```css
.loadbar {
	width: 280px;
	background-color: #fff;
	border: 1px solid #000;
}
.bar {
	font-family: arial;
	font-size: 12px;
	background-color: #00d0ff;
	text-align: center;
	font-weight: 700;
	width: 10%;
}
```

```html
<div class="loadbar">
	<div class="bar" id="bar">10%</div>
</div>
```

```js
var bar = document.getElementById('bar');
var i = 0;
function startbar() {
	showbar = setInterval("setbar()",500);
}
startbar();
function setbar() {
	i += 10;
	if(i >= 100) {
		clearInterval(showbar);
	}
	bar.style.width = i + '%';
	bar.innerHTML = i + '%';
}
```
