# 去掉字符串中重复的单词并着色

```js
;(function (window) {
	var entity = document.getElementById('entity');
	var entityResult = entity.innerHTML;
	// window.str = entityResult;
  
  //以下注释代码为字符串单词去重
	// var wordArray = entityResult.match(/\][a-z]+/gi); //匹配字符串中]后面的英文单词

	// var newWordArray = [];
	// var contains = {};
	// for (var i = 0, len = wordArray.length; i < len; i++) {

	// 	(function (word) {

	// 		if (!contains[word]) {
	// 			newWordArray.push(word);
	// 			contains[word] = true;
	// 		}

	// 	})(wordArray[i].substring(1));
	// }

	// console.log(newWordArray);

	var wordSet = {
		'diseasetype': 'ff00a0',
		'disease': 'ff0000',
		'complaintsymptom': '0000ff',
		'testresult': '00b8ff',
		'test': 'B8860B',
		'treatment': '00ff00'
	};

	for (var key in wordSet) {

		(function (word, color) {

			var reg = new RegExp('(\\b' + word + '\\b)', 'gi');
			entityResult = entityResult.replace(reg, '<span style="color:' + color + ';">$1</span>');/*$1匹配正则表达式中括号里面的内容，给匹配到的单词加标签并设置样式*/

		})(key, '#' + wordSet[key]);

	}

	entity.innerHTML = entityResult;

})(window);
```
