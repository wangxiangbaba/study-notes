JAVA

## JAVA语言的特点

# idea快捷键

ctrl+p选择构造器![image-20201205184609672](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201205184609672.png)

alt+enter创建对象

ctrl+alt+t 选择代码环绕

![image-20201205184703595](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201205184703595.png)

alt+insert创建构造器和get set方法等等

![image-20201205184734119](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201205184734119.png)

### 1.面向对象

两个基本概念：类、对象。

三大特性：封装、继承、多态。

### 2.健壮性

吸收了C/C++语言的优点，但去掉了其影响程序健壮性的部分（如指针、内存的申请与释放等），提供了一个相对安全的内存管理和访问机制。

### 3.跨平台性

通过java语言编写的应用程序在不同的系统平台上都可以运行，只需要在运行java程序的操作系统上，先安装一个java虚拟机(JVM)即可，在JVM中运行。

## JAVA两种核心机制

### 1.java虚拟机JVM

#### 定义

JVM是一个虚拟的计算机，具有指令集并使用不同的存储区域。负责执行指令、管理数据、内存、寄存器。

#### 特点

1.对于不同平台，有着不同的虚拟机。

2.只有某平台提供了对应的java虚拟机，Java程序才可以在此平台运行。

3.java虚拟机机制屏蔽了底层运行平台的差别，实现了“一次编译，到处运行”。

