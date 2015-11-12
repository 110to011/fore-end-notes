# 快速绘制三角形的方法

> 如何用border属性快速绘制一个三角形

```html
<div class="caret"></div>
```

```css
.caret {
  width: 0;
  height: 0;
  line-height: 0;
  border: 10px solid transparent;
  border-top-width: 0;
  border-bottom-color: #f90;
}
```
