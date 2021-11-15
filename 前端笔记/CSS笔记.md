# CSS笔记

## 标签选择器：

  **标签选择器：写上标签吗** 

​    `p {`

​      `color: green;`

​    `}`

## 类选择器：

 **类选择口诀：样式点（.）定义 结构类class定义 一个或多个 开发最常用** 

 `.saddlebrown {`

​      `color: saddlebrown;`

​    `}`  

​    `.red {`

​      `color: red;`

​    `}`

## id选择器：

**结构id调用只能调用一次** 

### id选择器多用于页脚等在一个页面上只出现一次的事物

   `#pink {`

​      `color: pink;`

​    `}`

## 通配符选择器：

  \* {

​      color: green;

​    }

 <!-- *在这里将所有的标签都转为了绿色 -->

## 字体：

### 字体系列：

​    `h2 {`

​      `font-size: 30px;`

​    `}`

### **font-size指定字体的大小**

​    `h2 {`

​      `font-family: '微软雅黑';`

​    `}`

### **CSS 属性 `font-family` 允许您通过给定一个有先后顺序的，由字体名或者字体族名组成的列表来为选定的元素设置字体。**

属性值用逗号隔开。浏览器会选择列表中第一个该计算机上有安装的字体，或者是通过 [`@font-face`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/@font-face) 指定的可以直接下载的字体。

应当至少在使用的 `font-family` 列表中添加一个通用的字体族名，因为无法保证用户的计算机内已经安装了指定的字体，也不能保证使用 [`@font-face`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/@font-face) 提供的字体移动能够正确地下载。提供通用的字体族使得浏览器可以在无法得到最佳字体的情况下使用一个相对接近的备选字体。

### font-weight（字体重量）：

只提供 和 两种值。`normal``bold`

但后面可以跟数字，但不要跟单位

  **700的后面不要跟单位 效果和bold等价 实际开发中我们更推荐用数字 400相当于normal 700相当于bold** 

### font-style：

**`font-style`** CSS 属性允许你选择 [`font-family`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/font-family) 字体下的 或 样式。`italic``oblique`

  **font-style: italic;**是**斜体**

**font-style: normal;**是**正常字体**

```
font-style: oblique;
```

```
font-style: oblique 10deg;
```

选择倾斜体，如果当前字体没有可用的倾斜体版本，会选用斜体（ ）替代

oblique后面跟着的便是度数，如10deg便是倾斜10deg

### 字体颜色：

   `div {`

​      `/* color: grey; */`

​      `/* color: #7700ffc2; */`

​      `color: rgb(255, 204, 213);`

​    `}`

### 文本对齐：

  **text-align: center;**

**本质上是让h1盒子里面的文字水平居中对齐**

并不控制块元素自己的对齐，只控制它的行内内容的对齐

![image-20210818103644848](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818103644848.png)

### 装饰文本：

 **text-decoration: underline;**

`text-decoration` 这个 CSS 属性是用于设置文本的修饰线外观的（下划线、上划线、贯穿线/删除线 或 闪烁）

![image-20210818140813289](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818140813289.png)

![image-20210818141143168](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818141143168.png)

   **`a {`**

​      **`/* 用于网页链接中取消下划线，使界面更加整洁 */`**

​      **`text-decoration: none;`**

​    **`}`**

## 字体复合属性：

 复合属性有严格的顺序要求 ：

###      font： font-style font-weight font-size/line-height font-family; 

   **`div {`**

​      **`font: italic 700 500px '微软雅黑';`**

​    **`}`**

## 文本缩进：

**`text-indent` 属性能定义一个块元素首行文本内容之前的缩进量。**

   **`p {`**

​      **`/* 文本的第一行空格 多用于文章内容排版 */`**

​      **`/* text-indent: 20px; */`**

​      **`text-indent: 2em;`**（**此处可以用于文章的排版 2em表示空出两格**）

​      **`/* em为当前元素一个文字的单位大小 */`**

​    **`}`**

## 行间距：

