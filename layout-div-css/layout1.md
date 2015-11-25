# 一列固定宽度居中 (参见dj-art.com)

```css
body {
	font-family: Arial,"宋体";
	font-size: 14px;
	color: #e6e6e6;
	margin: 0px;
	background: #7c7c7c;
}
.wrap {
	width: 960px;
	margin: 0 auto;
}
.header {
	height: 200px;
	background-color: #ccc;
}
.header h3 {
	text-align: center;
	margin: 0;
	line-height: 200px;
}
.content {
	height: 500px;
}
.left {
	float: left;
	width: 200px;
	height: 500px;
	background-color: #0ff;
}
.right {
	float: right;
	width: 760px;
	height: 500px;
	background-color: #f0f;
}
.list {
	list-style: none;
	margin: 0;
	padding: 0;
}
.list li {
	position: relative;
	height: 32px;
	margin: 0 0 5px 0;
	padding: 0;
}
.triangle {
	position: absolute;
	top: 0;
	left: 0;
	border-left: 32px solid #fde35b;
	border-bottom: 32px solid transparent;
	height: 0px;
	width: 0px;
	top: 0px;
	left: 0px;
}
.link {
	position: absolute;
	top: 0;
	left: 0;
	text-align: center;
	color: #fff;
	text-decoration: none;
	width: 200px;

	height: 32px;
	line-height: 32px;

	background-color: rgb(0, 131, 154);
}
.ranktext {
  position: absolute;
  top: 3px;
  left: 2px;
}
.ranktext a {
	color: #886235;
	font-size: 11px;
	font-weight: bold;
	text-decoration: none;
}
.footer {
	width: 960px;
	margin: 0 auto;
	text-align:center;
	padding-top:20px;
}
	
```

```html
<div class="wrap">
	<div class="header">
		<h3>一列固定宽度居中</h3>
	</div>
	<div class="content">
		<div class="left">
			<ul class="list">
				<li>
					<a href="#" class="link">javascript</a>
					<div class="triangle"></div>
					<div class="ranktext"><a href="javascript:;">1</a></div>
				</li>
				<li>
					<a href="#" class="link">javascript</a>
					<div class="triangle"></div>
					<div class="ranktext"><a href="javascript:;">2</a></div>
				</li>
				<li>
					<a href="#" class="link">javascript</a>
					<div class="triangle"></div>
					<div class="ranktext"><a href="javascript:;">3</a></div>
				</li>
				<li>
					<a href="#" class="link">javascript</a>
				</li>
				<li>
					<a href="#" class="link">javascript</a>
				</li>
			</ul>
		</div>
		<div class="right"></div>
	</div>
</div>
<div class="footer">
	Copyright © wxt.com
</div>
```
