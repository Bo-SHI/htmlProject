## CSS 基础语法

- CSS规则由两个主要的部分组成：选择器以及一条或多条声明

- 选择器为要更改的HTML元素

- 声明则由属性和值组成

**NOTE 1**： 当使用RGB百分比的时候，即时当值为0时也要写百分比。其他情况下不需要...
**NOTE 2**:  当值为若干单词的时候，需要给值加引号 p {font-family:"sans serif"}

- 多重声明需要使用分号，最后一个声明可加可不加，建议加上

- 是否包含空格不会影响CSS在浏览器中的效果



## CSS 高级语法

- 选择器分组：同一组的选择器可以分享相同的声明，同一分组的选择器需要用逗号将彼此分开。

- CSS中子元素将从父元素继承属性

**NOTE 3**： Netspace 4 无法理解继承，注意兼容性问题

- 如果不希望子元素继承父元素的属性，可以为子元素单独定义特殊规则


## CSS派生选择器

- 通过依据元素在其位置的上下文关系来定义样式

- 派生选择器也被称为后代选择器

- 后代选择器钟，规则左边的选择器一端包括两个或多个用空格分开的选择器

- 后代选择其中，两个元素之间的层次间隔可以是无限的


## CSS子元素选择器

- 与后代选择器相比，子元素选择器只能选择作为某元素子元素的元素

- 子元素选择器使用大于号(子结合符)


## CSS相邻兄弟选择器

- 相邻兄弟选择器可选择紧接在另一元素后的元素，且二者有相同的父元素

- 相邻兄弟选择器使用+作为相邻兄弟结合符


## CSS id 选择器

- id选择器可以为标有特定id的HTML元素制定特定的样式

- id选择器以‘#’来定义

- id选择器在同一个HTML文档中 仅且只能使用一次

- id选择器不能使用id词列表

- id选择器区分大小写


## CSS 类 选择器

- 类选择器以一个点号来显示

**NOTE 4**: 类选择器第一个字符不能用数字 (好多都不能用 比如 各种语言的变量名)

- 多类选择器 可以把两个类选择器链接在一起，仅可以选择同时包含这些类名的元素(前后顺序无关紧要)


## CSS 属性选择器

- 对带有制定属性的HTML元素设置样式

- 多属性选择器 将多个属性选择器链接在一起

### 类型
- [attribute]         选取带有指定属性的元素
- [attribute=value]   选取带有指定属性和值的元素
- [attribute~=value]  选取属性值中包含指定词汇的元素
- [attribute|=value]  选取属性值以指定值开头的元素 该值必须为整个单词
- [attribute^=value]  选取属性值以指定值开头的每个元素
- [attribute$=value]  选取属性值以指定值结尾的每个元素
- [attribute*=value]  选取属性值包含指定值的每个元素



## CSS 背景

- 所有的背景属性都不能继承

- CSS允许应用纯色作为背景 也允许使用背景图片创建相当复杂的效果

### 类型
- background-color 为元素设置背景色 默认值为tramsparent

- background-image 设置背景图像 默认值为none 必须设置  URL h1 {background-image:url(*.gif)}

- background-repeat 可以对背景图像进行平铺 默认值为 repeat   repeat-x、 repeat-y分别导致图像在水平 垂直方向进行平铺 no-repeat不允许图像平铺

- background-position 改变图像在背景中的位置 可以使用关键字 百分数值 长度值! 关键字为 center top buttom left right 一般关键字成对出现 如果只出现一个关键字 则认为另一个为center;
                    百分数值 同时作用于图像和元素 该属性的默认值是 0% 0%;   
                    长度值 解释的是元素内边距区左上角的偏移 偏移点是图像的左上角

- background-attachment 图像是否滚动 默认scroll滚动    fixed固定    inherit继承

