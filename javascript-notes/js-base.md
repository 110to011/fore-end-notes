怎样触发手机端的select
select透明度为0，外面包div，给其做监听事件

css+html
页面将html全渲染完成后，保证页面在没有css时为保证用户基本操作
添加收藏：将按钮改成超链接，给超链接绑定事件，将发给后台的http请求地址放到href中

### js基础知识

1. script中脚本块何时运行？

随网页加载，解释执行(即读到才执行，先读到先执行，后读到后执行)，其放置的先后顺序影响程序的执行结果。  
2. 什么是事件？

元素可以根据鼠标或键盘的不同操作响应不同的交互行为  
3. script最好放在body的最后，为什么？(优化问题)

这样可以不影响用户的使用，因为用户最想看到的是首先是页面，其次才是它的功能。  
4. 方法的调用：方法名(),调用才执行，不调用不执行  
5. JavaScript = ECMAScript（核心语法）+ DOM（操作网页内容）+ BOM（操作浏览器窗口）

* ECMAScript（核心语法）

a. 区分大小写

b. 字符串必须用单引号或双引号包裹

c. 每条语句结尾都建议有分号

* 注释(会占网页流量)

a. HTML注释：<!---->

b. CSS注释： /**/

c. js注释：//或/**/

* 字符串变量的内容一旦创建不可改变！若改变，只能创建新字符串，抛弃旧字符串。

var str = 'hh';

str = str + 'aa';

此过程一共创建了3个字符串


> 编程的最高境界：一次定义处处使用(对于重复编写的代码块都要封装为一个方法（执行一个专门功能的一组代码的序列）)，一次修改处处生效！
```js
function max(a,b,c) {

	var max = a;
	max = max > b ? max : b;
	max = max > c ? max : c;

	return max;
}
```
