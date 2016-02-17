#### 水平居中的方法

1. 单行/多行文字水平居中：
```css
text-align: center;
```
2. 一个div嵌套另一个div时，里面的div水平居中

```html
<div class="outer">
		<div class="inner">我是内层</div>
	</div>
```
```css
.inner {
  width: 100px;
  margin: 0 auto;
}
```

或者

```css
.outer {
  text-align: center;
}
.inner {
  display: inline-block;
}
```

或者

```css
.outer {
  position: relative;
}
.inner {
  position: absolute;
  left: 50%;
  width: 100px;
  margin-left: -50px;
}

```
