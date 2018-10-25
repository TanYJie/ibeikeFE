---
title: 垂直居中
date: 2018-10-25 15:06:46
tags: [HTML,CSS]
editor: 小黄冲鸭
---
## 单行文本  
设置父元素的height和line-height高度一致  
```
<p style="height: 50px;border: 2px solid cadetblue;">这是一个单行文本</p>  
<p style="height: 50px;border: 2px solid cadetblue;line-height: 50px">这是一个垂直居中的单行文本</p>  
```

## 多行文本  
1. 使用插入table(包括tbody、tr、td)标签，同时设置竖直居中的属性vertical-align:middle，在父元素设置此样式时，会对inline-block类型的子元素都有用  

```
<table>
    <tr>       
        <td style="height: 500px;background-color: #a73cff;">  
        <!--td默认vertical-align:middle-->
           <div>
                多行<br>文本<br>               
                <p>垂直</p>
                <p>居中</p>
            </div>
        </td>
    </tr>
</table>
```

2. 在chrom、firefox、IE8以上的浏览器可以设置块级元素的`display:table-tell`（设置为表格单元），激活vertical-align属性，本方法兼容性较差  

元素属于inline或是inline-block（table-cell也可以理解为inline-block水平）水平，其身上的vertical-align属性才会起作用  
```
<div style="margin:10px;height: 300px;width:100px;vertical-align: middle;display: table-cell;background-color: orange;color:green;">
    垂直<br>
    居中<br>
    方法
    <p>之二</p>
</div>
```

3. 使用flex布局`display:flex;align-items:center;`

```
<div style="display:flex;align-items:center; height:200px;background-color: purple;color:yellow;">
    垂直居中<br>
    方法三
</div> 
```