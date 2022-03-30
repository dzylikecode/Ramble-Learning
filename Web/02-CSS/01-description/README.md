---
title: README
date: 2022-03-20 10:16
---

# 简介

> CSS，指的是 Cascading Style Sheet（层叠样式表），它是用来控制网页外观的一门技术。
>
> HTML 控制网页的结构，CSS 控制网页的外观，JavaScript 控制网页的行为。

## CSS 引入方式

想要在一个页面引入 CSS，共有以下三种方式。

- 外部样式表
- 内部样式表
- 行内样式表

### 外部样式表

所谓的外部样式表，指的是把 CSS 代码和 HTML 代码单独放在不同的文件中，然后在 HTML 文档中使用 link 标签来引用 CSS 样式表。

外部样式表在单独文件中定义，然后在 HTML 文件的<head></head>标签对中使用 link 标签来引用。

```html
<link rel="stylesheet" type="text/css" href="文件路径" />
```

> rel 即 relative 的缩写，它的取值是固定的，即 stylesheet，表示引入的是一个样式表文件（即 CSS 文件）。
>
> type 属性取值也是固定的，即"text/css"，表示这是标准的 CSS。
>
> href 是 Hypertext Reference 的缩写
>
> 如果你使用外部样式表，必须使用 link 标签来引入，而 link 标签是放在 head 标签内的。

### 内部样式表

内部样式表，指的是把 HTML 代码和 CSS 代码放到同一个 HTML 文件中。其中，CSS 代码放在 style 标签内，并且 style 标签是放在 head 标签内部的。

```html
<style type="text/css">
  ……
</style>
```

> 如果使用内部样式表，CSS 样式必须在 style 标签内定义，而 style 标签是放在 head 标签内的。

### 行内样式表

内部样式表的 CSS 是在“style 标签”内定义的，而行内样式表的 CSS 是在“标签的 style 属性”中定义的。

```html
<!-- example -->
<div style="color:red;">绿叶，给你初恋般的感觉。</div>
```
