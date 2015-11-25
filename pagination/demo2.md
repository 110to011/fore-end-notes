# 异步分页-通过json方式渲染

> * page1.json

```json
{
	"pageNo" : 1,
	"pageSize" : 5,
	"totalPage" : 3,
	"data" : ["0001","0002","0003","0004","0005"]
}
```

> * page2.json

```json
{
	"pageNo" : 2,
	"pageSize" : 5,
	"totalPage" : 3,
	"data" : ["0006","0007","0008","0009","0010"]
}
```

> * page3.json

```json
{
	"pageNo" : 3,
	"pageSize" : 5,
	"totalPage" : 3,
	"data" : ["0011","0012","0013","0014","0015"]
}
```

```css
.pagination span,
.pagination a {
	display: inline-block;
	margin: 5px;
}
```

```html
<ul id="dataContainer"></ul>
<div id="pagination" class="pagination"></div>
<script type="text/javascript" src="page2.js"></script>
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

function getPageData(pageNo) {

	ajax('/page' + pageNo + '.json',function(data) {
		data = JSON.parse(data); //将字符串转换为对象
		render(data);
	});
}

var dataContainer = document.getElementById('dataContainer');
var pagination = document.getElementById('pagination');
function render(data) {
	var page = [];
	for(var i = 0,len = data.data.length;i < len;i++) {
		page.push('<li>' + data.data[i] + '</li>');
	}

	dataContainer.innerHTML = page.join('');

	var buttons = [];

	if(data.pageNo == 1) {
		buttons.push('<span>上一页</span>');
	}else {
		buttons.push('<a href="javascript:getPageData(' + (data.pageNo - 1) + ')">上一页</a>');
	}

	for(var j = 0;j < data.totalPage;j++) {

		if(data.pageNo === j + 1) {
			buttons.push('<span>' + (j + 1) + '</span>');
		} else {
			buttons.push('<a href="javascript:getPageData(' + (j + 1) +')">' + (j + 1) + '</a>');
		}
		
	}

	if(data.pageNo == data.totalPage) {
		buttons.push('<span>下一页</span>');
	}else {
		buttons.push('<a href="javascript:getPageData(' + (data.pageNo + 1) + ')">下一页</a>');
	}
	pagination.innerHTML = buttons.join('');
}
getPageData(1);
```
