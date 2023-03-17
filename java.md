# java代码规范

1. 对于类，方法的注释，要以javadoc的方式来写。

2. 非java doc的注释，是写给代码的维护者来看的。

3. 使用tab操作，实现缩进默认向右移动，使用shift+tab可使代码整体向左移。

4. 运算符和 = 两边习惯性各加一个空格。

5. 源代码使用utf - 8的编码。

6. 行宽度不要超过80字符。

7. 代码编写需要次行风格和行尾风格（推荐）。

   

# 路径详解

![image-20230307232130533](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345563.png)

## 相对路径

从当前目录开始定位，形成的一个路径

## 绝对路径

从顶级目录d，开始定位，形成的路径

## 需求

从abc\test100访问abc2\test200\hello.txt

## 方法

**相对路径**：..\\..\abc2\test200\hello.txt

**绝对路径**：d:\abc2\test200\hello.txt

## 常用的dos命令

1. 查看当前目录有什么内容 dir dir d:\abc2\test200

2. 切换到其他盘下：cd:change directory

   cd /D c: 

3. 切换到当前盘的其他目录下（使用相对路径和绝对路径分别演示）

   cd d:\abc2\test200 cd ..\\..\abc2\test200

4. 切换到上一级：cd..

5. 切换到根目录 ：cd\ 

6. 查看指定目录下的所有自己目录

   tree d:

7. 清屏cls

8. 退出指令 exit

# java API文档

API(Application Programming Interface,应用程序编程接口)是Java提供的基本编程接口。

中文在线文档：http://www.matools.com

Java类的组织形式

![image-20230309172646567](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345650.png)

使用方法：

1. 包>类>方法
2. 直接搜索

# 字符型本质

## 本质：

字符型存储到计算机中，需要将字符对应的码值（整数）找出来，比如'a'

存储：'a'>码值97>二进制（110 0001）>存储

读取：二进制（110 0001）>97>'a'>显示

## 字符编码表

ASCII(一个字节表示，一个128个字符，实际上一个字节可以表示256个字符，只用128个)

Unicode（固定的编码，使用两个字节来表示字符，字母和汉字统一都是占用两个字节）

utf-8（大小可变的编码，字母使用1个字节，汉字使用3个字节）

gbk（可以表示汉字，范围广，字母使用1个字节，汉字使用2个字节）

big5码（繁体中文，台湾，香港）

# String和基本类型转化

## 基本数据类型转Sting类型

语法：将基本类型的值+""即可实现自动转换

![image-20230309181204762](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345546.png)



## String类型转基本数据类型

语法：通过基本类型的包装类调用parseXX方法即可实现转换

![image-20230309181331052](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345261.png)

怎么把字符串转换成字符char > 将字符串的第一个字符得到

```java
String s5 = "123";
System.out.println(s5.charAt(0));
```

输出为1

## 补充

将String 类型进行转换时，要确保其可以转换成一个有效的数据，比如可以将"123"转换成一个整数，但不会把"hello"转换成一个整数。

# 逻辑运算符

## 介绍



1. 短路与&&，短路或||，取反！
2. 逻辑与&，逻辑或|，逻辑异或^![image-20230309184955245](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345062.png)

a&&b:当a和b同时为true时，结果为ture，否则为flase

a&b:当a和b同时为true时，结果为ture，否则为flase

a|b:当a和b，有一个为true，结果为true，否则为flase

a||b:当a和b，有一个为true，结果为true，否则为flase

!a:当a为true，结果为flase，当a为flase，结果为true

a^b:当a和b不同时，结果为true，否则为flase

## 区别

短路与（&&）和逻辑与（&）

![image-20230309190049724](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345564.png)

![image-20230309190230675](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345213.png)

短路或（||）和逻辑或（|）

![image-20230309190451233](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345576.png)

![image-20230309190517759](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345532.png)

因此在开发中基本使用短路或（||）和短路与（&&），效率更高。

# 标识符

## 标识符规则

1. 由26个英文字母大小写，0-9，——或&组成。

2. 数字不可以开头

3. 不可以使用关键字和保留字，但可以包含。

4. java严格区分大小写，长度无限制。

5. 标识符不能包含空格。

   

## 标识符规范

1. 包名：多单词组成时所有字母都小写：aaa.bbb.ccc//比如 com.yzd.com

2. 类名，接口名：多单词组成时，所有单词首字母大写：XxxYyyZzz[大驼峰]

   比如：ThankShotGame

3. 变量名，方法名：多单词组成时，第一个的单词小写，第二个但那次开始首字母大写：xxxYyyZzz[小驼峰]

   比如：thankShotGame

