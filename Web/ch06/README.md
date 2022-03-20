---
title: README
date: 2022-03-19 23:25
---
# 表格

## 基本结构

在HTML中，一个表格一般会由以下三个部分组成。
-  表格：table标签
-  行：tr标签
-  单元格：td标签
```html
<table>     <caption>表格标题</caption>     <tr>         <th>表头单元格 1</th>         <th>表头单元格 2</th>     </tr>     <tr>         <td>表行单元格 1</td>         <## td>表行单元格 2</td>     </tr>     <tr>         <td>表行单元格 3</td>         <td>表行单元格 4</td>     </tr> </table>
```

> tr，指的是table row（表格行）。td，指的是table data cell（表格单元格）。
> 表头单元格，使用th标签；表行单元格，使用td标签。
> th，指的是table header cell（表头单元格）。
-  显示上：浏览器会以“粗体”和“居中”来显示th标签中的内容，但是td标签不会。
-  语义上：th标签用于表头，而td标签用于表行。

## 语义化

thead、tbody和tfoot把表格划分为三部分：表头、表身、表脚。有了这三个标签，表格语义更加良好，结构更清晰，也更具有可读性和可维护性。

```html
<table>     <caption>表格标题</caption>     <!--表头--><thead>         <tr>             <th>表头单元格 1</th>             <th>表头单元格 2</th>         </tr>     </thead>     <!--表身--><tbody>         <tr>             <td>表行单元格 1</td>             <td>表行单元格 2</td>         </tr>         <tr>             <td>表行单元格 3</td>             <td>表行单元格 4</td>         </tr>     </tbody>     <!--表脚--><tfoot>         <tr>             <td>标准单元格 5</td>             <td>标准单元格 6</td>         </tr>     </tfoot> </table>
```

### 合并
- 行
```html
<td rowspan = "跨越的行数"></td>
<!-- example -->
     <table>         <tr>             <td>姓名:</td>             <td>小明</td>         </tr>         <tr>             <td rowspan="2">喜欢水果:</td>             <td>苹果</td>         </tr>         <tr>             <td>香蕉</td>         </tr>     </table>
```

![](./_image/2022-03-19/55cbe1e262ec117e6e576e01074948c0.jpg?c=1)

- 列
```html
<td colspan = "跨越的列数"></td>
```

