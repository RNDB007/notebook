# HTML与CSS

<font size='7' color='blue'>关键是随用随查</font>

## HTML

标签可以嵌套![image-20220125164456422](https://s2.loli.net/2022/01/25/6PrMNmK3xROLsQV.png)

### 段落和换行

#### 段落标签		

```html
<p> </p>  //paragraph
```

常用属性：

- align——对齐方式

#### 换行标签

```html
<br/>
```

 ### 列表

#### 无序列表

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

#### 有序列表

```html
<ol>   列表标签   ordered list
	<li></li>  列表项标签
    <li></li>  列表项标签
<ol>
```

常用属性：

- type——列表图标，有(1、a、A、i、I)

效果图：

![image-20220124203943399]()

### div

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

### span

与div一样，后期和CSS一起用，才会有更好的效果呈现。

### 格式化标签

所谓格式化，就是对字体进行的处理。

#### font

用于设置字体相关属性（typora也可以用）

常用属性：

color——字体颜色

size——字体大小

face——字体风格 

#### pre

定义预格式化的文本——保留空格、换行符（所见即所得）

#### b/strong

粗体

#### i

斜体

#### u

下划线

#### del

中划线

 #### sub

下标

#### sup 

上标

### 超链接a标签

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

### img标签

img元素向网页中嵌入一幅图像，不会自动换行

img标签外面套一个a标签，就可以实现点击图片跳转

常用属性：

src——必要属性，指出图片的地址（本地图片和网络资源均可）

title——当鼠标悬停在图片上时显示的元素 

alt——当图片加载失败时显示的文本

align——对齐方式

### 表格标签

```html
<table> </table> 表示表格
<tr> </tr> 表示表格中的行
<td> </td> 表示表格中的标准单元格
<th> </th> 表示表格中的表头单元格
```

tr中包含的是表格的一行。

tr中包含th或td。

table常用属性：

- border——表格的边框
- width——表格的宽度
- align——表格的对齐方式（表格对齐，和内容无关）
- style——CSS样式

td、th的常用属性

- rowspan——纵向合并，数值为合并的行数

- colspan——横向合并

### 表单（form）标签

用于向服务器传送数据。其他的丢了，不写了。

### input标签

是一个表单元素。如果需要提交，那么必须放到表单元素当中去。

常用属性

- type 元素的类型
   - text 文本框
  - password 密码框
  - radio 单选框（需要通过name属性来设置为一组，同组name相同）
  - checkbox 复选框
  - file 上传文件框（form要上传文件，需要设置一个enctype=”multiparty/form-data“属性，提交方式为post请求）
  - hidden 隐藏域
  - button 普通按钮
  - submit 提交按钮 
  - reset 重置按钮
  - date 日期框
  
- value 元素的值

- readonly 只读状态

### textarea和label标签

textarea是定义可输入多行文本的控件。

label用于元素聚焦。  有一个for属性，当for属性值与元素的id值相同时，点击文字会聚焦到相应的元素当中去。 

### button标签

html5新出的。注意与input标签的type中的属性相区别。button是双标签，标签之间可以添加内容（文本或标签等）

### select标签

与option标签结合，形成下拉框。

select常用属性：

- multiple： 设置下拉框可多选

- size ：设置下拉框可见选项数（出现上下滚动条）

- disabled：禁用该元素

select常用属性：

- selected——默认选中项

- disabled——禁用某个选项

- value——提交给服务器的选项值（如果没有设置value值，则提交option双标签中的文本值）

### 字符实体与标签分类

字符实体是为了打出来一些被语法占用的字符，如<\>等等

具体的自己百度查吧，此处不再手打，太浪费时间了。

标签分类：块级元素、行内元素、行内块状元素

## CSS

CSS指的是层叠样式表（Cascading Style Sheets），字面意思就是样式可以叠加。CSS负责美化页面。虽然HTML的某些属性可以设置样式效果，但细节处理不够好。且HTML实现样式效果回出现大量重复代码，且维护困难。

CSS最新版本是CSS3，能够做到网页和内容分离，对网页中的元素的位置排版等效果进行像素级的控制。

CSS需要依赖HTML。

### CSS的基本语法

```CSS
选择器{ 
    属性：属性值；
    属性：属性值；
    ......
    ......
}
```

 CSS语句有行内式、嵌入式（在head标签中嵌入style标签）、引入外联样式文件。（这里写了好多，但电脑又bug了，全部没保存，想看的时候去https://www.bilibili.com/video/BV1DL411H7SV?p=22 看吧）

### CSS的基本选择器

- 通用选择器：*， 选择所有元素  

- 元素选择器/标签选择器，其选择器写要选择的标签即可.
- id选择器：对元素指定id，选择器写#id即可。<font color='red'>注意id之前要加#</font>

- 类选择器： 对某一类元素指定class，对某一class进行指定。选择器写.class即可 <font color='red'>注意class之前要加.</font>

- 分组选择器：选择器填入多个即可。

```css
选择器1，选择器2，选择器3.....{
    属性：属性值；
    ......
    ......
}
```

#### 选择器的优先级

1. id选择器  权重值100
2. 类选择器  权重值10
3. 元素选择器  权重值1
4. 通用选择器  没有权重

行内样式，即写在标签属性当中的style属性，权重最高，为1000。

### CSS的组合选择器

- 后代选择器：选择指定元素的所有后代元素（以空格分隔）

<font color='red'>其实就是先指定一个元素，其所有被夹在这个元素中间的元素，都是这个元素的后代</font>

```css
<style>
	指定元素 指定元素{
		属性名：属性值；
        ......
        ......
}
</style>
```



- 子代选择器：选择指定元素的第一个后代元素（以>分隔）

```CSS
<style>
	指定元素>指定元素{
		属性名：属性值；
        ......
        ......
}
</style>
```



- 相邻兄弟选择器：选择指定元素相邻的下一个指定元素（只会向下找一个）（以+分隔）
- 普通兄弟选择器：选择指定元素后的指定同级元素（向下找多个）（以~分隔）

### CSS常用属性

#### 背景

![image-20220208171434878](https://s2.loli.net/2022/02/10/SHD8zFuQxLqIYNh.png)

#### 文本

a标签去除文本下划线

```css
a{
    text-decoration:none;
}
```

具体的有，设置下划线、中划线、上划线、首行缩进等等，具体看https://www.bilibili.com/video/BV1DL411H7SV?p=26吧。

#### 字体

注意点：

1. 当font-family的属性值包含空格或特殊字符时，需要将font-family的属性值用引号括起来
2. font-family有“后备”机制，可以为元素设置多种字体。当浏览器不识别第一种字体时，自动使用下一种字体。

![image-20220210171904566](https://s2.loli.net/2022/02/10/Jn9wUDXN6lQ78zZ.png)

还有font-size、font-style和font-weight。font-size设置字体大小，font-style设置字体风格，font-weight设置字体的粗细，具体用到再查。

#### 对齐方式

设置元素中字体的水平方向的对齐方式

#### display属性

规定元素生成框的类型，有：

- block：元素会被显示，且元素会变成块级元素，元素前后会有换行符
- none：元素会被隐藏
- inline：元素会显示为行内元素，元素前后没有换行符 
- inline-block：行内块级元素

| 块级元素     | 可以设置元素的宽高和边距，元素会自动换行     |
| ------------ | -------------------------------------------- |
| 行内元素     | 不可以设置元素的宽高和边距，元素不会自动换行 |
| 行内块级元素 | 可以设置元素的宽高和边距，元素不会自动换行   |

#### 浮动

属性名为float。属性值有none、left、right

1. 只有横向浮动，没有纵向浮动
2. 会将元素的display属性变更为block
3. 浮动元素的后一个元素会围绕着浮动元素（典型运用是文字围绕图片）
4. 浮动元素的前一个元素不会受到任何影响（如果要让两个块状元素并排显示，必须让两个块状元素都应用float）

### 盒子模型

border、padding、margin三个属性构成了盒子模型。

padding：内容与边框的距离

border：边框

margin：边框与外部空白的距离

#### 边框

边框有宽度、样式（实心空心等等）、颜色等属性。

```CSS
选择器名{
    border: 宽度 颜色 类型;
    border:2px #0000FF dotted;
}
```

也可以分开来设置

```css
选择器名{
    border-style:dotted  //上右下左顺序，可以依次设置
    border-width:2px;     //上右下左顺序，可以依次设置
    border-color:#0000FF;
}
```

设置一个属性，表示边框四边效果一致；

设置两个属性，表示上下一致，左右一致；

设置三个属性，表示上右下不一致，左右一致。 

#### padding（内边距）

内容与边框的距离。

```CSS
选择器名{
    padding：10px 20px 30px 40px;  //也遵循上右下左原则，同boarding
}
```

padding也可以用padding-left、padding-right、padding-top、padding-bottom来单独设置。
#### margin

设置一个元素的所有外边距的宽度，或者设置各边上外边距的宽度。

其所有设置与padding完全相同，名字改一下就行。
