### 常用的正则表达式

1. 验证手机号：(\+86)?\s+1[34578]\d{9}   

2. ?=x: 预判，前一个字符之后，必须紧跟x  

3. ?!x: 预判，前一个字符之后，不能跟x   

4. 匹配邮箱: \w+@\w+([-.]\w+)+  或者(\w+@\w+([-]\w+)*(\.\w+)+)  

5. 匹配中文姓名： [\u4e00-\u9fa5]{2,6}  

6. 找出html中所有的href
```html
<a(.+?)href\s*=['"](.*?)['"](.*?)>  
```
### RegExp对象  

 RegExp:专门封装一条正则表达式，提供使用正则表达式的常用API  
```js
var regExp1 = /正则表达式/ig; 
var regExp2 = new RegExp(pattern,attributes);  
var regExp1 = /\d{2,3}/ig;  
var regExp2 = new RegExp('\\d{2,3}','ig');
```
### 验证与查找的区别：

> 验证要求完整匹配，查找要求部分匹配(多加g)

* regExp.test('被检查的字符串') //test方法默认：只要找到就返回true;
> 进行验证即完整匹配时，前提是正则表达式中要前加^和后加$  

> 查找：exec:查找关键字的位置，也可以找到关键字的内容  

> var arr = regExp.exec('被查找的内容')，每次只能找到1个，但是每次自动修改regExp对象的lastIndex属性,此属性表示下次开始匹配的位置 
arr[0]:得到的是找到的关键字内容  
arr.index属性：得到的是所找到的关键字的位置
(indexOf不支持正则；search支持正则但是每次只能找1个；match可以找到所有内容但是得不到位置)  
exec就相当于indexOf+match  

### 两种模式
> * 贪婪模式：.+或.*默认先匹配整个字符串，再缩小范围  

> * 懒惰模式： (.+?)或(.*?)从第一个字符开始，向后扩展   

从正则表达式匹配的内容中，取一部分：RegExp.$n  
n:正则表达式中第n个分组(即第n个圆括号)，分组从1开始  

### String对象与正则表达式 
str = str.replace(/正则表达式/ig,'替换值');  
var arr = str.match(/正则表达式/ig);
str.split(/正则表达式/);  

> trim功能：去除字符串开始和结尾的空格。中间空格不去掉。对输入字符串的处理，多数要先清除开头结尾空格再处理。IE8不支持此方法
```js
function trim(str) {
	var regExp = /(^\s+)|(\s+$)/g;
	str = str.replace(regExp,'');
	return str;
}  
```

### Math API  
Math.round(num) 四舍五入取整  
Math.ceil(num) 向上取整  
Math.floor(num) 向下取整  

Math.pow(底数,幂)  
Math.sqrt(num) 平方根  
Math.abs(num) 取绝对值  
Math.max/min(值1,值2...,值n)  
快速找到数组中的最大值：var max = Math.max.apply(Math,arr)  

随机生成一个四位的随机验证码字符串  



