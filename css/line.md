```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		.content {
			position: relative;
			text-align: center;
			line-height: 48px;
		}
		h3 {
			position: relative;
			display: inline-block;
			margin: 0;
			font-size: 20px;
			background-color: #fff;
		}
		.content::before {
			/*z-index: -1;*/
			position: absolute;
			top: 50%;
			left: 0;
			right: 0;
			content: "";
			border-top: 1px solid #ccc;
		}

		.parallel {
			float: left;
			width: 48%;
			margin: 0 2px;
		}
	</style>
</head>
<body>
	<!-- 有两种使文字浮于线上方的方法：一是给h3加position:relative,二是给content的before加z-index:-1 -->
	<div class="content">
		<h3>就是一条线</h3>
	</div>

	<div class="content parallel">
		<h3>就是一条线</h3>
	</div>
	<div class="content parallel">
		<h3>就是一条线</h3>
	</div>
</body>
</html>
```
##### z-index和position:relative有两种适用场景：
> 当z-index设置为-1时，若父级的background-color:#fff，则线就会消失。所以当父级设置背景色时，它的before不能设置z-index为-1
> 当h3中有div等其他内容时h3设置为position:relative时就会影响其内部的元素
```