4. 常量名：所有单词都要大写，多单词之间每个单词都用下划线连接：XXX_YYY_ZZZ

   比如：定义一个所得税率TAX_RATE

   代码规范可以参照[阿里巴巴java开发手册]([前言 · GitBook (1994.github.io)](https://1994.github.io/p3c/))

# 进制

## 介绍

1. 二进制：0，1，满2进1，以0b或0B开头

2. 十进制：0-9，满10进1

3. 八进制：0-7，满8进1，以数字0开头

4. 十六进制：0-9及A（10）-F（15），满16进1，以0x或0X开头表示，此处的A-F不区分大小写

   

举例：

![image-20230309231123642](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345885.png)

## 进制转换

### 十进制转化

#### 二进制转十进制

从最低位（右边）开始，将每位的数提取出来，乘以2的（位数-1）次方，然后求和

![image-20230309233119963](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346832.png)

#### 八进制转十进制

从最低位（右边）开始，将每位的数提取出来，乘以8的（位数-1）次方，然后求和

![image-20230309233205015](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346907.png)

#### 十六进制转十进制

从最低位（右边）开始，将每位的数提取出来，乘以16的（位数-1）次方，然后求和

![image-20230309233435529](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346642.png)

#### 十进制转二进制

将该数不断地除以2，直到商为0为止，然后将每步得到的余数倒过来，就是对应的2进制。

![image-20230309233803291](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346027.png)

#### 十进制转八进制

将该数不断地除以8，直到商为0为止，然后将每步得到的余数倒过来，就是对应的8进制。

![image-20230309233936505](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346301.png)

#### 十进制转十六进制

将该数不断地除以16，直到商为0为止，然后将每步得到的余数倒过来，就是对应的16进制。

![image-20230309234101466](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346673.png)

### 二进制转化

#### 八进制转二进制

将八进制每一位，转化成对应的一个三位的二进制数

![image-20230310194658449](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346630.png)

#### 十六进制转二进制

将十六进制每一位，转化成对应的一个四位的二进制数

![image-20230310194803004](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346745.png)

#### 二进制转八进制

从低位开始，每三位一组，转成对应的八进制数

![image-20230310194414831](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346087.png)

#### 二进制转其十六进制

从低位开始，每四位一组，转成对应的十六进制数

![image-20230310194514926](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346189.png)

## 原码，反码，补码

1. 二进制的最高位是符号位，0代表正数，1代表负数。

2. 正数的原码，反码，补码都一样。

3. 负数的反码=原码符号位不变，其余位取反。

4. 负数的补码=反码+1。

5. 0的反码，补码都是0。

6. Java中的数都是有符号的。

7. 计算机在运算的时候，是以补码的方式进行运算的。

8. 当我们要看结果时需要看它的原码。

   

## 位运算符

按位与&：两位全为1，结果为1，否则为0。

按位或|：两位中有一位为1，结果为1，否则为0。

按位异或^:两位中一个为0，一个为1，结果为1，否则为0.

按位取反：0->1,1->0。

算数右移>>：低价溢出，符号位不变，并且用符号位补溢出的高位。

算数左移<<:符号位不变，低位补0。

逻辑右移>>>:低位溢出，高位补0。

补充：没有<<<符号

# 数组

## 数组赋值

基本数据类型的赋值为值传递。

![image-20230313202506512](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346978.png)

数组在默认情况下是引用传递，赋的是地址的值

![image-20230313202729355](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347020.png)

![image-20230313203441679](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347842.png)

## 数组拷贝

![image-20230313203817984](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347153.png)

![image-20230313203938938](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347447.png)



# 对象内存分布

示例图

![image-20230313221151419](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347838.png)

**注意：**

cat仅仅是对象名（对象引用）

new Cat()创建的对象空间（数据）才是真正的对象

**结构分析：**

1. 栈：一般存放基本数据类型（局部能量）
2. 堆：存放对象（Cat cat,数组）
3. 方法区：常量池（常量，比如字符串），类加载信息

**流程分析：**

1. 先加载Cat类信息（属性和方法信息，只加载一次）
2. 在堆中分配空间，进行默认初始化
3. 进行对象初始化，先默认初始化，接着进行指定初始化，最后完成构造器初始化
4. 把地址付给cat，cat指向对象

# 方法调用机制

![image-20230313231243571](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347615.png)

# 递归

![image-20230315172045420](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347320.png)

# 可变参数

**定义：**

java中允许将同一个类中多个同名同功能但参数个数不同的方法，封装成一个方法，可通过可变参数实现。

**基本语法:**

访问修饰符 返回类型 方法名（数据类型...形参名）{
}

![image-20230316163745830](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347119.png)

**细节注意：**

1. 可变数组的实参可以为0个或任意多个。
2. 可变数组的实参可以为数组。
3. 可变参数的本质就是数组。
4. 可变参数和普通类型的参数一起放在形参列表中，但必须保证可变参数在最后。
5. 一个形参列表只能出现一个可变参数

# IDEA快捷键

1. 删除当前行ctrl+Y
2. 复制当前行ctrl+D
3. 补全代码alt+/
4. 自动导入包或者自动实例化对象alt+enter
5. 快速格式化代码ctrl+alt+L
6. 生成构造器alt+insert(还有其他用法)
7. 查看一个类的层级关系，ctrl+H
8. 将光标放在一个方法上，输入ctrl+B,可以定位到方法
9. 自动分配变量名，加.var

# 包

1. 区分相同名字的类
2. 当类很多时，可以很好的管理类[看java API文档]
3. 控制访问范围

**包基本语法：**

package com.yzd

1. package 关键字，表示打包

2. com.yzd表示包名

   

**包的本质：**

实质上就是创建不同的的文件夹/目录来保存类文件，

![image-20230316215243186](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347713.png)

**命名规则：**

只能包含数字，字母，下划线，小圆点，但不可以用数字开头，不可以是关键字或保留字

![image-20230316220402923](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347864.png)

**命名规范：**

一般是小写字母+小圆点

com.公司名.项目名.业务模块名

列如com.yzd.oa.model

举例：

![image-20230316220647513](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171348570.png)

**常用的包：**

![image-20230316220903599](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171348419.png)

# 访问修饰符

1. 公开级别：public,对外公开
2. 受保护级别：protected，对子类和同一个包中的类公开
3. 默认级别：对同一个包的类公开
4. 私有级别：private，只有类本身可以访问

![image-20230316222347115](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171348081.png)

**注意：**

只有public和默认的可以修饰类

# 继承

## 细节



1. 子类继承了所有的属性和方法，但是私有属性和方法不可以在子类直接访问，要通过公共类方法访问。
2. 子类必须调用父类的构造器，完成父类的初始化
3. java是单继承，一个子类只可以有一个父类，一个父类可以有多个子类

## 本质

![image-20230317174027556](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171740109.png)

![image-20230317174237468](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171742782.png)

