### jQuery插件的写法

```js
(function($) {
	'use strict';

	var array_join = Array.prototype.join;

	var defaults = {
		team: 'fontend',
		member: ['lily','rose'],
		address: 'xierqi',
		time: new Date,
		foods: []
	};

	jQuery.eat = function(options) {
		// console.log(array_join.call(arguments,'and'));
		var str = defaults.team + '[' + defaults.member.join(',') + ']';

		// defaults.foods = options;
		
		options = jQuery.extend({},defaults,options);
		str += options.team + '[' + options.member.join(',') + ']';
		str += '在' + options.time;
		str += '去' + options.address + '吃';
		str += array_join.call(options.foods,'and');

		console.log(str);
	};
})(jQuery);
```
> extend方法有深拷贝和浅拷贝，当要扩展的对象是比较复杂的对象时，第一个参数是true时为深拷贝，将里面的参数一级一级覆盖

> 当第一个参数是false时为浅拷贝，全部进行覆盖
