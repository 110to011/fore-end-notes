> 1. 随机数

Math.random() 0<=n<1
取任意min-max之间的随机数公式
function random(max,min) {
	var rn = parseInt(Math.random()*(max-min+1)+min);
	console.log(rn);
}
random(100,60);

> 2. 求100-999之间的水仙花数（自恋数）
如153=1*1*1+5*5*5+3*3*3
循环次数已知可以用for循环，
循环条件num<=999,循环变量num=100,num++
循环体num=百位*百位*百位+十位*十位*十位+个位*个位*个位
function narcissus() {
	for(var num = 100;num <=999;num++) {
		var hd = parseInt(num / 100);
		var ten = parseInt((num % 100) / 10);
		var one = num % 10;
		var result = hd*hd*hd + ten*ten*ten + one*one*one;
		if(num == result) {
			console.log(num);
		}
	}
}
narcissus();

> 3. 九九乘法表
//每一行的结果的计算
// for(var i = 1;i <=9;i++) {
// 	str += i + '*9=' + (i*9) + ' ';  
// }
// console.log(str);
// for(var i = 1;i <=8;i++) {
// 	str += i + '*8=' + (i*8) + ' ';  
// }
// console.log(str);
for(var i = 1;i <= 9;i++) {
	var str = "";
	for(var j = 1;j <= i;j++) {
		str += j + '*' + i + '=' + i*j + ' ';  
	}
	console.log(str);
}

> 4. 统计学生成绩的平均分
循环条件input!=-1
循环变量:input
循环体:sum+=input;count++
var sum = 0;
var count = 0;
do {
//prompt得到的是字符串，要进行算数运算需要转化为整形
var input = parseInt(prompt('please input your scores,input -1 to stop'));
var arg;
if(input == -1) {
  break;
}else {
  sum += input;
  count++;
  }
}while(1);
arg = (sum / count).toFixed(2);
console.log('平均分是：',arg);
		
