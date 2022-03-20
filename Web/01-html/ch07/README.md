---
title: README
date: 2022-03-19 23:41
---
# 图片与链接

## src属性

```html
<img src="图片路径" />
```

## alt属性和title属性

-  alt属性用于描述图片，这个描述文字是给搜索引擎看的，并且当图片无法显示时，页面会显示alt中的文字。
![](./_image/2022-03-19/312a4f3a78febaec9f03b61df2fa0e63.jpg?c=1)
-  title属性也用于描述图片，不过这个描述文字是给用户看的，并且当鼠标指针移到图片上时，会显示title中的文字。
![](./_image/2022-03-19/443c91d46d2f0c1f4d474175ad713141.jpg?c=1)

## 图片格式

.jpg格式可以很好地处理大面积色调的图片，适合存储颜色丰富的复杂图片，如照片、高清图片等。此外，.jpg体积较大，并且不支持透明。
.png是一种无损格式，可以无损压缩以保证页面打开速度。此外，.png体积较小，并且支持透明，不过不适合存储颜色丰富的图片。
.gif图片效果最差，不过它适合制作动画。实际上，小伙伴们经常在QQ发的动图都是.gif格式的。

如果想要展示色彩丰富而高品质图片，可以使用.jpg格式；如果是一般图片，为了减少体积或者想要透明效果，可以使用.png格式；如果是动画图片，可以使用.gif格式。

### 超链接

超链接，英文名是hyperlink

```html
<a href="链接地址">文本或图片</a>
<!-- example -->
<a href="http://www.lvyestudy.com"><img src="img/lvye.png" alt="绿叶学习网"/></a>
<!-- open s tyle -->
<a href="链接地址" target="打开方式"></a>
```

![](./_image/2022-03-20/7930b4d5a7ab120dcceed30f1ad305d7.jpg?c=1)

>  超链接有两种，一种是“外部链接”，另外一种是“内部链接”。外部链接指向的是“外部网站的页面”，而内部链接指向的是“自身网站的页面”。
> 
> 类似相对路径

- 锚点链接
```html
<!DOCTYPE html> <html> <head>     <meta charset="utf-8" />     <title></title> </head> <body>     <div>         <a href="#article">推荐文章</a><br />         <a href="#music">推荐音乐</a><br />         <a href="#movie">推荐电影</a><br />     </div>     ……<br />     ……<br />     ……<br />     ……<br />     ……<br />     ……<br />     ……<br />     ……<br />     <div id="article">         <h3>推荐文章</h3>         <ul>             <li>朱自清-荷塘月色</li>             <li>余光中-乡愁</li>             <li>鲁迅-阿Q正传</li>         </ul>     </div>     ……<br />     ……<br />     ……<br />     ……<br />     ……<br />     ……<br />     ……<br />     ……<br />     <div id="music">         <h3>推荐音乐</h3>         <ul>             <li>林俊杰-被风吹过的夏天</li>             <li>曲婉婷-在我的歌声里</li>             <li>许嵩-灰色头像</li>         </ul>     </div>     ……<br />     ……<br />     ……<br />     ……<br />     ……<br />     ……<br />     ……<br />     ……<br />     <div id="movie">         <h3>推荐电影</h3>         <ul>             <li>蜘蛛侠系列</li>             <li>钢铁侠系统</li>             <li>复仇者联盟</li>         </ul>     </div> </body> </html>
```

想要实现锚点链接，需要定义两个。
-  目标元素的id。
-  a标签的href属性指向该id。



