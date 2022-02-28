# 尚硅谷入门视频教程

## 33 第一个java程序

1. 源代码文件为.java文件，经过javac.exe会编译成字节码文件。（javac 文件名，来进行编译）
2. 字节码文件再经过java.exe会变成可执行文件（文件名为源代码中写的类名 ），并运行。（java 类名，来运行）

## 37 文档注释

文档注释是java特有的，具体格式为：

```java
/**
@auther 111
@version v1.0
*/
```

注释内容可以JDK提供的工具javadoc所解析，生成一套以网页文件形式体现的该程序的说明文档。 

javadoc解析的类必须是public类型的。

具体命令行应该怎么用javadoc，可以看https://www.bilibili.com/video/BV1Kb411W75N?p=37&spm_id_from=pageDriver

## 40 第一个java程序总结

1. 一个源文件可以声明多个class，但只能有一个类声明为public class。且声明为public的类必须与文件名同名才可以。
2. System.out.Println()中的ln是line的意思，这个方法会输出后换行。
3. 编译后会生成一个或多个字节码文件，字节码文件的文件名与源文件中的类名相同。源文件中有几个class，就会生成几个字节码文件。

## 45 java命名规范

+ 包名：多单词组成时，所有字母都小写。
+ 类名、接口名：大驼峰
+ 变量名、方法名：小驼峰
+ 常量名：所有字母大写，单词之间用_隔开。

## 47 变量的注意点

+ Java中的每个变量的作用域在一对{}内。只有在作用域内才有效。

+ 声明long型常量，必须以l或L结尾。没带l会被当成int型常量，编译会通过。

```java
	long a=12345676544322l;
	long b=12235346456436L;
```

+ 声明float常量，后面必须加f或F。
+ boolean变量的值就是true或者false，（C里面可以用1、0，java不行）。

+ byte、short、char互相做运算时，会自动转化为int。
+ 变量的强制转换和C一模一样。

+ String是引用数据类型，不是基本数据库类型！
+ String和8中基本数据类型变量可以做计算，结果为Srting类型。

## 137 java如何查看某个类的源码

按住ctrl，再点击该类即可。方法ctrl+o即可查找。

## 139 数组

### 初始化

```java
int[] a=new int[5]; //动态初始化
int[] b=new int[]{1,2,3,4,5} //静态初始化
```

### 143 java的一维数组的内存结构

![image-20220224220030817](https://s2.loli.net/2022/02/24/gRu1ANl7CimJW2z.png)

+ String存放在<font color='red'>常量池</font>。

+ static存放在静态域。

+ 方法区包括常量池和静态域。

+ 放在方法中的变量都是局部变量。数组名存放在栈中，数组内容存放在堆中！（数组名其实就是堆空间中的首地址，相当于是一个指针）。
+ 只要有new关键字，就在堆中重新开辟了空间。   

### 二维数组初始化

```java
int[][] a=new int[5][]; //动态初始化
```

列可以写可以不写！！行则必须写！！！列的长度可以每个行都不同！！！

<font color='red'>如果写列，则在堆中开辟对应的空间，不写则为null，直到后面new了之后，才会有值</font>

### 二维数组内存结构

![image-20220225202601322](https://s2.loli.net/2022/02/25/1rBLS3X2G9Me6nw.png)

array2=array1，改变array2，也会改变array1.看内存结构很轻易的可以知道这个结论。

### 操作数组的工具类

Arrays。<font color='red'>单词后面加个s，一般就是操作该单词的工具类</font>

+ Arrays

![image-20220225211128526](https://s2.loli.net/2022/02/25/g7xnlsiSe1fYzCy.png)
## 面向对象

内存解析：

+ 引用类型的变量，只可能存储两类值，null或地址值（含变量的类型）

### 197 JVM内存结构

![image-20220228100459068](https://s2.loli.net/2022/02/28/5mdWVZqsYK7ST6f.png)new出来的结构存放在堆空间中。类的对象的属性（非static)也加载在堆空间中。

方法区：存放类的加载信息，常量池，静态域。
