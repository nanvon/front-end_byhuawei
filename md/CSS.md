# CSS
## CSS的引入
- 内联样式  
    > 将CSS样式直接写到HTML元素的`style`属性中
- 内部样式  
    > 将CSS样式写道`<style>`标签中
- 引入外部样式  
    > 精确通过`<link>`元素引入外部的一个CSS文件
- 导入外部样式  
    > 通过在`<style>`元素中，使用`@import`导入一个外部的CSS文件  


## CSS基本语法
### 一个基本结构、三个注意事项

* `选择器{样式名:样式值;}`

1. 分号分隔
2. 小写
3. 逗号分隔 

## CSS的特性
- 层叠样式
- 继承性

## CSS选择器

### 通配符选择器
通配符选择器，用`*`表示，对所有元素都生效
```css
*{property:vale; ......}
```
### 元素选择器
使用某个HTML元素名作为选择器
```css
h1{property:value;......}
```
### id选择器
可以在HTML标签上设置一个id属性值，且唯一不可重复
```css
#content{property:value;......}

<div id="content">HUAWEI</div>
```
### 类选择器
类指class属性，有相同class属性值的都会被选中，不具有唯一性，可以和元素选择器组合使用
```css
.title{property:value;......}

<div class="title">HUWEI</div>
```

### 属性选择器
用于对某种属性的元素设置CSS样式
```css
E[attribute]{property:value;......}
```
#### 属性的种类：
- `[attribute]`用于选取指定属性（attribute）的元素
- `[attribute=value]`用于指定属性（attribute）和指定属性值（value）的元素
- `[attribute~=value]`用于选取属性值中包含指定值的元素
- `[attribute|=value]`用于选取以指定值开头的属性值的元素


### 伪类选择器
指哪些处在一定状态的元素，以冒号开头

伪类：
> 这个从上往下的顺序很重要：`L`o`V`e `H``A`te 爱与恨
- `link` 表示未被访问的链接
- `visited` 表示已被访问的链接
- `hover` 鼠标经过链接上方时的状态
- `active` 链接被激活时的状态  

### 派生选择器
1. 后代选择器
```css
父元素 子元素{property:value;......}
```
> 注意：父元素与子元素之间至少有一个空格，可以有很多空格

```css
p span{color:red;}
```
2. 子元素选择器
```css
父元素 > 子元素{property:value;......}
```
用来选择作为某一个元素子元素的元素，与后代选择器的区别是后代选择器选择的是所有子元素，而子元素选择器只选**第一级**子元素
```css
p > span{color:red}
```

3. 相邻兄弟选择器
```css
父元素 + 子元素{property:value;......}
```
用来选择紧跟在一个元素**之后**的兄弟元素，这两个相邻源深路一定是同级元素

```css
div + p{color:red}
```