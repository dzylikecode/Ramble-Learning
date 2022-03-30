---
title: README
date: 2022-03-30 21:18
---

# 盒子模型

在 CSS 盒子模型理论中，页面中的所有元素都可以看成一个盒子，并且占据着一定的页面空间。

![](./_image/2022-03-30/c3ac8a22e986d2621aed083e075ecdad.jpg)

一个页面由很多这样的盒子组成，这些盒子之间会互相影响，因此掌握盒子模型需要从两个方面来理解：一是理解单独一个盒子的内部结构（往往是 padding），二是理解多个盒子之间的相互关系（往往是 margin）。

每个元素都看成一个盒子，盒子模型是由 content（内容）、padding（内边距）、margin（外边距）和 border（边框）这四个属性组成的。此外，在盒子模型中，还有宽度 width 和高度 height 两大辅助性属性。**记住，所有的元素都可以视为一个盒子**。

![](./_image/2022-03-30/8a35c8b7f8a90dd20037e689e2e07e4d.jpg)

## 内容区

内容区有三个属性：width、height 和 overflow。

当内容过多超出 width 和 height 时，可以使用 overflow 属性来指定溢出处理方法。

## 内边距

内边距，指的是内容区和边框之间的空间，可以看成是内容区的背景区域。

关于内边距的属性有五种，即 padding-top、padding-bottom、padding-left、padding-right 以及综合了以上四个方向的简写内边距属性 padding。

## 外边距

外边距，指的是两个盒子之间的距离，它可能是子元素与父元素之间的距离，也可能是兄弟元素之间的距离。外边距使得元素之间不必紧凑地连接在一起，是 CSS 布局的一个重要手段。

外边距的属性也有五种，即 margin-top、margin-bottom、margin-left、margin-right 以及综合了以上四个方向的简写外边距属性 margin。

CSS 允许给外边距属性指定负数值，当外边距为负值时，整个盒子将向指定负值的相反方向移动，以此可以产生盒子的重叠效果，这就是传说中的“负 margin 技术”。

## 边框

边框属性有 border-width、border-style、border-color 以及综合了三类属性的简写边框属性 border。

border-width:1px;border-style:solid;border-color:gray;等价于 border:1px solid gray;。

## example

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title></title>
    <style type="text/css">
      div {
        display: inline-block; /*将块元素转换为inline-block元素*/

        padding: 20px;
        margin: 40px;
        border: 2px solid red;
        background-color: #ffdead;
      }
    </style>
  </head>
  <body>
    <div>绿叶学习网</div>
  </body>
</html>
```

![](./_image/2022-03-30/621d9ff42b0f3d7e63a0bb4edcd95902.jpg)

- padding 是在元素内部，而 margin 是在元素外部。
- margin 看起来不属于 div 元素的一部分，实际上 div 元素的盒子模型是包含 margin 的。

> display:inline-block;表示将元素转换为行内块元素（即 inline-block），其中 inline-block 元素的宽度是由内容区撑起来的。我们之所以在这个例子中将元素转换为 inline-block 元素，也是为了让元素的宽度由内容区撑起来，以便更好地观察。

## 宽和高

> 元素的宽度（width）和高度（height）是针对内容区而言的。
>
> 只有块元素才可以设置 width 和 height，行内元素是无法设置 width 和 height 的（我们这里不考虑 inline-block 元素）。
>
> div 是块元素，因此可以设置 width 和 height。span 是行内元素，因此不可以设置 width 和 height。
>
> 要是没有给块元素设置 width，那么块元素就会延伸到整行
>
> 行内元素设置的 width 和 height 无法生效，它的宽度和高度只能由内容区撑起来。
> 如果我们想要为行内元素（如 span 等）设置宽度和高度，那该怎么办呢？
>
> 在 CSS 中，我们可以使用 display 属性来将行内元素转换为块元素，也可以将块元素转换为行内元素。

### padding 局部样式

```html
padding-top:像素值;padding-right:像素值;padding-bottom:像素值;padding-left:像素值;

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title></title>
    <style type="text/css">
      div {
        display: inline-block; /*将块元素转换为inline-block元素*/
        padding-top: 20px;
        padding-right: 40px;
        padding-bottom: 60px;
        padding-left: 80px;
        border: 2px solid red;
        background-color: #ffdead;
      }
    </style>
  </head>
  <body>
    <div>绿叶学习网</div>
  </body>
</html>
```

![](./_image/2022-03-30/f65abca0e6c7412f528b1fdb678e6fb7.jpg)

padding:20px;表示四个方向的内边距都是 20px。

padding:20px 40px;表示 padding-top 和 padding-bottom 为 20px，padding-right 和 padding-left 为 40px。

padding:20px 40px 60px 80px;表示 padding-top 为 20px，padding-right 为 40px，padding-bottom 为 60px，padding-left 为 80px。大家按照顺时针方向记忆就可以了。

![](./_image/2022-03-30/35d776d5cda0420000a51356ce714154.jpg)

### 外边距

```html
margin-top:像素值;margin-right:像素值;margin-bottom:像素值;margin-left:像素值;
```

### 外边距

```html
margin-top:像素值;margin-right:像素值;margin-bottom:像素值;margin-left:像素值;
```

- 只有父元素，没有兄弟元素时

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title></title>
    <style type="text/css">
      #father {
        display: inline-block; /*将块元素转换为inline-block元素*/
        border: 1px solid blue;
      }
      #son {
        display: inline-block; /*将块元素转换为inline-block元素*/

        padding: 20px;
        margin-top: 20px;

        margin-right: 40px;
        margin-bottom: 60px;
        margin-left: 80px;
        border: 1px solid red;
        background-color: #ffdead;
      }
    </style>
  </head>
  <body>
    <div id="father"><div id="son">绿叶学习网</div></div>
  </body>
</html>
```

![](./_image/2022-03-30/a0de732fcde4250d6a198c3265c4fd87.jpg)

- 有兄弟元素时

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title></title>
    <style type="text/css">
      #father {
        display: inline-block; /*将块元素转换为inline-block元素*/
        border: 1px solid blue;
      }
      #son {
        display: inline-block; /*将块元素转换为inline-block元素*/

        padding: 20px;
        margin-top: 20px;

        margin-right: 40px;
        margin-bottom: 60px;
        margin-left: 80px;
        border: 1px solid red;
        background-color: #ffdead;
      }
      .brother {
        height: 50px;
        background-color: lightskyblue;
      }
    </style>
  </head>
  <body>
    <div id="father">
      <div class="brother"></div>
      <div id="son">绿叶学习网</div>
      <div class="brother"></div>
    </div>
  </body>
</html>
```

![](./_image/2022-03-30/85466d0f231647c0e49c492d6d5d29f0.jpg)

> 当既有父元素，也有兄弟元素时，该元素会先看看四个方向有没有兄弟元素存在。如果该方向有兄弟元素，则这个方向的 margin 就是相对于兄弟元素而言。如果该方向没有兄弟元素，则这个方向的 margin 就是相对于父元素而言。
>
> padding 和 margin 的区别在于：padding 体现的是元素的“内部结构”，而 margin 体现的是元素之间的相互关系。

margin:20px;表示四个方向的外边距都是 20px。

margin:20px 40px;表示 margin-top 和 margin-bottom 为 20px，margin-right 和 margin-left 为 40px。

margin:20px 40px 60px 80px;表示 margin-top 为 20px，margin-right 为 40px，margin bottom 为 60px，margin-left 为 80px。大家按照顺时针方向记忆就可以了。

![](./_image/2022-03-30/1858e5dcd22b478233a7eb61585c1306.jpg)
