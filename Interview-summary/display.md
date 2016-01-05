1. 行内级元素 和 块级元素的区别?  
1.1. 行内级元素不会换新行,但是可以设置宽高、margin和padding  
1.2. 块级元素独占一行  
1.3. 行内元素  
设置宽高无效(高度可以通过line-height来设置)  
设置margin只有左右margin有效，上下无效。  
设置padding只有左右padding有效，上下则无效。

#### display: inline

* a
* span
**img**(虽然img是行内元素，但是可以设置其宽高。因为它是替换元素)
在文档类型定义（DTD）中对不同的元素规定了不同的类型
从元素本身的特点来讲，可以分为替换和不可替换元素。

> 替换元素  

就是浏览器根据元素的标签和属性，来决定元素的具体显示内容。浏览器会根据img标签的src属性的值来读取图片信息并显示出来，而如果查看(X)HTML代码，则看不到图片的实际内容；又例如根据input标签的type属性来决定是显示输入框，还是单选按钮等。

**替换元素**一般有内在尺寸，所以具有width和height，可以设定。例如你不指定img的width和height时，就按其内在尺寸显示，也就是图片被保存的时候的宽度和高度。

> 不可替换元素

(X)HTML的大多数元素是不可替换元素，即其内容直接表现给用户端（例如浏览器）。段落p是一个不可替换元素，文字“段落的内容”全被显示。
对于表单元素，浏览器也有默认的样式，包括宽度和高度。
* em
* br
* label
* strong
* sub - 下标 
* sup - 上标 

#### display: inline-block

* input
* select
* textarea

#### display: block


* div - 常用块级容易，也是css layout的主要标签 
* table - 表格 
* p - 段落
* ol - 排序表单 
* ul - 非排序列表
* dl - 定义列表 
* form - 交互表单 （只能用来容纳其它块元素） 
* h1 - 大标题 
* h2 - 副标题 
* h3 - 3级标题 
* h4 - 4级标题 
* h5 - 5级标题 
* h6 - 6级标题 
* hr - 水平分隔线 
* fieldset - form控制组 
* isindex - input prompt 
* menu - 菜单列表  
* pre - 格式化文本 
* address - 地址   

#### display: table  
#### display: list-item
#### display: flex
#### display: grid
#### display: none
#### display: table-cell
