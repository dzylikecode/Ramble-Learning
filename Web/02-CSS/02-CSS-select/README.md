---
title: README
date: 2022-03-20 18:04
---

# CSS 选择器

## id

id 属性具有唯一性，也就是说在一个页面中相同的 id 只能出现一次。

## class

我们可以为同一个页面的相同元素或者不同元素设置相同的 class，然后使得具有相同 class 的元素具有相同的 CSS 样式。

> 因为在同一个页面中，允许出现两个相同 class 的元素。这样可以使得我们对具有相同 class 的多个元素定义相同的 CSS 样式。

## concept

选择器的不同，在于选择方式不同，但是它们的最终目的是相同的，那就是把你想要的元素选中，然后才可以定义该元素 CSS 样式。

### 格式

```CSS
选择器{    属性 1 : 取值 1;    ……    属性n : 取值n;}
```

#### 元素选择器

元素选择器，就是“选中”相同的元素，然后给相同的元素定义同一个 CSS 样式。

![](./_image/2022-03-20/1889a7cd744dbce14aa22fc243e54213.jpg)

```html
<head>
  <meta charset="utf-8" />
  <title></title>
  <style>
    div{color:red;}​​
  </style>
</head>
```

> div{color:red;}表示把页面中所有的 div 元素选中，然后定义它们的文本颜色为红色。
>
> p 元素和 span 元素就没有被选中，因此这两个元素文本颜色就没有变红

#### id 选择器

为元素设置一个 id 属性，然后针对设置了这个 id 的元素定义 CSS 样式，

![](./_image/2022-03-20/fdfac1cbb5d230efdc2b88e6c11a3a9c.jpg)

> 对于 id 选择器，id 名前面必须要加上前缀#，否则该选择器无法生效。在 id 名前面加上#，表示这是一个 id 选择器。对于 id 选择器，id 名前面必须要加上前缀#，否则该选择器无法生效。在 id 名前面加上#，表示这是一个 id 选择器。

#### class 选择器

相同的元素”或者“不同的元素”定义相同的 class 属性，然后针对拥有同一个 class 的元素进行 CSS 样式操作。

![](./_image/2022-03-20/838da8c927affc0167db0ae72dd55021.jpg)

#### 后代选择器

就是选择元素内部中所有的某一种元素，包括子元素和其他后代元素（如孙元素）

![](./_image/2022-03-20/85bca75c616f407d9e05ba382c848016.jpg)

```html
<style type="text/css">
  #father1 div {color:red;}​​        #father2 span{color:blue;}​​
</style>

<div id="father1">
  <div>绿叶学习网</div>
  <div>绿叶学习网</div>
</div>
```

> #father1 div {color:red;}表示选中 id 为 father1 的元素下的所有 div 元素，然后定义它们的文本颜色为红色

#### 群组选择器

![](./_image/2022-03-20/56fcea6aecb982d99b0ab1a8475ef130.jpg)

```html
<style type="text/css">
  h3,
  div,
  p,
  span {
    color: red;
  }
</style>
<!-- equals below -->
<style type="text/css">
  h3 {
    color: red;
  }
  div {
    color: red;
  }
  p {
    color: red;
  }
  span {
    color: red;
  }
</style>
```
