###  数组

数组是引用类型的对象

原始类型：数据保存在变量本地

引用类型：数据不保存在变量本地！保存在'堆'中。由地址指向实际数据

> 引用类型的特点：

1. 可以保存多个数据，且数据个数随时可以改变
2. 引用类型可以保存多个值（原始类型中只能保存一个值，一个值无法精确描述一个东西,现实中往往用多个属性描述一样东西）
3. 使用引用类型的对象：使用变量，等效于使用对象的地址；使用对象地址，等效于使用对象本身

* var week = ['日','一','二','三','四','五','六'];

js中字符串放于栈中，而java中字符串放于堆中,凡是存储在堆中的都是对象
栈中创建一个变量空间，名为week

堆中创建一个大存储空间，地址是0x0901

栈中变量存储的是地址0x0901

堆空间中存储的是实际数据

week变量"引用"了堆中的一个数组对象

* var arr = new Array(num);
new要在堆中开辟空间

new Array在堆中创建一个数组类型的存储区域

num初始创建元素的个数

### 输入人员姓名并显示

```js
var items = [];
while((input = prompt('please input person')) != 'exit') {
	items[items.length] = input;
}
console.log(items);
```

### 栈中的变量生命周期与堆完全不同

* 全局变量

随网页生命周期

* 局部变量
* 
生命周期和所在方法的作用域环境栈有关，作用域创建，局部变量一同创建；作用域结束，局部变量一同消失。

### 何时使用关联数组？

数组元素的内容无法描述自己的意义时使用关联数组为每个元素起名

定义方式{'key1':'value1','key2':'value2'}

for in 专门遍历关联数组用的

```js
for(var key in obj) {
	//从第一个元素开始，将元素的key赋值给临时变量key
	obj[key]代表当前正在遍历的元素的值
}
```

> 创建一个函数bubbleSort(arr),实现冒泡排序(按值从小到大)

```js
var arr = [5,2,4,3,9,8,7];
function bubbleSort(arr) {
	//最外层是共进行length-1轮比较
	for(var n = 1;n < arr.length - 1;n++) {
		//每次比较查找剩余元素的最大数
		for(var i = 1;i < arr.length - n;i++) {//经过第n次比较将最大的值置换到最后
			if(arr[i] > arr[i+1]) {
				var box = arr[i];
				arr[i] = arr[i+1];
				arr[i+1] = box;
			}
	
		}
	}
	return arr;
}
var res = bubbleSort(arr);
//另法
for(var n = 1;n <= arr.length - 1;n++) {
	
	for(var i = 0,len = arr.length - n;i < len;i++) {
		<!--var curr = arr[i];-->
		<!--var next = arr[i+1];-->
		if(compareASC(arr[i],arr[i+1]) > 0) {
			var temp;
			temp = arr[i];
			arr[i] = arr[i+1];
			arr[i+1] = temp;
		}
	}
}
console.log(arr);
```
> 数组的常用方法

1. x.toString():任何对象都有此方法，将任何对象转为字符串，一般不主动调用，js在需要时自动调用
2. x.valueOf():同toString()
3. arr.join('分隔符'):将数组转为字符串。可自定义分隔符。典型用法：将字符拼接为单词或句子 chars.join('');
4. var newArr = arr.concat(元素值,[数组],...):将参数拆散成单个元素，追加到数组中,不会修改原数组，只能返回新数组对象
5. var subArr = arr.slice(start,end+1):截取数组下标从start开始，到end位置的元素，生成自数组对象。*含头不含尾*
6. arr.splice:删除、插入、替换
> 直接修改原数组，返回被删除的元素
* 删除：arr.splice(start,count);
* 替换：arr.splice(start,count,值1,值2,...);
* 插入：arr.splice(start,0,值1,值2,...);
```js
var arr1 = [5,2,4,3,9,8,7];
arr1.splice(1,2);
console.log(arr1);
arr1.splice(1,2,9,9)
console.log(arr1);
arr1.splice(1,0,5,6,8,0);
console.log(arr1);
```

7. arr.reverse():颠倒所有数组元素。

8. arr.sort():默认升序排列，改变原数组。
> 自定义sort排序方法使之支持升序和降序
```js
//定义比较器函数(定义任意两值比较策略的方法)
function compareASC(a,b) {
	return a - b;
}
//颠倒比较结果的正负，可以导致升序变降序
function compareDESC(a,b) {
	return b - a;
}
var arr = [1,4,9,2,8,3];
//将比较器函数传递给sort方法
var re = arr.sort(compareDESC);
console.log(re);
```
9. 栈和队列
* 实质上是一个数组，栈先进后出，只不过用一对儿方法模拟了栈
* 结尾入栈出栈：push:入栈，var last = arr.pop():出栈(弹出数组最后一个元素)
* 开头入栈出栈：unshift入栈，var first = arr.shift():出栈，从开头删除
