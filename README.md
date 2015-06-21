# dot5.css
半像素边框

## 常规设置
---
> 上边框

```html
<div class="dot5-top">上边框</div>
```

> 右边框

```html
<div class="dot5-right">右边框</div>
```

> 下边框

```html
<div class="dot5-bottom">下边框</div>
```

> 左边框

```html
<div class="dot5-left">左边框</div>
```

> 上下边框

```html
<div class="dot5-top dot5-bottom">上下边框</div>
```

> 左右边框

```html
<div class="dot5-left dot-right">左右边框</div>
```

> 上下左右边框

**上下左右边框必须嵌套，上下与左右样式可互相被包含，内部div不能设置margin，外部div不能设置padding；**
```html
<div class="dot5-top dot5-bottom">
    <div class="dot5-left dot-right">上下左右边框</div>
</div>
```

## 自定义设置
---
> 修改线条颜色

```css
<style>
.dot5-left::before,.dot5-right::after,.dot5-top::before,.dot5-bottom::after{border-color:#c00;}
</style>
```

> 修改线条粗细

```css
<style>
.dot5-left::before,.dot5-right::after{-webkit-transform:scaleX(0.2);transform:scaleX(0.2)}
.dot5-top::before,.dot5-bottom::after{-webkit-transform:scaleY(0.2);transform:scaleY(0.2)}
</style>
```

> 修改线条类型

```css
<style>
.dot5-top::before{border-top-style:dashed}
.dot5-right::after{border-right-style:dotted}
.dot5-bottom::after{border-bottom-style:double}
.dot5-left::before{border-left-style:dashed}
</style>
```

## DEMO

[http://ttghost.com/html/test/dot5/dot5.html](http://ttghost.com/html/test/dot5/dot5.html)


