---
title: README
date: 2022-03-30 17:40
---
# 背景样式

## 属性

![](./_image/2022-03-30/8a5428d417d37f9f093a3712b26e4428.jpg)

## 背景颜色

```CSS
background-color:颜色值;

<style type="text/css">         p         {             color:white;             background-color: hotpink;​​        }     </style>
```

![](./_image/2022-03-30/c923d529478d98905e1748cca4090ea6.jpg)

>  color属性用于定义“文本颜色”，而background-color属性用于定义“背景颜色”

## 背景图片样式

```CSS
background-image:url(图片路径);

<style type="text/css">         div{background-image: url(img/haizei.png);}​​    </style>
```

> 没有给div元素定义width和height，此时div元素的宽度和高度都为0，那背景图片肯定不会显示啊

## 背景图片重复

```CSS
background-repeat:取值;
```

![](./_image/2022-03-30/d37bbaa85117d3a7c7a1322c2378f2df.jpg)

```CSS
<!DOCTYPE html> <html> <head>     <meta charset="utf-8" />     <title></title>     <style type="text/css">         div         {             width:200px;             height:100px;             border: 1px solid silver;             background-image: url(img/fl ower.png);         }         #div2{background-repeat: repeat-x}​​        #div3{background-repeat: repeat-y}​​        #div4{background-repeat: no-repeat}​​    </style> </head> <body>     <div id="div1"></div>     <div id="div2"></div>     <div id="div3"></div>     <div id="div4"></div> </body> </html>
```

![](./_image/2022-03-30/c615de07c50ed28f5003873bf0bac1b6.jpg)

> 在这个例子中，第一个div元素由于没有定义background-repeat属性值，因此会采用默认值repeat。
> 
> 此外还需要注意一点，元素的宽度和高度必须大于背景图片的宽度和高度，才会有重复效果。

## 背景图片位置

```CSS
background-position:像素值/关键字;

background-position:水平距离 垂直距离;
background-position:水平距离 垂直距离;


```
- 像素
> 例如“background-position:12px 24px;”表示背景图片与该元素左上角的水平方向距离为12px，垂直方向距离为24px。
- 关键字
![](./_image/2022-03-30/7d9ce6450b97308aaee592d3b32ac7b2.jpg)

## 背景图片固定

```CSS
background-attachment:取值;
```


![](./_image/2022-03-30/b7cdf1c1517afc3c3bae3757da64c0af.jpg)


