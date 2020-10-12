# CSS
## 一、CSS的引入
- 内联样式  
    > 将CSS样式直接写到HTML元素的`style`属性中
- 内部样式  
    > 将CSS样式写道`<style>`标签中
- 引入外部样式  
    > 精确通过`<link>`元素引入外部的一个CSS文件
- 导入外部样式  
    > 通过在`<style>`元素中，使用`@import`导入一个外部的CSS文件  


## 二、CSS基本语法
### 一个基本结构、三个注意事项

* `选择器{样式名:样式值;}`

1. 分号分隔
2. 小写
3. 逗号分隔 

## CSS的特性
- 层叠样式
- 继承性

## 三、CSS选择器

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


### 选择器权重

权重规则：  

通配符选择器：0  
标签选择器：1  
类、伪类、属性选择器：10  
id选择器：100  
内联样式：1000  
特殊处理：`!important`（强制使用的含义）

## 四、CSS常用属性

### 1. 字体
> 使用`font-family`属性来定义字的字体  
> 属性值为字体的名称，可以设置多个字体名称，浏览器会按照顺序使用它的第一个支持的字体

- serif 衬线字体，常用于标题
- sans-serif 非衬线字体，常用于正文
- 等宽字体

#### 字体尺寸
> 使用`font_size`属性来定义文字的尺寸  
> 属性值为长度值，例如30px，也可以使用百分比，例如50%

#### 字体样式
> 使用`font-style`属性设置文字为斜体，向右侧倾斜  
> 默认属性值为`normal`显示标准效果  
> 当属性值为`italic`时显示倾斜效果

#### 字体粗细
> 使用`font-weight`属性设置文字的粗细  
> 默认值为`normal`,相当于400，显示效果为正常粗细  
> 当属性值为`bold`时，相当于700，显示为粗体  
> 当属性值为bolder时，显示更粗  
> 当属性值为lighter时，显示更细  
> 也可以设置属性值为一个具体数值：100/200/300/.../800/900

#### 简写属性
> 使用`font`属性来定义所有文字的样式  
> 各个属性值用空格分隔
> `font = font-family + font-size + font-style + font-weight

例如：
```css
p{font:monospace 50px bold italic}
```

### 2. 文本
#### 颜色
> `color`   
> 颜色名、十六进制颜色值、RGB颜色值

#### 行高
> `line-height`  
> 默认值：`normal`
> 其他属性值为长度值、百分比

#### 对齐方式
> `text-align`  
> 属性值：`left`左、`right`右、`center`中

#### 方向
> `direction`  
> 属性值：`ltr`左、`rtl`右

#### 缩进
> `text-indent`  
> 默认值：0，其他属性值：长度、百分比  
> `1em`表示一个字的宽度

#### 装饰线
> `text-decoration`  
> 属性值：`underline`下划线、`overline`上划线、`line-through`中划线  
> 默认值为`none`,表示没有线

#### 间隔
> `letter-spacing`  
> 属性值为长度值，可以为负值

#### 阴影
> `text-shadow`  
> 属性值为：X轴偏移量+Y轴偏移量+模糊距离+颜色  
> 例如：
```css
text-shadow:10px 10px 5px gray
```

### 3. 尺寸
#### 宽度和高度
> `width`宽度  
> `height` 高度  
> 属性值：`auto`、长度、百分比

#### 最小宽度和最小高度
> `min-width`最小宽度  
> `min-height`最小高度

#### 最大宽度和最大高度
> `max-width`最大宽度  
> `max-height`最大高度


### 4. 列表
- `list-style-image`   
用于指定一个图片作为列表项前面的标记  
默认值为`none`，可以设置一个图片的`url`作为标记图片

- `list-style-position`  
用于设置在什么位置显示列表项前面的标记  
默认值为`outside`，还可以设置为`inside`

- `list-style-type`  
用于设置列表项前面图片的类型  
默认值为`disc`，其他值：`circle`,`square`,`decimal`,`none`,`low-alpha`,`upper-alpha`...

- `list-style`  
这是一个简写属性  
`list-style` = `list-style-image` + `list-style-position`  + `list-style-type`   
例如：`ul{list-style: decimal inside}`