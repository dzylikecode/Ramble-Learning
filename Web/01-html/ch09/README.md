---
title: README
date: 2022-03-20 00:18
---

# 表单

在 HTML 中，表单标签有五种：form、input、textarea、select 和 option。

![](./_image/2022-03-20/0f86bce03fe8e19f7d83a1d6eab93713.jpg?c=1)

从外观上来划分，表单可以分为以下八种。

- 单行文本框
- 密码文本框
- 单选框
- 复选框
- 按钮
- 文件上传
- 多行文本框
- 下拉列表

## form

```html
<form>
  <input type="text" value="这是一个单行文本框" /><br />
  <textarea>这是一个多行文本框</textarea><br />
  <select>
    <option>HTML</option>
    <option>CSS</option>
    <option>JavaScript</option>
  </select>
</form>
```

![](./_image/2022-03-20/c46ef89712ea21893fd5c09e183478d4.jpg?c=1)

### 属性

![](./_image/2022-03-20/3bcb952dd5554f97fc885f316a350734.jpg?c=1)

#### name 属性

```html
<form name="myForm"></form>
```

#### method 属性

method 属性用于指定表单数据使用哪一种 http 提交方法。method 属性取值有两个，一个是 get，另外一个是 post。

```html
<form method="post"></form>
```

#### action 属性

action 属性用于指定表单数据提交到哪一个地址进行处理。

```html
form action="index.php"></form>
```

#### target 属性

用来指定窗口的打开方式

```html
<form target="_blank"></form>
```

#### enctype 属性

enctype 属性用于指定表单数据提交的编码方式。

## input

```html
<input type="表单类型" />
```

![](./_image/2022-03-20/d04f3cc14bf49b46a085ee63d682aaf4.jpg?c=1)

### 单行文本框属性

![](./_image/2022-03-20/dcf29c7395d12f60ce2f4b41208590a6.jpg?c=1)

```html
<form method="post">
  姓名：<input type="text" /><br />
  姓名：<input type="text" value="helicopter" />
</form>
```

![](./_image/2022-03-20/48fc6d27c5d5c553778cd87afbb7c8a6.jpg?c=1)

> 1.  value 属性用于设置单行文本框中默认的文本，如果没有设置，就是空白
> 2.  size 属性可以用来设置单行文本框的长度

### 密码文本框

在单行文本框中输入的字符可见，而在密码文本框中输入的字符不可见。

```html
<input type="password" />
```

### 单选框

```html
<input type="radio" name="组名" value="取值" />
```

name 属性表示单选按钮所在的组名，而 value 表示单选按钮的取值，这两个属性必须要设置。

```html
<form method="post">
  性别: <input type="radio" name="gender" value="男" />男
  <input type="radio" name="gender" value="女" />女
</form>
```

![](./_image/2022-03-20/19f249c19c1d657c479fcb2ef9788f09.jpg?c=1)

- add default option

```html
<input type="radio" name="gender" value="男" checked />男<input
  type="radio"
  name="gender"
  value="男"
  checked="checked"
/>男
```

**notice**:

- 没有加上 name 属性 => 可以同时选中两个选项
- name 取值不一样 => 两个选项还是可以被同时选取

> 为了得到更好的语义化，表单元素与后面的文本一般都需要借助 label 标签关联起来。

```html
<label><input type="radio" name="gender" value="男" />男</label
><label><input type="radio" name="gender" value="女" />女</label>
```

### 复选框

```html
<input type="checkbox" name="组名" value="取值" />
<!-- example -->
<form method="post">
  你喜欢的水果：<br />
  <input type="checkbox" name="fruit" value="苹果" />苹果
  <input type="checkbox" name="fruit" value="香蕉" />香蕉
  <input type="checkbox" name="fruit" value="西瓜" />西瓜
  <input type="checkbox" name="fruit" value="李子" />李子
</form>
```

一样可以添加 checked

### 按钮

#### 普通按钮

```html
<input type="button" value="取值" />
<!-- example -->
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title></title>
    <script>
      window.onload = function () {
        var oBtn = document.getElementsByTagName("input");
        oBtn[0].onclick = function () {
          alert("I ❤ HTML ！");
        };
      };
    </script>
  </head>
  <body>
    <form method="post"><input type="button" value="表白" /></form>
  </body>
</html>
```

#### 提交按钮 submit

```html
<input type="submit" value="取值" />

<!-- example -->

<form method="post">
  <input type="button" value="普通按钮" />
  <input type="submit" value="提交按钮" />
</form>
```

#### 重置按钮 reset

```html
<input type="reset" value="取值" />

<!-- example -->

<form method="post">
  账号：<input type="text" /><br />
  密码：<input type="password" /><br />
  <input type="reset" value="重置" />
</form>
```

> 重置按钮只能清空它所在 form 标签内表单中的内容，对于当前所在 form 标签之外的表单清除无效。
>
> 类似的，提交按钮也是

#### conclusion

- 普通按钮一般情况下都是配合 JavaScript 来进行各种操作的。
- 提交按钮一般都是用来给服务器提交数据的；
- 重置按钮一般用来清除用户在表单中输入的内容。

### 文件上传

```html
<input type="file" />

<!-- example -->

<form method="post"><input type="file" /></form>
```

## 多行文本框

```html
<textarea rows="行数" cols="列数" value="取值">默认内容</textarea>
```

## 下拉列表

```html
<select>
  <option>选项内容</option>
  ……
  <option>选项内容</option>
</select>
```

> 我们可以把下拉列表看成是一种特殊的无序列表

### select 标签属性

![](./_image/2022-03-20/a5b6b60c6c0530d7d719e05694162a4e.jpg?c=1)

> 默认情况下，下拉列表只能选择一项，我们可以通过 multiple 属性设置下拉列表可以选择多项。想要选取多项，可以使用“Ctrl+鼠标左键”来选取。

```html
<select multiple></select>

<select size="5"></select>
```

### option 标签属性

![](./_image/2022-03-20/be75136a64d5d3720aa7689a991e2655.jpg?c=1)

```html
<option selected>jQuery</option>

<option value="CSS">CSS</option>
```
