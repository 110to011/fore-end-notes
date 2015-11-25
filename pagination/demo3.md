# 异步分页-通过html方式渲染

> * index1.html

```html

<ul>
	<li>0001</li>
	<li>0002</li>
	<li>0003</li>
	<li>0004</li>
	<li>0005</li>
</ul>

<div class="pagination">
	<span>上一页</span>
	<span>1</span>
	<a href="javascript:getPageData(2)">2</a>
	<a href="javascript:getPageData(3)">3</a>
	<a href="javascript:getPageData(2)">下一页</a>
</div>

```


> * index2.html


```html

<ul>
	<li>0006</li>
	<li>0007</li>
	<li>0008</li>
	<li>0009</li>
	<li>0010</li>
</ul>

<div class="pagination">
	<a href="javascript:getPageData(1)">上一页</a>
	<a href="javascript:getPageData(1)">1</a>
	<span>2</span>
	<a href="javascript:getPageData(3)">3</a>
	<a href="javascript:getPageData(3)">下一页</a>
</div>

```
> * index3.html

```html

<ul>
	<li>0011</li>
	<li>0012</li>
	<li>0013</li>
	<li>0014</li>
	<li>0015</li>
</ul>

<div class="pagination">
	<a href="javascript:getPageData(2)">上一页</a>
	<a href="javascript:getPageData(1)">1</a>
	<a href="javascript:getPageData(2)">2</a>
	<span>3</span><span>下一页</span>
</div>

```


```css
.pagination span,
.pagination a {
	display: inline-block;
	margin: 5px;
}
```

```html
<div id="container"></div>
<script type="text/javascript" src="page3.js"></script>
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
function getPageData(pageNo) {

	ajax('/index' + pageNo + '.html',function(data) {
		container.innerHTML = data;
	});
}

getPageData(1);
```
