# HTML 标签

---

## 标签的种类

1. 单标签

```html
<input />
<img />
<br />  
<hr />
```

2. 双标签（大多数）

```html
<div></div>
<span></span>
```

## 标签定义

1. 元素
2. 属性
   - 名值对

---

## 常用标签

### 基本结构

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Document</title>
  </head>
  <body></body>
</html>
```

### 标题标签

```html
<h1></h1>
//一个HTML文档只能用一个
<h6></h6>
```

### 段落标签

```html
<p></p>
```

### 结构标签

div 标签

> 块标签、块级元素

span 标签

> 内联标签、一行文本：用来修饰文字

### 链接

> anchor

```html
<a></a>
```

- 属性
  - href
    > 表示链接的地址，可以使相对地址或者绝对地址
  - target
    > 表示点击链接后打开的方式，默认值为`_self`，代表在当前窗口打开新链接；`_blank`代表在新窗口中打开。

* 空链接

```html
<a href="javascript:void(0)">空链接</a> <a href="javascript:;">空链接2</a>
```

### base 标签

```html
<head>
  <base target="_blank" />
</head>
```

### 图片标签

```html
<img />
```

- 属性
  - src：图片的地址
  - alt：图片无法显示时的替代文本
  - height：高度
  - width：宽度
  - title：鼠标悬停时显示文字

### 列表标签

属性：`type`

- 无序列表
  ```html
  <ul>
    <li>q</li>
    <li>w</li>
    <li>e</li>
  </ul>
  ```
- 有序列表
  ```html
  <ol>
    <li>q</li>
    <li>w</li>
    <li>e</li>
  </ol>
  ```
- 自定义列表
  ```html
  <dl>
    <dt>q</dt>
    <dd>q</dd>
    <dd>w</dd>
    <dd>e</dd>
  </dl>
  ```

### 表格标签

#### 表格元素

表格：`<table></table>`  

行：`<tr></tr>`  

列：`<td></td>`  

表格标题：`<caption></caption>`  

表格首行标题：`<th></th>`  

表格边框：`<table border="5" width="500" height="200"></table>`  

单元格跨行：`colspan`  

单元格跨列：`rowspan`

表格单列背景颜色：
```html
    <col bgcolor="red"> 
    <col bgcolor="blue">
    <col bgcolor="yellow">
```
表格样式：
```html 
<colgroup span="4" width="300"></colgroup>
```

单元格间距(表格间距)：`cellspacing`

单元格边距(表格填充)：`cellpadding`

对齐：  

`align`
- center  
- right  
- left  

`valign`
- top
- bottom

#### 结构

表格头部：`<thead></thead>`  
表格主体：`<tbody></tbody>`  
表格底部：`<tfoot></tfoot>`

#### 快捷键
`tr*3>td*4`：创建三行四列

---

## 特殊字符

### 空格字符

> html 中多个空格只会显示出一个

```html
&nbsp;
```
