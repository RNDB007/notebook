# HTML与CSS

标签可以嵌套![image-20220125164456422](https://s2.loli.net/2022/01/25/6PrMNmK3xROLsQV.png)

## 段落和换行

### 段落标签		

```html
<p> </p>  //paragraph
```

常用属性：

- align——对齐方式

### 换行标签

```html
<br/>
```

 ## 列表

### 无序列表

```html
<ul>   列表标签   unordered list
	<li></li>  列表项标签
    <li></li>  列表项标签
<ul>
```

常用属性：

- type——列表图标，有(square、circle、disc)

效果图：

![image-20220124184338258](https://s2.loli.net/2022/01/24/f6IZWbHMmB9r5sJ.png)

### 有序列表

```html
<ol>   列表标签   ordered list
	<li></li>  列表项标签
    <li></li>  列表项标签
<ol>
```

常用属性：

- type——列表图标，有(1、a、A、i、I)

效果图：

![image-20220124203943399](https://s2.loli.net/2022/01/24/vYNeM9dIqnzRpKc.png)

## div

division的简称，常和CSS一起用

块级元素，宽度占整个屏幕，标签会自动换行。

常用于布局

<font color="red">块级元素占据其父元素（容器）的整个水平空间，垂直空间等于其内容高度，因此创建了一个“块”。通常浏览器会在块级元素前后另起一个新行</font>

常用属性：

- align——div元素中内容的对齐方式

![image-20220125150800264](https://s2.loli.net/2022/01/25/rMfGItoCRjs9PYB.png)

<font color="blue">            div和p标签有什么区别？</font>

div标签之间没有空隙，p标签之间存在空隙。他们的宽度都是屏幕宽度，而span标签是内容的宽度。

![image-20220125155549901](https://s2.loli.net/2022/01/25/dbzGcNl81FjrpQH.png)

## span

与div一样，后期和CSS一起用，才会有更好的效果呈现。

## 格式化标签

所谓格式化，就是对字体进行的处理。

### font

用于设置字体相关属性（typora也可以用）

常用属性：

color——字体颜色

size——字体大小

face——字体风格 

### pre

定义预格式化的文本——保留空格、换行符（所见即所得）

### b/strong

粗体

### i

斜体

### u

下划线

### del

中划线

 ### sub

下标

### sup 

上标

## 超链接a标签

该标签用于从一个页面链接到另外一个页面。

常用属性：

- href——定义跳转地址，可以定义相对路径、绝对路径、网络路径，默认值是当前地址。a标签必须包含该属性，不然就是普通的文本。

  href可以指向a标签的name属性值和其他标签的id属性值，来实现跳转,<font color='red'>记得前面有#号</font>

- target——设置窗口打开方式

> ​			_self   当前窗口打开（默认）
>
> ​			_blank 新开空白窗口打开
>
> ​			_parent
>
> ​			_top

name——用于本页面内的跳转

## img标签

img元素向网页中嵌入一幅图像，不会自动换行

img标签外面套一个a标签，就可以实现点击图片跳转

常用属性：

src——必要属性，指出图片的地址（本地图片和网络资源均可）

title——当鼠标悬停在图片上时显示的元素 

alt——当图片加载失败时显示的文本

align——对齐方式

## 表格标签

```html
<table> </table> 表示表格
<tr> </tr> 表示表格中的行
<td> </td> 表示表格中的标准单元格
<th> </th> 表示表格中的表头单元格
```

tr中包含的是表格的一行。

tr中包含th或td。

table常用属性：

border——表格的边框

width——表格的宽度

align——表格的对齐方式（表格对齐，和内容无关）

style——CSS样式
