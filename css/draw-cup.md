```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>cup</title>
	<style>
		body {
			margin: 0;
			background-color: #ccf;
		}
		.content {
			position: relative;
			margin: 100px auto 0;
			width: 300px;
			height: 360px;
			animation: cup 10s linear 3s 10;
		}

		@keyframes cup {
			0% {
				transform: rotateY(0deg);
			}
			25% {
				transform: rotateY(50deg);
			}
			50% {
				transform: rotateY(120deg);
			}
			100% {
				transform: rotateY(0);
			}
		}
		.cup-top {
			position: absolute;
			top: -25px;
		    width: 300px;
		    height: 50px;
		    background-color: #fff;
		    border-radius: 50%;
		    /*border: 1px solid #ccc;
		    box-shadow: 0 5px #fff,0 6px rgba(0,0,0,0.1) inset;*/
		    box-shadow: 0 4px 2px #fff,0 30px rgba(0, 0, 0, 0.03) inset;
		}
		.cup-body {
			position: absolute;
			width: 200px;
			height: 0;
			border-top: 360px solid #fcf;
			border-left: 50px solid transparent;
			border-right: 50px solid transparent;
		}
		.cup-bottom {
			position: absolute;
			left: 50px;
			bottom: -25px;
			width: 200px;
			height: 50px;
			border-radius: 50%;
			background-color: #fcf;
			box-shadow: 0 2px #fff;
		}
		h4 {
			position: absolute;
			left: 80px;
			bottom: 220px;
			margin: 0;
			font-size: 25px;
			letter-spacing: 2px;
		}
		.eng {
			bottom: 199px;
			font-size: 13px;
		}
		h5 {
			margin: 0;
			position: absolute;
			bottom: 64px;
			letter-spacing: 8px;
			font-size: 16px;
		}
		p {
			position: absolute;
			bottom: 41px;
			margin: 0;
			font-size: 14px;
			font-weight: 700;
		}
		.pic {
			position: absolute;
			left: 50%;
			bottom: 180px;
			margin-left: -100px;
			width: 200px;
			height: 100px;
			background: url(logo.png) no-repeat -10px 0/cover;
		}
	</style>
</head>
<body>
	<div class="content">
		<div class="cup-body">
			<div class="pic"></div>
			<!-- <h4>神州数码</h4>
			<h4 class="eng">Digital China</h4> -->
			<h5>中國智慧城市專家</h5>
			<p>Leading Sm@rt City in China</p>
		</div>
		<div class="cup-top"></div>
		<div class="cup-bottom"></div>
	</div>
	
</body>
</html>
```
