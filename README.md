# dot5.css

半像素边框

## 常规设置

- 上边框

```html
<div class="dot5-top">上边框</div>
```

- 右边框

```html
<div class="dot5-right">右边框</div>
```

- 下边框

```html
<div class="dot5-bottom">下边框</div>
```

- 左边框

```html
<div class="dot5-left">左边框</div>
```

- 上下边框

```html
<div class="dot5-top dot5-bottom">上下边框</div>
```

- 左右边框

```html
<div class="dot5-left dot-right">左右边框</div>
```

- 上下左右边框

**上下左右边框必须嵌套，上下与左右样式可互相被包含，内部div不能设置margin，外部div不能设置padding；**

```html
<div class="dot5-top dot5-bottom">
    <div class="dot5-left dot-right">上下左右边框</div>
</div>
```

## 自定义设置

- 修改线条颜色

```css
.dot5-left::before,
.dot5-right::after,
.dot5-top::before,
.dot5-bottom::after{
  border-color:#c00;
}
```

- 修改线条粗细

```css
.dot5-left::before,
.dot5-right::after{
  -webkit-transform:scaleX(0.2);
  transform:scaleX(0.2)
}
.dot5-top::before,
.dot5-bottom::after{
  -webkit-transform:scaleY(0.2);
  transform:scaleY(0.2)
}
```

**注意:**

iphone4及4s在边框缩放小于0.5时，solid线条并不变细，而是颜色变浅，而dotted及dashed类型不显示。所以推荐缩放不小于0.5


- 修改线条类型

```css
.dot5-top::before{
  border-top-style:dashed
}
.dot5-right::after{
  border-right-style:dotted
}
.dot5-bottom::after{
  border-bottom-style:double
}
.dot5-left::before{
  border-left-style:dashed
}
```


## DEMO

[http://fe1024.com/demos/dot5](http://fe1024.com/demos/dot5)


