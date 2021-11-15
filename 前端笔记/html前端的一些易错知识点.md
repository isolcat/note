# html前端的一些易错知识点

## alt和title容易弄混：

### alt是当图片无法显示时才出现的文字 title是当鼠标放在图片上时可以显现出来的文字



## <pre>标签是：

<pre> 标签的作用是预排版

![img](https://uploadfiles.nowcoder.com/images/20200821/5121786_1598022941664_632E97BFC1094BBEC5EF70E882A09EE0)

## 超链接代码：

### 表示打开一个新标签页的超链接代码是：

```
<a href=URL target=_blank>..</a>
```

**_blank:在新窗口打开 _self:在当前窗口打开 _parent:在父级窗口打开 _top:在最顶级窗口打开**

## HTML5是否向后兼容旧浏览器：

### **HTML5 被设计成尽可能向后兼容现有的 web 浏览器**

## 若浏览器最开始没有使用DOCTYPE会怎么办？



在 [HTML](https://developer.mozilla.org/zh-CN/docs/Glossary/HTML) 中，文档类型 doctype 的声明是必要的。在所有文档的头部，你都将会看到"<!DOCTYPE html>" 的身影。这个声明的目的是防止浏览器在渲染文档时，切换到我们称为“[怪异模式(兼容模式)](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Quirks_Mode_and_Standards_Mode)”的渲染模式。“<!DOCTYPE html>" 确保浏览器按照最佳的相关规范进行渲染，而不是使用一个不符合规范的渲染模式。



## <audio>的作用：

<audio>可以在开始标签和结束标签之间放置文本内容，这样老的浏览器就可以显示出不支持该标签的信息。

![image-20210808213559704](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210808213559704.png)

## 重绘与排版：

```
设置display:none后的元素只会导致浏览器的重排而不会重绘
```

#### 重排一定重绘，重绘不一定重拍

## 提问文字颜色时：

### 直接看权重 通过权重大小来判断是否为什么颜色

![image-20210808213901216](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210808213901216.png)

**标签的权重是1，类的权重是10 ，id的权重是100**

**ul#related span 的权重为 1+100+1=102**

**\#favorite .highlight 的权重为 100+10=110**

**highlight 的权重为 10**   故为orange

## 使div不会脱离文档流的属性：

```
position: fixed;
```

**浮动（float）、固定定位（fixed）和绝对定位（absolute）都会使元素脱离文档流，绝对定位相对于最近的开启了定位（即position不为static）的父元素进行定位**

**相对定位（relative），相对于自身初始位置进行定位，不脱离文档流**

## HTML5中一个页面不可以存在多个title元素

## HTML5中常用的新特性：

**canvas元素：用于定义图形（图表等），只是图形容器，必须使用脚本来绘制图形。**

**audio：用于音频播放。**

**video：用于视频播放。**

**article：规定独立的自包含内容。**

**header：定义文档的页眉，介绍相关信息。**

**section：定义文档中的节。**

**footer：定义文档的页脚，通常有文档的作者、版权信息、联系方式等。**

**nav：定义导航链接。**



**表单控件：**

**calender**

**date**

**time**

**email**

**url**

**search**

### 注：caption是定义表格标题 不是html5新增的标签

## 将搜索词高亮显示：

使用<mark>标签（mark标签为html5新增标签）

<img src="C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210808214612494.png" alt="image-20210808214612494" style="zoom: 50%;" />

## 关于屏幕尺寸标准：

| 超小屏幕（手机） | 小屏幕（平板） | 中等屏幕（桌面） | 大屏幕（桌面） |
| :--------------: | :------------: | :--------------: | :------------: |
|      <768px      |     >=768      |      >=992       |     >=1200     |
|     .col-xs-     |    .col-sm-    |     .col-md-     |    .col-lg-    |

## 可以被继承的属性：

**可以被继承的属性： 字体系列：font-family，font-size，font-style，font-weight，font-stretch，font-size-adjust； **

**列表相关：list-style，list-style-image，list-style-position，list-style-type，list-style-color； **

**文本系列：text-indent，text-align，line-height，word-spaceing，letter-spacing，text-transform，direction，color； **

**元素可见性：visibility；**

 **表格布局：caption-side，border-collapse，border-spacing，empty-cells，table-layout； 生成内容：quotes； 光标属性：cursor；**

 **页面样式：page，page-break-inside，Windows，orphans；** 

**声音样式属性：speak、speak-punctuation、speak-numeral、speak-header、speech-rate、volume、voice-family、pitch、pitch-range、stress、richness、、azimuth、elevation。**



### 可以被继承的属性主要有文本(font-)，颜色(背景颜色不可以！)，列表(list-style-type)，元素可见性visibility

## meta标签：



一个常用的针对移动网页优化过的页面的 viewport meta 标签大致如下：（**这些是meta可以控制的标签**）

```
<meta name=``"viewport"` `content=``"width=device-width, initial-scale=1.0"``>
```

- width：控制 viewport 的大小，可以指定的一个值，如 600，或者特殊的值，如 device-width 为设备的宽度（单位为缩放为 100% 时的 CSS 的像素）。
- height：和 width 相对应，指定高度。
- initial-scale：初始缩放比例，也即是当页面第一次 load 的时候缩放比例。
- maximum-scale：允许用户缩放到的最大比例。
- minimum-scale：允许用户缩放到的最小比例。
- user-scalable：用户是否可以手动缩放。

## 当窗口上下滚动时，能始终固定在视野顶端的是（div的直接父级元素是<body>）：

```
<div style=”position:fixed;top:0;”></div>
```

![img](https://uploadfiles.nowcoder.com/images/20170227/1657851_1488186318141_F7A9735109BDB2CFC3A63F76B0374318)

## 在 HTML 音频/视频 DOM 中，_____设置是否在页面加载后载入视频 ？

**preload 属性设置或返回是否在页面加载后立即加载音频/视频。 autoplay 属性设置或返回音视频是否在加载后即开始播放。 buffered 属性返回用户已缓冲音视频的时间范围。 controller 属性返回音视频的当前媒体控制器。**

![image-20210808215426960](C:\Users\HSDN\AppData\Roaming\Typora\typora-user-images\image-20210808215426960.png)

## 想要让<a></a>标签不进行跳转的方法：

![img](https://uploadfiles.nowcoder.com/images/20181221/153679231_1545386663154_68128F3DC3E4B58550ECBE2234C9C6C4)

## 在做一份调查报告时，要求将问题文类，同一表单内的数据在一组显示，并表明此类型的名称，如何将相同类型的表单进行分组？

![img](https://uploadfiles.nowcoder.com/images/20200220/956413803_1582172767959_09BB34A601252C50DBBCCA3FF147B81F)

## 块级元素 与 行内元素：

**1.块级元素**

![img](https://uploadfiles.nowcoder.com/images/20160731/213669_1469934373582_04341C4C965D57F74167CCE72D2EAF7B)

**2.行内元素**

![img](https://uploadfiles.nowcoder.com/images/20160731/213669_1469934384802_F3CB514AAFC503A1BCD00D1B81F87ED1)

**3.块级元素与行内元素的区别**

（1）块级元素会独占一行，其宽度自动填满其父元素宽度；

行内元素不会独占一行，相邻的行内元素会排列在同一行，直至一行排不下才会换行，其宽度随元素的内容而变化。

（2）块级元素可以包含行内元素和块级元素；行内元素不能包含块级元素。

（3）行内元素设置width、height、margin-top、margin-bottom、padding-top、padding-bottom无效。

**4.** **块级元素与行内元素的转换**

display:inline-block;

display:inline;

display:block;

**5.可变元素**

![img](https://uploadfiles.nowcoder.com/images/20160731/213669_1469934417678_1857554C0F0C54914B8DA215A3BD971D)