- background 可简写属性   body {background : #00FF00 url(*.gif) no-repeat fixed  center;}  



## CSS 文本

> 文本属性可以定义文本的外观
> 通过文本属性，可以改变文本的颜色、字符间距、对齐文本、装饰文本、对文本进行缩进等

- text-indent 文本缩进 可以为所有块级元素应用该属性，但是行内元素和图像之类的替换元素无法应用
                    可以使用负值
                    使用百分比，百分数要相对于缩进元素父元素的宽度
                    可以继承

- text-align 文本对齐 会影响一个元素中的文本行互相之间的对齐方式
                   将块级元素或表元素居中，需要在这些元素上适当的设置左右外边距  
                   left right center justify inherit
                   默认值是由浏览器决定的

- word-sapcing 改变字(单词)之间的标准间隔 默认值为normal 默认值与设置为0 效果一样
             接受一个正长度值或负长度值
             可以继承

- letter-spacing 改变字母之间的间隔 默认为normal
               接受一个正长度值或负长度值
               可以继承

- text-transform 处理文本的大小写
               默认值为 none 不做任何改动
               uppercase lowercase capitalize

- text-decoration 处理文本的样式
                默认值为 none
                underline overline line-through blink

- white-sapce 影响源文档中空格、换行和tab字符的处理
            默认值为 normal
            pre nowrap pre-line pre-wrap

- direction 设置文本方向 ltr rtl

- color 设置文本颜色

- line-heght 设置文本行高


## CSS 字体属性

- font-family 规定元素的字体系列 默认值由浏览器决定

- font-size 设置字体的尺寸 默认值 medium

- font-style 设置字体的风格 默认值 normal
           italic oblique inherit

- font-weight 设置文本的粗细 默认值normal

- font-variant 设置小型大写字母文本 默认normal
             small-caps inherit

- font 简写属性


## CSS 链接

#### 链接的四种状态：

> a:link 普通、未被访问的链接

> a:visited 用户已经访问过的链接

> a:hover 鼠标指针位于链接的上方

> a:active 链接被点击的时刻

- 当为链接的不同状态设置样式的时候：
a:hover 必须位于a:link a:visited 之后
a:active 必须位于a:hover之后

- 常见的链接样式 :
text-decoration
background-color


## CSS列表

> CSS列表属性允许你放置、改变列表项标志，或者将图像作为列表项标志

- list-style-type 列表项标志
- list-style-image列表项图片
- list-style-position列表标志位置
- list-style 简写

## CSS表格

> CSS表格可以极大改善表格的外观

- border 表格边框属性
- border-collapse 折叠边框 默认值 separate   collapse值会合并为一个单一的边框
- border-spacing 设置相邻单元格之间的距离 (仅用于边框分离模式) 值为 length length 单值定义水平垂直 双值分别定义水平和垂直
- caption-side 设置表格标题的位置 top bottom
- empty-cells 是否显示表格中的空单元格（仅用于边框分离模式）hide show(默认值)
- table-layout 用来显示表格单元格、行、列的算法规则 默认值auto   fixed


## CSS轮廓

>CSS轮廓是绘制于元素周围的一条线，位于边框边缘的外围，可起到突出元素的作用

>CSS outline属性规定元素轮廓的样式、颜色和深度

- outline 简写属性
- outline-style 轮廓的样式 none(默认值)  dotted dashed solid double groove ridge inset outset
- outline-color 轮廓的颜色
- outline-width 轮廓的宽度


## CSS框模型

> 元素框的最内部分是实际的内容，直接包围内容的是内边距。内边距呈现了元素的背景。内边距的边缘是边框。边框以外的是外边距，外边距默认是透明的，因此不会遮挡其后的任何元素

> 背景应用于元素的内容 内边距 和 边框组成的区域

> 内边距 边框 外边距 都是可选的 默认值为0

> CSS中 height width指的是内容区域的高度和宽度。增加内边距 边框和外边距不会影响内容区域的尺寸，但是会影响元素框的尺寸

> 外边距可以使负值


## CSS内边距

> padding  接受长度值或百分比  但是不允许是负值 百分数值是相对于父元素的width计算的，这一点和外边距一样
- padding-top
- padding-right
- padding-bottom
- padding-left


## CSS边框

> 元素的边框是围绕元素内容和内边距的一条或多条线

> CSS border属性可以规定元素边框的样式 颜色 和宽度

> border-style none(默认值)  hidden(同none 但是用于table时，可以解决边框冲突) dotted dashed solid double groove ridge insert outset
- border-stop-style
- border-right-style
- border-bottom-style
- border-left-style

> border-width 长度值 关键字 thin medium(默认值) thick
- border-top-width
- border-right-width
- border-bottom-width
- border-left-width

> border-color transparent(透明边框 相当于额外的内边距)
- border-top-color
- border-right-color
- border-bottom-color
- border-left-color

> 边框如果没有样式 就没有宽度 也没有颜色


## CSS外边距

> 围绕在元素边框的空白区域是外边距。设置外边距会在元素外创建额外的“空白”

> 设置外边距的最简单的方法是 margin
