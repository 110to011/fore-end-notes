# 异步分页-通过哈希分页

用到的几个html文件参见demo3中的

```css
.pagination span,
.pagination a {
	display: inline-block;
	margin: 5px;
}
```

```html
<div id="container"></div>
<script type="text/javascript" src="page4.js"></script>
```

```js
function ajax(url,callback) {
	var xhr = new XMLHttpRequest();
	
	xhr.open('GET',url,true);
	xhr.onreadystatechange = function() {
		if(xhr.readyState == 4 && xhr.status == 200) {
			callback(xhr.responseText);
		}
	}
	xhr.send();
}

var container = document.getElementById('container');
//异步分页，局部刷新；当把当前页复制到新的一页时内容也不会改变
function getPageData(pageNo) {
	location.hash = '#' + pageNo;
	ajax('/index' + pageNo + '.html',function(data) {
		container.innerHTML = data;
	});
}

var hash = location.hash;

getPageData(hash ? hash.substring(1) : 1);
```