**`line-height`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) 属性用于设置多行元素的空间量，如多行文本的间距。对于块级元素，它指定元素行盒（line boxes）的最小高度。对于非[替代](https://developer.mozilla.org/en-US/docs/Web/CSS/Replaced_element)的 inline 元素，它用于计算行盒（line box）的高度。

![image-20210818141705749](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818141705749.png)

## 样式表：

### 1.内部样式表：

![image-20210818141824994](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818141824994.png)

### 2.行内样式表：

![image-20210818141851253](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818141851253.png)

### 3.外部样式表：

![image-20210818141916789](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818141916789.png)

### 通过link来引用外部样式表，也是我们开发中最常用的方法

## 块元素：

![image-20210818142038309](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818142038309.png)

### **默认情况下，块级元素会新起一行。**

以下是 HTML 中所有的块级元素列表（虽然”块级“在新的 HTML5 元素中没有明确定义）

![image-20210818142443152](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818142443152.png)

![image-20210818142520455](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818142520455.png)

![image-20210818142554125](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818142554125.png)

## 行内元素：

![image-20210818143215017](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818143215017.png)

**HTML (超文本标记语言) 元素大多数都是行内元素或[块级元素](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Block-level_elements)。一个行内元素只占据它对应标签的边框所包含的空间**

![image-20210818143407742](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818143407742.png)

### 行内元素和块元素的区别：

### 默认情况下，行内元素不会以新行开始，而块级元素会新起一行。

## 行内块元素：

![image-20210818143517120](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818143517120.png)

### 相邻的行内块元素在同一行上，但有间隙

### 常见的行内块元素：

**img, input, textarea**

## 元素显示模式转换：

**`display`** 属性可以设置元素的内部和外部显示类型 *display types*。元素的外部显示类型 *outer display types* 将决定该元素在[流式布局](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Flow_Layout)中的表现（[块级或内联元素](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Flow_Layout)）；元素的内部显示类型 *inner display types* 可以控制其子元素的布局（例如：[flow layout](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Flow_Layout)，[grid](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Grid_Layout) 或 [flex](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Flexible_Box_Layout)）。

![image-20210818144512877](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818144512877.png)

### 还可以用来隐藏其他的元素（原先的位置消失）

![image-20210818152950857](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818152950857.png)

### 不同于**visibility**（仍占有原先的位置）

![image-20210818153051916](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818153051916.png)

## 背景：

### 背景颜色：

[CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)属性中的 **background-color** 会设置元素的背景色, 属性的值为颜色值或关键字"transparent（**透明**）"二者选其一.

### 背景图片：

**`background-image`** 属性用于为一个元素设置一个或者多个背景图像。

![image-20210818145438073](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818145438073.png)

### 背景平铺：

![image-20210818145711785](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818145711785.png)

![image-20210818145657763](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818145657763.png)

### 背景位置-方位名词：

**`background-position`** 为每一个背景图片设置初始位置。 这个位置是相对于由 [`background-origin`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/background-origin) 定义的位置图层的。

![image-20210818152317736](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818152317736.png)

![image-20210818152349632](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818152349632.png)

### 先X轴，再Y轴

![image-20210818152723310](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818152723310.png)

### 不可以连续两个方位名词



### 背景半透明：

![image-20210818152859429](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818152859429.png)

## 位置position：

![image-20210818153604710](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818153604710.png)

### 相对定位：

```
relative
```

**该关键字下，元素先放置在未添加定位时的位置，再在不改变页面布局的前提下调整元素位置（因此会在此元素未添加定位时所在位置留下空白）。position:relative 对 table-*-group, table-row, table-column, table-cell, table-caption 元素无效。**

### relative相对自己原来的位置进行移动，不脱标（后面的盒子不能使用他原来的位子）



### 绝对定位：

![image-20210818155237434](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818155237434.png)

```
absolute
```

**元素会被移出正常文档流，并不为元素预留空间，通过指定元素相对于最近的非 static 定位祖先元素的偏移，来确定元素位置。绝对定位的元素可以设置外边距（margins），且不会与其他边距合并。**

### 绝对定位水平垂直居中：

![image-20210818155628983](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818155628983.png)



### 固定定位：

![image-20210818155438721](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818155438721.png)

```
fixed
```

**元素会被移出正常文档流，并不为元素预留空间，而是通过指定元素相对于屏幕视口（viewport）的位置来指定元素位置。元素的位置在屏幕滚动时不会改变。打印时，元素会出现在的每页的固定位置。`fixed` 属性会创建新的层叠上下文。当元素祖先的 `transform`, `perspective` 或 `filter` 属性非 `none` 时，容器由视口改为该祖先。**



### 固定定位的小技巧（贴在版型边缘上）

![image-20210818155541938](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818155541938.png)





### *<u>**子绝父相**</u>*

**该口诀及其重要**

 **<!-- 子为绝对定位，父为相对定位 -->**

  **<!-- 相对定位可以占据一个位置，不会让下面的其他盒子进入，同时可以让子盒子呆在里面 -->**



### 粘性定位：

`.nav {`

​      **`/* 粘性定位必须添加top 或者left或者right */`**

​      **`position: sticky;`**

​      **`top: 0;`**

​      **`/* 当距离可视区域为0时，变成固定位置的效果 */`**

​      **`/* 但由于兼容性太差，不是特别常用 */`**

​      **`width: 800px;`**

​      **`height: 50px;`**

​      **`background-color: pink;`**

​      **`margin: 100px auto;`**`}`

![image-20210818160009921](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818160009921.png)

### 例如当用户下滑的时候，他会粘在用户浏览界面的顶部一直呆着（sticky作用）



## 复合选择器：

### 后代选择器：

![image-20210818160158871](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818160158871.png)

### 子代选择器：

![image-20210818160222589](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818160222589.png)

### 并集选择器：

![image-20210818160244637](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818160244637.png)

### 伪类选择器：

![image-20210818160348931](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818160348931.png)

**伪类连同伪元素一起，他们允许你不仅仅是根据文档 DOM 树中的内容对元素应用样式，而且还允许你根据诸如像导航历史这样的外部因素来应用样式（例如 [`:visited`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:visited)），同样的，可以根据内容的状态（例如在一些表单元素上的 [`:checked`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:checked)），或者鼠标的位置（例如 [`:hover`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:hover) 让你知道是否鼠标在一个元素上悬浮）来应用样式。**



### focus选择器：

![image-20210818160542321](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210818160542321.png)

## 盒子模型：

## 边框border：

### border-width：可以设置盒子模型的边框宽度。

### 设置四个边不同宽度 则顺序为上右下左（顺时针）

![image-20210819085029012](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819085029012.png)

### border-style：用来设定元素所有边框的样式。

![image-20210819085135617](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819085135617.png)

![image-20210819085145508](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819085145508.png)

### border-color：

用于设置元素四个边框颜色的快捷属性

![image-20210819085338422](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819085338422.png)

### 边框的复合写法：

![image-20210819085420072](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819085420072.png)

### 边框会影响实际盒子的大小



### 圆角边框：

### border-radius

##### 允许你设置元素的外边框圆角。当使用一个半径时确定一个圆形，当使用两个半径时确定一个椭圆。这个(椭)圆与边框的交集形成圆角效果。

![image-20210819085535336](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819085535336.png)



### 盒子阴影：

##### 用于在元素的框架上添加阴影效果。你可以在同一个元素上设置多个阴影效果，并用逗号将他们分隔开。该属性可设置的值包括阴影的X轴偏移量、Y轴偏移量、模糊半径、扩散半径和颜色。

**box-shadow**

![image-20210819090408253](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819090408253.png)

### 文字阴影：

`**text-shadow**为文字添加阴影。

![image-20210819090528786](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819090528786.png)

### 块级盒子水平居中对齐：

![image-20210819090629032](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819090629032.png)

### 内边距：padding

![image-20210819092632870](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819092632870.png)

### 外边距：margin

![image-20210819092724253](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819092724253.png)

### 外边距合并：

![image-20210819092803802](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819092803802.png)

### 清除内外边距：

![image-20210819092837452](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819092837452.png)

### 行内和行内块元素水平居中对齐：

![image-20210819092914753](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819092914753.png)

属性定义行内内容（例如文字）如何相对它的块父元素对齐。`text-align` 并不控制块元素自己的对齐，只控制它的行内内容的对齐。

## CSS3:

### 新增属性选择器：

![image-20210819093244306](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819093244306.png)

### 新增伪类选择器：

![image-20210819093312285](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819093312285.png)

### 新增伪元素选择器：

![image-20210819093342238](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819093342238.png)

![image-20210819093413821](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819093413821.png)

![image-20210819093427533](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819093427533.png)

### CSS3过渡：

#### transition

过渡可以为一个元素在不同状态之间切换的时候定义不同的过渡效果。比如在不同的伪元素之间切换，像是 [`:hover`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:hover)，[`:active`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:active) 或者通过 JavaScript 实现的状态变化。

![image-20210819093522949](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819093522949.png)

#### 谁过渡给谁加

![image-20210819093618142](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819093618142.png)

### 盒子计算大小：

### <!--盒子大小为：width+padding+border-->

![image-20210819093724457](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819093724457.png)

### 盒子宽度calc函数：

![image-20210819093753341](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819093753341.png)

### 图片模糊处理：

**`filter`** CSS属性将模糊或颜色偏移等图形效果应用于元素。滤镜通常用于调整图像，背景和边框的渲染。

![image-20210819093838557](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819093838557.png)

## 浮动：

float CSS属性指定一个元素应沿其容器的左侧或右侧放置，允许文本和内联元素环绕它。该元素从网页的正常流动(文档流)中移除，尽管仍然保持部分的流动性（与[绝对定位](https://developer.mozilla.org/zh-CN/docs/Web/CSS/position#absolute_positioning)相反）。

![image-20210819093925223](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819093925223.png)

![image-20210819093939726](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819093939726.png)

### 浮在半空中，曾所在的位置被其他盒子占据

### <!-- 任何元素都可以浮动，不管原先是什么模式的元素，添加浮动后都具有行内块元素特点 -->

如果行内块元素有了浮动，则不需要转换成块级/行内块元素可以直接给高度和宽度

####   <!-- 如果块级元素没有设置宽度，默认宽度和父级一样宽，但是添加浮动后，他的大小根据内容来决定 -->

#### 清除浮动：

 **`clear`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) 属性指定一个元素是否必须移动(清除浮动后)到在它之前的浮动元素下面。`clear` 属性适用于浮动和非浮动元素。

![image-20210819094137859](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819094137859.png)

![image-20210819094203175](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819094203175.png)

### overflow：

CSS属性 **overflow** 定义当一个元素的内容太大而无法适应 [块级格式化上下文](https://developer.mozilla.org/zh-CN/docs/Web/Guide/CSS/Block_formatting_context) 时候该做什么。它是 [`overflow-x`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/overflow-x) 和[`overflow-y`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/overflow-y)的 [简写属性 ](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Shorthand_properties)。

![image-20210819094259890](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819094259890.png)

## CSS高级导读：

[CSS](https://developer.mozilla.org/en-US/docs/CSS) 的 `outline` 属性是在一条声明中设置多个轮廓属性的[简写属性](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Shorthand_properties) ， 例如 [`outline-style`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/outline-style), [`outline-width`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/outline-width) 和 [`outline-color`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/outline-color)。 

 **`resize`** CSS 属性允许你控制一个元素的可调整大小性。

![image-20210819100600950](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819100600950.png)

![image-20210819100621558](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819100621558.png)

### 单行文本溢出省略号显示：

![image-20210819100654390](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819100654390.png)

### 多行文本溢出省略号显示：

![image-20210819100724894](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819100724894.png)

### 精灵图导读：

![image-20210819100814541](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819100814541.png)

### 鼠标样式：cursor

![image-20210819100838715](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819100838715.png)

### 图片底部空白缝隙解决方案：

**`vertical-align`** 用来指定行内元素（inline）或表格单元格（table-cell）元素的垂直对齐方式。

![image-20210819101020238](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819101020238.png)

## CSS三大特性：

### 层叠性：

![image-20210819101121793](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819101121793.png)

### 继承性：

![image-20210819101144616](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819101144616.png)

### 优先级：

![image-20210819101201329](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819101201329.png)

### 权重的叠加：

![image-20210819101222829](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819101222829.png)

### 行高的继承：

![image-20210819101240230](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210819101240230.png)

