# 普通分页-数据在本地获取时

```css
<style type="text/css">
		.pagination input {
			display: inline-block;
			margin: 5px;
		}
	</style>
```

```html
<ul id="dataContainer"></ul>
<div id="pagination" class="pagination"></div>
<script type="text/javascript" src="data.js"></script><!--放置本地数据-->
<script type="text/javascript" src="page.js"></script><!--显示数据和分页，绑定点击事件-->
```

```js
var dataContainer = document.getElementById('dataContainer');
var pagination = document.getElementById('pagination');

var pageSize = 5; //每页显示5条数据
var current = 1; //当前页索引

//获取每一页的数据
function getPage(pageNo) { //pageNo从1开始，索引从0开始
	var page = []; //将取到的数据放入page中，显示到ul中
	current = pageNo;
	// 每页的起始编号与结束编号
	var firstNo = (pageNo - 1)*pageSize;
	var lastNo = pageNo*pageSize - 1;

	if(lastNo > data.length - 1) {
		lastNo = data.length - 1;
	}
	for(var i = firstNo;i <= lastNo;i++) {

		page.push('<li>' + data[i] + '</li>');
	}
	dataContainer.innerHTML = page.join('');
}

//产生分页按钮
function generatePagination() {
	totalPage = Math.ceil(data.length / pageSize);

	var pages = ['<input type="button" value="上一页">'];
	for(var i = 0;i < totalPage;i++) {
		pages.push('<input type="button" value ="'+ (i+1) +'">');
	}
	pages.push('<input type="button" value ="下一页">');

	pagination.innerHTML = pages.join('');
	bindPageNoEvent();
}

//绑定点击事件
function bindPageNoEvent() {
	var pageButtons = document.querySelectorAll('input');
	var	len = pageButtons.length;
	for(var i = 0;i < len;i++) {
		(function(button) {

			button.addEventListener('click',function() {
				
				var pageNo = this.value;
				
				if(pageNo == '上一页') {
					pageNo = current - 1;
			
					if(pageNo === 0) {
						return false;
					}
				} else if(pageNo == '下一页') {
					pageNo = current + 1;

					if(pageNo === totalPage + 1) {
						return false;
					}
				}
				getPage(pageNo);
			});
		})(pageButtons[i]);
	}
}

getPage(1);
generatePagination();
```