![img](file:///D:\WeGame\Download\1392070089\Image\C2C\LQO8R29[}K0{P{4YQW2C1~Y.png)

### 2.垃圾收集机制

不再使用的内存空间应回收——垃圾回收。

在C/C++等语言中，由程序员负责回收无用内存。

java语言消除了程序员回收无用内存空间的责任，它提供了一种系统级线程跟踪存储空间的分配情况，并在JVM空闲时，检查并释放那些可以被释放的存储空间。

垃圾回收在java程序运行过程中自动进行，程序员无法精确控制和干预。

Java程序还会出现内存泄漏和内存溢出问题吗？会的！

## JDK、JRE、JVM三者关系

![img](file:///D:\WeGame\Download\1392070089\Image\C2C\Image1\`FFSVKWFGVLCBI52MNT8YWN.png)

## JAVA编程代码中是严格区分大小写的

## JAVA的编译

.java文件（源文件）经过javac.exe的编译后成为.class文件（字节码文件）然后用java.exe运行字节码文件得出结果。---需要注意的是用javac.exe编译的.java文件生成的.class文件的名字是.java文件中代码声明的类的名字。如果.java文件中存在着多个类名，就会编译出多个类名的.class文件。

在cmd环境下运行编译java文件的时候  在用javac编译文件的时候  javac+文件名.java   文件名是不用区分大小写的   应为微软系统环境下不区分大小写  而在平常的java编程中   java是严格区分大小写的  但是java命令和后缀名必须小写

![image-20201013162748101](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201013162748101.png)

下面两种情况为   大小写如果运行失败的话  说明安装了classpath环境变量   没有classpath环境变量的话   可以直接不区分大小写运行.class文件   在classpath路径下去找文件  需要区分大小写   没有classpath环境变量的话  直接在当前目录下寻找.class文件 不用区分大小写

![image-20201013163440471](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201013163440471.png)

![image-20201013163452591](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201013163452591.png)



## JAVA代码的注释

注释的内容不参与编译   也就是说.class文件中不包含注释信息  只能在.java中看到

### 1.单行注释   

//   +内容

### 2.多行注释  

 /*    +内容     */

多行注释不可嵌套使用

### 3.文档注释  

 				/**

​						@auther  指定java程序的作者

​						@version 指定源文件的版本

​					*/

文档注释的内容可以被JDK提供的工具javadoc所解析，生成一套以网页文件形式体现的该程序的说明文档。需要代码运行 代码范式如下  javadoc -d 文件夹名(英文) -author -version xx.java

## API

全程Application Programming Interface应用程序编程接口，是java提供的基本编程接口

Java语言技工了大量的基础类，因此Oracle也为这些基础类提供了相应的API文档，用于告诉开发者如何使用这些类，以及这些类里包含的方法。

下载地址：http://www.oracle.com/technetwork/java/javase/downloads/index.html

## public

在一个java源文件中可以声明多个class。但是，只能最多一个类声明为public。且声明的类必须 和源文件同名

## main()

程序的入口是main()方法。格式是固定的

格式为：public static void main(String[] args) { }

其中args为arguments参数   是可以替换的  比如a，b 

中括号可以放在参数后面例如public static void main(String args[] ) { }

## 输出语句

System.out.println();这个输出语句后会换行  先输出后换行

System.out.print.();这个输出语句后不换行





## 每日习题

### daiy1

1.JDK,JRE,JVM三者之间的关系，以及JDK，JRE包含的主要结构有哪些？

JDK=JRE+Java的开发工具(例如：javac.exe,java.exe,javadoc.exe)

JRE=JVM+Java核心类库

2.为什么要配置path变量？如何配置？

因为我们要在任何文件路径下都可以执行java开发工具。

找到path环境变量，建立JAVA_HOME变量=bin的上一层目录

path=%JAVA_HOME%\bin

3.常用的几个命令行操作有哪些（至少四个）

cd  md rd del cd.. cd/

4.创建如下的类，是的运行的话可以输出：

![image-20201014114740951](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201014114740951.png)

class testday1 
{
	public static void main(String[] args) 
	{
		System.out.println("姓名：习大大");
		System.out.println("");
		S xystem.out.println("性别:男");
		System.out.print("家庭住址：北京市中南海");
	}
}

class testday1 
{
	public static void main(String[] args) 
	{
		System.out.println("姓名：习大大\n");
		System.out.println("性别:男");
		System.out.print("家庭住址：北京市中南海");
	}
}

![image-20201014115508734](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201014115508734.png)

5.编译和运行上述代码的指令

编译javac day1.java

运行java testday1

## JAVA基本语法（上）

### 1.关键字和保留字

#### 关键字

##### 定义

被java语言赋予了特殊含义，用作专门用途的字符串（单词）

##### 特点

关键字中所有的字母都为小写

![image-20201014120957392](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201014120957392.png)

true   false   null



#### 保留字

###### 定义

现有的java版本尚未使用，但以后版本可能会作为关键字使用，自己命名标识符时要避免使用这些保留字。

goto  const



### 2.标识符文

#### 定义

java对各种变量、方法和类等要素命名时使用的字符序列成为标识符

tips:凡是自己可以起名字的地方都叫标识符，比如类名  变量名  方法名  接口名  包名。。。

#### 定义合法标识符规则

<u>不遵循以下规则，则编译不通过。</u>

1.由26个英文字母大小写，0~9，_或$组成

2.数字不可以开头

3.不可以使用关键字和保留字，但能包含关键字和保留字

4.java中严格区分大小写，长度无限制

5.标识符不能包含空格

#### java中的名称命名规范

包名：多单词组成时所有的字母都小写：xxxyyyzzz

类名、接口名：多单词组成时，所有单词的首字母大写：XxxYyyZzz

变量名、方法名：多单词组成石，第一个单词首字母小写，第二个单词开始每个单词首字母大学：xxxYyyZyy

常量名：所有字母都大写，多单词是每个单词用下划线链接：XXX_YYY_ZZZ

tips1：在起名字是，为了提高阅读性，要尽量有意义，“见名知意”

tips2：java采用unicode字符集，因此标识符也可以使用汉字声明，但是不建议使用



### 3.变量

#### 变量的概念

内存中的一个存储区域

该区域的数据可以在同一类型范围内不断变化

变量是程序中最基本的存储单元。包含变量类型、变量名和存储的值

#### 变量的作用

用于在内存中保存数据

#### 使用变量注意

java中的每个变量都必须先声明，后使用

使用变量名来访问这块区域的数据

变量的作用域：其定义所一对{}内

变量只有在其作用域内才有效

同一个作用域内，不能定义重名的变量

#### tips

变量需要先声明赋值，然后才能使用

不赋值会编译错误 提示没有初始化变量

变量都定义在其作用域内。在作用域内，它是有效的，出了作用域他就失效了。

同一个作用域内，不可以声明两个同名的变量

声明long型变量，必须用 "l" 或者 "L"结尾

声明float型变量，必须用 "f" 或者 "F"结尾

通常定义整型变量时，使用int型

通常定义浮点变量时，使用double型，因为范围更大，精度更高，而且可以省略末尾字母对比float

变量不能重名，不能重复定义

#### JAVA定义的数据类型

##### 按照数据类型分类

![image-20201029174458897](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201029174458897.png)

8种基本数据类型：byte,short,int,long,float,double,char,boolean

3种引用数据类型：class,interface,array[ ]

![image-20201029180015448](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201029180015448.png)

整型：byte(1字节=8bit)，short(2字节)，in(4字节)，long8(字节)

![image-20201030153612444](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201030153612444.png)

浮点类型:float,double 

 

字符型:char(1字符=2字节)

定义char型变量，通常使用一对 ' '单引号，内部只能写一个字符

表示方式:1.声明一个字符   2.转义字符 :\n换行符，\t制表符(空一格)等等   3.直接使用Unicode值来表示字符型常量

char c1 = 'a';

布尔型:true,false

常常在条件判断或者循环结构中使用

##### 按照变量在类中声明的位置分类

![image-20201029175752230](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201029175752230.png)

###### 成员变量

###### 局部变量

#### 基本数据类型转换

这里讨论的只是7种类=基本数据类型变量间的运算，不包含boolean类型的 

![image-20201103213824416](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201103213824416.png)

##### 1.自动类型提升

结论： long的容量）

![image-20201104144304058](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201104144304058.png)

特别的：当byte,char,short三种类型的变量做运算时，结果为int

java在做运算时，如果操作数均在int范围内，那么一律在int的空间内运算

##### 2.强制类型转换

#### 强制类型转换

![image-20201103213856614](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201103213856614.png)

1.需要使用强转符：()，括号内为数据类型

2.强制类型转换，可能导致精度损失

![image-20201105144821436](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201105144821436.png)

整型常量，默认类类型为 int型

浮点型常量，默认类型为double型

![image-20201104151215926](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201104151215926.png)

#### 字符串类型：String

![image-20201104151500668](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201104151500668.png)

String属于引用数据类型，翻译为：字符串

声明String类型变量时，使用一对" "

String可以和8种基本数据类型变量做运算，且运算只能是连接运算：+

String和其他8中数据类型做运算时，运算的结果仍然是String类型

```java
String isHandsome=scan.next();

ishandsome.equals("是")
```

引用equals函数可以判断输入端输入的汉字是否对对应函数内的字符 从而判断true或者false

对于char型的获取，Scanner没有提供相关方法，只能获取一个字符串

```java
String gender=scan.next();
char genderChar=gender.charAt(2);
System.out.println(genderChar);
```

char 使用这种方法可以获取特定的字符串中单个位置的字符从0开始对应

#### java在cmd中编译出现GBK不可映射字符解决方法

javac  -encoding UTF-8  ××.java 

#### 进制之间的转换

![image-20201104175308657](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201104175308657.png)

计算机底层都以补码方式才存储数据

#### 习题

![image-20201104165457091](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201104165457091.png)



## 运算符

### 算数运算符 

![image-20201105143926888](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201105143926888.png)

取余运算

取余运算结果的符号与被取余数相同

开发中经常使用%来判断能否被除尽的情况

自增1不会改变变量本身的数据类型

byte b1=127;

b1++;

此时输出的b1为-128

01111111  +  1  =  11111111；二进制模式上其已经转换为负数的-128了



### 赋值运算符 

![image-20201105160919043](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201105160919043.png)

### 比较运算符（关系运算符） 

![image-20201105181556660](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201105181556660.png)

### 逻辑运算符 

![image-20201105182852385](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201105182852385.png)

逻辑运算符操作的都是boolean类型的变量



区分& 与 &&

相同点1：&和&&的运算结果相同

相同点2：当符号左边是true时，二者都会执行符号右边的运算

不同点：当符号左边是false时，&继续执行符号右边的运算，&&不再执行符号右边的运算。

开发中推荐使用&&



区分| 与 ||

相同点1：运算结果都相同

相同点2：当符号左边是false时，二者都会执行符号右边的运算

不同点：放符号左边时true时，|继续执行符号右边的运算，而||不再执行符号右边的运算 

开发中推荐使用||

### 位运算符  

![image-20201106145350240](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201106145350240.png)

位运算操作的都是整型的数据

<<：在一定范围内，每向左移一位，相当于*2

右移符：在一定范围内，每向右移一位，相当于/2

左移右移 正负数均可

![image-20201106152107741](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201106152107741.png)

![image-20201106152638327](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201106152638327.png)

### 三元运算符

![image-20201106155826571](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201106155826571.png)

三元运算符可以嵌套使用

凡是可以使用三元运算符的地方，都可以改写为if-else

 但是能用if-else的地方，不一定都能用三元运算符

三元较于if-else更加简洁

```java
int c=(a=b)?a:b;
```



### 运算优先级

![image-20201106163233995](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201106163233995.png)

想优先运算直接加()

## 程序流程控制

![image-20201106164830489](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201106164830489.png)

### 分支结构

#### if-else(条件判断结构)

![image-20201106164905395](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201106164905395.png)

if(){}

if(){}else{}

if(){}else if(){}else if(){}...else{} 

如果if-else结构中的执行语句只有一行时，对应的{}可以省略，但是不建议省略

#### switch-case

![image-20201107182239601](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201107182239601.png)

switch结构中的表达式，只能是如下的6种数据类型之一：byte,short,char,int,枚举类型（JDK5.0新增）,String(JDK7.0新增)

 case后面只能声明常量，不能声明范围 数字,单个字符，字符串均可（字符格式 'a'，字符串格式"abc"）

break关键字是可选的

default相当于if-else结构中的else，default结构是可选的，而且位置是灵活的

如果switc-case中的多个case执行语句相同，则可以考虑合并

#### 开发中分支结构的选择

1.凡是可以使用switch-case的结构，都可以转换为if-else，反之不成立

2.当我们写分支结构时，当发现既可以使用switch-case的同时又可以使用（同时,switch-case中case表达式的取值情况不太多）if-else时，可以优先选择switch-case（switch-case执行效率稍微高点）

### Scanner的使用

如何从键盘获取不同类型的变量：需要使用Scanner类

具体实现步骤： 

1.导包：import java.util.Scanner;

2.Scanner的实例化：Scanner scan=new Scanner(System.in);

3.对于char型的获取，Scanner没有提供相关方法，只能获取一个字符串

```java
String gender=scan.next();
char genderChar=gender.charAt(2);
System.out.println(genderChar);
```

char 使用这种方法可以获取特定的字符串中单个位置的字符从0开始对应

tips:需要根据对应的数据类型，来输入指定类型的值。如果输入的数据类型与要求的类型不匹配时，会报异常:InputMIsMatchException导致程序终止

### 如何获取随机数

Math.random()获取的随机数范围为[0.0,1.0)

Math.random返回的是double数据类型

公式：[a,b]   a,b为int类型

( int) ( Math.random()*( b-a+1 ) )+a

### 循环结构

在某些条件满足的情况下，反复执行特定代码的功能

![image-20201109140150346](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201109140150346.png)

循环结构的四个组成部分

1.初始化条件

2.循环条件（是boolean类型）

3.循环体

4.迭代

一旦在循环中执行到break，就跳出循环

#### for循环

```java
for(1初始化条件;2循环条件（是boolean类型）;4迭代条件){
	3循环体
}
```

1-2-3-4-2-3-4- - - - - - 2

for中初始换条件只在for中有效，出了for中就无效了

开发中使用for和while中更多一些，较少使用do-while

#### while循环

```java
1初始化条件;
while(2循环条件){
	3循环体;
	4.迭代;
}
```

while循环千万小心不能丢了迭代条件，一旦丢了，就可能导致死循环  我们写程序的过程中要避免死循环

while中的i出了循环以后，仍可以调用，因为i是在while外面的定义的

for循环和while循环时可以相互转换的

区别：for循环和while循环的初始化条件部分的作用范围不停

注意：1.不在循环条件部分限制次数的结构：for(;;)或者while(true)

2.结束循环有两种方式

方式一：循环条件部分返回false

方式二：在循环体中，执行break

#### do-while循环

```java
1.初始化条件
do{
	3循环体;
	4.迭代;
}while(2循环条件);
```

执行过程：1-3-4-2-3-4-2--------2

do-while循环至少会执行一次循环体

#### 嵌套循环使用

1.将一个循环结构A声明在另一个循环结构B的循环体中，就构成了嵌套循环

2.外层循环：循环结构B

   内层循环：循环结构A

3.说明

1.内层循环遍历一遍，只相当于外层循环循环体执行了一次

2.假设外层循环需要执行m次，内层循环需要执行n次，此时内层循环的循环体一共执行了m*n次

#### 特殊关键字的使用break,continue

关键字的后面不能声明语句

##### break

swith-case循环结构中使用	结束当前循环

##### coninue

循环结构中皆可使用	结束当次循环

```java
label:for(int i=1;i<=4;i++){
    for(int j=1;j<=10;j++){
        if(j%4==0){
            //break;//默认跳出包裹此关键字最近的循环
            //continue;//默认跳出包裹此关键字最近的循环
            //break label;//结束指定标识的一层循环结构
            continue label;//结束指定标识label的一层循环结构
        }
        System.out.print(j);
    }
    System.out.println();
}
```



#### 特殊流程控制语句return

![image-20201109190908646](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201109190908646.png)

### 课后习题



循环结构是如何最后退出循环的，有哪些不同的情况说明

1.循环条件返回false

2.在循环结构内，一旦执行到break，跳出循环

## 数组

数组（array），十多个相同类型数据按一定顺序排列的集合，并使用一个名字命名，并通过编号的方式对这些数据进行统一管理

数组的概念：数组名，下标（或者索引），元素，数组的长度

数组的特点：数组是有序排列的

数组属于引用数据类型的变量，数组的元素既可以是基本数据类型，也可以是引用数据类型（String等）

创建数组对象会在内存中开辟一整块的连续的空间，而数组名中引用的是这块连续空间的首地址

数字长度一旦确定，就不能修改

我们可以直接通过下标或者索引的方式调用指定位置的元素，速度很快

### 一维数组

![image-20201110221959049](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201110221959049.png)

![image-20201110222404770](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201110222404770.png)

一维数组静态初始化：数组的初始化和数组元素的赋值操作同时进行

```java
int[] names = new int[]{1,2,3};
int names[] = new int[]{1,2,3};
```

一维数组动态初始化：数组的初始化和数组元素的赋值操作分开进行

```java
int[]   ids;
ids =   new int[]{1001,1002,1003,1004};
```

错误数组写法

```java
int[] arr=new int[];
int[5] arr=new int[5];
int[] arr=new int[3]{1,2,3};
```

### 组的分类

按照维度：一维数组，二维数组，三维数组（多维数组）。。。。

按照元素的数据类型分：基本数据类型元素的数组，引用数据类型的数组（即对象数组 ）

### 通过角标的方式调用使用数组的指定位置元素

数组的角标索引从0开始，到数组的长度减1结束

### 数组元素的默认初始化值

数组元素是整型：初始化值为0

浮点型：初始值为0.0

char型：0或者'\u0000'  不是'0'

布尔型boolean：初始值为false

引用数据类型：null

### 数组的内存解析



### 二维数组

静态初始化：

```java
int[][] arr=new int[][]{{1,2,3},{4,5},{6,7,8}};
int[] arr[]=new int[][]{{1,2,3},{4,5},{6,7,8}};
```

动态初始化1：

```java
String[][] arr=new String[3][2];
```

 动态初始化2：

```java
String[][] arr=new String[3][];
```

规定：二维数组分为外层数组的元素，内层数组的元素

```java
int[] arr=new int[4][3];
```

外层元素：

```
arr[1],arr[1]
```

内层元素：

```
arr[0][1],arr[1][2]
```

#### 二维数组元素的初始化值

针对于初始化方式一：

```java
int[][] arr = new int[4][3];
```

外层元素的初始化值为：地址值

内层元素的初始化值为：与一维数组初始化值相同

针对于初始化方式二：

```java
int[][] arr = new int[4][];
```

外层元素的初始化值为：null

内层元素的初始化值为：不能调用，否则就会报错 控指针异常

### 数组中设计到的常见算法

#### 1.数组元素的赋值（杨辉三角，回形数等）

##### 杨辉三角

```java
public class 杨辉三角 {
    public static void main(String[] args) {
        // write your code here;
        int[][] yanghui = new int[10][];
        for(int i=0;i< yanghui.length;i++){
            yanghui[i] = new int[i+1];
            yanghui[i][0]=1;
            yanghui[i][i]=1;
                for(int j=1;j<yanghui[i].length-1;j++){
                    yanghui[i][j]=yanghui[i-1][j-1]+yanghui[i-1][j];
                }
        }
        for(int i=0;i< yanghui.length;i++){
            for(int j=0;j< yanghui[i].length;j++){
                System.out.print(yanghui[i][j] + " ");
            }
            System.out.println();
        }
    }
```

##### 回形数

```java
Scanner getnum = new Scanner(System.in);
System.out.println("请输入一个数：");
int size = getnum.nextInt();
int start = 0;                                       //起始点坐标
int end = size-1;                              //终止点坐标
int values = 1;                                      //每个元素的值
int arr[][] = new int [size][size];                       //创建二维数组
while(true) {                                                     //循环打印
    for(int i = start;i <= end;i++) {
        arr[start][i] = values;
        values++;
    }                    //打印第一行


    for(int i = start + 1; i<= end;i++) {
        arr[i][end] = values;
        values++;
    }                      //打印最后一列


    for(int i = end - 1;i >= start;i--) {
        arr[end][i] = values;
        values++;
    }                 //打印最后一行

    for(int i = end - 1; i >= start + 1;i--) {
        arr[i][start] = values;
        values++;     //打印第一列
    }

    start++;
    end--;

    if(start >= end) {
        break;                          //当起始点坐标和终止点坐标相等时跳出
    }
}


//奇数回形数
if(size % 2 != 0) {                              //输入的数为偶数是可以直接打印，当输入的数为奇数是，为最中间的数赋值
    arr[end][start] = values;
}



for(int i = 0;i < arr.length ;i++) {                       //遍历输出
    for(int j = 0; j < arr[i].length ;j++) {
        System.out.print(arr[i][j] + "\t");
    }
    System.out.println();
}
```

#### 2.求数值型数组中元素的最大值，最小值，平均数，总和等

```java
int[] arr=new int[10];
        int maxValue=arr[0];
        int minValue=arr[0];
        int sum=0;
        for(int i=0;i< arr.length;i++){
            arr[i]=(int)(Math.random()*90)+10;
            System.out.print(arr[i]+"\t");
            if(maxValue<arr[i]){
                maxValue=arr[i];
            }
            if(minValue>arr[i]){
                minValue=arr[i];
            }
            sum+=arr[i];
        }
        double average=(double)(sum)/10;
        System.out.println();
        System.out.println("最大值为："+maxValue);
        System.out.println("最小值为："+minValue);
        System.out.println("总和为为："+sum);
        System.out.println("平均数为为："+average);
```

#### 3.数组的复制，反转，查找（线性查找，二分法查找）

##### 数组的复制

```java
int[] arr1,arr2;
arr1=new int[]{2,3,5,7,11,13,17,19};
for(int i=0;i< arr1.length;i++) {
    System.out.print(arr1[i]+"\t");
}
arr2=arr1;/**不能称作数组的赋值*/
/**arr1和arr2是什么关系*/
/**arr1和arr2地址值相同，都指向了堆空间的唯一的一个数组实体*/
for(int i=0;i<arr2.length;i++){
    if(i%2==0){
        arr2[i]=i;
    }
}
System.out.println();
for(int i=0;i< arr1.length;i++) {
    System.out.print(arr1[i]+"\t");
}
```

```java
int[] arr1,arr3;
arr1=new int[]{2,3,5,7,11,13,17,19};
for(int i=0;i< arr1.length;i++) {
    System.out.print(arr1[i]+"\t");
}
arr3=new int[arr1.length];
System.out.println();
for(int i=0;i< arr3.length;i++){
    arr3[i]=arr1[i];
    System.out.print(arr3[i]+"\t");
}/**数组的复制*/
```

##### 数组的反转

```java
String[] arr=new String[]{"JJ","DD","MM","BB","GG","AA"};
String[] arr1=new String[arr.length];
for(int i=0;i< arr.length;i++) {
    System.out.print(arr[i]+"\t");
}
for(int i=0;i< arr.length/2;i++){
        String temp = arr[i];
        arr[i] = arr[arr.length - i - 1];
        arr[arr.length - i - 1] = temp;
}
System.out.println();
for(int i=0;i< arr.length;i++) {
    System.out.print(arr[i]+"\t");
}
```



##### 数组的线性查找

```java
String[] arr = new String[]{"JJ", "DD", "MM", "BB", "GG", "AA"};
String[] arr1 = new String[arr.length];
String dest = "BB";
boolean isFlag = true;
for (int i = 0; i < arr.length; i++) {
    if (dest.equals(arr[i])) {
        System.out.println("找到了指定的元素:"+dest+"\n位置为" + i);
        isFlag = false;
        break;
    }
}
if (isFlag) {
    System.out.println("很遗憾没有找到");
}
```

##### 数组的二分法查找

前提：所要查找的数组必须有序

```java
    int[] arr2=new int[]{-98,-34,2,34,54,66,79,105,210,333};
    int dest=-34;
    int head=0;
    int end=arr2.length-1;
    boolean isFlag=true;
    while(head<=end){
        int middle=(head+end)/2;
        if(dest== arr2[middle]){
            System.out.println("找到了指定的元素"+dest+"\n位置为"+middle);
            isFlag=false;
            break;
        }else if(arr2[middle]>dest){
            end=middle-1;
        }else{
            head=middle+1;
        }
    }
    if(isFlag){
        System.out.println("很抱歉没有找到");
    }
```

#### 4.数组元素的排序算法 

##### 内部排序

整个排序过程不需要借助于外部存储器（如磁盘等），所有排序操作都在内存中完成

##### 外部排序

参与排序的数据非常多，数据量非常大，计算机无法把整个排序过程放在内存中完成，必须借助于外部存储器（如磁盘）。外部排序最常见的是多路归并排序，可以认为外部排序是由多次内部排序组成

##### 十大内部排序算法

选择排序（直接选择排序，堆排序）	交换排序（冒泡排序，快速排序）	插入排序（直接插入排序，折半插入排序，Shell排序）	归并排序	桶式排序	基数排序

![image-20201111204008055](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201111204008055.png)

![image-20201113155430303](file://C:/Users/13920/AppData/Roaming/Typora/typora-user-images/image-20201113155430303.png?lastModify=1605254279)

![image-20201113155512836](file://C:/Users/13920/AppData/Roaming/Typora/typora-user-images/image-20201113155512836.png?lastModify=1605254279)

![image-20201113165043275](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201113165043275.png)

###### 冒泡排序

![image-20201111205116250](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201111205116250.png)

```java
int[] arr=new int[]{43,45,855,1615,4,-21,-2,-55,-555};
for(int i=0;i< arr.length;i++){
    System.out.print(arr[i]+" ");
}
for(int i=0;i< arr.length-1;i++){
    boolean isFlag=false;//标记元素是否产生交换
    for(int j=0;j< arr.length-1-i;j++){
        if(arr[j]>arr[j+1]){
            int temp=arr[j];
            arr[j]=arr[j+1];
            arr[j+1]=temp;
            isFlag=true;
        }
    }
    if(isFlag){//元素没有产生交换 说明已经排序完成 结束循环
        break;
    }
}
System.out.println();
for(int i=0;i< arr.length;i++){
    System.out.print(arr[i]+" ");
}
```

###### 快速排序

![image-20201113151415356](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201113151415356.png)

```java
public static void quickSort(int[] arr,int low,int high){
    int i,j,temp,t;
    if(low>high){
        return;
    }
    i=low;
    j=high;
    //temp就是基准位
    temp = arr[low];

    while (i<j) {
        //先看右边，依次往左递减
        while (temp<=arr[j]&&i<j) {
            j--;
        }
        //再看左边，依次往右递增
        while (temp>=arr[i]&&i<j) {
            i++;
        }
        //如果满足条件则交换
        if (i<j) {
            t = arr[j];
            arr[j] = arr[i];
            arr[i] = t;
        }

    }
    //最后将基准为与i和j相等位置的数字交换
    arr[low] = arr[i];
    arr[i] = temp;
    //递归调用左半数组
    quickSort(arr, low, j-1);
    //递归调用右半数组
    quickSort(arr, j+1, high);
}


public static void main(String[] args){
    int[] arr = {10,7,2,4,7,62,3,4,2,1,8,9,19};
    quickSort(arr, 0, arr.length-1);
    for (int i = 0; i < arr.length; i++) {
        System.out.print(arr[i]+" ");
    }
}
```

###### 堆排序

堆的两个特点（缺一不可）：1.是一颗完全二叉树	2.父节点永远大于子节点

```java
public static void heapSort(int[] arr) {
    if (arr == null || arr.length <= 1) return;
    // 建堆。
    buildHeap(arr);
    int len = arr.length;
    while (len > 1) {
        // 把堆顶和最后一个元素交换。
        swap(arr, 0, len - 1);
        // 交换完之后，逻辑上去掉最后一个元素。
        len--;
        // 重新调整堆的顺序。
        heapfy(arr, 0 , len);

        // 把每一趟排序的结果也输出一下。
        print(arr);
    }
}

private static void buildHeap(int[] arr) {
    // 最后一个非叶子结点：2i + 1 >= arr.length  -->  i >= (arr.length - 1) / 2
    for (int i = (arr.length - 1) / 2 - 1; i >= 0; i--) {
        heapfy(arr, i, arr.length);
    }
}

// 调整堆的顺序，保持大顶堆。
private static void heapfy(int[] arr, int i, int len) {
    while (true) {
        int maxPostion = i;
        int leftChild = 2 * i + 1;  // 左孩子索引。
        int rightChild = 2 * i + 2; // 右孩子索引。

        // 若左孩子大于最大值，则更新最大值。
        if (leftChild < len && arr[leftChild] > arr[maxPostion]) {
            maxPostion = leftChild;
        }

        // 若右孩子大于最大值，则更新最大值。
        if (rightChild < len && arr[rightChild] > arr[maxPostion]) {
            maxPostion = rightChild;
        }

        if (maxPostion == i) {
            break;  // 若已经是大顶堆了，则退出循环。
        } else {
            swap(arr, i, maxPostion);   // 若不是大顶堆，则交换位置。
            i = maxPostion;
        }
    }
}

private static void swap(int[] arr, int i, int j) {
    int temp = arr[i];
    arr[i] = arr[j];
    arr[j] =temp;
}

public static void main(String[] args) {
    int[] arr = {6, 9, 1, 4, 5, 8, 7, 0, 2, 3};

    System.out.print("排序前:  ");
    print(arr);

    heapSort(arr);

    System.out.print("排序后:  ");
    print(arr);
}

// 打印数组
public static void print(int[] arr) {
    if (arr == null)    return;

    for(int i : arr) {
        System.out.print(i + " ");
    }
    System.out.println();
}
```

###### 归并排序

```java
public static void main(String[] args) {
    int[] arr = {11,44,23,67,88,65,34,48,9,12};
    int[] tmp = new int[arr.length];    //新建一个临时数组存放
    mergeSort(arr,0,arr.length-1,tmp);
    for(int i=0;i<arr.length;i++){
        System.out.print(arr[i]+" ");
    }
}

public static void merge(int[] arr,int low,int mid,int high,int[] tmp){
    int i = 0;
    int j = low,k = mid+1;  //左边序列和右边序列起始索引
    while(j <= mid && k <= high){
        if(arr[j] < arr[k]){
            tmp[i++] = arr[j++];
        }else{
            tmp[i++] = arr[k++];
        }
    }
    //若左边序列还有剩余，则将其全部拷贝进tmp[]中
    while(j <= mid){
        tmp[i++] = arr[j++];
    }

    while(k <= high){
        tmp[i++] = arr[k++];
    }

    for(int t=0;t<i;t++){
        arr[low+t] = tmp[t];
    }
}

public static void mergeSort(int[] arr,int low,int high,int[] tmp){
    if(low<high){
        int mid = (low+high)/2;
        mergeSort(arr,low,mid,tmp); //对左边序列进行归并排序
        mergeSort(arr,mid+1,high,tmp);  //对右边序列进行归并排序
        merge(arr,low,mid,high,tmp);    //合并两个有序序列
    }
}
```

### Arrays工具类的使用

![image-20201113165357641](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201113165357641.png)

### 数组使用中的常见异常

#### 数组角标越界的异常

ArrayIndexOutOfBoundsExcetion

#### 空指针异常

NullPointerException

## java方法

### 什么是方法

![image-20201116165205535](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201116165205535.png)

### 方法的定义及调用

![image-20201116172910995](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201116172910995.png)

![image-20201116173320946](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201116173320946.png)

![image-20201116174736782](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201116174736782.png)

### 方法重载

![image-20201116175338589](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201116175338589.png)

### 命令行传参

![image-20201116180249608](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201116180249608.png)

### 可变参数

![image-20201116181406540](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201116181406540.png)

### 递归

![image-20201116191350733](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201116191350733.png)

## 面向对象(上)

java面向对象学习的三条主线

1.java类及类的成员：属性，方法，构造器，代码块，内部类

2.面向对象的三大特征：封装性，继承性，多态性，（抽象性）

3.其他关键字：this，super，static，final，abstract，interface，package，import

![image-20201113183131068](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201113183131068.png)

![image-20201113183705500](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201113183705500.png)

![image-20201113184926322](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201113184926322.png)

![image-20201113185915878](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201113185915878.png)

![image-20201113190708091](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201113190708091.png)

### 类

#### 1.设计类，就是设计类的对象

属性=成员变量=field=域，字段

方法=成员方法=函数=method

创建类的对象=类的实例化=实例化类

![image-20201113191233944](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201113191233944.png)

![image-20201113191704055](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201113191704055.png)

#### 2.类和对象的使用（面向对象思想落地的实现）

1.创建类，设计类的成员

2.创建类的对象

3.通过“对象.属性”或者“对象.方法”调用对象的结构  

## 面向对象

### 初识面向对象

![image-20201120162317885](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201120162317885.png)

### 方法回顾和加深

![image-20201117163610107](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201117163610107.png)

引用传递：一般是传递一个对象，本质还是值传递

### 对象的创建分析

![image-20201120162618995](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201120162618995.png)

一个类中只有属性和方法

一个类即使是什么都不写，他也会存在一个方法、在class文件中自动生成构造器

构造器作用：1.使用new关键字，必须要有构造器，本质是在调用构造器 2.用来初始化值

注意：一旦定义有参构造，无参构造就必须显示定义，也就是定义一个空的无参构造

![image-20201120171921099](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201120171921099.png)

static和类一起在静态方法区中加载 

![image-20201120192638753](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201120192638753.png)

### 面向对象三大特性

封装继承多态

![image-20201120195537976](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201120195537976.png)

#### 封装

1.提高程序的安全性，保护数据

2.隐藏代码的实现细节

3.统一接口

4.提供系统的可维护性

#### 继承

![image-20201122144844188](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201122144844188.png)

子类继承了父类，就会拥有父类的全部方法

 继承优先级：public 	protected	default	private

在java中，所有的类都默认直接或者间接继承object类

一个子类只能有一个父类，一个父类可以有多个子类

私有的可以被继承，但是无法访问

![image-20201122154347371](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201122154347371.png)

子类默认调用了父类的无参构造，且代码必须在第一行

##### super注意点

1.super调用父类的构造方法，必须在构造方法的第一个

2.super必须只能出现在子类的方法或者构造方法中

3.super和this不能同时调用构造方法

super与this的区别

代表对象的不同：

​	this：本身调用者这个对象

​	super：代表父类对象的引用

​	this：没有继承也可以使用

​	super：只能在继承条件下才能使用

构造方法的区别

​	this();本类的构造

​	super();父类的构造

##### 方法重写

重写需要有继承关系，子类重写父类的方法

1.方法名必须相同

2.参数列表必须相同

3.修饰符：范围可以扩大，不能缩小	public>protected>default>private

4.抛出的异常:范围可以扩大缩小，不能扩大	public>protected>default>private

子类的方法和父类需要一致，方法体不同

非静态方法重写

重写都是方法的重写，与属性无关

为什么要重写？

1.父类的功能，子类不一定需要，或者不一定满足

ideal快捷键	alt+insert：override重写

#### 多态

![image-20201122161415892](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201122161415892.png)

instanceof	类型转换（引用类型之间的转换）

```java
一个对象的实际类型是确定的，可以指向的引用类型就不确定了
Student s1=new Student();

Person  s2=new Student();父类的引用指向子类
    Student能调用的方法都是自己的或者父类的
    Person父类型可以指向子类，但是不能调用子类独有的方法

```

new对象能执行哪些方法，主要看对象左边的类型，和右边关系不大

多态注意事项

1.多态是方法的多态：属性没有多态

2.父类和子类，有联系	类型不同的话 就会出现类型转换异常！ClassCastException

3.存在的条件：继承关系，方法要重写，父类的引用指向子类对象father f1=new Son();

无法重写的方法

1.static方法属于类，不属于实例

2.final常量  存在于常量池

3.private方法

##### instanceof

instanceof	类型转换（引用类型之间的转换），判断一个对象是什么类型

X instanceof Y	 XY存在父子关系 ，编译就通过，X指向的对象与Y存在父子关系也可以

类型之间的转换

![image-20201122171224205](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201122171224205.png)

1.子类转换成父类，可能丢失自己的一些方法

2.子类转换成为父类：向上转型  直接转

3.父子转换为子类：需要强制转换	((Student)studen).go();

4.方便方法的调用，减少重复的代码，有效提高利用率

##### static

![image-20201124162650303](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124162650303.png)

![image-20201124162843026](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124162843026.png)

类被final修饰后 就无法被继承

### 抽象类和接口

##### 抽象类

![image-20201124163300480](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124163300480.png)

![image-20201124163454349](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124163454349.png)

![image-20201124163553274](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124163553274.png)

加入子类也是abstract  那么就是孙子类实现方法

extends类是单继承	但是接口可以多继承

不能new抽象类，只能靠子类去实现他

抽象类中可以写普通方法

抽象方法必须在抽象类中

抽象类作用：提高开发效率，可扩展性

##### 接口

![image-20201124164509466](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124164509466.png)

接口中的所有定义其实都是抽象的public abstract

![image-20201124165010193](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124165010193.png)

![image-20201124165847286](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124165847286.png)

接口都需要有实现类

实现了接口的类，必须要在类中重写接口中的方法

利用接口实现多继承  一个类可以连接多个接口

接口的作用：

1.约束

2.定义一些方法，让不同的人实现

3.方法都是public abstract修饰的

4.定义的数值常量字符都是public static final修饰的

5.接口不能被实例化	因为接口中没有构造方法

6.implements可以实现多个接口

7.必须要重写接口中的方法

### 内部类及OOP实战

![image-20201124170356494](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124170356494.png)

一个java类中可以有多个class类，但是只能有一个public class类

#### 成员内部类

内部类可以获得外部类的私有属性，私有方法

#### 静态内部类

![image-20201124171929299](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124171929299.png)

#### 局部内部类

![image-20201124172021732](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124172021732.png)

#### 匿名内部类

![image-20201124172157414](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124172157414.png)

## Error和Exception

### 什么是异常

![image-20201124172909900](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124172909900.png)

### 异常体系结构

![image-20201124173653296](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124173653296.png)

![image-20201124173923892](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124173923892.png)

![image-20201124174330689](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124174330689.png)

![image-20201124174605912](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124174605912.png)

### java异常处理机制

![image-20201124175104717](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124175104717.png)

### 处理异常

![image-20201124175537189](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124175537189.png)

可以不要finally代码块

ctrl+alt+T  可以自动生成一些嵌套循环代码

![image-20201124180850139](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124180850139.png)

### 自定义异常



### 总结



## 捕获的抛出异常

主动抛出异常，一般在方法中使用	假设在此方法中处理不了这个异常，就在方法上抛出异常

## 自定义异常及经验小结

![image-20201124183345941](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124183345941.png)

![image-20201124184910840](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201124184910840.png)



## 多线程

### 基本概念：程序，进程，线程

![image-20201201193012972](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201201193012972.png)

![image-20201202194347975](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201202194347975.png)

![image-20201202195259763](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201202195259763.png)

![image-20201202195929296](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201202195929296.png)

### 线程的创建和使用

```java
class MyThread extends Thread{

    @Override
    public void run() {
        for (int i = 0; i < 100; i++) {
            if(i%2==0){
                System.out.println(i);
            }
        }
    }
}
public class ThreadTest {
    public static void main(String[] args) {
//        创建子类的对象
        MyThread t1 = new MyThread();
//        通过此对象调用start():1.启动当前线程   2.调用当前线程的run()
        t1.start();
    }
}
```

要想创建多个线程，必须创建多个对象

![image-20201203154359256](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201203154359256.png)

![image-20201203154442180](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201203154442180.png)

![image-20201203163610843](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201203163610843.png)

![image-20201203164702575](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201203164702575.png)

```java
测试Thread的常用方法
* 1.strat():启动当前线程，调用当前线程的run()方法
* 2.run():通常需要重写Thread类中的此方法，将创建的线程要执行的操作声明在此方法中
* 3.currentThread():静态方法，返回当前代码的线程
* 4.getName():获取当前线程的名字
* 5.setName():设置当前线程的名字
* 6.yield():释放当前cpu的执行权，cpu被哪个线程抢到是随机的
* 7.join():在线程a中调用线程b中的join()方法，此时线程a就进入阻塞状态，
* 直到线程b完全执行完以后，线程a才结束阻塞状态
* 8.stop():已过时。当执行此方法时，强制结束当前线程
* 9.sleep(long millitime):让当前线程睡眠指定millitime毫秒，
* 在指定的millitime毫秒内，当前线程时阻塞状态
* 10.isAlive():判断当前线程是否存活
*
* 线程的优先级
* 1.MAX_PRIORITY:10
* 2.MIN_PRIORITY:1
* 3.NORM_PRIORITY:5  默认优先级
*
* 如何获取和设置当前线程的优先级：
* getPriority():获取优先级
* setPriority(int x):设置优先级
* 高优先级的线程要抢占低优先级的cpu执行权，但是只是从概率上讲，高优先级的线程高概率被
* 执行并不意味着只有当高优先级的线程执行完后，低优先级才执行
*
*/
```

### 创建多线程的两种方式

1.继承Thread类

```java
/**
 * @author wangxiang
 * @create 2020-12-02-20:12
 * 多线程的创建
 * 方式一：继承于Thread类
 * 1.创建一个继承于Thread类的子类
 * 2.重写Thread类的run()-->此线程执行的操作声明在run()中
 * 3.创建Thread类的子类的对象
 * 4.通过此对象调用start()
 * 例子：遍历100以内的所有的偶数
 */
class MyThread extends Thread{

    @Override
    public void run() {
        for (int i = 0; i < 100; i++) {
            if(i%2==0){
                System.out.println(i);
            }
        }
    }
}
public class ThreadTest {
    public static void main(String[] args) {
//        创建子类的对象
        MyThread t1 = new MyThread();
//        通过此对象调用start():1.启动当前线程   2.调用当前线程的run()
        t1.start();
    }
}
```

2.Runnable接口

```java
/**
 * @author wangxiang
 * @create 2020-12-03-19:54
 * 例子：创建三个窗口卖票，总票数为100张  使用Runnable方法
 */
class windiow1 implements Runnable{
    private int ticket=100;
    @Override
    public void run() {
        while(true){
            if(ticket>0){
                System.out.println(Thread.currentThread().getName()+":卖票，票号为："+ticket);
                ticket--;
            }else {
                break;
            }
        }
    }
}
public class WindowsTestRunnable {
    public static void main(String[] args) {
        windiow1 w1 = new windiow1();
        Thread t1 = new Thread(w1);
        Thread t2 = new Thread(w1);
        Thread t3 = new Thread(w1);
        t1.setName("线程1：");
        t2.setName("线程2：");
        t3.setName("线程3：");
        t1.start();
        t2.start();
        t3.start();
    }
}
```

#### 比较创建线程的两种方式

开发中，优先选择：实现Runnable接口的方式

原因：1.实现的方式没有类的单继承的局限性

​           2.实现的方法更适合来处理多个线程有共享数据的情况

两者之间的联系：Thread类本身也实现了Runnable接口

两种方式都需要重写run()方法，将线程要执行的逻辑声明在run()中

### 线程的生命周期

![image-20201203201510945](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201203201510945.png)

![image-20201203203335839](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201203203335839.png)

### 线程的同步

```java
package com.company;

/**
 * @author wangxiang
 * @create 2020-12-03-19:54
 * 例子：创建三个窗口卖票，总票数为100张  使用Runnable方法
 *
 * 问题1：卖票过程中出现了重票，错票--》出现了线程的安全问题
 *
 * 问题出现的原因：当某个线程操作车票的过程中，
 * 尚未操作完成时，其他线程参与进来，也来操作车票
 *
 * 如何解决？    当一个线程在操作ticket的时候，其他线程不能参与进来，直到
 * 线程a操作完的时候，其他线程才开始操作ticket，这种情况即使线程a出现了阻塞，
 * 也不能被改变
 *
 * 在java中，我们通过同步机制，来解决线程的安全问题
 *
 * 方法一：同步代码块
 * 关键字：synchronized(同步监视器){
 *      //需要被同步的代码
 * }
 *说明：操作共享数据的代码，就是需要被同步的代码
 *  共享数据：多个线程共同操作的变量，比如：ticket就是共享数据1
 *  同步监视器：俗称：锁  任何一个类的对象都可以来充当锁
 *  要求：多个线程必须要公用同一把锁🔒
 *  补充：在实现Runnable接口创建多线程的方式中，我们可以考虑使用this充当同步监视器
 *  在继承Thread类创建多线程的方式中，慎用this充当同步监视器，
 *  可以考虑使用当前类充当同步监视器  XX.class
 *
 *
 *
 * 方法二：同步方法如果操作共享数据的代码完整的声明在一个方法中，我们不妨将此方法
 * 声明同步的
 *
 * 关于同步方法的总结：
 *      1.同步方法仍然涉及到同步监视器，只是不需要我们显式的声明
 *      2.非静态的同步方法，同步监视器是this
 *      3.静态的同步方法，同步监视器是当前类本身
 *
 *
 *
 * 同步的方式：解决了线程的安全问题，但是操作同步代码时，
 * 只能有一个线程参与，其他线程等待，相当于是一个单线程的过程，效率低
 */
class Window1 implements Runnable{
    private int ticket=100;
    @Override
    public void run() {
        while(true){
            synchronized(Window1.class) {//对象唯一就可用this指向当前唯一对象w1或者  Window1.class
                if (ticket > 0) {
                    try {
                        Thread.sleep(100);
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                    System.out.println(Thread.currentThread().getName() + ":卖票，票号为：" + ticket);
                    ticket--;
                } else {
                    break;
                }
            }
        }
    }
}
public class WindowsTestRunnable {
    public static void main(String[] args) {
        Window1 w1 = new Window1();
        Thread t1 = new Thread(w1);
        Thread t2 = new Thread(w1);
        Thread t3 = new Thread(w1);
        t1.setName("线程1：");
        t2.setName("线程2：");
        t3.setName("线程3：");
        t1.start();
        t2.start();
        t3.start();
    }
}
```

```java
package com.company;

/**
 * @author wangxiang
 * @create 2020-12-03-19:24
 * 例子：创建三个窗口卖票，总票数为100张
 */

class window extends Thread{
    private static  int ticket=100;
    private static Object obj=new Object();
    @Override
    public void run() {
        while(true) {
            synchronized (window.class) {//可用obj或者window.class
                if (ticket > 0) {
                    try {
                        Thread.sleep(100);
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                    System.out.println(Thread.currentThread().getName() + ":卖票，票号为：" + ticket);
                    ticket--;
                } else {
                    break;
                }
            }
        }
    }
}
public class WindowsTest {
    public static void main(String[] args) {
        window w1 = new window();
        window w2 = new window();
        window w3 = new window();
        w1.setName("窗口1");
        w2.setName("窗口2");
        w3.setName("窗口3");
        w1.start();
        w3.start();
        w2.start();

    }
}
```

```java
package com.atguigu.java;

/**
 * @author wangxiang
 * @create 2020-12-05-16:48
 * <p>
 * 使用同步方法来实现Runnable接口的线程安全问题
 */
class Window2 implements Runnable {
    private int ticket = 100;

    @Override
    public synchronized void run() {
        while (true) {
        show();
        }
    }
    private synchronized void show(){//同步监视器就是this默认this
        if (ticket > 0) {
            try {
                Thread.sleep(100);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
            System.out.println(Thread.currentThread().getName() + ":卖票，票号为：" + ticket);
            ticket--;
        }
    }
}

public class WindowTest2 {
    public static void main(String[] args) {
        Window2 w2 = new Window2();
        Thread t1 = new Thread(w2);
        Thread t2 = new Thread(w2);
        Thread t3 = new Thread(w2);
        t1.setName("线程1：");
        t2.setName("线程2：");
        t3.setName("线程3：");
        t1.start();
        t2.start();
        t3.start();
    }
}
```



```java
package com.atguigu.java;

/**
 * @author wangxiang
 * @create 2020-12-05-17:04
 *
 * 使用同步方法处理继承Thread类的方式中的线程安全问题
 */
class window extends Thread{
    private static int ticket=100;
    @Override
    public void run() {
        while(true){
            show();
        }
    }
    private static synchronized void show(){//同步监视器：window.class
        if(ticket>0){
            try {
                Thread.sleep(100);
            } catch (Inte rruptedException e) {
                e.printStackTrace();
            }
            System.out.println(Thread.currentThread().getName()+":卖票，票号为："+ticket);
            ticket--;
        }
    }
}

public class WindowTest3 {
    public static void main(String[] args) {
        window w1 = new window();
        window w2 = new window();
        window w3 = new window();
        w1.setName("窗口1");
        w2.setName("窗口2");
        w3.setName("窗口3");
        w1.start();
        w3.start();
        w2.start();
    }
}
```

```java
package com.atguigu.java;
手写单例模式
/**
 * @author wangxiang
 * @create 2020-12-05-17:36
 * <p>
 * 使用同步机制将单例模式中的懒汉式改写为线程安全的
 */
public class BankTest {

}

class Bank {//懒汉式

    private Bank() {
    }

    private static Bank instance = null;

    private static Bank getInstance() {
        if (instance == null) {
            instance = new Bank();
        }
        return instance;
    }
}

class Bank1 {//懒汉式+锁

    private Bank1() {
    }

    private static Bank1 instance = null;

    private static synchronized Bank1 getInstance() {
        if (instance == null) {
            instance = new Bank1();
        }
        return instance;
    }
}

class Bank2 {//懒汉式+锁效率高

    private Bank2() {
    }

    private static Bank2 instance = null;

    private static Bank2 getInstance() {

        //效率稍差
//        synchronized (Bank2.class) {
//            if (instance == null) {
//                instance = new Bank2();
//            }
//            return instance;
//        }
//        方式二效率较高
        if (instance == null) {
            synchronized (Bank2.class) {
                if (instance == null) {
                    instance = new Bank2();
                }
            }
        }
        return instance;
    }
}
```



### ![image-20201205182733135](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201205182733135.png)

```java
package com.atguigu.java;

import java.util.concurrent.locks.ReentrantLock;

/**
 * @author wangxiang
 * @create 2020-12-03-19:24
 *
 * 解决线程安全问题的方式三：Lock锁--》JDK5.0新增
 */

class wiodow implements Runnable{
    private int ticket=100;
    //第一步实例化ReentrantLock
    private ReentrantLock lock=new ReentrantLock();//ctrl+p选择构造器

    @Override
    public void run() {
        while(true){
            try {
                //第二部调用锁定lock方法
                lock.lock();
                if (ticket > 0) {
                    try {
                        Thread.sleep(100);
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                    System.out.println(Thread.currentThread().getName() + ":卖票，票号为：" + ticket);
                    ticket--;
                } else {
                    break;
                }
            }finally {
                //第三步调用解锁unlock()的方法
                lock.unlock();
            }
        }
    }
}

public class WindowsTest {
    public static void main(String[] args) {
        wiodow w = new wiodow();
        Thread w1 = new Thread(w);
        Thread w2 = new Thread(w);
        Thread w3 = new Thread(w);
        w1.setName("窗口1");
        w2.setName("窗口2");
        w3.setName("窗口3");
        w1.start();
        w3.start();
        w2.start();

    }
}
```

### 多线程面试题

synchronized与lock的异同

相同：二者都可以解决线程安全问题

不同：synchronized机制属于在执行完相应的同步代码以后，自动的释放同步监视器

lock需要手动的启动同步（lock()），同时结束同步也需要手动的实现(unlock())



如何解决线程安全问题？有几种方式

三种：1.synchronized同步代码块	2.synchronized同步方法	3.Lock锁方法



sleep()和wait()方法的异同？

相同点：一旦执行方法，都可以使得当前的线程进入阻塞状态

不同点：1.两个方法声明的位置不哦那个：Thread类中声明sleep()，Object类中声明wait()

​				2.调用的范围不同：sleep()可以在任何需要的场景下调用，wait() 必须使用在同步代码块或者同步方法中

​				3.关于是否释放同步监视器：如果两个方法都是使用在同步代码块或者同步方法中，sleep()不会释放锁同步监视器，wait()会释放锁

![image-20201207193101954](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201207193101954.png)

```java
package com.atguigu.java;

/**

 * @author wangxiang

 * @create 2020-12-07-19:34
   */
   class Clerk{
   private int productCount=0;

   public synchronized void produceProduct() {//生产产品
       if(productCount<20){
           productCount++;
           System.out.println(Thread.currentThread().getName()+":开始生产第"+productCount+"个产品");
           notify();
       }else {
   //            大于20等待
           try {
               wait();
           } catch (InterruptedException e) {
               e.printStackTrace();
           }
       }
   }

   public synchronized void consumeProduct() {//消费产品
       if(productCount>0){
           System.out.println(Thread.currentThread().getName()+":开始消费第"+productCount+"个产品");
           productCount--;
           notify();
       }else {
   //            小于0等待
           try {
               wait();
           } catch (InterruptedException e) {
               e.printStackTrace();
           }
       }
   }
   }

class Producer extends  Thread{//生产者
    private Clerk clerk;

    public Producer(Clerk clerk) {
        this.clerk = clerk;
    }
    
    @Override
    public void run() {
        System.out.println(Thread.currentThread().getName()+"：开始生产产品");
        while (true){
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
    
            clerk.produceProduct();
        }
    }

}

class Consumer extends Thread{
    private Clerk clerk;

    public Consumer(Clerk clerk) {
        this.clerk = clerk;
    }
    
    @Override
    public void run() {
        System.out.println(Thread.currentThread().getName()+"：开始消费产品");
        while (true){
            try {
                Thread.sleep(2000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
    
            clerk.consumeProduct();
        }
    }

}

public class ProductTest {
    public static void main(String[] args) {
        Clerk clerk=new Clerk();

        Producer p1 = new Producer(clerk);
        p1.setName("生产者1");
    
        Consumer c1 = new Consumer(clerk);
        c1.setName("消费者1");
        Consumer c2 = new Consumer(clerk);
        c2.setName("消费者2");
    
        p1.start();
        c1.start();
        c2.start();
    
    }

}




```



![image-20201205185757906](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201205185757906.png)

### 线程的死锁问题

![image-20201205175759033](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201205175759033.png)

```java
package com.atguigu.java;

/**
 * @author wangxiang
 * @create 2020-12-05-18:02
 *
 * 演示线程的死锁问题
 *
 * 我们使用同步时，要避免出现死锁
 *
 */
public class Deadlock {
    public static void main(String[] args) {
        StringBuffer s1 = new StringBuffer();
        StringBuffer s2 = new StringBuffer();
        new Thread() {
            @Override
            public void run() {
                synchronized (s1) {
                    s1.append("a");
                    s2.append("1");
                    try {
                        Thread.sleep(100);
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                    synchronized (s2) {
                        s1.append("b");
                        s2.append("2");
                        System.out.println(s1);
                        System.out.println(s2);
                    }
                }

            }
        }.start();
        new Thread(new Runnable() {
            @Override
            public void run() {
                synchronized (s2) {
                    s1.append("c");
                    s2.append("3");
                    try {
                        Thread.sleep(100);
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                    synchronized (s1) {
                        s1.append("d");
                        s2.append("4");
                        System.out.println(s1);
                        System.out.println(s2);
                    }
                }
            }
        }).start();
    }
}
```

### 线程的通信

![image-20201205175759033](file://C:/Users/13920/AppData/Roaming/Typora/typora-user-images/image-20201205175759033.png?lastModify=1607341220)

```java
package com.atguigu.java;

/**
 * @author wangxiang
 * @create 2020-12-07-19:34
 */
class Clerk{
    private int productCount=0;

    public synchronized void produceProduct() {//生产产品
        if(productCount<20){
            productCount++;
            System.out.println(Thread.currentThread().getName()+":开始生产第"+productCount+"个产品");
            notify();
        }else {
//            大于20等待
            try {
                wait();
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }

    public synchronized void consumeProduct() {//消费产品
        if(productCount>0){
            System.out.println(Thread.currentThread().getName()+":开始消费第"+productCount+"个产品");
            productCount--;
            notify();
        }else {
//            小于0等待
            try {
                wait();
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}

class Producer extends  Thread{//生产者
    private Clerk clerk;

    public Producer(Clerk clerk) {
        this.clerk = clerk;
    }

    @Override
    public void run() {
        System.out.println(Thread.currentThread().getName()+"：开始生产产品");
        while (true){
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }

            clerk.produceProduct();
        }
    }
}

class Consumer extends Thread{
    private Clerk clerk;

    public Consumer(Clerk clerk) {
        this.clerk = clerk;
    }

    @Override
    public void run() {
        System.out.println(Thread.currentThread().getName()+"：开始消费产品");
        while (true){
            try {
                Thread.sleep(2000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }

            clerk.consumeProduct();
        }
    }
}

public class ProductTest {
    public static void main(String[] args) {
        Clerk clerk=new Clerk();

        Producer p1 = new Producer(clerk);
        p1.setName("生产者1");

        Consumer c1 = new Consumer(clerk);
        c1.setName("消费者1");
        Consumer c2 = new Consumer(clerk);
        c2.setName("消费者2");

        p1.start();
        c1.start();
        c2.start();

    }
}
```

### JKD5.0新增线程创建方式	

![image-20201207201541855](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201207201541855.png)

![image-20201207202906528](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201207202906528.png)

```java
package com.atguigu.java;

import java.util.concurrent.Callable;
import java.util.concurrent.ExecutionException;
import java.util.concurrent.FutureTask;

/**
 * @author wangxiang
 * @create 2020-12-07-20:21
 * 创建线程方法三：实现Callable接口--JDK5.0新增
 */

/**步骤1：创建一个Callable的实现类*/
class NumThread implements Callable{
    /**步骤2：实现call方法，将此线程需要执行的操作声明在call()*/
    @Override
    public Object call() throws Exception {
        int sum=0;
        for (int i = 0; i <= 100; i++) {
            if(i%2==0){
                System.out.println(i);
                sum+=i;
            }
        }
        return sum;
    }
}

public  class CallableTest {
    public static void main(String[] args) {
        /**步骤3：创建Callable接口实现类的对象*/
        NumThread numThread=new NumThread();
        /**步骤4：将此Callable接口实现的对象numThread作为参数传递到FutureTask()构造器当中，去创建FutureTask的对象*/
        FutureTask futureTask=new  FutureTask(numThread);
        /**步骤5：将FutureTask的对象作为参数传递到Thread类的构造器当中，创建Thread对象，并调用statr()方法*/
        new Thread(futureTask).start();

        try {
            /**步骤6：获取Callable中的call方法的返回值，需要返回值就操作此步骤，不需要在call()方法中return null;*/
// get()返回值即为FutureTask构造器参数Callable实现类重写的call()的返回值
            Object sum = futureTask.get();
            System.out.println("总和为："+sum);
        } catch (InterruptedException e) {
            e.printStackTrace();
        } catch (ExecutionException e) {
            e.printStackTrace();
        }
    }
}
```

 如何理解实现Callable接口的方式创建多线程比实现Runnable接口创建多线程方式强大？

 1.call()可以有返回值

2.call()可以抛出异常，被外面的操作捕获，获取异常的信息

3.Callable是支持泛型的

![image-20201207201606043](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201207201606043.png)



![image-20201207213434050](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201207213434050.png)

```java
package com.atguigu.java;

import java.util.concurrent.Callable;
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;

/**
 * @author wangxiang
 * @create 2020-12-07-21:32
 * 线程池创建线程
 */
class NumberThread1 implements Runnable{
    @Override
    public void run() {
        for (int i = 0; i <=100; i++) {
            if(i%2==0){
                System.out.println(Thread.currentThread().getName()+":"+i);
            }
        }
    }
}

class NumberThread2 implements Runnable{
    @Override
    public void run() {
        for (int i = 0; i <=100; i++) {
            if(i%2!=0){
                System.out.println(Thread.currentThread().getName()+":"+i);
            }
        }
    }
}

class NumberThread3 implements Callable {
    @Override
    public Object call() throws Exception {
        for (int i = 0; i <=100; i++) {
            if(i%2!=0){
                System.out.println(Thread.currentThread().getName()+":"+i);
            }
        }
        return null;
    }
}

public class ThreadPool {
    public static void main(String[] args) {
//步骤1：提供执行线程数量的线程池
        ExecutorService executorService = Executors.newFixedThreadPool(10);
//步骤2：执行指定线程的操作，需要提供实现Runnable接口或者Callable接口实现类的对象
        executorService.execute(new NumberThread1());//适合适用于Runnable
        executorService.execute(new NumberThread2());//适合适用于Runnable
        executorService.submit(new NumberThread3());//适合适用于Callable
        executorService.shutdown();//关闭连接池
    }
}
```



## java常用类的概述

![image-20201208124521018](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208124521018.png)

![image-20201208124714261](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208124714261.png)

![image-20201208125038214](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208125038214.png)

![image-20201208132920892](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208132920892.png)

![image-20201208133153614](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208133153614.png)

![image-20201208133921066](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208133921066.png)

![image-20201208140031726](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208140031726.png)

```java
import org.junit.Test;

/**
 * @author wangxiang
 * @create 2020-12-08-12:54
 */
public class StringTest {
     @Test
    public void test4(){
        String s1="javaEEhadoop";
        String s2="javaEE";
        String s3=s2+"hadoop";
        System.out.println(s1==s3);//fasle

        final String s4="javaEE";//s4为常量
        String s5=s4+"hadoop";
        System.out.println(s1==s5);//true
    }
    
    @Test
    public void test3(){
        String s1="javaEE";
        String s2="hadoop";
        String s3="javaEEhadoop";
        String s4="javaEE"+"hadoop";
        String s5=s1+"hadoop";
        String s6="javaEE"+s2 ;
        String s7=s1+s2;
//结论：1.常量与常量的拼接结果在常量池。且常量池中不会存在相同内容的常量
//     2.只要其中有一个是变量，结果就在堆中
        System.out.println(s3==s4);//true
        System.out.println(s3==s5);//false
        System.out.println(s3==s6);//false
        System.out.println(s5==s6);//false
        System.out.println(s3==s7);//false
        System.out.println(s5==s6);//false
        System.out.println(s5==s7);//false
        System.out.println(s6==s7);//false

        String s8=s4.intern();
        System.out.println(s4==s8);//true
    }

//    String 的实例化方式
//    方式一：通过字面量定义的方式
//    方式二：通过new+构造器的方式

//    面试题：String s=new String("abc");方式创建对象，在内存中创建了几个对象？
//    答：两个  一个是堆空间的new结构，另一个是char[]对应的常量池中的数据："abc"

    @Test
    public void test2(){
//通过字面量定义的方式此时的s1和s2的数据javaEE声明在方法去中的字符串常量池中
        String s1="javaEE";
        String s2="javaEE";

//通过new+构造器的方式：此时的s3和s4保存的地址值，是数据在堆空间中开辟空间以后对应的地址值
        String s3=new String("javaEE");
        String s4=new String("javaEE");

        System.out.println(s1==s2);//true
        System.out.println(s1==s3);//false
        System.out.println(s4==s3);//false
        System.out.println(s4==s1);//false

        System.out.println("**************");
        Person p1 = new Person("TOM", 12);
        Person p2 = new Person("TOM", 12);
        System.out.println(p1.name.equals(p2.name));//true
        System.out.println(p1.name==p2.name);//true
    }

//    String:字符串，使用一队""引起来表示
//    2.String声明为final，不可被继承
//    2.String实现了Serializable接口：表示字符串是支持序列化的
//             实现了Comparable接口：String可以比较大小
//    3.String内部定义了final char[] value用于存储字符串数据
//    4.String：代表不可变的字符序列，简称：不可变 性
//  体现：1.当对字符串重新赋值时，需要重写指定内存区域赋值，不能使用原有的value进行赋值
//  2.当对现有的字符串进行连接操作时，需要重新指定内存区域赋值，不能使用原有的value进行赋值
//  3.当调用String的replace()方法修改字符时，需要重新指定内存区域赋值，不能使用原有的value进行赋值
//    5.通过字面量的方式（区别于new）给一个字符串赋值，此时的字符串值声明在字符串常量池中
//    6.字符串常量池中是不会存储相同内容的字符串的
    @Test
    public void test1(){
        String s1="abc";//字面量
        String s2="abc";
//        s1="hello";
        s1=s2;
        System.out.println(s1==s2);//比较s1和 s2的地址值   String为对象
        System.out.println(s1);
        System.out.println(s2);
        System.out.println("************");

        String s3="abc";
        s3+="def";
        System.out.println(s3);

        String s4="abc";
        String s5 = s4.replace('a', 'm');
        System.out.println(s4);
        System.out.println(s5);
    }

}
```

```java
package com.company;

/**
 * @author wangxiang
 * @create 2020-12-08-14:48
 *
 * String面试题
 */
public class Test1 {
    String str=new String("good");
    char[] ch={'t','e','s','t'};

    public void change(String str,char ch[]){
        str="test ok";
        ch[0]='b';
    }

    public static void main(String[] args) {
        Test1 ex = new Test1();
        ex.change(ex.str, ex.ch);
        System.out.println(ex.str);//good
        System.out.println(ex.ch);//test
    }
}
```

### String常用方法

![image-20201208151356010](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208151356010.png)

![image-20201208151414286](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208151414286.png)

![image-20201208151444120](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208151444120.png)

```JAVA
package com.company;

import com.sun.scenario.effect.impl.sw.sse.SSEBlend_SRC_OUTPeer;
import org.junit.Test;

import javax.swing.*;

/**
 * @author wangxiang
 * @create 2020-12-08-15:16
 */
public class StringMethodTest {

    @Test
    public void test4(){
        String s1="北京尚硅谷教育北边办事处";
        String s2 = s1.replace("北", "东");

        System.out.println(s1);//北京尚硅谷教育北边办事处
        System.out.println(s2);//东京尚硅谷教育东边办事处

        String s3 = s1.replace("北京", "上海");
        System.out.println(s3);//上海尚硅谷教育北边办事处
    }



    @Test
    public void test3() {
        String s1 = "helloworld";
        boolean b1 = s1.endsWith("ld");
        System.out.println(b1);//true

        boolean b2 = s1.startsWith("He");
        System.out.println(b2);//false

        boolean b3 = s1.startsWith("ll", 2);
        System.out.println(b3);//true

        String s2="wo";
        System.out.println(s1.contains(s2));//true

        System.out.println(s1.indexOf("lo"));//3
        System.out.println(s1.indexOf("lol"));//-1

        System.out.println(s1.indexOf("lo", 5));//-1

        String s3="hellorworld";
        System.out.println(s3.lastIndexOf("or"));//7

        System.out.println(s3.lastIndexOf("or", 6));//4

        //什么情况下，indexOf(str)和lastIndexOf(str)返回值相同？
        //情况一：存在唯一的str  情况二：不存在str 空字符
    }


    @Test
    public void test2() {
        String s1 = "HelloWorld";
        String s2 = "helloworld";
        System.out.println(s1.equals(s2));//false
        System.out.println(s1.equalsIgnoreCase(s2));//true

        String s3 = "abc";
        String s4 = s3.concat("def");
        System.out.println(s4);//abcdef

        String s5 = "abc";
        String s6 = new String("abe");
        System.out.println(s5.compareTo(s6));//-2  设计到字符串排序

        String s7 = "北京尚硅谷教育";
        String s8 = s7.substring(2);
        System.out.println(s7);
        System.out.println(s8);//尚硅谷教育

        String s9 = s7.substring(2, 5);//左闭右开区间
        System.out.println(s9);//尚硅谷
    }

    @Test
    public void test1() {
        String s1 = "HelloWorld";
        System.out.println(s1.length());
        System.out.println(s1.charAt(0));
        System.out.println(s1.charAt(8));
        System.out.println(s1.charAt(9));
//        s1="";
        System.out.println(s1.isEmpty());
        String s2 = s1.toLowerCase();
        System.out.println(s1);
        System.out.println(s2);

        String s3 = "   he  llo   world   ";
        String s4 = s3.trim();
        System.out.println("-----" + s3 + "-----");
        System.out.println("-----" + s4 + "-----");
    }
}
```

![image-20201209134239214](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201209134239214.png)

![image-20201209135434621](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201209135434621.png)

### String常见算法题目

![image-20201209145213030](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201209145213030.png)



![image-20201209145552101](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201209145552101.png)

```java
package com.company;

import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;

import org.junit.Test;

/*
 * 1.模拟一个trim方法，去除字符串两端的空格。
 * 
 * 2.将一个字符串进行反转。将字符串中指定部分进行反转。比如将“abcdefg”反转为”abfedcg”
 * 
 * 3.获取一个字符串在另一个字符串中出现的次数。
      比如：获取“ab”在 “cdabkkcadkabkebfkabkskab”    
      中出现的次数
      
4.获取两个字符串中最大相同子串。比如：
   str1 = "abcwerthelloyuiodef“;str2 = "cvhellobnm"//10
   提示：将短的那个串进行长度依次递减的子串与较长  
   的串比较。

5.对字符串中字符进行自然顺序排序。"abcwerthelloyuiodef"
提示：
1）字符串变成字符数组。
2）对数组排序，选择，冒泡，Arrays.sort(str.toCharArray());
3）将排序后的数组变成字符串。

 */
public class  StringExer {

   // 第1题
   public String myTrim(String str) {
      if (str != null) {
         int start = 0;// 用于记录从前往后首次索引位置不是空格的位置的索引
         int end = str.length() - 1;// 用于记录从后往前首次索引位置不是空格的位置的索引

         while (start < end && str.charAt(start) == ' ') {
            start++;
         }

         while (start < end && str.charAt(end) == ' ') {
            end--;
         }
         if (str.charAt(start) == ' ') {
            return "";
         }

         return str.substring(start, end + 1);
      }
      return null;
   }

   // 第2题
   // 方式一：
   public String reverse1(String str, int start, int end) {// start:2,end:5
      if (str != null) {
         // 1.
         char[] charArray = str.toCharArray();
         // 2.
         for (int i = start, j = end; i < j; i++, j--) {
            char temp = charArray[i];
            charArray[i] = charArray[j];
            charArray[j] = temp;
         }
         // 3.
         return new String(charArray);

      }
      return null;

   }

   // 方式二：
   public String reverse2(String str, int start, int end) {
      // 1.
      String newStr = str.substring(0, start);// ab
      // 2.
      for (int i = end; i >= start; i--) {
         newStr += str.charAt(i);
      } // abfedc
         // 3.
      newStr += str.substring(end + 1);
      return newStr;
   }

   // 方式三：推荐 （相较于方式二做的改进）
   public String reverse3(String str, int start, int end) {// ArrayList list = new ArrayList(80);
      // 1.
      StringBuffer s = new StringBuffer(str.length());
      // 2.
      s.append(str.substring(0, start));// ab
      // 3.
      for (int i = end; i >= start; i--) {
         s.append(str.charAt(i));
      }

      // 4.
      s.append(str.substring(end + 1));

      // 5.
      return s.toString();

   }

   @Test
   public void testReverse() {
      String str = "abcdefg";
      String str1 = reverse3(str, 2, 5);
      System.out.println(str1);// abfedcg

   }

   // 第3题
   // 判断str2在str1中出现的次数
   public int getCount(String mainStr, String subStr) {
      if (mainStr.length() >= subStr.length()) {
         int count = 0;
         int index = 0;
         // while((index = mainStr.indexOf(subStr)) != -1){
         // count++;
         // mainStr = mainStr.substring(index + subStr.length());
         // }
         // 改进：
         while ((index = mainStr.indexOf(subStr, index)) != -1) {
            index += subStr.length();
            count++;
         }

         return count;
      } else {
         return 0;
      }

   }

   @Test
   public void testGetCount() {
      String str1 = "cdabkkcadkabkebfkabkskab";
      String str2 = "ab";
      int count = getCount(str1, str2);
      System.out.println(count);
   }

   @Test
   public void testMyTrim() {
      String str = "   a   ";
      // str = " ";
      String newStr = myTrim(str);
      System.out.println("---" + newStr + "---");
   }

   // 第4题
   // 如果只存在一个最大长度的相同子串
   public String getMaxSameSubString(String str1, String str2) {
      if (str1 != null && str2 != null) {
         String maxStr = (str1.length() > str2.length()) ? str1 : str2;
         String minStr = (str1.length() > str2.length()) ? str2 : str1;

         int len = minStr.length();

         for (int i = 0; i < len; i++) {// 0 1 2 3 4 此层循环决定要去几个字符

            for (int x = 0, y = len - i; y <= len; x++, y++) {

               if (maxStr.contains(minStr.substring(x, y))) {

                  return minStr.substring(x, y);
               }

            }

         }
      }
      return null;
   }

   // 如果存在多个长度相同的最大相同子串
   // 此时先返回String[]，后面可以用集合中的ArrayList替换，较方便
   public String[] getMaxSameSubString1(String str1, String str2) {
      if (str1 != null && str2 != null) {
         StringBuffer sBuffer = new StringBuffer();
         String maxString = (str1.length() > str2.length()) ? str1 : str2;
         String minString = (str1.length() > str2.length()) ? str2 : str1;

         int len = minString.length();
         for (int i = 0; i < len; i++) {
            for (int x = 0, y = len - i; y <= len; x++, y++) {
               String subString = minString.substring(x, y);
               if (maxString.contains(subString)) {
                  sBuffer.append(subString + ",");
               }
            }
            System.out.println(sBuffer);
            if (sBuffer.length() != 0) {
               break;
            }
         }
         String[] split = sBuffer.toString().replaceAll(",$", "").split("\\,");
         return split;
      }

      return null;
   }
   // 如果存在多个长度相同的最大相同子串：使用ArrayList
// public List<String> getMaxSameSubString1(String str1, String str2) {
//    if (str1 != null && str2 != null) {
//       List<String> list = new ArrayList<String>();
//       String maxString = (str1.length() > str2.length()) ? str1 : str2;
//       String minString = (str1.length() > str2.length()) ? str2 : str1;
//
//       int len = minString.length();
//       for (int i = 0; i < len; i++) {
//          for (int x = 0, y = len - i; y <= len; x++, y++) {
//             String subString = minString.substring(x, y);
//             if (maxString.contains(subString)) {
//                list.add(subString);
//             }
//          }
//          if (list.size() != 0) {
//             break;
//          }
//       }
//       return list;
//    }
//
//    return null;
// }

   @Test
   public void testGetMaxSameSubString() {
      String str1 = "abcwerthelloyuiodef";
      String str2 = "cvhellobnmiodef";
      String[] strs = getMaxSameSubString1(str1, str2);
      System.out.println(Arrays.toString(strs));
   }

   // 第5题
   @Test
   public void testSort() {
      String str = "abcwerthelloyuiodef";
      char[] arr = str.toCharArray();
      Arrays.sort(arr);

      String newStr = new String(arr);
      System.out.println(newStr);
   }
}
```

### StringBuffer类

![image-20201209145833978](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201209145833978.png)

![image-20201209161633279](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201209161633279.png)

![image-20201209161655913](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201209161655913.png)

### StringBuilder  

![image-20201209145921159](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201209145921159.png)

```java
//    String,StringBuffer,StringBuilder三者的异同
//    String:不可变的字符序列：底层使用char[]存储
//    StringBuffer:不可变的字符序列：线程安全  效率偏低  底层使用char[]存储
//    StringBuilder:可变的字符序列：线程不安全 效率偏高  底层使用char[]存储
//    开发选择  多线程有共享数据用StringBuffer   单线程用StringBuilder
//    效率对比：StringBuilder>StringBuffer>String
//    建议：开发中建议使用：StringBuffer(int capacity)或者StringBuilder(int capacity)

//    StringBuffer扩容问题：如果要添加的数组底层数组（长度为16）装不下了，那就需
//    要扩容底层的数组默认情况下：扩容为原来容量的2倍+2，代码为左移一位+2，
//    同时将原有的数组中的元素赋值到新的数组中
```

```java
package com.company;

import org.junit.Test;

/**
 * @author wangxiang
 * @create 2020-12-09-15:02
 */
public class StringBufferBuuilderTest {
    @Test
    public void test2(){
        StringBuffer s1 = new StringBuffer("abc");
        s1.append(1);
        s1.append('1');
        System.out.println(s1.toString());
        System.out.println(s1);
//        s1.delete(2,4);
//        s1.replace(2,4,"hello");
//        s1.insert(2, false);
        s1.reverse();
        System.out.println(s1);
        System.out.println(s1.length());
        String s2=s1.substring(1, 3);
        System.out.println(s2);

        char result=s1.charAt(3);
        System.out.println(result);

//        总结：
//        增：append(xxx)
//        删：delete(int start,int end)
//        改：setCharAt(int n,char ch)/ replace(int start,int end,String str)
//        查：charAt(int n)
//        插：insert(int n,xxx)
//        长度：length()
//        遍历：for+charAt() / toString()
    }




//    String,StringBuffer,StringBuilder三者的异同
//    String:不可变的字符序列：底层使用char[]存储
//    StringBuffer:不可变的字符序列：线程安全  效率偏低  底层使用char[]存储
//    StringBuilder:可变的字符序列：线程不安全 效率偏高  底层使用char[]存储
//    开发选择  多线程有共享数据用StringBuffer   单线程用StringBuilder

//    效率对比：StringBuilder>StringBuffer>String
//    建议：开发中建议使用：StringBuffer(int capacity)或者StringBuilder(int capacity)

//    StringBuffer扩容问题：如果要添加的数组底层数组（长度为16）装不下了，那就需
//    要扩容底层的数组默认情况下：扩容为原来容量的2倍+2，代码为左移一位+2，
//    同时将原有的数组中的元素赋值到新的数组中

    @Test
    public void test1(){
        StringBuffer sb1 = new StringBuffer("abc");
        sb1.setCharAt(0, 'm');
        System.out.println(sb1);
    }

}
```





### JDK之前的日期时间API

![image-20201209165211814](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201209165211814.png)

![image-20201209165230126](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201209165230126.png)

![image-20201209165835391](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201209165835391.png)

```java
package com.company;

import org.junit.Test;
import org.omg.CORBA.PUBLIC_MEMBER;
import sun.util.calendar.LocalGregorianCalendar;

import java.util.Date;

/**
 * @author wangxiang
 * @create 2020-12-09-16:53
 * <p>
 * JDK之前的日期时间API测试
 */
public class DateTimeTest {

//    Date类
//    java.util.Date类（父类）
//    1.两个构造器的使用
//      构造器一：Date() 创建了一个对应当前时间的Date对象
//        Date date1 = new Date();
//        System.out.println(date1.toString());
//        System.out.println(date1.getTime());
//
//        构造器二：创建指定毫秒数的Date对象
//        Date date2 = new Date(1607504706472L);
//        System.out.println(date2.toString());

//    2.两个方法的使用
//        1.toString():显示当前的年月日时分秒
//        2.getTime():返回当前Date与1970.1.1 0:0:0之间的以毫秒为单位的时间差
//    java.sql.Date（子类）

//    3.java.sql.Date对应着数据库中的日期类型的变量
//    如何实例化？
//       创建java.sql.Date对象
//        java.sql.Date date3 = new java.sql.Date(1607505003681L);
//        System.out.println(date3.toString());//2020-12-09
//
//    sql.Date-->util.Date 转换  直接赋值     属于子父类
//
//    util.Date-->sql.Date
//        将java.util.Date对象-->java.sql.Date对象
////        1.面向对象方式
//        Date date4=new java.sql.Date(1607505003681L);
//        java.sql.Date date5= (java.sql.Date) date4;
////        2.
//        Date date6=new Date();
//        java.sql.Date date7=new java.sql.Date(date6.getTime());


    @Test
    public void test2(){
//      构造器一：Date() 创建了一个对应当前时间的Date对象
        Date date1 = new Date();
        System.out.println(date1.toString());

        System.out.println(date1.getTime());

//      构造器二：创建指定毫秒数的Date对象
        Date date2 = new Date(1607504706472L);
        System.out.println(date2.toString());

//       创建java.sql.Date对象
        java.sql.Date date3 = new java.sql.Date(1607505003681L);
        System.out.println(date3.toString());//2020-12-09

//        将java.util.Date对象-->java.sql.Date对象
//        1.面向对象方式
        Date date4=new java.sql.Date(1607505003681L);
        java.sql.Date date5= (java.sql.Date) date4;
//        2.
        Date date6=new Date();
        java.sql.Date date7=new java.sql.Date(date6.getTime());
    }


    //  1.System类中的currentTimeMillis()
    @Test
    public void test() {
        long time = System.currentTimeMillis();
//        返回当前时间与1970.1.1 0:0:0之间的以毫秒为单位的时间差
//        称为时间戳
        System.out.println(time);
    }
}
```

![image-20201213151528654](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201213151528654.png)

```java
package com.company;

import org.junit.Test;

import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.Date;

/**
 * @author wangxiang
 * @create 2020/12/13
 *
 * JDK8之前的日期时间的API测试
 *
 * 3.SimpleDateFormat
 * 4.Calendar
 */
public class DateTimeTest1 {
//    SimpleDateFormat的使用：SimpleDateFormat对日期Date类的格式化何解析
//    1.两个操作
//    1.1   格式化：日期-->字符串
//    1.2   解析：格式化的逆过程：字符串-->日期

//    2.SimpleDateFormat的实例化
    @Test
    public void testSimpleDateFormat() throws ParseException {
//        实例化SimpleDateFormat:使用默认的构造器
        SimpleDateFormat sdf = new SimpleDateFormat();

//        格式化：日期-->字符串
        Date date = new Date();
        System.out.println(date);
        String format = sdf.format(date);
        System.out.println(format);

//        解析：字符串-->日期
        String str="20-12-13 下午3:27";
        Date date1 = sdf.parse(str);
        System.out.println(date1);

//        按照指定的方式格式化和解析：调用带参的构造器
//        SimpleDateFormat sdf1 = new SimpleDateFormat("yyyyy.MMMMM.dd GGG hh.mm aaa");
        SimpleDateFormat sdf1 = new SimpleDateFormat("yyyy-MM-dd hh:mm:ss");
//        格式化
        String format1 = sdf1.format(date);
        System.out.println(format1);//2020-12-13 03:43:38
//        解析
        Date date2 = sdf1.parse("2020-12-13 03:43:38");
        System.out.println(date2);

    }
}
```

```java
//    练习1：字符串"2020.09-08"转换为java.sql.Date
    @Test
    public void test1() throws ParseException {
        String str="2020-09-08";
        SimpleDateFormat sdf1 = new SimpleDateFormat("yyyy-MM-dd");
        Date date1 = sdf1.parse(str);
        java.sql.Date date2=new java.sql.Date(date1.getTime());
        System.out.println(date2);
    }
```

```java
//    练习2：一渔夫执行操作"三天打鱼两天晒网"
//    1990-01-01开始执行  提问某年某月某日是在打鱼还是晒网
//    举例：2020-09-08
//    总天数%5 ==1，2，3  ：打鱼
//    总天数%5 ==4，0     ：晒网
//    总天数的计算？
    @Test
    public void test2() throws ParseException {
        String str1="2020-09-08";
        SimpleDateFormat sdf1 = new SimpleDateFormat("yyyy-MM-dd");
        Date date1 = sdf1.parse(str1);
        String str2="1990-01-01";
        SimpleDateFormat sdf2 = new SimpleDateFormat("yyyy-MM-dd");
        Date date2 = sdf1.parse(str2);
        long time1=date1.getTime();
        long time2=date2.getTime();
        long time3=time1-time2;
        long time4=time3/1000;
        int day=(int)time4;
        int alldays=day/86400+1;
        System.out.println(alldays);
        if(alldays%5==1 || alldays%5==2 || alldays%5==3){
            System.out.println("今天是在打鱼");
        }
        if(alldays%5==4 || alldays%5==0){
            System.out.println("今天是在晒网");
        }
    }
```

![image-20201213163432153](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201213163432153.png)

![image-20201213185110031](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201213185110031.png)

![image-20201213185851716](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201213185851716.png)

![image-20201213190052803](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201213190052803.png)

![image-20201213190252885](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201213190252885.png)



![image-20201222163419956](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201222163419956.png)

![image-20201222163602743](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201222163602743.png)

```java
package com.company;

import org.junit.Test;

import java.time.Instant;
import java.time.OffsetDateTime;
import java.time.ZoneOffset;


//Instant了类似于java.util.Date
/**
 * @author wangxiang
 * @create 2020/12/22
 */
public class InstantTest {
    @Test
    public void test1(){
//        now():获取本初子午线对应的标准时间
        Instant instant = Instant.now();
        System.out.println(instant);

//        添加时间的偏移量
        OffsetDateTime offsetDateTime = instant.atOffset(ZoneOffset.ofHours(8));
        System.out.println(offsetDateTime);

//        获取对应的毫秒数  距离1970年
        long l = instant.toEpochMilli();
        System.out.println(l);

//        通过给定的毫秒数，过去Instant实例
        Instant instant1 = Instant.ofEpochMilli(1608627049345L);
        System.out.println(instant1);

    }
}
```

![image-20201222165319237](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201222165319237.png)

![image-20201222170726431](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201222170726431.png)



### java比较器

![image-20201222180324826](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201222180324826.png)

```JAVA
import com.company.Goods;
import org.junit.Test;

import java.util.Arrays;

/**
 * @author wangxiang
 * @create 2020/12/22
 *
 * 一 java中的对象，正常情况下，只能进行比较：== 或 !=  不能使用>或者<
 *  但是在开发场景中，我们需要对多个对象进行排序，言外之意，就需要比较对象的大小
 *      如何实现？使用两个接口：Comparable  Comparator
 *
 * 二 Comparable接口使用
 *
 *
 *
 */
public class CompareTest {
//    Comparable接口使用举例: 自然排序
//    1.像String，包装类等实现了Comparable接口，重写了comparaTo()方法，
//    给出了比较两个对象大小的方式
//    2.像String,包装类重写compareTo()方法以后,进行了从小到大的排列
//    3.重写comparaTo()的规则:
//    如果当前对象this大于形参对象obj,则返回正整数
//    如果当前对象this小于形参对象obj,则返回负整数
//    如果当前对象this等于形参对象obj,则返回零
//    4.对于自定义类来说,如果需要排序,我们可以让自定义类实现Comparable接口,
//    重写compareTo()方法,在compareTo(obj)方法中指明如何排序
    @Test
    public void test1(){
        String[] arr=new String[]{"AA","CC","MM","GG","DD","ZZ"};
        Arrays.sort(arr);
        System.out.println(Arrays.toString(arr));
    }
    @Test
    public void test2(){
        Goods[] arr=new Goods[4];
        arr[0]=new Goods("联想",600);
        arr[1]=new Goods("华为",35);
        arr[2]=new Goods("华硕",400);
        arr[3]=new Goods("镭射",37);

        Arrays.sort(arr);
        System.out.println(Arrays.toString(arr));
    }
}
```

```JAVA
package com.company;

/**
 * @author wangxiang
 * @create 2020/12/22
 * 商品类
 */
public class Goods implements Comparable{
    private String name;
    private double price;

    public Goods() {
    }

    public Goods(String name, double price) {
        this.name = name;
        this.price = price;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public double getPrice() {
        return price;
    }

    public void setPrice(double price) {
        this.price = price;
    }

    @Override
    public String toString() {
        return "Goods{" +
                "name='" + name + '\'' +
                ", price=" + price +
                '}';
    }

//    指明商品比较大小的方式
    @Override
    public int compareTo(Object o) {
       if(o instanceof Goods){
           Goods goods=(Goods)o;
           if(this.price>goods.price){
               return 1;
           }else if(this.price<goods.price){
               return -1;
           }else {
               return 0;
           }
//           方式二
//           return Double.compare(this.price,goods.price);
       }
       throw new RuntimeException("传入的数据类型不一致!");
    }
}
```

![image-20201223123644967](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201223123644967.png)

```java
package com.company;

import org.junit.Test;

import java.util.Arrays;

/**
 * @author wangxiang
 * @create 2020/12/23
 */
public class Comparator {
    @Test
    public void test1(){
        String[] arr=new String[]{"AA","CC","MM","GG","DD","ZZ"};
        Arrays.sort(arr, new java.util.Comparator<String>() {
            @Override
            public int compare(String o1, String o2) {
                if(o1 instanceof String && o2 instanceof String){
                    String s1=(String) o1;
                    String s2=(String) o2;
                    return -s1.compareTo(s2);//加负号  从大到小
                }
                throw new RuntimeException("输入的数据类型不一致");
            }
        });
    }
}
```

Comparable接口与Comparator的使用对比

Comparable接口的方式一旦指定，保证Comparable接口实现的类的对象在任何位置都能

比较大小

Comparator接口属于临时性的比较

### System类

![image-20201223131428447](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201223131428447.png)

![image-20201223134737877](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201223134737877.png)

![image-20201223134917279](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201223134917279.png)

![image-20201223135304362](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201223135304362.png)

## 枚举类与注解

### 如何定义枚举类

![image-20201223140931971](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201223140931971.png)

![image-20201223142400176](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201223142400176.png)

```java
package com;

import com.sun.xml.internal.bind.v2.runtime.property.StructureLoaderBuilder;

/**
 * @author wangxiang
 * @create 2020/12/23
 *
 * 1.枚举类的使用
 */
public class SeasonTest {

     public static void main(String[] args) {
        Season spring = Season.SPRING;
        System.out.println(spring);
    }
}


//自定义枚举类
class Season{
//    1.声明Season对象的属性:private final修饰
    private final String seasonName;
    private final String seasonDesc;

//    2.私有化类的构造器,并给对象属性赋值
    private Season(String seasonName, String seasonDesc){
        this.seasonName=seasonName;
        this.seasonDesc=seasonDesc;
    }

//    3.提供当前枚举类的多个对象:public static final
    public static final Season SPRING=new Season("春天","春暖花开");
    public static final Season SUMMER=new Season("夏天","夏日炎炎");
    public static final Season AUTUMN=new Season("秋天","秋高气爽");
    public static final Season WINTER=new Season("冬天","寒风凛凛");

//    4.其他诉求，获取枚举类对象的属性

    public String getSeasonName() {
        return seasonName;
    }

    public String getSeasonDesc() {
        return seasonDesc;
    }
//    4.其他诉求：提供toString()

    @Override
    public String toString() {
        return "Season{" +
                "seasonName='" + seasonName + '\'' +
                ", seasonDesc='" + seasonDesc + '\'' +
                '}';
    }
}
```





### 如何使用关键字enum定义枚举类



![image-20201223151145179](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201223151145179.png)

###  

### 实现接口的枚举类

```java
package com;

import com.sun.scenario.effect.impl.sw.sse.SSEBlend_SRC_OUTPeer;
import com.sun.xml.internal.bind.v2.runtime.property.StructureLoaderBuilder;

/**
 * @author wangxiang
 * @create 2020/12/23
 *
 * 使用enum定义枚举类
 * 说明：定义的枚举类默认继承于java.lang.Enum
 *
 * Enum类中的常用方法
 *
 * 4.使用enum关键字定义的枚举类实现接口的情况
 *  情况一：实现接口，在enum类中实现抽象方法
 *  情况二：
 */
public class Season1Test {

    public static void main(String[] args) {
        Season1 summer = Season1.SUMMER;
//        toString()方法
        System.out.println(summer.toString());

//        values()
        System.out.println("********");
        Season1[] values = Season1.values();
        for (int i = 0; i < values.length; i++) {
            System.out.println(values[i]);
        }

//        valueOf(String objName):根据提供的objName，返回与objName同名的对象
//        如果没有objName的枚举类对象，则抛出异常：IllegalArgumentException
        Season1 winter = Season1.valueOf("WINTER");
        System.out.println(winter);

        winter.show();
    }
}

interface Info{
    void show();
}


//自定义枚举类
enum Season1 implements Info{

//    1.提供当前枚举类的对象，多个对象之间用,隔开，末尾对象用;结束
        SPRING("春天","春暖花开"){
    @Override
    public void show() {
        System.out.println("这是春天");
    }
},
        SUMMER("夏天","夏日炎炎"){
            @Override
            public void show() {
                System.out.println("这是夏天");
            }
        },
        AUTUMN("秋天","秋高气爽"){
            @Override
            public void show() {
                System.out.println("这是秋天");
            }
        },
        WINTER("冬天","寒风凛凛"){
            @Override
            public void show() {
                System.out.println("这是冬天");
            }
        };

//    2.声明Season对象的属性:private final修饰
    private final String seasonName;
    private final String seasonDesc;

//    3.私有化类的构造器,并给对象属性赋值
    private Season1(String seasonName, String seasonDesc){
        this.seasonName=seasonName;
        this.seasonDesc=seasonDesc;
    }

//    4.其他诉求，获取枚举类对象的属性

    public String getSeasonName() {
        return seasonName;
    }

    public String getSeasonDesc() {
        return seasonDesc;
    }
//    4.其他诉求：提供toString()

    @Override
    public String toString() {
        return "Season1{" +
                "seasonName='" + seasonName + '\'' +
                ", seasonDesc='" + seasonDesc + '\'' +
                '}';
    }

//    @Override
//    public void show() {
//        System.out.println("这是一个季节");
    }
```

### 注解

![image-20201223155743004](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201223155743004.png)

![image-20201223155943336](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201223155943336.png)

![image-20201223160246021](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201223160246021.png)

![image-20201223160354474](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201223160354474.png)

![image-20201223160426118](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201223160426118.png)

![image-20201223160613651](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201223160613651.png)

![image-20201223184624670](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201223184624670.png)

![image-20201223185748398](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201223185748398.png)

![image-20201224135340305](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201224135340305.png)

![image-20201224140138106](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201224140138106.png)

![image-20201224144050106](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201224144050106.png)

![image-20201224145615631](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201224145615631.png)

![image-20201224145631681](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201224145631681.png)







## jvm内存解析

![image-20201208150016699](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208150016699.png)

 ![image-20201208150042811](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208150042811.png)

![image-20201208150513467](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208150513467.png)

![image-20201208150528860](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208150528860.png)

![image-20201208150823238](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208150823238.png)

![image-20201208150845542](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208150845542.png)

![image-20201208150855798](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201208150855798.png)



## 集合

### java集合框架概述

 ![image-20201224152451579](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201224152451579.png)

![image-20201224155331806](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201224155331806.png)

![image-20201224155557455](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201224155557455.png)

![image-20201224155820292](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201224155820292.png)

![image-20201224155844525](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201224155844525.png)

![image-20201224161932783](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201224161932783.png)









### Collection接口方法

![image-20201224181231980](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201224181231980.png)

![image-20201224181239761](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201224181239761.png)

### Iterator迭代器接口

![image-20201224203147908](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201224203147908.png)

![image-20201224203406777](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201224203406777.png)

![image-20201224204222162](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201224204222162.png)

![image-20201225135305052](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225135305052.png)

![image-20201225140054591](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225140054591.png)

![image-20201225140339437](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225140339437.png)

```java
package com;

import org.junit.Test;

import java.util.*;

/**
 * @author wangxiang
 * @create 2020/12/24
 *
 * 向Collection接口的实现类的对象中添加数据obj时，要求obj所在类要重写equals()
 */
public class CollectionTest {
    @Test
    public void test1(){
        Collection coll=new ArrayList();

//        add(Object e):将元素e添加到集合coll中
        coll.add("AA");
        coll.add("BB");
        coll.add(123);
        coll.add(new Date());
        coll.add(new String("TOM"));
        coll.add(new Person("王祥",21));

//        size()：获取添加的元素的个数
        System.out.println(coll.size());


//        addAll(Collection coll1):将coll1集合中的元素添加到当前集合中
        Collection coll1=new ArrayList();
        Collection coll2=new ArrayList();
        coll1.add("AC");
        coll1.add("SDW");
        coll1.add(123);
        coll1.add("BC");
        coll1.add("SDWA");
        coll2.add("AA");
        coll2.add("BB");
        coll.addAll(coll1);

        System.out.println(coll.size());

        System.out.println(coll);

//        clear()：清空集合元素
//        coll.clear();

//        isEmpty()：判断当前集合是否为空，是否有元素
        System.out.println(coll.isEmpty());

//        contains(Object obj):判断当前集合中  是否包含obj
        boolean contains = coll.contains("SDW");
        System.out.println(contains);

//        containsAll(Collection coll1):判断coll1中的所有元素是否都存在与当前集合中
        boolean b = coll.containsAll(coll1);
        System.out.println(b);

        coll.remove(123);
        System.out.println(coll);

//        removeAll(Collection call1):从当前集合中移除coll1中的所有元素
        coll.removeAll(coll1);
        System.out.println(coll);

//        retainAll(Collection coll2):求元素交集
        coll.retainAll(coll2);
        System.out.println(coll);

//        equals(Object obj):比较两个集合是否是相等的
        System.out.println(coll.equals(coll1));

//        hashCode()：返回当前对象的哈希值
        System.out.println(coll.hashCode());

//        集合->数组：toArray()
        Object[] arr = coll.toArray();
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i]);
        }
        System.out.println();

//        数组->集合：调用Arrays类的静态方法asList()
        List<String> list = Arrays.asList(new String[]{"AA", "BB", "CC", "DD", "EE"});
        System.out.println(list);

        List<Integer> arr1 = Arrays.asList(123, 456);
        System.out.println(arr1);

//        iterator()迭代器接口:返回Iterator接口的实例，用于遍历集合元素
        Collection coll3=new ArrayList();
        coll3.add("AA");
        coll3.add("BB");
        coll3.add(123);
        coll3.add(new Date());
        coll3.add(new String("TOM"));
        coll3.add(new Person("王祥",21));

        Iterator iterator = coll3.iterator();

//        方式一:
//        System.out.println(iterator.next());
//        System.out.println(iterator.next());
//        System.out.println(iterator.next());
//        System.out.println(iterator.next());
//        System.out.println(iterator.next());
//        System.out.println(iterator.next());

//        方式二：不推荐
//        for (int i = 0; i < coll3.size(); i++) {
//            System.out.print(iterator.next()+",");
//        }

//        方式三：推荐
        while(iterator.hasNext()){
            System.out.print(iterator.next()+",");
        }
    }

    @Test
    public void test2(){
        Collection coll=new ArrayList();

//        add(Object e):将元素e添加到集合coll中
        coll.add("AA");
        coll.add("BB");
        coll.add(123);
        coll.add(new Date());
        coll.add(new String("TOM"));
        coll.add(new Person("王祥",21));

        Iterator iterator = coll.iterator();
//        删除集合中的TOM元素
        while (iterator.hasNext()){
            Object obj = iterator.next();
            if("TOM".equals(obj)){
                iterator.remove();
            }
        }

        Iterator iterator1 = coll.iterator();
        while (iterator1.hasNext()){
            System.out.println(iterator1.next());
        }
    }

    @Test
    public void test3(){
        Collection coll=new ArrayList();

//        add(Object e):将元素e添加到集合coll中
        coll.add("AA");
        coll.add("BB");
        coll.add(123);
        coll.add(new Date());
        coll.add(new String("TOM"));
        coll.add(new Person("王祥",21));

//        使用foreach遍历
//        内部仍然调用迭代器
        for(Object obj:coll){
            System.out.println(obj);
        }
    }

    @Test
    public void test4(){
        int[] arr=new int[]{1,2,3,4,5,6};
        for(int i:arr){
            System.out.println(i);
        }
    }
    
}
```









### Collection子接口一：List

![image-20201225141424681](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225141424681.png)

ArrayList，LinkedList，Vector三者的异同？

同：三个类都实现了List接口，存储数据的特点相同：存储是有序的，可重复的数据

不同：

* ArrayList:作为List接口的主要实现类，线程不安全，所以效率高，
* 底层使用Object[] elementDate存储
* LinkedList:底层使用双向链表存储，对于频繁的插入，删除操作，使用此类效率比ArrayList
* 效率高
* Vector:作为List接口的古老实现类，线程安全，效率低，

![image-20201225144830398](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225144830398.png)

![image-20201225150501476](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225150501476.png)

![image-20201225151702694](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225151702694.png)



![image-20201225151653131](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225151653131.png)

![image-20201225151707870](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225151707870.png)

![image-20201225152017594](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225152017594.png)

![image-20201225153058240](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225153058240.png)

![image-20201225153743554](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225153743554.png)

![image-20201225171426571](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225171426571.png)

```java
package com;

import org.junit.Test;

import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;

/**
 * @author wangxiang
 * @create 2020/12/25
 *
 * ArrayList:作为List接口的主要实现类，线程不安全，所以效率高，
 * 底层使用Object[] elementDate存储
 * LinkedList:底层使用双向链表存储，对于频繁的插入，删除操作，使用此类效率比ArrayList
 * 效率高
 * Vector:作为List接口的古老实现类，线程安全，效率低，
 * 底层使用Object[] elementDate存储
 *
 */
public class ListTest {
    @Test
    public void test1(){
        ArrayList list = new ArrayList();
        list.add(123);
        list.add(456);
        list.add("AA");
        list.add(new Person("TOM",23));
        list.add(456);

        System.out.println(list);

//
        list.add(1,"BB");//在1的位置插入BB
        System.out.println(list);

        List list1 = Arrays.asList(1, 2, 3);
        list.addAll(list1);
        System.out.println(list.size());
        System.out.println(list);

        System.out.println(list.get(1));

//        如果不存在返回-1
        int i = list.indexOf(456);
        System.out.println(i);

        int i1 = list.lastIndexOf(456);
        System.out.println(i1);

//        remove(index);删除index位置上的元素
        Object remove = list.remove(0);
        System.out.println(remove);
        System.out.println(list);

        List list2 = list.subList(2, 4);
        System.out.println(list2);


    }

}
```







### Collection子接口二：Set

![image-20201225174809217](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225174809217.png)

![image-20201225174813276](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225174813276.png)

![image-20201225174820850](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225174820850.png)

![image-20201225174825096](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225174825096.png)

![image-20201225190811583](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225190811583.png)

![image-20201225190819189](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225190819189.png)

![image-20201225210400105](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225210400105.png)

![image-20201225211215044](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225211215044.png)

![image-20201225211415294](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201225211415294.png)

hash底层：数组+链表的结构 

```java
package com.Set;

import com.Person;
import org.junit.Test;

import java.util.HashSet;
import java.util.Iterator;
import java.util.LinkedHashSet;
import java.util.Set;

/**
 * @author wangxiang
 * @create 2020/12/25
 *
 * HashSet:作为Set接口的主要实现类,线程不安全，可以存储null值
 * LinkedHashSet:HashSet的子类，遍历其内部数据时可以按照添加的顺序遍历
 * TreeSet:可以按照添加元素，对象的指定属性，进行排序
 *
 * Set接口中没有额外定义新的方法，使用的都是Collection中声明过的方法
 *
 * Set
 *  无序性：不等于随机性，存储的数据在底层数组中并非按照数组索引的顺序添加。
 *  而是根据数据的哈希值确定的
 *  不可重复性：保证添加的元素按照equals方法判断时，不能返回true。即相同的元素
 *  只能添加一个
 *
 *  要求：向Set中添加数据，其所在的类一定要重写hashCode()和equals()
 *  要求：重写的hashCode()和equals()尽可能保持一致性：相等的对象bi必须具有相等的散列码
 *
 */
public class SetTest {
    @Test
    public void test1(){
        Set set=new HashSet();
        set.add(456);
        set.add(123);
        set.add("AA");
        set.add(new Person("TOM",12));
        set.add(new Person("TOM",12));
        set.add("cc");
        set.add(123);

        Iterator iterator = set.iterator();
        while (iterator.hasNext()){
            System.out.println(iterator.next());
        }

        for(Object obj:set){
            System.out.println(obj);
        }
    }

    @Test
    public void test2(){
        Set set=new LinkedHashSet();
        set.add(456);
        set.add(123);
        set.add("AA");
        set.add(new Person("TOM",12));
        set.add(new Person("TOM",12));
        set.add("cc");
        set.add(123);

        Iterator iterator = set.iterator();
        while (iterator.hasNext()){
            System.out.println(iterator.next());
        }

        for(Object obj:set){
            System.out.println(obj);
        }


    }
}
```

### 面试题

![image-20201226144638414](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226144638414.png)

```java
package com.Test;

/**
 * @author wangxiang
 * @create 2020/12/26
 */
public class MyDate implements Comparable{
    private int year;
    private int month;
    private int day;

    public MyDate() {
    }

    public MyDate(int year, int month, int day) {
        this.year = year;
        this.month = month;
        this.day = day;
    }

    public int getYear() {
        return year;
    }

    public void setYear(int year) {
        this.year = year;
    }

    public int getMonth() {
        return month;
    }

    public void setMonth(int month) {
        this.month = month;
    }

    public int getDay() {
        return day;
    }

    public void setDay(int day) {
        this.day = day;
    }

    @Override
    public String toString() {
        return "MyDate{" +
                "year=" + year +
                ", month=" + month +
                ", day=" + day +
                '}';
    }

    @Override
    public int compareTo(Object o) {
        if(o instanceof MyDate){
            MyDate m=(MyDate)o;
            int minusYear=this.getYear()-m.getYear();
            if(minusYear != 0){
                return minusYear;
            }
            int minusMonth=this.getMonth()-m.getMonth();
            if(minusMonth != 0){
                return minusMonth;
            }

            return this.getDay()-m.getDay();
        }
        throw new RuntimeException("输入的数据类型不一致");
    }
}
```

```java
package com.Test;

/**
 * @author wangxiang
 * @create 2020/12/26
 */
public class Employee implements Comparable{
    private String name;
    private int age;
    private MyDate brithday;

    public Employee() {
    }

    public Employee(String name, int age, MyDate brithday) {
        this.name = name;
        this.age = age;
        this.brithday = brithday;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public MyDate getBrithday() {
        return brithday;
    }

    public void setBrithday(MyDate brithday) {
        this.brithday = brithday;
    }

    @Override
    public String toString() {
        return "Employee{" +
                "name='" + name + '\'' +
                ", age=" + age +
                ", brithday=" + brithday +
                '}';
    }

    @Override
    public int compareTo(Object o) {
        if(o instanceof Employee ){
            Employee e=(Employee)o;
            return this.name.compareTo(e.name);
        }else {
            throw new RuntimeException("输入数据类型不匹配");
        }
    }
}
```

```java
package com.Test;

import org.junit.Test;

import java.util.Comparator;
import java.util.Iterator;
import java.util.TreeSet;

/**
 * @author wangxiang
 * @create 2020/12/26
 */
public class EmployeeTest {//自然排序
    @Test
    public void test1(){
        Employee employee1 = new Employee("刘德华",55,new MyDate(1964,6,5));
        Employee employee2 = new Employee("张三丰",46,new MyDate(1978,12,8));
        Employee employee3 = new Employee("赵无极",86,new MyDate(1964,7,4));
        Employee employee4 = new Employee("徐三强",82,new MyDate(1964,12,29));
        Employee employee5 = new Employee("华子",13,new MyDate(1964,9,15));

        TreeSet set = new TreeSet();
        set.add(employee1);
        set.add(employee2);
        set.add(employee3);
        set.add(employee4);
        set.add(employee5);

        Iterator iterator = set.iterator();
        while(iterator.hasNext()){
            System.out.println(iterator.next());
        }
    }

    @Test
    public void test2(){//按照生日日期的先后排序


        Employee employee1 = new Employee("刘德华",55,new MyDate(1964,6,5));
        Employee employee2 = new Employee("张三丰",46,new MyDate(1978,12,8));
        Employee employee3 = new Employee("赵无极",86,new MyDate(1964,7,4));
        Employee employee4 = new Employee("徐三强",82,new MyDate(1964,12,29));
        Employee employee5 = new Employee("华子",13,new MyDate(1964,9,15));

        TreeSet set = new TreeSet(new Comparator() {
            @Override
            public int compare(Object o1, Object o2) {
                if(o1 instanceof Employee && o2 instanceof Employee){
                    Employee e1=(Employee)o1;
                    Employee e2=(Employee)o2;
                    MyDate b1 = e1.getBrithday();
                    MyDate b2 = e2.getBrithday();
                    return b1.compareTo(b2);
                }
                throw new RuntimeException("输入的数据类型不一致");
            }
        });
        set.add(employee1);
        set.add(employee2);
        set.add(employee3);
        set.add(employee4);
        set.add(employee5);

        Iterator iterator = set.iterator();
        while(iterator.hasNext()){
            System.out.println(iterator.next());
        }
    }
}
```

![image-20201226155538363](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226155538363.png)

![image-20201226160037140](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226160037140.png)

![image-20201226160655865](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226160655865.png)

骗过了hash检测，重新计算的哈希值找到的位置没有数据





### Map接口

![image-20201226162044329](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226162044329.png)

![image-20201226164942115](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226164942115.png)

![image-20201226164807435](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226164807435.png)



![image-20201226170414951](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226170414951.png)

```java
package com.MapTest;

import org.junit.Test;

import java.util.Collection;
import java.util.HashMap;
import java.util.Map;
import java.util.Set;

/**
 * @author wangxiang
 * @create 2020/12/26
 */
public class MapTest {
    @Test
    public void test1(){
        Map map = new HashMap();
        map.put("AA",123);
        map.put("AA",87);
        map.put(45,123 );
        map.put("BB",456);
        map.put("DD",785);

        System.out.println(map);

//        遍历所有的key急：keySet()
        Set set = map.keySet();
        for(Object obj:set){
            System.out.print(obj+",");
        }

        System.out.println();

//        遍历所有的value集:value()
        Collection values = map.values();
        for(Object obj:values){
            System.out.print(obj+",");
        }

        System.out.println();

//        遍历所有的key-value:entrySet()
        Set set1 = map.entrySet();
        for(Object obj:set1){
            System.out.print(obj+",");
        }

        System.out.println(map.get(45));

        System.out.println(map.size());

        boolean bb = map.containsKey("BB");
        System.out.println(bb);

        boolean b = map.containsValue(123);
        System.out.println(b);

        Map map1 = new HashMap();
        map1.put("CC",123);
        map1.put("DD",87);

        map.putAll(map1);
        System.out.println(map);

//        remove(Object key)
        Object value = map.remove("CC");
        Object value1 = map.remove("CCC");
        System.out.println(value);
        System.out.println(value1);
        System.out.println(map);

        map.clear();
        System.out.println(map.size());
        System.out.println(map);

        System.out.println(map.isEmpty());

    }
}
```

```java
import com.Person;
import org.junit.Test;

import java.util.Comparator;
import java.util.Set;
import java.util.TreeMap;

/**
 * @author wangxiang
 * @create 2020/12/26
 */
public class TreeMapTest {
    @Test
    public void test1() {
        TreeMap map = new TreeMap(new Comparator() {
            @Override
            public int compare(Object o1, Object o2) {
                if(o1 instanceof Person && o2 instanceof Person){
                    Person p1=(Person)o1;
                    Person p2=(Person)o2;
                    return Integer.compare(p1.getAge(),p2.getAge());
                }
                throw new RuntimeException("输入的数据类型不一致");
            }
        });
        Person p1 = new Person("TOM", 12);
        Person p2 = new Person("Jack", 13);
        Person p3 = new Person("ROSE", 25);
        Person p4 = new Person("David", 58);
        map.put(p1, 95);
        map.put(p2, 60);
        map.put(p3, 85);
        map.put(p4, 35);

        Set set = map.entrySet();
        for(Object obj:set){
            System.out.println(obj);
        }


    }
}
```





![image-20201226191339060](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226191339060.png)









### 面试题

HashMap的底层实现原理？

![image-20201226171738693](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226171738693.png)

![image-20201226172231148](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226172231148.png)

![image-20201226180355863](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226180355863.png)

HashMap和Hashtable的异同？



CurrentHashMap与Hashtable的异同？





![image-20201226172635867](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226172635867.png)

![image-20201226172643091](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226172643091.png)



### Map接口常用方法

![image-20201226181232017](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226181232017.png)





### Collections工具类

![image-20201226192350580](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226192350580.png)

![image-20201226192430350](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226192430350.png)



![image-20201226194921530](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226194921530.png)

```java
package com;

import org.junit.Test;

import java.util.ArrayList;
import java.util.Collections;
import java.util.List;

/**
 * @author wangxiang
 * @create 2020/12/26
 */
public class CollectionsTest {
    @Test
    public void test1() {
        List list = new ArrayList();
        list.add(123);
        list.add(-123);
        list.add(99);
        list.add(15);
        list.add(765);
        list.add(2);

        System.out.println(list);

        Collections.reverse(list);
        System.out.println(list);

        Collections.shuffle(list);
        System.out.println(list);
        
        Collections.sort(list);
        System.out.println(list);

        Collections.swap(list,1,2);
        System.out.println(list);

//        返回的list1就是安全的线程
        List list1 = Collections.synchronizedList(list);

    }
}
```







![image-20201226195251500](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226195251500.png)

![image-20201226195425684](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226195425684.png)

![image-20201226195517933](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201226195517933.png)





## 泛型

### 为什么要有泛型

![image-20201227131542141](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201227131542141.png)

![image-20201227132302183](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201227132302183.png)

![image-20201227132450939](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201227132450939.png)









### 在集合中使用泛型









### 自定义泛型

![image-20201228121325180](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228121325180.png)

![image-20201228122110630](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228122110630.png)

![image-20201228122939937](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228122939937.png)

![image-20201228123047021](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228123047021.png)

泛型方法，可以声明为静态的，原因：泛型参数是在调用方法时确定的，并非再实例化确定

泛型方法所属的类是不是泛型类型都没关系

泛型方法：在方法中出现了泛型的结构，泛型参数与类的泛型参数都没有任何关系

```java
public static <E> List<E> copyFromArrayToList(E[] arr){
    ArrayList<E> list = new ArrayList<>();
    for(E e:arr){
        list.add(e);
    }
    return list;
}
```



### 泛型在继承上的体现

![image-20201228145701457](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228145701457.png)







### 通配符的使用



![image-20201228163244069](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228163244069.png)

![image-20201228164552420](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228164552420.png)



### 泛型应用举例



![image-20201228165240483](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228165240483.png)

![image-20201228165539954](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228165539954.png)



## IO流

### File类的使用

![image-20201228180902799](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228180902799.png)

![image-20201228181435017](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228181435017.png)

![image-20201228182127051](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228182127051.png)

![image-20201228183640633](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228183640633.png)

![image-20201228183701004](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228183701004.png)

![image-20201228183709974](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228183709974.png)

![image-20201228192900328](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228192900328.png)

![image-20201228193500113](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201228193500113.png)









### IO流原理及流的分类

![image-20201229133458497](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201229133458497.png)

![image-20201229133706519](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201229133706519.png)

![image-20201229134025151](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201229134025151.png)

![image-20201229135450673](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201229135450673.png)

对于文本文件(txt,java,c,cpp)，使用字符流处理

对于非文本文件(jpg,mp3,mp4,avi,doc,ppt...)，使用字节流处理

```java
package IO;

import org.junit.Test;

import java.io.File;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;

/**
 * @author wangxiang
 * @create 2020/12/29
 */
public class FileInpuOutputStreamTest {
    @Test
    public void test1() {
        FileInputStream fis = null;
        try {
            File file1 = new File("hello.txt");

            fis = new FileInputStream(file1);

            byte[] buffer=new byte[5];
            int len;//记录每次读取的字节的个数

            while((len=fis.read(buffer)) != -1){
                String str=new String(buffer,0,len);
                System.out.print(str);
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            try {
                if(fis != null)
                fis.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }


    }
}
```

```java
package IO;

import org.junit.Test;

import java.io.*;

/**
 * @author wangxiang
 * @create 2020/12/29
 */
public class FileReaderWriterTest {
    public static void main(String[] args) {
        File file1 = new File("hello.txt");//相较于当前工程
        System.out.println(file1.getAbsolutePath());
    }

    @Test
    public void test1() {

        FileReader fr = null;
        try {
            File file1 = new File("hello.txt");//相较于当前Module
            System.out.println(file1.getAbsolutePath());

            fr = new FileReader(file1);

//        数据的读入：read()：返回读入的一个字符，如果达到文件末尾，返回-1
            int data = fr.read();
            while (data != -1) {
                System.out.print((char) data);
                data = fr.read();
            }


            int data1;
            while ((data1 = fr.read()) != -1) {
                System.out.print((char) data1);
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            //        流的关闭操作,否则容易导致内存泄漏
            try {
                if (fr != null)
                    fr.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }

    @Test
    public void test2() {
        FileReader fr = null;
        try {
            File file1 = new File("hello.txt");//相较于当前Module
            fr = new FileReader(file1);

            char[] cbuf = new char[5];
            int len;
            while ((len = fr.read(cbuf)) != -1) {
//                for (int i = 0; i < len; i++) {
//                    System.out.print(cbuf[i]);
//                }
//                System.out.println();
                String str = new String(cbuf, 0, len);
                System.out.print(str);
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            try {
                if (fr != null)
                    fr.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }

    @Test
    public void test3()  {
        FileWriter fw = null;
        try {
            File file1 = new File("hello1.txt");

            fw = new FileWriter(file1, false);
            //false对原有文件进行内容覆盖
//        true对原有文件进行追加内容添加

            fw.write("I hava a dream!\n");
            fw.write("YOu  IADCDA DA ");
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            try {
                if (fw != null)
                    fw.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }


    }

    @Test
    public void test4()  {
        FileReader fr = null;
        FileWriter fw = null;
        try {
            File file1 = new File("hello.txt");
            File file2 = new File("hello2.txt");

            fr = new FileReader(file1);
            fw = new FileWriter(file2);

            char[] cbuf = new char[5];
            int len;//记录读入数据的长度
            while ((len = fr.read(cbuf)) != -1) {
                for (int i = 0; i < len; i++) {
                    fw.write(cbuf, 0, len);
                }

            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {

            try {
                if(fw!=null)
                fw.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
            try {
                if(fr!=null)
                fr.close();
            } catch (IOException e) {
                e.printStackTrace();
            }

        }

    }

}
```



### 节点流(或文件流)





### 缓冲流

```java
package IO;

import org.junit.Test;

import java.io.*;

/**
 * @author wangxiang
 * @create 2020/12/29
 *
 * 缓冲流的使用
 */
public class BufferedTest {

    @Test
    public void test1(){

        BufferedInputStream bis = null;
        BufferedOutputStream bos = null;
        try {
            File srcFile=new File("简历照片.jpeg");
            File destFile=new File("简历照片3.jpeg");

            FileInputStream fis = new FileInputStream(srcFile);
            FileOutputStream fos = new FileOutputStream(destFile);

            bis = new BufferedInputStream(fis);
            bos = new BufferedOutputStream(fos);

            byte[] buffer=new byte[10];
            int len;

            while ((len=bis.read(buffer)) != -1){
                bos.write(buffer,0,len);
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            try {
                if(bos != null)
                bos.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
            try {
                if(bis != null)
                bis.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }

//        资源关闭，先关外层流，再关内层流
//        bos.close();
//        bis.close();
//        关闭外层流的同时，内层流也会自动的进行关闭
//        fos.close();
//        fis.close();
    }
}
```

```java
package IO;

import org.junit.Test;

import java.io.*;

/**
 * @author wangxiang
 * @create 2020/12/29
 *
 * 缓冲流的使用
 */
public class BufferedTest {

    @Test
    public void test1(){

        BufferedInputStream bis = null;
        BufferedOutputStream bos = null;
        try {
            File srcFile=new File("简历照片.jpeg");
            File destFile=new File("简历照片3.jpeg");

            FileInputStream fis = new FileInputStream(srcFile);
            FileOutputStream fos = new FileOutputStream(destFile);

            bis = new BufferedInputStream(fis);
            bos = new BufferedOutputStream(fos);

            byte[] buffer=new byte[10];
            int len;

            while ((len=bis.read(buffer)) != -1){
                bos.write(buffer,0,len);
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            try {
                if(bos != null)
                bos.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
            try {
                if(bis != null)
                bis.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }

//        资源关闭，先关外层流，再关内层流
//        bos.close();
//        bis.close();
//        关闭外层流的同时，内层流也会自动的进行关闭
//        fos.close();
//        fis.close();
    }

    public void copyFileWithBuffered(String srcPath,String destPath){
        BufferedInputStream bis = null;
        BufferedOutputStream bos = null;
        try {
            File srcFile=new File(srcPath);
            File destFile=new File(destPath);

            FileInputStream fis = new FileInputStream(srcFile);
            FileOutputStream fos = new FileOutputStream(destFile);

            bis = new BufferedInputStream(fis);
            bos = new BufferedOutputStream(fos);

            byte[] buffer=new byte[10];
            int len;

            while ((len=bis.read(buffer)) != -1){
                bos.write(buffer,0,len);
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            try {
                if(bos != null)
                    bos.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
            try {
                if(bis != null)
                    bis.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }

    @Test
    public void test2(){

        BufferedReader br = null;
        BufferedWriter bw = null;
        try {
            br = new BufferedReader(new FileReader(new File("hello.txt")));
            bw = new BufferedWriter(new FileWriter(new File("helloX.txt")));

            char[] cbuf=new char[1024];
            int len;
            while ((len=br.read(cbuf)) != -1){
                bw.write(cbuf,0,len);
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            try {
                if(br != null)
                br.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
            try {
                if(bw != null)
                bw.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }


    }
}
```

![image-20201229184359629](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201229184359629.png)

```java
package IOTest;

import org.junit.Test;

import java.io.*;

/**
 * @author wangxiang
 * @create 2020/12/29
 */
public class PicTest {

//    图片的加密
    @Test
    public void test1(){

        FileInputStream fis = null;
        FileOutputStream fos = null;
        try {
            fis = new FileInputStream(new File("简历照片.jpeg"));
            fos = new FileOutputStream(new File("简历照片secret.jpeg"));

            byte[] buffer=new byte[20];
            int len;
            while ((len=fis.read(buffer)) != -1){
                for (int i = 0; i < len; i++) {
                    buffer[i]= (byte) (buffer[i]^5);
                }
                fos.write(buffer,0,len);
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            try {
                if(fos != null)
                fos.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
            try {
                if(fis != null)
                    fis.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }


    }

//    图片的解密
    @Test
    public void test2(){

        FileInputStream fis = null;
        FileOutputStream fos = null;
        try {
            fis = new FileInputStream(new File("简历照片secret.jpeg"));
            fos = new FileOutputStream(new File("简历照片解密.jpeg"));

            byte[] buffer=new byte[20];
            int len;
            while ((len=fis.read(buffer)) != -1){
                for (int i = 0; i < len; i++) {
                    buffer[i]= (byte) (buffer[i]^5);
                }
                fos.write(buffer,0,len);
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            try {
                if(fos != null)
                    fos.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
            try {
                if(fis != null)
                    fis.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }


    }

    @Test
    public void test3()  {

        InputStreamReader isr1 = null;//使用系统默认的
        try {
            FileInputStream fis = new FileInputStream("hello.txt");
            isr1 = new InputStreamReader(fis);
//        字符集转换
//        InputStreamReader isr2 = new InputStreamReader(fis,"UTF-8");
//        使用设置的字符集

            char[] cbuf=new char[20];
            int len;
            while ((len=isr1.read(cbuf)) != -1){
                String str = new String(cbuf,0,len);
                System.out.print(str);
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            if(isr1 != null)
                try {
                    isr1.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
        }
    }

    @Test
    public void test4() throws IOException {

        File file1 = new File("hello.txt");
        File file2 = new File("hello_gbk.txt");

        FileInputStream fis = new FileInputStream(file1);
        FileOutputStream fos = new FileOutputStream(file2);

        InputStreamReader isr = new InputStreamReader(fis,"utf-8");
        OutputStreamWriter osw = new OutputStreamWriter(fos,"gbk");

        char[] cbuf=new char[20];
        int len;
        while ((len=isr.read(cbuf)) != -1){
            osw.write(cbuf,0,len);
        }

        osw.close();
        isr.close();
    }
}

```



### 转换流![image-20201229191740753](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201229191740753.png)

![image-20201229191838336](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201229191838336.png)

![image-20201229192551351](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201229192551351.png)

![image-20201230123138895](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201230123138895.png)

![image-20201230124755995](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201230124755995.png)

![image-20201230130011350](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201230130011350.png)

![image-20201230130021166](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201230130021166.png)



### 标准输入,输出流





### 打印流





### 数据流





### 对象流



![image-20201231152339277](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231152339277.png)

![image-20201231152330584](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231152330584.png)

![image-20201231160326397](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231160326397.png)

自定义类序列化

```java
package ObjectInputOutputStreamTest;

import java.io.Serializable;

/**
 * @author wangxiang
 * @create 2020/12/31
 *
 * Person需要满足如下的要求，方可序列化
 * 1.需要实现接口，Serializable
 * 2.当前类提供一个全局常量：serialVersionUID
 * 3.除了当前Person类需要实现Serializable接口之外，还必须保证
 * 其内部所有属性也必须是可序列化的
 */
public class Person implements Serializable {
    private String name;
    private int age;

    public static final long serialVersionUID=421465456456456L;

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public Person() {
    }

    @Override
    public String toString() {
        return "Person{" +
                "name='" + name + '\'' +
                ", age=" + age +
                '}';
    }
}
```



### 随机存储文件流

![image-20201231162004174](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231162004174.png)

![image-20201231162918903](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231162918903.png)

![image-20201231164803052](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231164803052.png)

![image-20201231173250596](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231173250596.png)





### NIO2中Path,Paths,Files类的使用

![image-20201231173307627](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231173307627.png)

![image-20201231173856900](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231173856900.png)

![image-20201231174042484](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231174042484.png)

![image-20201231174102817](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231174102817.png)

![image-20201231174121876](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231174121876.png)





## 网络编程



### 网络编程概述

![image-20201231175031921](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231175031921.png)

![image-20201231175214084](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231175214084.png)

![image-20201231180652489](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231180652489.png)

![image-20201231180813110](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231180813110.png)









### 网络通信概述





### 通信要素1：IP和端口号

![image-20201231181632840](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231181632840.png)

![image-20201231184642189](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231184642189.png)







### 通信要素2：网络协议

![image-20201231185446807](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231185446807.png)

![image-20201231185547532](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231185547532.png)

![image-20201231185600848](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231185600848.png)

![image-20201231191027052](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231191027052.png)

![image-20201231191108923](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20201231191108923.png)













### TCP网络编程

```java
package 网络编程;

import org.junit.Test;

import java.io.*;
import java.net.InetAddress;
import java.net.ServerSocket;
import java.net.Socket;

/**
 * @author wangxiang
 * @create 2021/1/1
 */
public class TCPTest3 {

    @Test
    public void client(){

        Socket socket = null;
        OutputStream os= null;
        FileInputStream fis = null;
        InputStream is=null;
        ByteArrayOutputStream baos=null;
        try {
            socket = new Socket(InetAddress.getByName("127.0.0.1"),9090);

            os = socket.getOutputStream();

            fis = new FileInputStream(new File("简历照片.jpeg"));

            byte[] buffer=new byte[1024];
            int len;
            while ((len= fis.read(buffer)) != -1){
                os.write(buffer,0,len);
            }

//           关闭数据的输出
            socket.shutdownOutput();

            is = socket.getInputStream();
            baos = new ByteArrayOutputStream();
            byte[] buffer1=new byte[20];
            int len1;
            while ((len1= is.read(buffer1)) != -1){
                baos.write(buffer1,0,len1);
            }
            System.out.println(baos.toString());

        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            if(fis != null)
                try {
                    fis.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            if(os != null)
                try {
                    os.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            if(socket != null)
                try {
                    socket.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            if(is != null)
                try {
                    is.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            if(baos != null)
                try {
                    baos.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
        }
    }

    @Test
    public void server(){

        ServerSocket serverSocket = null;
        Socket socket = null;
        InputStream is = null;
        FileOutputStream fos = null;
        OutputStream os=null;

        try {
            serverSocket = new ServerSocket(9090);

            socket = serverSocket.accept();

            is = socket.getInputStream();

            fos = new FileOutputStream(new File("beauty5.jpeg"));


            byte[] buffer=new byte[1024];
            int len;
            while ((len= is.read(buffer)) != -1){
                fos.write(buffer,0,len);
            }

            System.out.println("图片传输完成");
            os = socket.getOutputStream();
            os.write("你好，照片我已经收到".getBytes());

        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            if(fos != null)
                try {
                    fos.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            if(is != null)
                try {
                    is.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            if(socket != null)
                try {
                    socket.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            if(serverSocket != null)
                try {
                    serverSocket.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            if(os != null)
                try {
                    os.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }

        }
    }
}
```







### UDP网络编程

![image-20210101132236932](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210101132236932.png)

```java
package 网络编程;

import org.junit.Test;

import java.io.IOException;
import java.net.DatagramPacket;
import java.net.DatagramSocket;
import java.net.InetAddress;
import java.net.SocketException;

/**
 * @author wangxiang
 * @create 2021/1/1
 */
public class UDPTest {

    @Test
    public void send(){
        DatagramSocket socket = null;
        try {
            socket = new DatagramSocket();

            String str="我是UDP方式发送的导弹";
            byte[] data = str.getBytes();
            InetAddress inet = InetAddress.getLocalHost();
            DatagramPacket packet = new DatagramPacket(data,0,data.length,inet,9090);

            socket.send(packet);
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            socket.close();
        }
    }

    @Test
    public void receiver() throws IOException {
        DatagramSocket socket = new DatagramSocket(9090);

        byte[] buffer=new byte[100];

        DatagramPacket packet = new DatagramPacket(buffer,0,buffer.length);

        socket.receive(packet);

        System.out.println(new String(packet.getData(),0,packet.getLength()));


    }

}
```



### URL编程

![image-20210101133743125](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210101133743125.png)





## 反射



### java反射机制概述

![image-20210101140517072](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210101140517072.png)

![image-20210101140710706](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210101140710706.png)

![image-20210101141152378](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210101141152378.png)



![image-20210101141327083](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210101141327083.png)

![image-20210101220612788](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210101220612788.png)![image-20210101222227751](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210101222227751.png)

![image-20210101221140764](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210101221140764.png)

```java
package 反射;

import org.junit.Test;

import java.lang.reflect.Constructor;
import java.lang.reflect.Field;
import java.lang.reflect.InvocationTargetException;
import java.lang.reflect.Method;

/**
 * @author wangxiang
 * @create 2021/1/1
 */
public class ReflectionTest {

    @Test
    public void test1(){
        Person p1 = new Person("TOM",12);
        p1.age=10;
        System.out.println(p1.toString());
        p1.show();
    }

//    反射后
    @Test
    public void test2() throws NoSuchMethodException, IllegalAccessException, InvocationTargetException, InstantiationException, NoSuchFieldException {
        Class<Person> clazz = Person.class;
//      通过反射，创建Person类的对象
        Constructor cons = clazz.getConstructor(String.class, int.class);
        Person p1 = (Person) cons.newInstance("TOM", 12);
        System.out.println(p1.toString());

//      通过反射，调用对象指定的属性和方法
//        调用属性
        Field age = clazz.getDeclaredField("age");
        age.set(p1,10);
        System.out.println(p1.toString());

//        调用方法
        Method show = clazz.getDeclaredMethod("show");
        show.invoke(p1);

        System.out.println("*************");

//        调用私有的属性构造器方法
//        调用私有构造器
        Constructor cons1 = clazz.getDeclaredConstructor(String.class);
        cons1.setAccessible(true);
        Person p2 = (Person) cons1.newInstance("jerry");
        System.out.println(p2.toString());

//        调用私有属性
        Field name = clazz.getDeclaredField("name");
        name.setAccessible(true);
        name.set(p1,"ROSE");
        System.out.println(p1.toString());

//        调用私有方法
        Method showNation = clazz.getDeclaredMethod("showNation", String.class);
        showNation.setAccessible(true);
        String nation = (String) showNation.invoke(p1, "中国");
        System.out.println(nation);

    }
```



```java
package 反射;

/**
 * @author wangxiang
 * @create 2021/1/1
 */
public class Person {
    private String name;
    public int age;

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    private Person(String name) {
        this.name = name;
    }

    public Person() {
    }

    @Override
    public String toString() {
        return "Person{" +
                "name='" + name + '\'' +
                ", age=" + age +
                '}';
    }

    public void show(){
        System.out.println("你好，我乃孙悟空");
    }

    private String showNation(String nation){
        System.out.println("我的国籍是"+nation);
        return nation;
    }
}
```

​	

### 理解Class类并获取Class实例

```JAVA
//    获取Class的实例的方式
    @Test
    public void test3() throws ClassNotFoundException {
//        方式一：调用运行时类的属性：.class
        Class<Person> clazz1 = Person.class;
        System.out.println(clazz1);

//        方式二：通过运行时类的对象,调用getClass()
        Person p1 = new Person();
        Class<? extends Person> clazz2 = p1.getClass();
        System.out.println(clazz2);

//        方式三：调用Class的静态方法：forName(String classPath) 使用较多
        Class clazz3 = Class.forName("反射.Person");
        System.out.println(clazz3);

//        方式四：使用类的加载器：ClassLoader  了解
        ClassLoader classLoader = ReflectionTest.class.getClassLoader();
        Class clazz4 = classLoader.loadClass("反射.Person");
        System.out.println(clazz4);
    }
```

![image-20210102121530820](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210102121530820.png)

![image-20210102122615922](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210102122615922.png)









### 类的加载与ClassLoader的理解

![image-20210102124517456](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210102124517456.png)

![image-20210102124649316](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210102124649316.png)

![image-20210102130510726](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210102130510726.png)

代码块与显示赋值  谁在前面谁先执行

![image-20210102130732891](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210102130732891.png)

![image-20210102132129613](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210102132129613.png)







### 创建运行时类的对象











### 获取运行时类的对象

```java
package 反射2;

import org.junit.Test;
import 反射1.Person;

import java.lang.annotation.Annotation;
import java.lang.reflect.Constructor;
import java.lang.reflect.ParameterizedType;
import java.lang.reflect.Type;

/**
 * @author wangxiang
 * @create 2021/1/2
 */
public class OtherTest {

    //    获取构造器结构
    @Test
    public void test1() {
        Class<Person> clazz = Person.class;

//        getConstructors()：获取当前运行时类中声明为public的构造器
        Constructor<?>[] constructors = clazz.getConstructors();
        for (Constructor c : constructors) {
            System.out.println(c);
        }
        System.out.println();

//        getDeclaredConstructors():获取当前运行时类中声明的所有构造器
        Constructor<?>[] declaredConstructors = clazz.getDeclaredConstructors();
        for (Constructor c : declaredConstructors) {
            System.out.println(c);
        }
    }

    @Test
    public void test2() {

        Class<Person> clazz = Person.class;
        //        获取运行时类的父类
        Class<? super Person> superclass = clazz.getSuperclass();
        System.out.println(superclass);

        //        获取运行时类带泛型的父类
        Type genericSuperclass = clazz.getGenericSuperclass();
        System.out.println(genericSuperclass);
    }

    //        获取泛型类型
    @Test
    public void test3() {
        Class<Person> clazz = Person.class;
        Type genericSuperclass = clazz.getGenericSuperclass();
        ParameterizedType parameterizedType = (ParameterizedType) genericSuperclass;
        Type[] actualTypeArguments = parameterizedType.getActualTypeArguments();
        System.out.println(((Class) actualTypeArguments[0]).getName());
    }

    //    获取运行时类实现的接口
    @Test
    public void test4() {
        Class<Person> clazz = Person.class;
        Class<?>[] interfaces = clazz.getInterfaces();
        for (Class c : interfaces) {
            System.out.println(c);
        }

        System.out.println();

//      获取运行时类父类的接口
        Class<?>[] interfaces1 = clazz.getSuperclass().getInterfaces();
        for (Class c : interfaces1) {
            System.out.println(c);
        }
    }

    //    获取运行时类所在的包
    @Test
    public void test5() {
        Class<Person> clazz = Person.class;
        Package aPackage = clazz.getPackage();
        System.out.println(aPackage);
    }

    //    获取运行时类声明的注解
    @Test
    public void test6() {
        Class<Person> clazz = Person.class;
        Annotation[] annotations = clazz.getAnnotations();
        for (Annotation a : annotations) {
            System.out.println(a);
        }
    }
}
```





### 调用运行时类的指定结构







### 反射的应用：动态代理

![image-20210103135418449](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210103135418449.png)

![image-20210103140035329](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210103140035329.png)

![image-20210103220056171](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210103220056171.png)

![image-20210103220349283](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210103220349283.png)

![image-20210103223628621](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210103223628621.png)

## Lambda表达式

![image-20210103224241719](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210103224241719.png)

![image-20210103230329897](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210103230329897.png)

![image-20210103230524015](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210103230524015.png)





## 函数式(Functional)接口

如果一个接口中，只声明了一个抽象方法，则此接口就称为函数式接口

![image-20210104134943172](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104134943172.png)

![image-20210104135041404](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104135041404.png)

![image-20210104135440891](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104135440891.png)

![image-20210104135814379](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104135814379.png)







## 方法引用与构造器引用

![image-20210104142732028](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104142732028.png)





## 强大的StreamAPI



![image-20210104162136932](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104162136932.png)

![image-20210104162131890](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104162131890.png)

![image-20210104162328506](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104162328506.png)

![image-20210104162521939](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104162521939.png)

![image-20210104163013531](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104163013531.png)

![image-20210104163414406](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104163414406.png)

![image-20210104163828540](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104163828540.png)

![image-20210104164109842](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104164109842.png)

![image-20210104164756924](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104164756924.png)

![image-20210104164818411](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104164818411.png)

![image-20210104164827392](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104164827392.png)

![image-20210104175013213](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104175013213.png)

![image-20210104175057989](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104175057989.png)

![image-20210104183210236](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104183210236.png)

![image-20210104183157378](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104183157378.png)

![image-20210104183709554](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104183709554.png)

![image-20210104184140744](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104184140744.png)

```java
package StreamAPI;

import com.sun.scenario.effect.impl.sw.sse.SSEBlend_SRC_OUTPeer;
import org.junit.Test;
import org.omg.CORBA.PUBLIC_MEMBER;
import 方法引用.Employee;
import 方法引用.EmployeeData;

import java.util.*;
import java.util.stream.Collectors;
import java.util.stream.IntStream;
import java.util.stream.Stream;

/**
 * @author wangxiang
 * @create 2021/1/4
 */
public class SteamAPITest {
    //    创建Stream方式一：通过集合
    @Test
    public void test1() {

        List<Employee> employees1 = EmployeeData.getEmployees();

//        default Stream<E> stream():返回一个顺序流

        Stream<Employee> stream1 = employees1.stream();

//        default Stream<E> parallelStream():返回一个顺序流
        Stream<Employee> employeeStream = employees1.parallelStream();

//    创建Stream方式一：通过数组
        int[] arr1 = new int[]{1, 2, 3, 4, 5, 6};
        IntStream stream = Arrays.stream(arr1);

        Employee employee2 = new Employee(1001, "TPM");
        Employee employee3 = new Employee(1002, "rose");
        Employee[] arr2 = new Employee[]{employee2, employee3};

        Stream<Employee> stream2 = Arrays.stream(arr2);

//    创建Stream方式三：通过Stream的of()
        Stream<Integer> integerStream = Stream.of(1, 2, 3, 4, 5, 6);

//    创建Stream方式四：创建无限流
//        迭代
        Stream.iterate(0, t -> t + 2).limit(10).forEach(System.out::println);
//        生成
        Stream.generate(Math::random).limit(10).forEach(System.out::println);
    }

    //    筛选与切片
    @Test
    public void test2() {
        List<Employee> employees1 = EmployeeData.getEmployees();

        Stream<Employee> stream = employees1.stream();
        stream.filter(e -> e.getSalary() > 7000).forEach(System.out::println);

        System.out.println();

        employees1.stream().limit(3).forEach(System.out::println);

        System.out.println();

        employees1.stream().skip(3).forEach(System.out::println);

        System.out.println();

        employees1.add(new Employee(1010, "刘强东", 40, 8000));
        employees1.add(new Employee(1010, "刘强东", 40, 8000));
        employees1.add(new Employee(1010, "刘强东", 40, 8000));
        employees1.add(new Employee(1010, "刘强东", 40, 8000));
        employees1.add(new Employee(1010, "刘强东", 40, 8000));

        employees1.stream().distinct().forEach(System.out::println);

    }

    //    映射
    @Test
    public void test3() {
        List<String> list = Arrays.asList("aa", "bb", "cc", "dd");
        list.stream().map(str -> str.toUpperCase()).forEach(System.out::println);

//        练习：获取员工姓名长度大于3的员工的姓名
        List<Employee> employees = EmployeeData.getEmployees();
        Stream<String> namesStream = employees.stream().map(e -> e.getName());
        namesStream.filter(name -> name.length() > 3).forEach(System.out::println);

        ArrayList list1 = new ArrayList();
        list1.add(1);
        list1.add(2);
        list1.add(3);

        ArrayList list2 = new ArrayList();
        list2.add(4);
        list2.add(5);
        list2.add(6);

        list1.addAll(list2);
        System.out.println(list1);

        System.out.println();
//        练习2：
        Stream<Stream<Character>> streamStream = list.stream().map(SteamAPITest::fromStringToStream);
        streamStream.forEach(s -> {
            s.forEach(System.out::println);
        });

        System.out.println();

//        flatMap
        Stream<Character> characterStream = list.stream().flatMap(SteamAPITest::fromStringToStream);
        characterStream.forEach(System.out::println);

        System.out.println();
        List<Integer> list3 = Arrays.asList(12, 34, 56, 854, 8845, 8135, 123);
        list3.stream().sorted().forEach(System.out::println);

        System.out.println();
        List<Employee> employees1 = EmployeeData.getEmployees();
        employees1.stream().sorted((e1, e2) -> {
            int ageValue = Integer.compare(e1.getAge(), e2.getAge());
            if (ageValue != 0) {
                return ageValue;
            } else {
                return -Double.compare(e1.getSalary(), e2.getSalary());
            }
        }).forEach(System.out::println);

    }

    //    将字符串中的多个字符构成的集合转换为对用的Stream的实例
    public static Stream<Character> fromStringToStream(String str) {
        ArrayList<Character> list = new ArrayList<>();
        for (Character c : str.toCharArray()) {
            list.add(c);
        }
        return list.stream();
    }

    //    Stream的终止操作
    @Test
    public void test4() {
//        练习：是否所有的员工的年龄都大于18
        List<Employee> employees = EmployeeData.getEmployees();
        boolean allMatch = employees.stream().allMatch(e -> e.getAge() > 18);
        System.out.println(allMatch);

//        练习：是否存在员工的工作大于1000
        boolean b = employees.stream().anyMatch(e -> e.getSalary() > 10000);
        System.out.println(b);

//        练习:是否存在员工姓"雷"
        boolean lei = employees.stream().noneMatch(e -> e.getName().startsWith("雷"));
        System.out.println(lei);

        Optional<Employee> first = employees.stream().findFirst();
        System.out.println(first);

        Optional<Employee> any = employees.parallelStream().findAny();
        System.out.println(any);

    }

    @Test
    public void test5() {
        List<Employee> employees = EmployeeData.getEmployees();

        long count = employees.stream().filter(e -> e.getSalary() > 5000).count();
        System.out.println(count);

//      练习：返回最高的工资
        Stream<Double> salaryStream = employees.stream().map(e -> e.getSalary());
        Optional<Double> max = salaryStream.max(Double::compare);
        System.out.println(max);

//      练习：返回最低的工资的员工
        Optional<Employee> min = employees.stream().min(Comparator.comparingDouble(Employee::getSalary));
        System.out.println(min);

//        内部迭代
        employees.stream().forEach(System.out::println);

        employees.forEach(System.out::println);
    }

    //    归约
    @Test
    public void test6() {
//        练习：计算1-10的自然数的和
        List<Integer> list = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);
        Integer sum = list.stream().reduce(0, Integer::sum);
        System.out.println(sum);

//        练习：计算公司所有员工工资的总和
        List<Employee> employees = EmployeeData.getEmployees();
        Stream<Double> salaryStream = employees.stream().map(Employee::getSalary);
        Optional<Double> sumMoney = salaryStream.reduce(Double::sum);
        System.out.println(sumMoney);
    }

    //    收集
    @Test
    public void test7(){
        List<Employee> employees = EmployeeData.getEmployees();
//        练习：查找工资大于6000的员工，结果返回一个List或Set
        List<Employee> employeeList = employees.stream().filter(e -> e.getSalary() > 6000).collect(Collectors.toList());
        employeeList.forEach(System.out::println);

        Set<Employee> employeeSet = employees.stream().filter(e -> e.getSalary() > 6000).collect(Collectors.toSet());
        employeeSet.forEach(System.out::println);

    }
}
```





## Optional类

![image-20210104184305711](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104184305711.png)

![image-20210104184656818](C:\Users\13920\AppData\Roaming\Typora\typora-user-images\image-20210104184656818.png)

















