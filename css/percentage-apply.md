## CSS中百分比应用在哪些属性上

* `top`
  > 相对于最近的父元素`position`为非`static`的高度
  > 
  > 容器顶部位置相对于父元素顶部位置
  
* `right`
  > 相对于最近的父元素`position`为非`static`的宽度
  > 
  > 容器右侧位置相对于父元素右侧位置
  
* `bottom`
  > 相对于最近的父元素`position`为非`static`的高度
  > 
  > 容器底部位置相对于父元素底部位置
  
* `left`
  > 相对于最近的父元素`position`为非`static`的宽度
  > 
  > 容器左侧位置相对于父元素左侧位置
  
* `margin`
  > 四个方向均是相对于父元素的宽度
  
* `width`
  > 相对于父元素的宽度
  
* `height`
  > 相对于父元素的高度
  > 
  > 哪些情况下生效??
  
* `max-width`
  > 相对于父元素的宽度
  
* `max-height`
  > 相对于父元素的高度
  
* `min-width`
  > 相对于父元素的宽度
  
* `min-height` 
  > 相对于父元素的高度
  
* `padding`
  > 四个方向均是相对于父元素的宽度

* `border-radius`
  > * 写法 `border-radius: [top-left-x] [top-right-x] [bottom-right-x] [bottom-eft-x] / [top-left-y] [top-right-y] [bottom-right-y] [bottom-left-y]`;
  > 
  > x相对于父容器宽度(包含border-width)
  > 
  > y相对于父容器高度(包含border-width)
  
* `font-size`
  > 相对于继承的字体大小
  
* `line-height`
  > 相对于继承的字体大小
  
* `background-size`
  > background-size-width: 相对于容器的宽度
  > background-size-height: 相对于容器的高度
  
* `background-position`
  > 当background-image铺满整个容器的时候，background-position为百分比的时候失效
  > 
  > background-position-x: 为(容器宽度-背景图片background-size-x)的百分比
  > 
  > background-position-y: 为(容器高度-背景图片background-size-y)的百分比
  
* `background-image gradient`
  > 相对于background-size
  
* `translate`
* `vertical-align`
  > 相对于自身line-height 
  > 
  > 向上为正数
* `text-indent`
  > 只对第一行文本生效
  > 
  > 相对于父容器宽度
