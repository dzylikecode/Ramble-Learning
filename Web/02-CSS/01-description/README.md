---
title: README
date: 2022-03-20 10:16
---
# 简介

>  CSS，指的是Cascading Style Sheet（层叠样式表），它是用来控制网页外观的一门技术。
> 
> HTML控制网页的结构，CSS控制网页的外观，JavaScript控制网页的行为。

## CSS引入方式

想要在一个页面引入CSS，共有以下三种方式。
-  外部样式表
-  内部样式表
-  行内样式表
### 外部样式表

所谓的外部样式表，指的是把CSS代码和HTML代码单独放在不同的文件中，然后在HTML文档中使用link标签来引用CSS样式表。

外部样式表在单独文件中定义，然后在HTML文件的<head></head>标签对中使用link标签来引用。

```html
<link rel="stylesheet" type="text/css" href="文件路径" />
```
>  rel即relative的缩写，它的取值是固定的，即stylesheet，表示引入的是一个样式表文件（即CSS文件）。
> 
> type属性取值也是固定的，即"text/css"，表示这是标准的CSS。
> 
> href是Hypertext Reference的缩写
> 
>  如果你使用外部样式表，必须使用link标签来引入，而link标签是放在head标签内的。

### 内部样式表

内部样式表，指的是把HTML代码和CSS代码放到同一个HTML文件中。其中，CSS代码放在style标签内，并且style标签是放在head标签内部的。

```html
<style type="text/css"> …… </style>
```

> 如果使用内部样式表，CSS样式必须在style标签内定义，而style标签是放在head标签内的。

### 行内样式表

内部样式表的CSS是在“style标签”内定义的，而行内样式表的CSS是在“标签的style属性”中定义的。

```html
<!-- example -->
<div style="color:red;">绿叶，给你初恋般的感觉。</div>
```





