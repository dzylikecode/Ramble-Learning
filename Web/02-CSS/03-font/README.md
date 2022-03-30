---
title: README
date: 2022-03-20 22:57
---
# 字体样式
- word中的字体样式

![](./_image/2022-03-20/7b7931a3007d67c6e8a844b5feb559c5.jpg)

- 字体样式属性

![](./_image/2022-03-20/10a0b894ff5d5fa5347b3f3e43301a67.jpg)


## 字体类型

```CSS
font-family: 字体 1, 字体 2, ..., 字体N;
<style type="text/css">         #div1 {font-family:Arial;}         #div2 {font-family: "Times New Roman";}         #div3 {font-family: "微软雅黑";}     </style>

<style type="text/css">         p{font-family:Arial,Verdana,Georgia;}     </style>
```

>  对于font-family属性，如果字体类型只有一个英文单词，则不需要加上双引号；如果字体类型是多个英文单词或者是中文，则需要加上双引号
> 
> p{font-family:Arial,Verdana,Georgia;}这一句的意思是：p元素优先使用Aria字体来显示，如果你的电脑没有装Arial字体，那就接着考虑Verdana字体。如果你的电脑还是没有装Verdana字体，那就接着考虑Georgia字体……

## 字体大小

```CSS
font-size:像素值;
```

>  font-size属性取值有两种，一种是“关键字”，如small、medium、large等。另外一种是“像素值”，如 10px、16px、21px等。
> px，全称pixel（像素）

## 字体粗细

```CSS
font-weight:取值;
```

> font-weight属性取值有两种：一种是100～900的“数值”；另外一种是“关键字”。
> 
> ![](./_image/2022-03-22/162cfbf7f3d1ea9ed77ff026d77b9cad.jpg)

## 字体风格

```CSS
font-style:取值;
```

> ![](./_image/2022-03-22/0ae202360b770a545ab8dc38ab951fc4.jpg)
> 
> 有些字体有斜体italic属性，但有些字体却没有italic属性。oblique是让没有italic属性的字体也能够有斜体效果。

## 字体颜色

```CSS
color:颜色值;

<style type="text/css">         #p1{color:gray;}         #p2{color:orange;}         #p3{color:red;}     </style>
<style type="text/css">         #p1{color: #03FCA1;}         #p2{color: #048C02;}         #p3{color: #CE0592;}     </style>
```

> color属性取值有两种：一种是“关键字”，另外一种是“16 进制RGB值”。除了这两种，其实还有RGBA、HSL等
> 
> 浏览器解析CSS是有一定顺序的，在这个例子中，第二个p元素一开始就使用元素选择器定义了一次color:red;，然后用id选择器定义了一次color:blue;。因此后面的会覆盖前面的，最终显示为蓝色。

