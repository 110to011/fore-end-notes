### 内置对象

> ECMAScript标准中已经定义好的，由浏览器厂商已经实现的标准对象。其中封装了专门的数据和操作数据常用的API。

> js中的内置对象如下：

1. String

创建原始类型字符串变量：放于栈中
var gender = 'female';//直接量
var priceString = String(150.5);//类型转换
创建引用类型字符串对象
var carType = new String('BMW');//放于堆中，要自己释放，不会自动释放
只有new才可以在堆中创建对象

2. Boolean

3. Number
前三个是包装类型(专门封装原始类型的数据，并提供对数据常用操作的内置类型。有包装类型的原因是让原始类型的数据可以像引用类型一样，拥有方法和属性)
何时使用包装类型：只要用原始类型的数据调用方法或访问属性时，js引擎都会自动创建对应的包装类型对象。方法调用完，包装类型对象自动释放。

4. Array

5. Date

6. Math

7. Error

8. Function 

9. Object

10. Global

###字符串的使用

字符串内容一旦创建不可改变，若修改，则要创建新字符串；保存新结果，替换旧字符串
规律：所有字符串API，均需要变量接收返回值！
字符串类型的底层是用字符数组实现的，访问可以通过str[i]
var str = 'Hello';
str += 'World';
共创建了三个string对象

str.length: 返回str字符串中字符的个数
大小写转换：
转小写：str.toLowerCase()
转大写：str.toUpperCase()
获取指定位置字符：var char = str.charAt(index);//在index位置的字符
获取指定位置字符的unicode编号：var num = str.charCodeAt(index);

优化：
频繁对字符串+=，要用数组代替！
每个子字符串放入数组
join('')拼接数组元素

### 字符串的三大操作

1. 查找关键字
var index = str.indexOf('关键字');//从头开始查找关键字首次出现的位置
查找成功返回关键字所在位置，若未找到返回-1
var index = str.indexOf('关键字',from);//from:开始查找的位置,从from开始向后查找

从最后一个字符开始向前找：
var index = str.lastIndexOf('关键字',from);//从from位置开始向前查找

2. 替换关键字
str.replace(reg,'新值');默认replace仅替换第一个关键字

3. 获取子字符串

var subStr = str.slice(start,end+1)//支持负值做参数
str.substring(start,end+1)//不支持负值
str.substr(start,count);

4. 检索字符串
indexOf()

5. 分隔字符串

var substr = split(separator[,count]);
将一个字符串中每个单词的首字母变成大写
var str = 'nothing is imposibile to a willing heart';
function exchange(str) {
	var words = str.split(' ');
	for(var i = 0;i < words.length;i++) {
		words[i] = words[i][0].toUpperCase() + words[i].substring(1);
	}
	str = words.join(' ');
	return str;
}

计算一段字符串中 英文字符、中文字符、数字、其他字符的数量
判断字符的种类：unicode范围
48-57: 0-9 数字字符
65-90: A-Z 大写字母
97-122: a-z 小写字母
19968-40869: 汉字

> ```js
var str = '选购AppleCare+,延保2年';
function count(str) {
  var engCount = 0;
  var numCount = 0;
  var chsCount = 0;
  var other = 0;
  for(var i = 0;i < str.length;i++) {
  	var num = str.charCodeAt(i);
  	if(num >= 19968 && num <= 40869) {
  		chsCount++;
  	}else if((num >= 65 && num <= 90) || (num >=97 && num <=122)) {
  		engCount++;
  	}else if(num >= 48 && num <= 57) {
  		numCount++;
  	}else {
  		other++;
  	}
  }
  document.write('<br>' + '汉字:' + chsCount + '<br>' + '数字:' + numCount
  	+ '<br>' + '字母:' + engCount
  	+ '<br>' + '其他字符:' + other + '<br>');
}

	```
### 模式匹配

可以设置查找或替换的规则
何时使用模式匹配：要查找的关键字可能发生有规律的变化。
如何使用：先定义模式：/关键字/模式
var reg = /no/ig;//i表示忽略大小写，g表示全局查找/替换

获得所有关键字的内容： var kwords = str.match(reg);
只能取得关键字内容，无法确定每个关键字的位置，kwords.length是找到关键字的个数，若未找到则返回null；只要有可能返回null，就要先判断!=null再处理

var index = str.search(reg)和indexOf完全相同，indexOf不支持模式查找，search是indexOf的模式查找版

### 什么是正则表达式？
字符串中字符出现的规律
何时使用它？验证字符串格式，查找和替换关键字
银行卡查询密码：6位数字
用户名：字母、数字、_的组合

var str = 'yes Yes';
var reg = /yes/ig;
var words = str.match(reg);
document.write(words + '<br>');
str = str.replace(reg,'***');
document.write(str + '<br>');
document.write('共替换' + words.length + '处');

所有单个大小写字母、数字都是一个正则表达式
以原文写出来的是必须的,[]是多选一，[^xxxx]表示除了xxxx都行，^必须放在[]中的第一个位置，否则作为普通字符匹配

-表示字符的范围：备选字符连续的范围,可以局部使用
如：[0-9] [a-z] [A-Z] [a-zA-Z] 
汉字： [\u4e00-\u9fa5]

> 正则表达式中可以用元字符引用进行简化

\d 匹配一个数字[0-9]

\D 匹配一个非数字

\w 匹配一个数字/字母/下划线 [a-zA-Z_] 字母数字下划线

\W 匹配一个非数字/字母/下划线 等价于[^0-9a-zA-Z_] 

\s 匹配空格
 
 . 匹配所有
 特殊符号转为原文用\,比如\.
