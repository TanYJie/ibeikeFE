---
title: 水平居中
date: 2018-10-25 15:01:48
categories: CSS
tags: [HTML,CSS]
editor: quierunt
---
在网页设计时常常需要将页面的元素居中放置，不同的元素有不同的方法，这里列举出了元素水平居中的一些常用方法：

> * 行内元素的水平居中
> * 块级元素的水平居中

## 行内元素的水平居中

当元素为文本或图片等行内元素时，可以通过`text-align: center;`来实现。如：

```
<p class="text1" style="border: 3px solid #FFB2A1;">这是一个段落</p>
<p class="text2" style="border: 3px solid #FFB2A1; text-align: center;">居中后的段落</p>
```

## 块级元素的水平居中

当元素为块级元素时，`text-align: center;`就不起作用了，这时分两种情况。

### 定宽块级元素
通过左右`margin`为`auto`来实现。如:

```
<div class="item1" style="width: 200px; height: 50px; border: 3px solid #A1C7FF;">宽度固定为200px的div</div>
<div class="item2" style="width: 200px; height: 50px; border: 3px solid #A1C7FF; margin: 0 auto;">居中后的div</div>
```

### 不定宽块级元素
可以通过以下方法来实现居中:

```
<div class="item3" style="border: 3px solid #FFEDA1;">这是一个不定宽的div</div>
<br/>
```

**方法一**：使用`table`标签和设置左右`margin`为`auto`来实现水平居中：

```
<table style="margin: 0 auto;"><tbody><tr><td>
<div class="item3" style="border: 3px solid #FFEDA1;">使用table标签居中不定宽div</div>
</td></tr></tbody></table>
<br/>
```

**方法二**：通过`display: inline;`将块级元素变成行内元素，然后通过`text-align: center;`实现水平居中：

```
<div class="container1" style="border: 3px solid #FFB2A1; text-align: center;">
<div class="item4" style="border: 3px solid #FFEDA1; display: inline;">使用display: inline; 变成行内元素来居中不定宽div</div></div>
<br/>
```

**方法三**：通过给父元素设置`float`，然后给父元素设置`position: relative;`和`left: 50%;`，子元素设置`position: relative;`和`left: -50%;`来实现水平居中：

```
<div class="container2" style="float: left; position: relative; left: 50%;">
<div class="item5" style="border: 3px solid #FFEDA1; position: relative; left: -50%;">使用float、position来居中不定宽div</div></div>
<br/>
```

以上就是不同元素常用的水平居中方法啦。