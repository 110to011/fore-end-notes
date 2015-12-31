### each方法
```js
		//each方法可以遍历数组元素
		// jQuery.each(array,callback);

		//单纯的数组最好不要用jQuery的each方法
		//因为其实现中是for循环中遍历每个元素，将对象this传回去
		//而且将DOM中的东西加入进去，简单的循环方法里面嵌套了很多的调用，消耗的东西更多。

		// jQuery.each([1,2,3],function(index,ele) {
		// 	console.log(this,index,ele); //遍历单纯的数组时,this是不可控的,在此是Number的实例
		// });


		//each方法可以遍历jQuery元素

		jQuery.each($('script'),function(index,ele) {
		console.log(this,index,ele); //遍历jQuery的数组时,this指的是ele
		});

		jQuery.each = function(array,callback) {
		//for
		//
		};

		jQuery.fn.each = function(callback) {
		jQuery.each(this,callback);
		return this;

		};

		$('script').each();
```
### map方法
```js
		//map方法与each方法的不同在于
		//回调方法中参数的顺序不同，后者是元素和索引，前者是索引和元素
		//前者的this是指window,后者的this是指元素
		//map方法遍历循环每一个元素，回调方法中必须有返回值，此返回值作为新的元素插入到新的数组中，此新数组作为返回值返回给a
		//each方法遍历循环每一个元素，如果是jQuery对象则返回jQuery数组
		var a = jQuery.map($('script'),function() {
		// return arguments[0].src;
		console.log(this,arguments[0],arguments[1]);
		});

		var b = jQuery.each($('script'),function() {
		console.log(this,arguments[0],arguments[1]);
		})

		//jQuery中map的实现
		jQuery.map = function(array,callback) {
		var result = [];

		for(var i = 0,len = array.length;i < len;i++) {
			// result.push(callback(array[i],i));
			result[result.length] = callback(array[i],i);
		}
	}

		//当定义一个方法时，其参数未知时可以通过arguments属性来获取其传递的参数，它代表实际传递的几个参数
		function a() {
		console.log(arguments);
		}
		a(1,2,3);
		a.length是0

		function b(a,b){}
		b.length是2

		//方法也有返回值，其返回值为参数的个数

		a=b
		a的返回值为b
		function b(a,b){}
```
### data方法
```js
		//data方法有三个参数：元素、名称、值(ele,name,data)
		jQuery.data(document.body,'wxt','ting');//返回值为data即ting
		jQuery.data(document.body,'wxt',{name:'ting'});//返回值为{name:'ting'}

		//不传第三个参数是取值，传第三个参数是赋值
		jQuery.data(document.body,'wxt')

		//jQuery.fn.data 的参数为key与value
		jQuery.data(jQuery.fn)

		//不赋值时若想取得值可以通过在元素中添加data-name='data'的方式在js中通过以下代码得到name的值
		jQuery('body').data('wxt')//得到值xiaoting
```
### extend方法
```js
		//extend方法的参数是对象而不是方法,可以用来进行方法的扩展
		jQuery.extend({
		// eat: function(food) {
		// 	console.log('eat');
		// 	console.log('\n%s',food);
		// },
		eat: function() {
			console.log('eat');
			console.log('\n',Array.prototype.join.call(arguments,'and'));
		},
		sing: function() {
			console.log('sing');
		}
		});

		//一般jQuery.fn的方法会返回this,目的是方便链式调用
		jQuery.fn.extend({
		// eat: jQuery.eat,
		// sing： jQuery.sing
		// eat: function(food) {
		// 	jQuery.eat(food);
		// 	return this;
		// },

		// 一个方法调用另一个方法而不知道那个方法接收哪些参数的情况下可以用apply的方式
		eat: function() {
			jQuery.eat.apply(jQuery,arguments);
			return this;
		},

		sing: function() {
			jQuery.sing();
			return this;
		}
		});

		//当传多个对象时已知情况是对各个对象
		//进行合并，且后面的值会将前面的值覆盖
		//另一种情况是全部覆盖
		jQuery.extend({a:1,b:2},{c:3});
```
