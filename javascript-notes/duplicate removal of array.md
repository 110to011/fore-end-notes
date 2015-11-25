# 数组去重

> 思路：首先定义一个空的对象和一个存放结果的数组，然后遍历数组，设置对象中的键为数组中的元素，判断当对象中的键所对应的值为false时，
说明是第一次出现，将键存入结果数组，将其对应的值置为true,再次进行判断

```js
var arr = ['1','1','2','4'];

var obj = {};
var result = [];
for(var i = 0,len = arr.length;i < len;i++) {
	var key = arr[i];
	
	if(!obj[key]) {
		result.push(key);
		obj[key] = true;
	}

}
console.log(result);

```
