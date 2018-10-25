---
title: 外边距合并
date: 2018-10-25 15:08:03
tags: [CSS]
editor: 天亮了
---
## 外边距合并的场景
1. 相邻元素合并  
2. 父子合并  
3. 自己合并  

### 相邻元素合并
当一个元素出现在另一个元素上面时，第一个元素的下外边距（margin-bottom）与第二个元素的上外边距（margin-top)会发生合并，如下图所示：
![1.gif](https://upload-images.jianshu.io/upload_images/14142208-58e006a7a86b0d41.gif?imageMogr2/auto-orient/strip)
测试代码如下：
```
<div style="margin-bottom: 20px;width: 100px;height: 100px;background-color: yellow">
</div>
<div style="margin-top: 10px;width:100px;height: 100px;background-color: gray">
</div>
```
### 父子合并
当一个元素包含在另一个元素中时（假设没有内边距或边框把外边距分隔开），它们的上和/或下外边距也会发生合并，如下图所示：
![2.gif](https://upload-images.jianshu.io/upload_images/14142208-caf43ec476a4c90e.gif?imageMogr2/auto-orient/strip)
测试代码如下：
```
<div style="margin-top: 20px;width:300px;height:300px;background-color: gray">
	<div style="margin-top: 10px;width: 200px;height: 200px;background-color: yellow">
	</div>
</div>
```
## 自己合并
一个空元素，它有外边距，但是没有边框或填充。在这种情况下，上外边距与下外边距就碰到了一起，它们会发生合并：
![3.gif](https://upload-images.jianshu.io/upload_images/14142208-2f33e67c9ec4017b.gif?imageMogr2/auto-orient/strip)
测试代码如下：
```
<div style="margin-top: 20px;margin-bottom: 20px;">
</div>
<div style="height:100px;width:100px;background-color: gray">
```
如果这个空元素遇到另外一个元素的外边距，它还会发生合并：
![4.gif](https://upload-images.jianshu.io/upload_images/14142208-27f1aff322f60e10.gif?imageMogr2/auto-orient/strip)
测试代码如下：
```
<div style="margin-top: 20px;margin-bottom: 20px;">
</div>
<div style="margin-top: 20px;height:100px;width:100px;background-color: gray">
```