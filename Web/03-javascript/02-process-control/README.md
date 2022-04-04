---
title: README
date: 2022-03-31 15:28
---
# 流程控制

## 选择结构

```Javascript
if(条件 1) {     if(条件 2)     {         当"条件 1"和"条件 2"都为true时执行的代码     }     else     {         当"条件 1"为true、"条件 2"为false时执行的代码     } } else {     if(条件 2)     {         当"条件 1"为false、"条件 2"为true时执行的代码     }     else     {         当"条件 1"和"条件 2"都为false时执行的代码     } }

switch(判断值) {     case 取值 1:         语块 1;break;     case 取值 2:         语块 3;break;     ……     case 取值n:         语块n;break;     default:         语句块n+1; }
```

## 循环结构

```Javascript
while(条件) {     //当条件为true时，循环执行 }

do {     …… }while(条件);

for(初始化表达式;条件表达式;循环后操作) {     …… }
```

```html
<!DOCTYPE html> <html> <head>     <meta charset="utf-8" />     <title></title>     <script>         for (var i = 2; i < 5; i++)         {             var str = "<p style='font-size:" + i * 5 + "px'>高筑墙，广积粮，缓称王。</p>";             document.write(str);         }     </script> </head> <body> </body> </html>
```







