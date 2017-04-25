## 使用css3绘制小黄人
```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		.body {
			margin: 0;
			padding: 0;
		}
		.wrapper {
			margin: 100px auto;
			width: 300px;
		}
		.littleH {
			position: relative;
		}
		.bodyH {
			position: absolute;
			width: 240px;
			height: 400px;
			border: 5px solid #000;
			border-radius: 115px;
			background: rgb(249,217,70);
			overflow: hidden;
			z-index: 2; 
		}
		/*裤子*/
		.bodyH .condoleBelt {
			position: absolute;
		}
		.bodyH .trousers {
			position: absolute;
			bottom: 0;
			width: 100%;
			height: 100px;
			border-top: 6px solid #000;
			background-color: rgb(32,116,160);
		}
		.trousers_top {
			position: absolute;
			bottom: 100px;
			left: 34px;
			width: 160px;
			height: 60px;
			border: 6px solid #000;
			border-bottom: none;
			border-radius: 0 0 5px 5px;
			background-color: rgb(32,116,160);
		}
		.bodyH .condoleBelt .left,
		.bodyH .condoleBelt .right {
			position: absolute;
			top: -90px;
			left: -35px;
			z-index: 2;
			width: 100px;
			height: 16px;
			border: 5px solid #000;
			background-color: rgb(32,116,160);
			-webkit-transform: rotate(45deg);
			transform: rotate(45deg);
		}
		.bodyH .condoleBelt .left:after,
		.bodyH .condoleBelt .right:after {
			content: '';
			position: absolute;
			left: 88px;
			top: 4px;
			width: 8px;
			height: 8px;
			border-radius: 50%;
			background: #000;
		}
		.bodyH .condoleBelt .left:after {
			left: 5px;

		}
		.bodyH .condoleBelt .left {
			top: -88px;
			left: 165px;
			-webkit-transform: rotate(-45deg);
		}
	
		.pocket {
			position: absolute;
			bottom: 65px;
			left: 84px;
			width: 60px;
			height: 45px;
			border: 6px solid #000;
			border-radius: 0 0 25px 25px;
		}
		.line_left {
			position: absolute;
			bottom: 63px;
			right: 0;
			width: 30px;
			height: 30px;
			border-bottom: 6px solid #000;
			border-right: 6px solid #000;
			border-bottom-right-radius: 100px;
			-webkit-transform: rotate(75deg);
			transform: rotate(75deg);
		}
		.line_right {
			position: absolute;
			left: 0;
			bottom: 60px;
			width: 30px;
			height: 30px;
			border-bottom: 6px solid #000;
			border-left: 6px solid #000;
			border-bottom-left-radius: 100px;
			-webkit-transform: rotate(-75deg);
			transform: rotate(-75deg);
		}
		.line_bottom {
			position: absolute;
			left: 118px;
			bottom: 0;
			height: 40px;
			border: 3px solid #000;
			border-radius: 3px;
		}
		/*眼睛*/
		.eyes {
			position: relative;
			z-index: 3;
		}
		.eyes .leftEye,
		.eyes .rightEye {
			position: absolute;
			top: 60px;
			left: 27px;
			width: 85px;
			height: 85px;
			border-radius: 50%;
			border: 6px solid #000;
			background-color: #fff;
		}
		.eyes .leftEye {
			left: 124px;
		}
		.eyes .leftEye .left_blackEye,
		.eyes .rightEye .right_blackEye {
			position: absolute;
			top: 24px;
			left: 22px;
			width: 40px;
			height: 40px;
			border-radius: 50%;
			background-color: #000;
			-webkit-animation: blackeye 5s ease-in infinite;
			animation: blackeye 5s ease-in infinite;
		}
		@-webkit-keyframes blackeye {
			0%,20%,50%,70%,100% {
				-webkit-transform: translateX(0);
			}
			30%,40% {
				-webkit-transform: translateX(15px);
			}
			80%,90% {
				-webkit-transform: translateX(-15px);
			}
		}
		.eyes .leftEye .left_blackEye .left_white,
		.eyes .rightEye .right_blackEye .right_white {
			position: absolute;
			top: 7px;
			left: 17px;
			width: 20px;
			height: 20px;
			border-radius: 50%;
			background-color: #fff;
			-webkit-animation: whiteeye 5s ease-in-out infinite;
		}
		@-webkit-keyframes whiteeye {
			0,20%,50%,70%,100% {
				-webkit-transform: translateX(0);
			}
			30%,40% {
				-webkit-transform: translate3d(3px,4px,0);
			}
			80%,90% {
				-webkit-transform: translate3d(-15px,4px,0);
			}
		}
		.eyes .leftEye .left_blackEye .left_white {
			top: 4px;
			left: 17px;
		}
		.eyes .leftEye:after,
		.eyes .rightEye:after {
			content: '';
			position: absolute;
			top: 37px;
			left: -30px;
			width: 28px;
			height: 18px;
			background-color: #000;
			-webkit-transform: skewX(20deg) rotate(7deg);
			transform: skewX(20deg) rotate(7deg);
		}
		.eyes .leftEye:after {
			left: 89px;
			top: 37px;
			-webkit-transform: skewX(-20deg) rotate(-7deg);
			transform: skewX(-20deg) rotate(-7deg);
		}
		.mouse {
			position: relative;
		}
		.mouse .mouse_shape {
			position: absolute;
			top: 175px;
			left: 98px;
			z-index: 3;
			width: 55px;
			height: 35px;
			border: 5px solid #000;
			border-bottom-left-radius: 30px;
			background-color: #fff;
			-webkit-transform: rotate(-35deg);
			transform: rotate(-35deg);
			-webkit-animation: mouse 5s ease-in-out infinite;
		}
		@-webkit-keyframes mouse {
			40%,43% {
				width: 45px;
				height: 25px;
				top: 180px;
			}
			0%,35%,48%,100% {
				width: 55px;
				height: 35px;
				top: 175px;
				-webkit-transform: rotate(-35deg);
			}
		}
		.mouse .mouse_shape:after {
			content: '';
			position: absolute;
			top: -16px;
			left: 3px;
			width: 70px;
			height: 32px;
			border-bottom: 5px solid #000;
			border-radius: 35px 26px 5px 5px;
			background-color: rgb(249,217,70);
			-webkit-transform: rotate(34deg);
			-moz-transform: rotate(34deg);
			-ms-transform: rotate(34deg);
			-o-transform: rotate(34deg);
			transform: rotate(34deg);
			-webkit-animation: mouse_mask 5s ease-in-out infinite;
		}
		@-webkit-keyframes mouse_mask {
			40%,43% {
				width: 60.5px;
				top: -19.3px;
				left: 1.5px;
			}
			0%,35%,48%,100% {
				width: 70px;
				top: -16px;
				left: 3px;
				-webkit-transform: rotate(33deg);
			}
		}
		.hands {
			position: relative;
		}
		.hands .rightHand,
		.hands .leftHand {
			position: absolute;
			top: 220px;
			left: -23px;
			width: 80px;
			height: 80px;
			border: 6px solid #000;
			border-radius: 25px;
			background-color: rgb(249,217,70);
			-webkit-transform: rotate(40deg);
			-moz-transform: rotate(40deg);
			-ms-transform: rotate(40deg);
			-o-transform: rotate(40deg);
			transform: rotate(40deg);
		}
		.hands .leftHand {
			left: 182px;
			top: 220px;
			-webkit-transform: rotate(-40deg);
			-moz-transform: rotate(-40deg);
			-ms-transform: rotate(-40deg);
			-o-transform: rotate(-40deg);
			transform: rotate(-40deg);
			-webkit-animation: leftHand .8s ease-in-out infinite;
		}
		.hands .rightHand {
			-webkit-animation: rightHand .8s ease-in-out infinite;
		}
		@-webkit-keyframes leftHand {
			0%,50%,100% {
				-webkit-transform: rotate(-40deg);
			}
			80% {
				-webkit-transform: rotate(-37deg) translateX(-1px);
			}
		}
		@-webkit-keyframes rightHand {
			0%,50%,100% {
				-webkit-transform: rotate(40deg);
			}
			30% {
				-webkit-transform: rotate(37deg) translateX(1px);
			}
		}
		.hands .leftHand:after,
		.hands .rightHand:after {
			content: '';
			position: absolute;
			top: 50px;
			left: 13px;
			width: 6px;
			border: 3px solid #000;
			border-radius: 3px;
			-webkit-transform: rotate(90deg);
			-moz-transform: rotate(90deg);
			-ms-transform: rotate(90deg);
			-o-transform: rotate(90deg);
			transform: rotate(90deg);
		}
		.hands .leftHand:after {
			left: 53px;
			top: 50px;
			-webkit-transform: rotate(-90deg);
			-moz-transform: rotate(-90deg);
			-ms-transform: rotate(-90deg);
			-o-transform: rotate(-90deg);
			transform: rotate(-90deg);
		}
		.feet {
			position: relative;
		}
		.feet .left_foot,
		.feet .right_foot {
			position: absolute;
			top: 406px;
			left: 88px;
			width: 36px;
			height: 50px;
			border-bottom-right-radius: 6px;
			border-bottom-left-radius: 9px;
			background-color: #000;
			-webkit-transform-origin: right top;
			-moz-transform-origin: right top;
			-ms-transform-origin: right top;
			-o-transform-origin: right top;
			transform-origin: right top;
		}
		.feet .right_foot {
			-webkit-animation: rightfoot .8s ease-in-out infinite;
		}
		@-webkit-keyframes rightfoot {
			0,50%,100% {
				-webkit-transform: rotate(0deg);
			}
			80% {
				-webkit-transform: rotate(10deg);
			}
		}

		.feet .left_foot {
			border-bottom-right-radius: 9px;
			border-bottom-left-radius: 6px;
			left: 130px;
			-webkit-transform-origin: left top;
			 -moz-transform-origin: left top;
			 -ms-transform-origin: left top;
			 -o-transform-origin: left top;
			 transform-origin: left top; 
			 -webkit-animation: leftfoot .8s ease-in-out infinite;
		}
		@-webkit-keyframes leftfoot {
			0,50%,100% {
				-webkit-transform: rotate(0deg);
			}
			30% {
				-webkit-transform: rotate(-10deg);
			}
		}
		.feet .left_foot:after,
		.feet .right_foot:after {
			content: '';
			position: absolute;
			left: -36px;
			top: 14.4px;
			width: 60px;
			height: 35px;
			border-radius: 20px 10px 21px 15px;
			background-color: #000;
			-webkit-transform: rotate(5deg);
			-moz-transform: rotate(5deg);
			-ms-transform: rotate(5deg);
			-o-transform: rotate(5deg);
			transform: rotate(5deg);
		}
		.feet .left_foot:after {
			left: 13px;
			border-radius: 10px 20px 15px 21px;
			-webkit-transform: rotate(-5deg);
			-moz-transform: rotate(-5deg);
			-ms-transform: rotate(-5deg);
			-o-transform: rotate(-5deg);
			transform: rotate(-5deg);
		}
		.hair {
			position: relative;
		}
		.left_hair_one {
			position: absolute;
			top: -17px;
			left: 17px;
			width: 130px;
			height: 100px;
			border-radius: 50%;
			border-top: 8px solid #000;
			-webkit-transform: rotate(27deg);
			-moz-transform: rotate(27deg);
			-ms-transform: rotate(27deg);
			-o-transform: rotate(27deg);
			transform: rotate(27deg);
			-webkit-animation: lefthair 2s ease-in-out infinite;
			/*-moz-animation: lefthair 2s ease-in-out infinite;
			-ms-animation: lefthair 2s ease-in-out infinite;
			-o-animation: lefthair 2s ease-in-out infinite;*/
			/*animation: lefthair 2s ease-in-out infinite;*/
		}
		.left_hair_two {
			position: absolute;
			top: -10px;
			left: 45px;
			width: 80px;
			height: 80px;
			border-radius: 50%;
			border-top: 6px solid #000;
			-webkit-transform: rotate(15deg);
			-moz-transform: rotate(15deg);
			-ms-transform: rotate(15deg);
			-o-transform: rotate(15deg);
			transform: rotate(15deg);
		}
		.groundShadow {
			position: relative;
			left: 25px;
			top: 455px;
			width: 200px;
			height: 2px;
			border-radius: 50%;
			background-color: rgba(0,0,0,.3);
			box-shadow: 0 0 2px 4px rgba(0,0,0,.3);
		}
		@-webkit-keyframes lefthair {
			0%,25%,31%,100% {}
			30% {
				-webkit-transform: translate3d(-3px,-1px,0);
			}
		}
	</style>
</head>
<body>
	<!--容器-->
	<div class="wrapper">
		<!-- 小黄人 -->
		<div class="littleH">
			<!-- 身体 -->
			<div class="bodyH">
				<!-- 裤子 -->
				<div class="trousers">
					<!-- 吊带 -->
					<div class="condoleBelt">
						<div class="left"></div>
						<div class="right"></div>
					</div>
					<!-- 裤子突出的矩形部分 -->
					<div class="trousers_top"></div>
					<!-- 裤带 -->
					<div class="pocket"></div>
					<!-- 裤子上的三条线 -->
					<span class="line_left"></span>
					<span class="line_right"></span>
					<span class="line_bottom"></span>
				</div>
			</div>
			<!-- 头发 -->
			<div class="hair">
				<span class="left_hair_one"></span>
				<span class="left_hair_two"></span>
			</div>
			<!-- 眼睛 -->
			<div class="eyes">
				<div class="leftEye">
					<div class="left_blackEye">
						<div class="left_white"></div>
					</div>
				</div>
				<div class="rightEye">
					<div class="right_blackEye">
						<div class="right_white"></div>
					</div>
				</div>
			</div>
			<!-- 嘴巴 -->
			<div class="mouse">
				<div class="mouse_shape"></div>
			</div>
			<!-- 双手 -->
			<div class="hands">
				<div class="leftHand"></div>
				<div class="rightHand"></div>
			</div>
			<!-- 双脚 -->
			<div class="feet">
				<div class="left_foot"></div>
				<div class="right_foot"></div>
			</div>
			<!-- 脚底阴影 -->
			<div class="groundShadow"></div>
		</div>
	</div>
</body>
</html>
```
