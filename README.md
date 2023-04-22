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

# 方法重写

1. 子类方法的参数，方法名称，要和父类方法的参数，方法名称一致。

2. 子类方法的返回类型要和父类的一致，或者是父类返回类型的子类

   父类的返回类型为Obiect,子类的返回方法可以为String

3. 子类方法不能缩小父类方法的访问权限

   

# 多态

## 方法的多态

1. 方法重载

2. 方法重写

   

## 对象的多态

1. 一个对象的编译类型和运行类型可以不一致
2. 编译类型在定义对象时已经确定，无法改变
3. 运行类型是可以改变的
4. 编译类型看 = 号的左边，运行类型看 = 号的右边



![image-20230317220946420](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303172209586.png)

## 向上转型

**本质：**

父类引用指向子类的对象

**语法：**

父类类型   引用名 = new 子类类型（）;

**特点：**

编译类型看左边，运行类型看右边。

可以调用父类的所有成员（遵循访问权限）

不可以调用子类的特有成员;

最终的运行效果看子类的具体实现

**总结：**

可以调用那些成员看编译类型，具体方法的运行结果先看运行类型

## 向下转型

1. 子类类型  引用名 = （子类类型）父类引用
2. 只能强制转换父类的引用，不可以强转父类的对象
3. 要求父类的引用必须指向的是当前对象目标类型的对象
4. 可以调用子类类型中所有的对象

## 细节

属性没有重写，属性的结果直接看编译类型

instanceOf 用于判断对象的运行类型是否为XX类型或XX类型的子类型

## 动态绑定机制

1. 当调用对象方法时，该方法会和该对象的内存地址/运行类型绑定
2. 属性没有动态绑定机制，哪里声明，就在那里使用

# Object类详解

## equals

**==**是一个比较运算符

1. 既可以判断基本类型，也可以判断引用类型
2. 判断基本类型时，判断的是值是否相等
3. 判断引用类型时，判断的是地址是否相等

**equals**是Object类中的方法，只可以判断引用类型，默认判断地址是否相等，但Integer,String重写了父类方法，用于判断内容是否相等

## hashCode

1. 提高具有哈希结构的容器的效率
2. 两个引用，指向的是同一个对象，哈希值是一样的
3. 两个引用，指向的不是同一个对象，哈希值是不一样的
4. 哈希值主要根据地址号来的，不可以将其完全等价成地址

## toString

**默认返回：**

全类名+@+哈希值的十六进制

子类往往重写toString方法，用于返回对象的属性信息

直接输出一个对象时，等价于调用它的toString方法

# 代码块

没有方法名，没有返回，没有参数，只有方法体，不用通过对象或类显式调用，而是加载类时，或创建对象是隐式调用

## 基本语法

[修饰符]{
代码

}；

**注意：**

1. 修饰符可选，要写的话，只可以写static
2. 代码块分为两类，使用static修饰的是静态代码块，没有修饰的为普通代码块
3. 逻辑语句可以为任意逻辑语句
4. ;号可以有，也可以省略

**好处：**

1. 相当于另一种形式的代码块，对构造器的一种补充形式，可以进行初始化的操作
2. 如果多个构造器中都有重复的语句，可以抽取到初始化代码块中，提高代码的重用性

## 细节

1. static代码块也叫做静态代码块，作用是进行类的初始化，随着类的加载而执行，并且只执行一次，如果是普通代码块，每创建一个对象，就执行一次

2. 类什么时候进行加载：

   1. 创建对象实例化时
   2. 创建子类对象时，父类也会被加载
   3. 使用类的静态成员时

3. 普通的代码块创建一次就会被隐式调用一次，如果只是调用类的静态成员，则不会调用普通代码块

4. 创建一个对象时，在一个类的调用顺序

   1. 调用静态代码块和静态属性初始化（静态代码块和静态属性初始化的优先级一样，如果有多个，则按照他们定义的顺序调用）
   2. 调用普通代码块和普通属性初始化（普通代码块和普通属性初始化的优先级一样，如果有多个，则按照他们定义的顺序调用）
   3. 调用构造器初始化

5. 构造器的最前面隐含了super()和调用普通代码块，新写一个类时，静态相关的代码块，属性初始化，在类加载时就已经完成，因此是优先于构造器和普通代码块的![image-20230320162335021](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303201623440.png)

6. 创建一个子类对象时，他们的静态代码块，静态属性初始化，普通代码块，普通属性初始化，构造方法的调用顺序

   1. 父类的静态代码块和静态属性

   2. 子类的静态代码块和静态属性

   3. 父类的普通代码块和普通属性

   4. 父类的构造方法

   5. 子类的普通代码块和普通属性

   6. 子类的构造方法

      ![image-20230320163648816](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303201636893.png)

      ![image-20230320163816400](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303201638608.png)

      ![image-20230320163853266](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303201638336.png)

      ![image-20230320163926024](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303201639106.png)

      ![image-20230320164000304](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303201640384.png)

7. 静态代码块只可以直接调用静态成员，普通代码块可以调用任意成员

   

# 单例模式

## 饿汉式

![image-20230320190039714](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303201900101.png)

## 懒汉式

![image-20230320191453615](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303201914923.png)

**区别：**

饿汉式和懒汉式的创建时机不同，饿汉式是类加载时创建，懒汉式是使用时才创建

饿汉式：存在资源浪费问题

懒汉式：存在线程安全问题

# final

1. final修饰的属性又叫做常量，一般用XX_XX_XX命名
2. final修饰的属性在定义时必须赋初值，并且不可以修改，可以在以下位置
   1. 定义时
   2. 在构造器中
   3. 在代码块中
3. 如果final修饰的属性是静态的，则初始化的位置只可以是定义时和在代码块时，不可以在构造器中
4. final类不可以继承，但是可以进行实例化对象
5. 如果类不是final类，但是含有final方法，该方法不可以重写，但是可以被继承
6. final 和static往往搭配使用，效率更高，不会导致类加载，底层编译进行了优化处理
7. 包装类都是final类型，不可以被继承
8. 构造器不可以用final修饰

# 抽象类

当父类中一些方法不能确定时，可以使用abstract关键字来修饰，该方法也就成为了抽象方法，用abstract修饰的该类也就是抽象类

## 细节

1. 抽象类不可以被实例化
2. 抽象类中可以没有抽象方法，还可以有实现方法
3. 类中一旦有抽象方法，该类必须时抽象类
4. abstract只可以修饰类和方法
5. 抽象类可以有任意成员（本质还是类）
6. 抽象类不可以有实体
7. 一个类继承了抽象类，则必须实现抽象类的方法，或者本身也是抽象类
8. 抽象方法不可以用privite,final,static来修饰

# 接口

## 基本介绍

语法：

```java
intterface 接口名{
	//属性
	//方法（1.抽象方法 2.默认实现方法 3。静态方法）
}

class 类名 implements 接口{
	自己属性
	自己方法
	必须实现的接口的抽象方法
}
```

**小结：**

1. 在jdk7.0 之前接口中所有的方法都没有方法体

2. 在jdk8.0之后接口可以有静态方法，默认方法，也就是接口中可以有方法的具体实现

   

## 细节

1. 接口不可以被实例化
2. 接口中的所有方法都是public方法，接口中抽象方法，可以不用abstract修饰
3. 一个普通类实现接口，就必须实现接口的所有方法
4. 抽象类实现接口，可以不用实现接口的方法
5. 一个类可以同时实现多个接口
6. 接口中的属性都是final的，而且是public static final 修饰
7. 接口中属性的访问形式：接口名.属性名
8. 接口不可以继承别的类，但是可以继承别的多个接口
9. 接口的修饰符只可以是public和默认的，和类一样

## 接口 VS 继承

当子类继承了父类，就自动拥有了父类的功能

如果子类需要扩展功能，可以通过实现接口的方式扩展

可以理解为，实现接口是对于java 单继承机制的一种补充

## 接口的多态特性

1. 多态参数（接口引用可以指向实现了接口的类的对象实例）

![image-20230321192902785](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303211929401.png)

2. 多态数组

3. 接口的多态传递

   ![image-20230321193537270](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303211935335.png)

# 内部类

一个类的内部有完整的嵌套了另一个类结构，被嵌套的类称为内部类，属于类的第五大成员，**类的成员包含{属性，方法，构造器，代码块，内部类}**

**基本语法：**

```
class Outer{//外部类
	class Inner{
	//内部类
	}
}
class Other{
//外部其他类
}
```

## 局部内部类

**定义：**

定义在外部类的局部位置，通常在方法中，并且有类名

1. 可以直接访问外部类的所有成员，包括私有的
2. 不可以添加访问修饰符，因为它的地位就是一个局部变量，局部变量不可以使用修饰符，但是可以用final修饰，因为局部变量中也含有final
3. 作用域：仅仅在定义它的方法或代码块中
4. 局部内部类--访问--->>外部类的成员（直接访问）
5. 外部类--访问--->局部内部类的成员（创建对象，再进行访问，必须在作用域中）
6. 外部其他类不可以访问局部内部类（因为局部内部类的地位是一个局部变量）
7. 如果外部类和局部内部类的成员重名时，默认遵循就近原则，如果想要访问外部类的成员，则可以使用（外部类名.this.成员）访问

## 匿名内部类

### 介绍

**定义：**

1. 本质是类
2. 内部类
3. 该类没有名字
4. 同时还是一个对象

**基本语法：**

new 类和接口（参数列表）{

​	类体

}；

**方法匿名内部类：**

![image-20230323184903937](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303231849523.png)

**接口匿名内部类：**

![image-20230323185341098](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303231853215.png)

### 细节

**1.基于类调用**

![image-20230323190114944](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303231901621.png)

**2.直接调用**

![image-20230323185957404](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303231859438.png)

3. 可以调用外部类的所有成员，包括私有的
4. 不可以添加访问修饰符，因为它的地位就是一个局部变量
5. 作用域：仅仅在定义它的方法或代码块中
6. 匿名内部类--访问---外部类成员（直接访问）
7. 外部其他类不可以访问内部类（本质就是一个局部变量）
8. 如果外部类和匿名内部类的成员重名时，匿名内部类访问的时候，遵循就近原则，如果想要访问外部类成员，则可以使用（外部类名.this.成员）访问

###  内部类使用

![image-20230323194009442](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303231940540.png)

## 成员内部类

1. 可以访问外部类的所有成员，包括私有的
2. 可以添加任意访问修饰符（public,protected,默认,private），因为它的地位就是一个成员
3. 和外部类的其他成员一样
4. 成员内部类访问外部类，直接访问
5. 外部类访问内部类，创建成员内部类的对象，使用相关的属性
6. 外部其他类访问内部类：
   1. 外部类.内部类 XXX = 外部类.new.内部类（）;
   2. 在外部类中编写一个方法，返回内部类对象

7. 如果外部类和匿名内部类的成员重名时，匿名内部类访问的时候，遵循就近原则，如果想要访问外部类成员，则可以使用（外部类名.this.成员）访问

## 静态内部类

静态内部类是定义了在外部类的成员变量，并且有static修饰

1. 可以直接访问外部类的所有静态变量，包括私有的，但是不可访问非静态成员

2. 可以添加任意访问修饰符（public,protected,默认,private），因为它的地位就是一个成员

3. 作用域:为一个类体

4. 外部类访问内部类，创建成员内部类的对象，使用相关的属性

5. 外部其他类访问内部类

   1. 外部类.内部类 XXX = new 外部类.内部类（）;
   2. 在外部类中编写一个方法，返回内部类对象

   

6. 如果外部类和匿名内部类的成员重名时，匿名内部类访问的时候，遵循就近原则，如果想要访问外部类成员，则可以使用（外部类名.this.成员）访问,如果是静态成员变量，则不用this

# 枚举

## 自定义枚举

1. 将构造器私有化，目的防止直接new
2. 去掉setXxx方法，防止属性被修改
3. 在Season内部，直接创建固定的对象
4. 优化，可以加入 final 修饰符
5. 枚举对象名通常全部大写

![image-20230323215658225](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303232157363.png)

## 关键字实现枚举

1. 使用关键字enum替代class
2. 使用SPRING("春天"，"温暖")，常量名（实参列表）
3. 如果有多个常量，使用,号间隔
4. 使用enum来实现枚举时，先定义常量，写在前面

![image-20230325150843436](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303251508296.png)

### 注意

1. 在使用enum关键字实现枚举时，默认会继承Enum类，而且是final类

   ![image-20230325152054204](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303251520490.png)

2. 如果使用的是无参构造器，则实参列表和小括号可以省略

3. 枚举对象必须放在枚举类的行首

4. enum类不可以在继承其他类，但是可以实现接口

### 常用方法

![image-20230325152701078](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303251527031.png)

# 注解

## Override 

![image-20230325154612873](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303251546369.png)

![image-20230325154805696](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303251548411.png)

1. @Override 只可以修饰方法，不可以修饰别的属性
2. 查看@Override的注解源码为@Target(ElementType.METHOD),说明其只可以修饰方法
3. @Target是修饰注解的注解，称为元注解

## Deprecated

1. @Deprecated 修饰某个元素，表明该元素已经过时，但仍然可以使用
2. 可以修饰方法，类，字段，包，参数等
3. @Deprecated 可以用作版本升级过渡使用

## SuppressWarnings

1. 当我们不希望看到一些警告时，可以使用@SuppressWarings来隐藏警告

2. 在{""}中，可以填入希望抑制的警告信息 

3. 关于SuppressWarnings作用范围和放的位置有关

   

## 元注解

![image-20230325161127812](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201645002.png)

![image-20230325161412614](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201645630.png)

# 异常处理

## 概念

选中代码块 --> 使用ctrl + alt + t -> 选中 try catch

异常分类：

1. error(错误)：Java无法解决的严重问题，比如JVM系统内部错误，资源耗尽
2. Exception：因为编程问题或者偶然的外在因素造成的一般性问题，可以使用针对性的代码进行处理，Exception又分为两大类，运行时异常，编译时异常

## 异常体系图

![image-20230325164022033](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646499.png)

## 五大运行时异常

NullPointerException(空指针异常)

ArithmeticExpection(算术异常)

ArrayIndexOutOfBoundsExpection(数组下标越界异常)

ClassCastException(类转换异常)

NumberFormatExpection(数字格式异常)

## 异常处理机制

**try-catch-finally**

![image-20230325165439950](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646918.png)

**throws**

![image-20230325165809784](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646469.png)

## try-catch

```java
try{
	//可疑代码
	//将异常生成的对应异常对象，传递给catch块
}catch(异常){
	//对异常的处理
}
//如果没有finally也是可以的
```

### 细节

1. 如果异常发生了，则异常发生后面的代码不会进行，直接进入到catch语句
2. 如果没有异常，则顺序执行try代码块，不会进入catch代码块
3. 如果希望无论是否发生异常，都执行某段代码（比如关闭连接，释放资源等），可以使用finall代码块
4. 可以有多个catch代码块，要求子类异常写在前面，父类异常写在后面
5. 也可以使用try-finally配合使用，相当于没有捕获异常，因此程序会直接崩溃/退出

## throws

1. 对于编译异常，必须用throws或者try-catch处理
2. 对于运行异常，如果没有处理，默认用throws处理
3. 子类重写父类方法时，对抛出异常的规定：子类抛出的异常类型要和父类的异常一致，或者是父类抛出异常的子类型
4. 如果在throws过程中，如果有try-catch，则认为异常已经处理

## 自定义异常

1. 自定义异常名继承Exception或者RuntimeException
2. 如果继承Exception,属于编译异常
3. 如果继承RuntimeException,属于运行异常（一般继承RuntimeException）

![image-20230325190748732](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646859.png)

**实例演示：**

![image-20230325191211875](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646405.png)

[更加具体的异常问题参照于锦泉的备忘笔记]（[try-catch,throw和throws的使用 | 锦泉^-^ (arthurjq.com)](https://arthurjq.com/2021/06/01/java/throw/)）

# 常用类

## 包装类

### 概念

![image-20230325195659858](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646573.png)

 **示例图：**![image-20230325200413396](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646141.png)

![image-20230325200442761](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646687.png)

![image-20230325200509466](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646198.png)

### 装箱与拆箱

```java
演示int <--> Integer 的装箱与拆箱
//jdk5之前是手动装箱和拆箱
//手动装箱int -->integer
int n1 =100;
Integer integer = new Integer(n1);
//在jdk9之后在使用会报错显示下面语句
'Integer(int)' is deprecated and marked for removal
//或者
Integer integer1 = Integer.valueOf(n1);

//手动拆箱
//Integer ->int
int i = integer.intValue();

//jdk5之后可以实现自动装箱和拆箱
int n2 = 200;
//自动装箱 Int ->Integer
Integer integer2 = n2;
 //自动拆箱
int n3 = integer2;
```

其余包装类均可以参照int类型

### 包装类方法

**类型转化**

```java
//包装类（Integer）->String
        Integer i = 100;
        //方式一
        String str1 = i + "";
        //方式二
        String str2 = i.toString();
        //方式三
        String str3 = String.valueOf(i);

        //String 转包装类（Integer）
        String str4 = "123456";
        //方式一
        Integer i2 = Integer.parseInt(str4);
        //方式二
        Integer i3 = new Integer(str4);
        //该方法已经被弃用
		'Integer(java.lang.String)' is deprecated and marked for removal
```

可以直接查找某个包装类的方法

![image-20230325223335476](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201647279.png)

一些常用方法

![image-20230325223413125](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201647583.png)

### Integer面试题

![image-20230325224114390](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201647980.png)

```java
//Integer.valueOf源码如下
 @IntrinsicCandidate
    public static Integer valueOf(int i) {
        if (i >= IntegerCache.low && i <= IntegerCache.high)
            return IntegerCache.cache[i + (-IntegerCache.low)];
        return new Integer(i);
    }
```

![image-20230325225251402](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201647746.png)

## String

### 概念

1. String 对象用于保存字符串

2. 字符串的字符使用的是Unicode字符编码，一个字符占两个字节

3. 字符串的字符有许多构造器，实现了构造器重载

4. String类实现了 接口 Serializable[String 可以串行化：可以在网络中传输]

   ​							接口 Comparable [String 对象可以比较大小]

5. String 是final 类， 不可以被其他类继承

6. String 有属性 private final char value[];用于存放字符串内容

7. 注意:value 是一个final类型，不可以被修改（不可以修改地址，不代表是值）

### 创建机制

```java
		//方式一:直接赋值
        String s = "yzd";
        //方式二：调用构造器
        String yzd = new String("yzd");
        //方式一：先从常量池中查看是否有“yzd”，如果有，则直接指向，如果没有则重新创建，然后指向，s最终指向的是常量池中的空间地址
        //方式二：先在堆中创建空间，里面维护了value属性，指向常量池的yzd空间，如果常量池没有“yzd”，重新创建，如果有通过value指向，最终指向的是堆中的空间地址
        
```

![image-20230326205743749](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201647196.png)

### 字符串特性

![image-20230326214107268](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201647559.png)

![image-20230326214039327](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201647128.png)

![image-20230326214003483](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201647568.png)

![image-20230326214238349](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201648082.png)

### Srtring常用方法

![image-20230326215218828](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201648458.png)

## StringBuffer

### 概念

1. StringBuffer的直接父类是AbstractStringBulider

2. StringBuffer 实现了Serialzable,即SttringBuffer的对象可以串行化

3. 在父类 AbstractStringBulider 有属性char[] value,但不是final，该value数组存放字符串内容，因此存放在堆中

4. StringBuffer是final类，不可以被继承

   ![image-20230326222322461](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201648317.png)

### 转换

**构造器使用：**

![image-20230326222825282](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201648425.png)

**类型转化：**

![image-20230326223254775](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201648266.png)

### 常用方法

1. 增：append

2. 删：delete(m,n)

   删除[m,n)的字符

3. 改：replace(m,n,S)

   修改[m,n)的字符改为S

4. 查：indexOf

   查找指定字符在字符串第一次出现的位置，如果找不到就返回-1

5. 插：insert(m,S)

   在原来索引为m的位置插入S字符，原来m位置的字符往后面移动

   

## StringBulider

### 概念

一个可变的字符序列，提供了一个StringBuffer兼容的API，但不可保证同步（不是线程安全的），用在字符串缓冲区被单个线程使用的时候，在可能的情况下，建议优先使用该类

在StringBulider上经常使用的时append,insert

1. StringBulider的直接父类是AbstractStringBulider

2. StringBulider 实现了Serialzable,即SttringBulider的对象可以串行化

3. 在父类 AbstractStringBulider 有属性char[] value,但不是final，该value数组存放字符串内容，因此存放在堆中

4. StringBulider是final类，不可以被继承

5. StringBulider中的方法，没有做互斥的处理，即没有synchronized关键字，因此在单线程情况下使用

![image-20230327195349006](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201649293.png)

![image-20230327195658857](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201649904.png)

## Math

### 常用方法

![image-20230327200551812](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201649615.png)

## Arrays

### sort 排序

![image-20230327202146313](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201649818.png)

![image-20230327202312553](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201649635.png)

![image-20230327202423833](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201649826.png)

![image-20230327202500729](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201649644.png)

### binarySearch查找

![image-20230327203300551](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201650891.png)

### copyOf拷贝

![image-20230327203521337](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201650590.png)

### fill填充

![image-20230327203612757](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201650569.png)

###  asList

![image-20230327203939433](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201650342.png)

## System

### exit

![image-20230327205124141](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201650238.png)

### arraycopy

![image-20230327205438349](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201650659.png)

### currentTimeMillens

![image-20230327205642350](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201650377.png)

## 大数处理

### BigInteger

![image-20230327210342977](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201650720.png)

![image-20230327210354375](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201651735.png)

### BigDecimal

![image-20230327210506144](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201651786.png)

![image-20230327211016497](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201651070.png)

## Date

### 第一代日期类

1. Date:精确到毫秒，代表特定的瞬间
2. SimpleDateFormat：格式和解析日期的类，它允许进行格式化（日期->文本）和解析(文本->日期)和规范化

![image-20230327220025982](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201651680.png)

![image-20230327220045778](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201651965.png)

### 第二代日期类Calendar

![image-20230327220550019](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201651582.png)

### 第三代日期类

**获取时间**

![image-20230327221116195](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201651310.png)

![image-20230327221500230](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201651206.png)

**格式化**

![image-20230327221920088](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652211.png)

**时间戳**

![image-20230327222047457](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652063.png)

# 集合

1. 可以动态的保存任意多个元素

2. 提供了一系列方便的操作对象的方法：add,remove,set,get等

3. 使用集合删除，增加元素更加简单明了

   

## 集合体系图

1. 集合主要是两组（单列集合，双列集合）
2. Collection接口有两个重要的子接口List Set，他们的实现子类都是单列集合
3. Map接口的实现子类是双列集合，存放的K-V

**单列集合**

![image-20230328191004490](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652008.png)

**双列集合**

![image-20230328191253680](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652696.png)

## Collection方法

```java
 List list = new ArrayList();//使用List接口进行接收
        //add添加单个元素
        list.add("tom");
        list.add(10);
        list.add("jack");
        System.out.println("list="+list);
        //remove删除指定元素
        list.remove(0);//删除第一个元素
        list.remove("jack");//删除某个指定元素
        System.out.println("list="+list);
        //contains查询元素是否存在
        System.out.println(list.contains("jack"));
        //size获取元素的个数
        System.out.println(list.size());
        //isEmpty判断是否为空
        System.out.println(list.isEmpty());
        //clear清空
        list.clear();
        //addAll添加多个元素
        ArrayList list1 = new ArrayList();
        list1.add("123");
        list1.add("abc");
        list.addAll(list1);
        //containsALL查找多个元素
        System.out.println(list.containsAll(list1));
        //removeAll三处多个元素
        list.removeAll(list1);
```

## 迭代器遍历

### 介绍

1. Iterator对象称为迭代器，主要用于遍历Collection集合中的元素
2. 实现了Collection接口的集合类都有一个Iterator()方法，用于返回一个实现了Iterator接口的对象，即返回一个迭代器
3. Iterator结构

![image-20230328195852604](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652240.png)

![image-20230328201214868](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652984.png)

**实现迭代器的快捷键-->itit**

**增强for实现遍历**

1. 使用增强for，在Collection集合
2. 增强for，底层依旧是迭代器

```java
for(Object book: col){
	System.out.println("book="+book);
}
```

快捷键方式 I

### 实例演示

```java
import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

public class Main {
    @SuppressWarnings({"all"})
    public static void main(String[] args) {
        List list = new ArrayList();
        list.add(new Dog("小黑", 18));
        list.add(new Dog("小白",16));

        for(Object dog:list){
            System.out.println(dog);
        }
        System.out.println("++++++++++++++++++++++");
        Iterator iterator = list.iterator();
        while(iterator.hasNext()){
            Object dog = iterator.next();
            System.out.println(dog);
        }
    }

}
class Dog{
    private String name;
    private int age;

    public Dog(String name, int age) {
        this.name = name;
        this.age = age;
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

    @Override
    public String toString() {
        return "Dog{" +
                "name='" + name + '\'' +
                ", age=" + age +
                '}';
    }
}
```

## List接口

1. List集合类的元素是有序的（添加顺序和取出顺去是一致的），且可以重复
2. List集合的每个元素都有其对应的顺序索引，即支持索引
3. List容器中的元素都有一个整数型的序号记录其在容器中的位置，可以根据序号存取容器中的元素

![image-20230328205056613](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652456.png)

### 常用方法

```java
 List list = new ArrayList();
        list.add("张三丰");
        list.add("贾宝玉");
        //void add(int index,Object ele):在index位置插入ele元素
        //在index = 1的位置插入一个对象
        list.add(1,"tom");
        System.out.println("list="+list);
        //boolean addAll(int index,Collection eles):从index位置开始将eles中所有元素添加进来
        List list1 = new ArrayList();
        list1.add("jack");
        list1.add("tom");
        list.addAll(1,list1);
        System.out.println("list:"+list);
        //Object get(int index)获取index位置上的元素
        System.out.println(list.get(0));
        //int indexOf(Object obj)返回obj在集合中首次出现的位置
        System.out.println(list.indexOf("tom"));
        //int lastIndexOf(Object  obj):返回obj在当前集合中最后出现的位置
        System.out.println(list.lastIndexOf("tom"));
        //Object remove(int index):移除指定index位置的元素，并返回该元素
        list.remove(0);
        //Object set(int index,Object ele):设置指定位置上index位置的元素为ele，相当于时替换
        list.set(1,"AAA");
        //List subList(int fromIndex,int toIndex):返回从fromIndex到toIndex位置的子集合
        //注意返回的子集合为 fromIndex<=subList<toIndex
        List returnlist = list.subList(0,2);
```

### 遍历方式

```java
import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;
@SuppressWarnings({"all"})
public class Main {
    public static void main(String[] args) {
        //List的实现子类ArrayList,LinkedList,Vector的使用相同
        List list = new ArrayList();
        list.add("张三丰");
        list.add("贾宝玉");
        list.add("jack");
        //遍历
        //1.迭代器
        Iterator iterator = list.iterator();
        while (iterator.hasNext()) {
            Object obj =  iterator.next();
            System.out.println(obj);
        }
        System.out.println("-------------------------");
        //2.增强for循环
        for (Object obj:list) {
            System.out.println(obj);
        }
        System.out.println("-------------------------");
        //3.普通for循环
        for (int i = 0; i < list.size(); i++) {
            System.out.println(list.get(i));
        }
        }


    }

```

## ArrayList

### 注意事项

1. ArrayList可以加入null，并且可以加入多个
2. ArrayList是由数组来实现数据储存的
3. ArrayList基本等同于Vector，除了ArrayList是线程不安全的（执行效率高），在多线程的情况下不建议使用ArrayList

### 扩容机制

1. ArrayList中维护了一个Object类型的数组elementData

   transient Object[] elementData;//transient 表示瞬间，短暂的，表示该属性不会被序列化

2. 当创建ArrayList对象时，如果使用的为无参构造器，则初始elementData的容量为0，第一次添加，则扩容为10，如需要再次扩容，则扩容为1.5倍

3. 如果使用的为指定大小的构造器，则构造器elementData的容量为指定大小，如需扩容，则直接扩容为1.5倍

### 底层分析

![image-20230401192227488](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652126.png)

****

![image-20230401192802815](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652795.png)

![image-20230401194346452](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652809.png)

## Vector

### 注意事项

1. 类型说明

   ![image-20230401201807348](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652279.png)

2. Vector底层也是一个对象数组，protected Object[] elementData

3. Vector是线程同步的，即线程安全，操作方法带有synchronized

   ![image-20230401202014813](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652439.png)

4. 在开发时需要考虑线程安全时，使用Vector

## LinkedList

### 底层结构

1. LinkedList底层实现了双向链表和双端队列特点
2. 可以添加任意元素，包括null
3. 线程不安全，没有实现同步

![image-20230401203940457](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652463.png)

## List集合选择

![image-20230401213715518](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652771.png)

## Set接口

**基本介绍：**

1. 无序（添加和取出的顺序不一致），没有索引
2. 不允许重复元素，所以最多包含一个null

**常用方法：**

和List接口一样，Set接口也是Collection的子接口，因此，常用方法和Collection接口一样

**遍历方法：**

1. 迭代器
2. 增强for

**注意：**但是无法使用索引的方式获取

## HashSet

1. HashSet实现了Set接口

2. HashSet实质上是HashMap

   ```java
   public HashSet(){
   	map = new HashMap<>();
   }
   ```

   

3. 可以存放null值，但是只可以有一个null

4. HashSet不保证元素是有序的，取决于hash后，在确认索引的结果

5. 不可以有重复的元素/对象

### 底层分析

1. 先获取元素的哈希值（hashcode方法）
2. 对哈希值进行运算，得到一个索引值为要存放在哈希表中的位置号
3. 如果该位置没有其他元素，则直接存放，如果位置有其他元素，则需要进行equals判断（并非一定要比较内容），如果相等，则不用添加，如不相等，则以链表的形式添加
4. HashSet的底层是HashMap，第一次添加时，table数组扩容到16，临界值(threshold)是16*0.75（加载因子）=12
5. 如果table数组到了临界值12，就会扩容到32，新的临界值就是32*0.75=24，以此类推
6. 在java8中，如果一条链表的元素个数到达TREEIFY_THRESHOLD(默认为8)，并且table的大小>=MIN_TREEIFY_CAPACITY(默认为64)，就会进行树化（红黑树），否则仍会进行数组扩容机制

## LinkedHashSet

![image-20230405150120866](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201653891.png)

1. LinkedHashSet是HashSet的子类
2. LinkedHashSet底层是LinkedHashMap，底层维护了一个数组+双向链表
3. LinkedHashSet根据元素的hashCOde值来决定元素的储存位置,同时使用链表维护元素的次序，是的元素看起来是以插入顺序保证的
4. LinkedHashSet不允许添加重复元素

## TreeSet

1. 当我们使用无参构造器时，创建的TreeSet，仍然是无序的

2. 使用TreeSet提供的一个构造器，可以传入一个比较器(Comparator)并指定排序规则

   ```java
   public static void main(String[] args) {
           TreeSet treeSet = new TreeSet(new Comparator() {
               @Override
               public int compare(Object o1, Object o2) {
                   return ((String)o1).compareTo((String) o2);
               }
           });
           treeSet.add("tom");
           treeSet.add("jack");
           treeSet.add("jreey");
           System.out.println(treeSet);
       }
   ```

   

## Map接口

1. Map与Collection并列存在，用于保存具有映射关系的数据：Key-Value（双列元素）
2. Map中的key和value可以是任何引用类型的数据，会封装到HAshMap$Node对象中
3. Map中的key不允许重复，当有相同的key时，相当于替换value
4. Map中的Value可以重复
5. Map中的key可以为null,value也可以为null，但是注意key有且仅有一个null,value可以有多个null
6. 常用String类作为Map的key
7. key和value之间存在单向一对一关系，通过key总可以找到对应的value
8. Map存放数据的key-value示意图，一对k-v是放在HashMap$Node中，因为Node实现了Entry接口，有的书也称一堆k-v就是一个Entry

### 常用方法

```java
public static void main(String[] args) {
        Map map = new HashMap();
        //put:添加
        map.put("张三","李四");
        map.put("tom","jack");
        map.put(null,null);
        map.put("liming",null);
        //remove:根据键删除映射关系
        map.remove(null);
        //get:根据键获取值
        Object peo = map.get("张三");
        Object peo1 = map.get("张");
        System.out.println(peo);//李四
        System.out.println(peo1);//null
        //size:获取元素个数
        System.out.println(map.size());
        //isEmpty:判断个数是否为0
        System.out.println(map.isEmpty());
        //clear:清除
        map.clear();
        //containsKey:查找键是否存在
        System.out.println(map.containsKey("tom"));
    }
```

### 遍历方法

```java
 public static void main(String[] args) {
        Map map = new HashMap();
        map.put("张三","李四");
        map.put("tom","jack");
        map.put(null,null);
        map.put("liming",null);
        //第一组:先取出所有的Key,通过Key取出对应的Value
        Set keyset = map.keySet();
        //1.增强for
        for (Object key:keyset) {
            System.out.println(key + "-"+ map.get(key));
        }
        //2.迭代器
        Iterator iterator = keyset.iterator();
        while (iterator.hasNext()) {
            Object key =  iterator.next();
            System.out.println(key + "-" +map.get(key));
        }
        //第二组:把所有的Value取出
        Collection values = map.values();
        //1.增强for
        for (Object value:values) {
            System.out.println(value);
        }
        //2.迭代器
        Iterator iterator1 = values.iterator();
        while (iterator1.hasNext()) {
            Object value =  iterator1.next();
            System.out.println(value);
        }
        //第三组:通过EntrySet来获取 K-V
        Set entrySet = map.entrySet();//使用EntrySet<Map.Entry<K,V>>
        //1.增强for
        for (Object entry:entrySet) {
            Map.Entry m = (Map.Entry)entry;
            System.out.println(m.getKey()+"-"+m.getValue());
        }
        //迭代器
        Iterator iterator2 = entrySet.iterator();
        while (iterator2.hasNext()) {
            Object next =  iterator2.next();
            Map.Entry m = (Map.Entry)next;
            System.out.println(m.getKey()+"-"+m.getValue());
        }
    }
```

**练习**

![image-20230405174709382](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201653710.png)

```java
package demo;

import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;
import java.util.Set;

@SuppressWarnings({"all"})
class Test{
    public static void main(String[] args) {
        Map map = new HashMap();
        map.put("00001",new employee("tom",10000,"00001"));
        map.put("00002",new employee("jerry",20000,"00002"));
        map.put("00003",new employee("jack",30000,"00003"));
        Set keySet = map.keySet();
        System.out.println("第一种");
        for (Object key:keySet) {
            employee em = (employee)map.get(key);
            if(em.getSalary()>18000)
            System.out.println(em);
        }
        System.out.println("第二种");
        Iterator iterator = keySet.iterator();
        while (iterator.hasNext()) {
            Object key =  iterator.next();
            employee em = (employee)map.get(key);
            if(em.getSalary()>18000)
            System.out.println(em);
        }
        System.out.println("第三种");
        Set entrySet = map.entrySet();
        for (Object set:entrySet) {
            Map.Entry m = (Map.Entry)set;
            employee em = (employee) m.getValue();
            if(em.getSalary()>18000)
            System.out.println(em);
        }
        System.out.println("第四种");
        Iterator iterator1 = entrySet.iterator();
        while (iterator1.hasNext()) {
            Object next =  iterator1.next();
            Map.Entry m = (Map.Entry)next;
            employee em = (employee) m.getValue();
            if(em.getSalary()>18000)
            System.out.println(em);
        }
    }
}
@SuppressWarnings({"all"})
class employee{
    private String name;
    private int salary;
    private String id;

    public employee(String name, int salary, String id) {
        this.name = name;
        this.salary = salary;
        this.id = id;
    }

    public int getSalary() {
        return salary;
    }

    @Override
    public String toString() {

        return "employee{" +
                "name='" + name + '\'' +
                ", salary=" + salary +
                ", id='" + id + '\'' +
                '}';
        }


}
```

### 小结

1. Map接口的常用实现类：HashMap,HAshtable和Properties
2. HashMap是Map接口使用频率最高的实现类
3. HashMap是以Key-val对的方式来储存数据的
4. Key不可以重复，但是Value可以重复，允许使用null
5. 如果添加1相同的Key，会覆盖原来的Key-val等于修改
6. 和HashSet相同，不会保证映射的顺序，因为底层是以hash表的方式进行储存
7. HashMap没有实现同步，因此线程是不安全的

## Hashtable

1. 存放的元素是键值对：K-V
2. Hashtable的键和值都不能为null否则会抛出NullPointerException
3. HashTable的使用方法基本上和HashMap一致
4. HashTable是线程安全的，HashMap是线程不安全的

**底层分析：**

1. 底层有数组Hashtable$Entry[] 初始化大小为11
2. 临界值 threshold 8 = 11*0.75
3. 扩容机制：当数量大于临界值时，按照*2+1的方式进行扩容

## Properties

1.  Properties类继承Hashtable类并且实现了Map接口，也是使用键值对的形式进行数据储存

2.  使用特点与Hashtable相似

3.  Properties还用于从xxx.Properties文件中，加载数据到Properties类对象，并进行读取与修改

```java
public static void main(String[] args) {
        Properties properties = new Properties();
        //添加
        properties.put("john",100);
        properties.put("lucy",100);
        properties.put("lic",100);
        //修改
        properties.put("lic",88);
        //查找
        System.out.println(properties.get("lic"));
        //删除
        properties.remove("lic");
    }
```

## TreeMap

1. 当我们使用无参构造器时，创建的TreeMap，仍然是无序的

2. 使用TreeMap提供的一个构造器，可以传入一个比较器(Comparator)并指定排序规则

   ```java
       public static void main(String[] args) {
           TreeMap treeMap = new TreeMap(new Comparator() {
               @Override
               public int compare(Object o1, Object o2) {
                   return ((String)o1).compareTo((String)o2);
               }
           });
           treeMap.put("tom","300");
           treeMap.put("jack","200");
           treeMap.put("areey","100");
           System.out.println(treeMap);
       }
   ```

   

## 集合选择

1. 判断储存类型（一组对象[单列]或一组键值对[双列]）

2. 一组对象[单列]：collection接口

   允许重复：List

   ​		增改多：LinkedList[底层维护了一个双向链表]

   ​		改查多：ArrayList[底层维护 Object类型的可变数组]

   不允许重复：Set

   ​		无序：HashSet[底层是HashMap,维护了一个哈希表（数组+链表+红黑树）]

   ​		排序：TreeSet

   ​		插入和取出顺序一致：LinkedHashSet，维护数组+双向链表

3. 一组键值对：Map

   键无序：HashMap[底层是哈希表 jdk7:数组+链表，jdk8:数组+链表+红黑树]

   键排序：TreeMap

   键插入和取出顺序一致:LinkedHashMap

   读取文件:Propreties

   

## Collections工具类

### 排序

```java
public static void main(String[] args) {
        List list = new ArrayList();
        list.add("tom");
        list.add("smith");
        list.add("jack");
        list.add("miss");
        //reversr(List)反转List中元素的顺序
        Collections.reverse(list);
        //shuffle(List)对元素进行随机排序
        Collections.shuffle(list);
        //sort(List)根据元素的自然顺序进行排序
        Collections.sort(list);
        //sort(List,Comparator)按照指定的顺序进行排序
        // 列如按照字符串的长度进行排序
        Collections.sort(list, new Comparator() {
            @Override
            public int compare(Object o1, Object o2) {
                return ((String)o1).length()-((String)o2).length();
            }
        });
        //swap(List,int,int),将集合i处和集合j处的元素进行交换
        Collections.swap(list,0,1);
        System.out.println(list);
    }
```

### 查找替换

```java
 public static void main(String[] args) {
        List list = new ArrayList();
        list.add("tom");
        list.add("smith");
        list.add("jack");
        list.add("miss");
        //Object max(Collection):根据元素自然排序的最大值
        System.out.println(Collections.max(list));
        //Object max(Collection,Comparator):按照指定的顺序返回集合中的最大元素
        Object maxobj = Collections.max(list, new Comparator() {
            @Override
            public int compare(Object o1, Object o2) {
                return ((String)o1).length()-((String)o2).length();
            }
        });
        System.out.println(maxobj);
        //Object min(Collection)
        //Object min(Collection,Comparator)同上
        //int frequency(Collection,Object)返回集合1中元素出现的次数
        System.out.println(Collections.frequency(list,"tom"));
        //void copy(List dest,List src):将src中的元素拷贝到dest上
        List list1 = new ArrayList();
        //为了完成一次拷贝需要先给list1赋值，避免下标越界
        for (int i = 0; i < list.size(); i++) {
            list1.add("");
        }
        Collections.copy(list1,list);
        System.out.println(list);
        //boolean replaceAll(List list,Object oldVal,Object newVal)
        Collections.replaceAll(list,"tom","汤姆");
        System.out.println(list);
    }
```



# 泛型

1. 泛型又称为参数化类型，是jdk5.0以后出现的新特性，解决数据类型的安全性问题
2. 在类声明或实例化时只需要指定好需要的具体类型即可
3. java泛型可以保证如果程序在编译时没有发生警告，运行就不会产生ClassCastException异常，同时代码更加简洁，健壮
4. 作用：可以在类声明时通过一个标识表示类中某个属性的类型，或者某个方法的返回值类型，或者是参数类型

```java
public class Test {
    public static void main(String[] args) {
        person<String> stringperson = new person<String>("123");
    }
}
class person<E>{
    E s;

    public person(E s) {
        this.s = s;
    }
    public E getS(){
        return s;
    }
}
```

## 语法

 **声明：**

interface接口<T>{}和class类<K,V>{}

1. 其中，T，K，V不代表值，表示类型

2. 任意字母都可以，常用T表示，是Type的缩写

   

实例化:

在类名后面指定类型参数的值（类型）

```java
List<String> strlist = new ArrayList<String>();
Iterator<Customer> iterator = customers.iterator();
```

## 注意事项

1. T,K,V只能是引用类型，不能是基本数据类型

2. 在给泛型指定了类型后，可以传入该类型或者子类型

3. 泛型的定义形式

   ```java
   第一种
   ArrayList<Integer> list1 = new ArrayList<Integer>();
   在实际开发中往往会简写，编译器会进行类型推断
   ArrayList<Integer> list = new ArrayList<>();
   ```

4. ```java
   ArrayList arrayList = new ArrayList();
   相当于
   ArrayList<Object> objects = new ArrayList<>();
   ```

   

   

# 自定义泛型

## 自定义泛型类

**基本语法**

class 类名 <T,R...>{//...表示可以有多个泛型成员}

**注意细节**

1. 普通成员可以使用泛型（属性，方法）
2. 使用泛型的数组，不能进行初始化
3. 静态方法中不能使用类的泛型
4. 泛型类的类型，是在创建对象是确定的
5. 如果在创建对象时，没有指定类型，默认为Object

```java
public class Test {

}
//1. Tiger后面具有泛型，一般将Tiger称为自定义泛型类
//2. T,R,M 为泛型的标识符
//3. 泛型的标识符可以有多个
//4. 普通成员可以使用泛型(属性，方法)
//5. 使用泛型的数组不可以初始化（数组在new时无法确定空间大小）
//6. 静态方法无法使用泛型（在类加载时，类仍未创建，JVM无法完成初始化）

class Tiger<T,R,M>{
    String name;
    R r;
    M m;
    T t;

    public Tiger(String name, R r, M m, T t) {
        this.name = name;
        this.r = r;
        this.m = m;
        this.t = t;
    }
}
```

## 自定义泛型接口

**基本语法**

interface接口名<T,R...>{

}

**注意细节**

1. 接口中，静态成员也不能使用泛型

2. 泛型接口的类型，在继承接口或者实现接口时确定

3. 没有指定类型，默认为Object

   

## 自定义泛型方法

**基本语法**

修饰符 <T,R...> 返回类型 方法名（参数列表）{

}

**注意细节**

1. 泛型方法，可以定义在普通类中，也可以定义在泛型类中
2. 当泛型方法调用时，类型便会确定
3. public void eat(E e){},修饰符后没有<T,R...> eat方法不是泛型方法，而是使用了泛型

# 泛型的继承与通配符

1. 泛型不具备继承性

   ```java
   List<Object> list = new ArraryList<String>();
   //该代码不正确
   ```

2. <?>:支持任意泛型类型

3. <? extends A>:支持A类以及A类的子类，规定了泛型的上限

4. <?super A>:支持A类以及A类的子类，不限于父类，规定了泛型的下限

# JUnit使用

在测试对象前加上@Test，在按下alt+enter,选择添加5.8版本

# 绘图机制

```java
import javax.swing.*;
import java.awt.*;

public class Main extends JFrame {//JFrame对应一个窗口
    private Mypanel mp = null;
    public static void main(String[] args) {
        new Main();
    }

    public Main(){
        //初始化面板
        mp = new Mypanel();
        //把面板放入窗口
        this.add(mp);
        //设置窗口大小
        this.setSize(400,300);
        //当点击窗口的小x程序退出
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setVisible(true);
    }
}
class Mypanel extends JPanel {
    //1. Mypanel是一个画板
    //2. Graphics是一个画笔
    //3. Graphics提供了许多画图方法
    @Override
    public void paint(Graphics g) {
        super.paint(g);//调用父类的方法完成初始化
        //画圆形drawOval
        g.drawOval(10,10,100,100);
        //画直线 drawLine
        g.drawLine(10,10,100,100);
        //画矩形边框 drawRect
        g.drawRect(10,10,50,50);
        //设置画笔颜色 setColor
        g.setColor(Color.green);
        //填充矩形 fillRect
        g.fillRect(10,10,50,50);
        //填充椭圆 fillOval
        g.fillOval(10,10,100,100);
        //画图片 drawImage
        //1.获取图片资源
        Image image = Toolkit.getDefaultToolkit().getImage(Mypanel.class.getResource("Snipaste_2022-11-04_17-36-21.png"));
        g.drawImage(image,10,10,252,168,this);
        //画字符串 drawString
        g.setColor(Color.BLUE);
        g.setFont(new Font("隶书",Font.BOLD,50));
        g.drawString("中国",100,100);
    }
}
```

# 事件处理机制

java事件处理是采用的“委派事件模型”，当事件发生时，产生事件的对象，会把“信息”传递给“事件的监听者”处理，这里所说的“信息”实质上就是java.awt.event事件库里某个类所创建的对象，把它称为事件的对象。

1. 事件源：事件源是一个产生事件的对象，比如按钮，窗口
2. 事件：事件就是承载事件源状态改变的对象，比如当键盘事件，鼠标事件，窗口事件等等，会生成一个事件对象，该对象保存着当前事件很多信息，比如KeyEvent对象有含有被按下键的Code值，java.awt.event包和javax.swing.event包中定义了各种事件类型

# 多线程

1. 线程是由进程创建的，是进程的一个实体
2. 一个进程可以拥有多个线程
3. 单线程：同一时刻，只允许执行一个线程
4. 多线程：同一时刻，可以执行多个线程
5. 并发：同一时刻，多个任务交替执行，造成一种“貌似同时”的错觉，单核cpu实现的多任务就是并发
6. 并行：同一个时刻，多个任务同时进行，多核cpu可以实现并行

## 继承Thread

**简单演示：**

```java
public class Main {
    public static void main(String[] args) {
        //创建一个Cat对象，可以当作线程使用
        Cat cat = new Cat();
        cat.start();//启动线程
    }
}
class Cat extends Thread{
    //1.当一个类继承了Thread类，该类本身可以被当作线程使用
    //2.我们会重写run方法，写上自己的业务代码
    //3. run Thread类实现了Runnable接口的run方法
    /*
    @Override
    public void run() {
        Runnable task = holder.task;
        if (task != null) {
            task.run();
        }
    }
     */
    int times;
    @Override
    public void run() {//重写run方法
        //每隔一秒在控制台输出一次
        while(true) {
            System.out.println("喵喵，我是小猫咪"+(++times));
            //让该线程休眠一秒
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                throw new RuntimeException(e);
            }
            if(times==8){
                break;
            }
        }
    }
}
```

### 多线程机制

```java
public class Main {
    public static void main(String[] args) throws InterruptedException {
        //创建一个Cat对象，可以当作线程使用
        Cat cat = new Cat();
        cat.start();//启动线程->最终会执行Cat的run方法
        /*
            public void start() {
            synchronized (this) {
                // zero status corresponds to state "NEW".
                if (holder.threadStatus != 0)
                    throw new IllegalThreadStateException();
                start0();
            }
        }
        真正实现多线程的是start0方法
         */
        //当main线程启动一个子线程Thread-0,主线程不会阻塞，继续进行
        for (int i = 0; i < 60; i++) {
            System.out.println("主线程进行"+i);
            Thread.sleep(1000);
        }
    }
}
class Cat extends Thread{
    //1.当一个类继承了Thread类，该类本身可以被当作线程使用
    //2.我们会重写run方法，写上自己的业务代码
    //3. run Thread类实现了Runnable接口的run方法
    /*
    @Override
    public void run() {
        Runnable task = holder.task;
        if (task != null) {
            task.run();
        }
    }
     */
    int times;
    @Override
    public void run() {//重写run方法
        //每隔一秒在控制台输出一次
        while(true) {
            System.out.println("喵喵，我是小猫咪"+(++times));
            //让该线程休眠一秒
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                throw new RuntimeException(e);
            }
            if(times==80){
                break;
            }
        }
    }
}
```

## 实现Runnable

```java
public class Test {
    public static void main(String[] args) {
        Dog dog = new Dog();
        //dog.start();无法调用start
        //创建Thread对象，把dog对象(实现了Runnable)放入Thread
        Thread thread = new Thread(dog);
        thread.start();
    }
}
class Dog implements Runnable{
    int count;
    @Override
    public void run() {
        while (true){
            System.out.println("汪，小狗汪汪叫"+(++count)+" 线程名称:"+Thread.currentThread().getName());
            //休眠一秒
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                throw new RuntimeException(e);
            }
            if (count==10){
                break;
            }
        }
    }
}

```

![image-20230408215451325](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201653152.png)

## 线程终止

1. 当线程完成任务后，会自动退出
2. 还可以通过使用变量来控制run()方法退出的方式停止线程，即通知方式

```java
public class Test {
    public static void main(String[] args) throws InterruptedException {
        Dog dog = new Dog();
        //dog.start();无法调用start
        //创建Thread对象，把dog对象(实现了Runnable)放入Thread
        Thread thread = new Thread(dog);
        thread.start();
        //main方法休眠10s后退出
        Thread.sleep(10*1000);
        dog.setLoop(false);
    }
}
class Dog implements Runnable{
    int count;
    private boolean Loop = true;

    public void setLoop(boolean loop) {
        Loop = loop;
    }

    @Override
    public void run() {
        while (Loop){
            System.out.println("汪，小狗汪汪叫"+(++count)+" 线程名称:"+Thread.currentThread().getName());
            //休眠一秒
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                throw new RuntimeException(e);
            }
            }
        }
    }
```

## 常用方法

**第一组：**

1. setName：设置线程名称
2. getName: 返回该线程的名称
3. start: 使该线程开始执行，java虚拟机底层调用该线程的start0方法
4. run:调用该线程对象的run方法
5. setPriority:更改线程的优先级
6. getPriority: 获取线程的优先级
7. sleep: 在指定的毫秒数内让当前执行的线程休眠
8. interrupt:中断线程

**第二组：**

1. yield:线程的礼让，让出cpu，让其他线程执行，但礼让的时间不一定确定，所以礼让不一定成功。

2. join：线程的插队，插队的线程一旦成功，则先执行完插入的线程的所有任务。

   ```java
   public class Test {
       public static void main(String[] args) throws InterruptedException {
           Dog dog = new Dog();
           //dog.start();无法调用start
           //创建Thread对象，把dog对象(实现了Runnable)放入Thread
           Thread thread = new Thread(dog);
           thread.start();
           //输出五次hello后中断
           for (int i = 0; i < 20; i++) {
               Thread.sleep(1000);
               System.out.println("主线程吃包子"+i);
               if (i==5){
                   thread.join();
               }
           }
       }
   }
   class Dog implements Runnable{
       int count;
   
       @Override
       public void run() {
               for (int i = 0; i < 20; i++) {
                   try {
                       Thread.sleep(1000);
                   } catch (InterruptedException e) {
                       throw new RuntimeException(e);
                   }
                   System.out.println("子线程吃包子"+i);
               }
           }
       }
   ```

   

## 守护线程

1. 用户线程：也称为工作线程，当线程的任务执行完或通知方式结束
2. 守护线程：一般是为工作线程服务，当所有的用户线程结束，守护线程自动结束
3. 常见的守护线程：垃圾回收机制

```java
public class Test {
    public static void main(String[] args) throws InterruptedException {
        Dog dog = new Dog();
        //dog.start();无法调用start
        //创建Thread对象，把dog对象(实现了Runnable)放入Thread
        Thread thread = new Thread(dog);
        //将子线程设置为守护线程，当主线程结束时随之结束
        thread.setDaemon(true);
        thread.start();
        for (int i = 0; i < 10; i++) {
            Thread.sleep(1000);
            System.out.println("主线程吃包子"+i);
        }
    }
}
class Dog implements Runnable{
    int count;

    @Override
    public void run() {
            for (int i = 0; i < 20;i++ ) {
                try {
                    Thread.sleep(1000);
                } catch (InterruptedException e) {
                    throw new RuntimeException(e);
                }
                System.out.println("子线程吃包子"+i);
            }
        }
    }
```

## 线程的七大状态

![image-20230409184114472](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201653002.png)

## 线程同步机制

1. 在多线程编程中，一些敏感数据不允许被多个线程同时访问，此时就使用同步访问技术，保证数据在任意同一时刻，最多有一个线程访问，以保证数据的完整性
2. 当有一个线程在对内存进行操作时，其他线程都不可以对这个内存地址进行操作，直到该线程完成操作，其他线程才可以对该内存地址进行操作

**实现方法：**

1. 同步代码块

   ```java
   synchronized(对象){//得到对象的锁，才能操作同步代码
   	//需要被同步的代码
   }
   ```

2. synchronized还可以放在方法声明中，表示整个方法为同步方法

   ```java
   public synchronized void m(String name){
   	//需要同步的代码
   }
   ```

   

## 互斥锁

1. java语言中，引入了对象互斥锁的概念，来保证共享数据的完整性
2. 每一个对象都对应一个可称为"互斥锁"的标记，这个标记用来保证在任意时刻，只能有一个线程来访问该对象
3. 关键字synchronized来与对象的互斥锁联系，当某个对象用synchronized修饰时，表明该对象在任一时刻只能有一个线程访问
4. 同步的局限性：导致程序的执行效率要降低
5. 同步方法（非静态的）的锁可以是this，也可以是其他对象（要求是同一个对象）
6. 同步方法（静态的）的锁为当前类本身

## 线程死锁

```java
public class Test {
    public static void main(String[] args) throws InterruptedException {
        DeadLock a = new DeadLock(true);
        DeadLock b = new DeadLock(false);
        new Thread(a).start();
        new Thread(b).start();
    }
}
class DeadLock implements Runnable{

    static Object o1 = new Object();
    static Object o2 = new Object();
    boolean flag;

    public DeadLock(boolean flag) {
        this.flag = flag;
    }

    @Override
    public void run() {
            if (flag){
                synchronized (o1){
                    System.out.println("1");
                    synchronized (o2){
                        System.out.println("2");
                    }
                }
            }else {
                synchronized (o2){
                    System.out.println("3");
                    synchronized (o1){
                        System.out.println("4");
                    }
                }
            }
        }
    }
```

## 释放锁

1. 当代码块的同步方法，同步代码块执行结束
2. 当前线程在同步方法，同步代码块中遇到break,return 
3. 当前线程在同步方法，同步代码块中出现了未处理的Error或Exception，导致异常结束
4. 当前线程在同步方法，同步代码块中执行了线程对象的wait()方法，当前线程暂停，并且释放锁

**不会释放锁的情况：**

1. 线程在执行同步方法，同步代码块中，程序调用了Thread.sleep(),Thread.yield()方法1暂停线程的执行，不会释放锁
2. 线程在执行同步代码块时，其他线程调用了该线程的suspend()方法将线程挂起，该线程不会释放锁（尽量避免使用suspend()和resume()来控制线程，方法不再推荐使用）

# IO流

流：数据在数据源（文件）和程序（内存）之间经历的路径

输入流：数据从数据源（文件）到程序（内存）的路径

输出流：数据从程序（内存）到数据源（文件）的路径

![image-20230417210408674](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201653996.png)

## 创建文件

```java
import java.io.File;
import java.io.IOException;
public class Main {

    public static void main(String[] args) {
        //方式一：new File(String pathname)
        //根据路径构建一个File对象
        String filePath = "e:\\test.txt";
        File file = new File(filePath);
        try {
            file.createNewFile();
            System.out.println("创建成功");
        } catch (IOException e) {
            throw new RuntimeException(e);
        }
        //方法二；new File(File parent,String child)
        //根据父目录文件+子路径构建
        File parenrfile = new File("e:\\");
        String filename1 = "test1.txt";
        //此处的file仅仅是一个对象，只有进行下面的creatNewFile才会有文件产生
        File file1 = new File(parenrfile, filename1);
        try {
            file1.createNewFile();
            System.out.println("创建成功");
        } catch (IOException e) {
            throw new RuntimeException(e);
        }
        //方法三：new File(String parent,String child)//根据父母录+子路径构建
        String parentPath = "e:\\";
        String filename2 = "test2.txt";
        File file2 = new File(parentPath, filename2);
        try {
            file2.createNewFile();
            System.out.println("创建成功");
        } catch (IOException e) {
            throw new RuntimeException(e);
        }
    }
}

```

## 获取文件信息

```java
import java.io.File;

public class Test {

    public static void main(String[] args) {
        new Test().info();
    }
    //获取文件信息
    public void info(){
        //创建文件对象
        File file = new File("E:\\teat.txt");
        //调用相应的方法，得到对应信息
        System.out.println("文件名:"+file.getName());
        System.out.println("文件绝对路径:"+file.getAbsoluteFile());
        System.out.println("文件父级目录:"+file.getParent());
        System.out.println("文件大小(字节):"+file.length());
        System.out.println("文件是否存在:"+file.exists());
        System.out.println("是否为一个文件:"+file.isFile());
        System.out.println("是否为一个目录:"+file.isDirectory());
    }
}

```

## 目录操作

```java
import java.io.File;

public class Test {

    public static void main(String[] args) {
        new Test().m();
        new Test().m2();
        new Test().m3();
    }
    //判断文件e:\test.txt是否存在，存在就删除
    public void m(){
        String filePath = "e:\\test.txt";
        File file = new File(filePath);
        if (file.exists()){
            if(file.delete()){
                System.out.println(filePath+"删除成功");
            }
            else {
                System.out.println(filePath+"删除失败");
            }
        }else {
            System.out.println("该文件不存在");
        }
    }
    //判断目录d:\demo1是否存在，存在就删除
    public void m2(){
        String filePath = "d:\\demo1";
        File file = new File(filePath);
        if (file.exists()){
            if(file.delete()){
                System.out.println(filePath+"删除成功");
            }
            else {
                System.out.println(filePath+"删除失败");
            }
        }else {
            System.out.println("该目录不存在");
        }
    }
    //判断目录e:\\demo\\a\\b,是否存在，没有就创建
    public void m3(){
        String filePath = "e:\\demo\\a\\b";
        File file = new File(filePath);
        if (file.exists()){
            System.out.println("该目录存在");
        }else {
            //使用mkdirs创建多级目录，使用mkdir创建一级目录
                if(file.mkdirs()){
                    System.out.println(filePath+"创建成功");
                }
                else {
                    System.out.println(filePath+"创建失败");
                }
        }
    }
}

```

## IO流原理

分类：

1. 按操作数据单位不同分为：字节流二进制文件，字符流文本文件
2. 按数据流的流向不同分为：输入流，输出流
3. 按流的角色不同分为：节点流，处理流/包装流

| 抽象基类 | 字节流       | 字符流 |
| -------- | ------------ | ------ |
| 输入流   | InputStream  | Reader |
| 输出流   | OutputStream | Writer |

1. java IO流的共涉及40多个类，实际上非常规则，都是从如上4个抽象基类派生的
2. 由着四个类派生的子类名称都是以其父类名作为子类后缀

## FileInputStream

![image-20230420193357077](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222319800.png)

```java
import java.io.FileInputStream;
import java.io.IOException;

public class Test {

    public static void main(String[] args) {

    }
    //使用read()读取
    @org.junit.jupiter.api.Test
    public void readFile(){
        String filePath = "e:\\test.txt";
        FileInputStream fileInputStream = null;
        int readData = 0;
        try {
            //创建fileInputStream对象
             fileInputStream = new FileInputStream(filePath);
            //从该输入流读取一个字节的数据，如没有输入，该方法停止
            //当返回-1时表示完成
            while ((readData = fileInputStream.read()) !=-1){
                System.out.print((char)readData);
            }
        } catch (IOException e) {
            throw new RuntimeException(e);
        }finally {
            //关闭文件流释放资源
            try {
                fileInputStream.close();
            } catch (IOException e) {
                throw new RuntimeException(e);
            }
        }
    }
    @org.junit.jupiter.api.Test
    //使用read(byte [])读取
    public void readFile1(){
        String filePath = "e:\\test.txt";
        FileInputStream fileInputStream = null;
        byte [] buffer = new byte[8];
        int len;
        try {
            //创建fileInputStream对象
            fileInputStream = new FileInputStream(filePath);
            //从该输入流读取一个字节的数据，如没有输入，该方法停止
            //当返回-1时表示完成
            //如果读取正常返回实际读取字节数
            while ((len = fileInputStream.read(buffer)) !=-1){
                System.out.print(new String(buffer,0,len));
            }
        } catch (IOException e) {
            throw new RuntimeException(e);
        }finally {
            //关闭文件流释放资源
            try {
                fileInputStream.close();
            } catch (IOException e) {
                throw new RuntimeException(e);
            }
        }
    }
}

```

## FileOutputStream

![image-20230420200653426](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222319928.png)

```java
import java.io.FileOutputStream;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {

    }
    @org.junit.jupiter.api.Test
    public void writeFile(){
        //创建FileOutPutStream
        String filePath = "e:\\test.txt";
        FileOutputStream fileOutputStream = null;
        try {
            // 得到fileOutputStream对象
            // 1.new FileOutputStream(filePath)会覆盖原来内容
            // 2.new FileOutputStream(filePath,true)会追加原来内容
            fileOutputStream = new FileOutputStream(filePath);
            //写入一个字节
            fileOutputStream.write('a');
            //写入一个字符串
            String str = "hello word";
            fileOutputStream.write(str.getBytes());
            //写入一个字符串,控制写入长度
            fileOutputStream.write(str.getBytes(),0,str.length());
        } catch (IOException e) {
            throw new RuntimeException(e);
        }finally {
            try {
                fileOutputStream.close();
            } catch (IOException e) {
                throw new RuntimeException(e);
            }
        }
    }
}
```

## 文件拷贝

```java
import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        //文件拷贝 将C:\\Users\\17946\\Pictures\\1.png拷贝到E:\\
        //1.创建文件的输入流，将文件输入到程序
        //2.创建文件的输出流，将程序输出到文件
        FileInputStream fileInputStream = null;
        FileOutputStream fileOutputStream = null;
        String srcFilePath = "C:\\Users\\17946\\Pictures\\1.png";
        String destFilePath = "E:\\1.png";

        try {
            fileInputStream = new FileInputStream(srcFilePath);
            fileOutputStream = new FileOutputStream(destFilePath);
            //定义一个字节数组
            byte[] bytes = new byte[1024];
            int readLen = 0;
            while ((readLen = fileInputStream.read(bytes))!=-1){
                fileOutputStream.write(bytes,0,readLen);//一定要使用这个方法
            }
            System.out.println("拷贝成功");
        } catch (IOException e) {
            throw new RuntimeException(e);
        } finally {
            if (fileInputStream!=null){
                try {
                    fileInputStream.close();
                } catch (IOException e) {
                    throw new RuntimeException(e);
                }
            }
            if (fileOutputStream!=null){
                try {
                    fileOutputStream.close();
                } catch (IOException e) {
                    throw new RuntimeException(e);
                }
            }
        }
    }

}
```

## FileReader

![image-20230422145209611](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222319048.png)

**相关方法：**

1. new FileReader(File/String)
2. read:每次读取单个字符，返回该字符，如果读到文件末尾返回-1
3. read(char[]):批量读取多个字符到数组，返回读取到的字符数，如果到文件末尾返回-1

相关API：

1. new String(char[]):将char[]转换成String
2. new String(char[],off,len):将char[]指定部分转换成String

```java
//单个字符读取文件
import java.io.FileReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        String filePath = "E:\\test.txt";
        //创建fileReader对象
        FileReader fileReader = null;
        int data = ' ';
        try {
            fileReader = new FileReader(filePath);
            //循环读取
            while ((data = fileReader.read())!=-1){
                System.out.print((char)data);
            }
        } catch (IOException e) {
            throw new RuntimeException(e);
        } finally {
            if (fileReader!=null){
                try {
                    fileReader.close();
                } catch (IOException e) {
                    throw new RuntimeException(e);
                }
            }
        }
    }

}
```

```java
//字符数组读取
import java.io.FileReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        String filePath = "E:\\test.txt";
        //创建fileReader对象
        FileReader fileReader = null;
        int datalen = 0;
        char[] chars = new char[8];
        try {
            fileReader = new FileReader(filePath);
            //循环读取
            while ((datalen = fileReader.read(chars))!=-1){
                System.out.print(new String(chars,0,datalen));
            }
        } catch (IOException e) {
            throw new RuntimeException(e);
        } finally {
            if (fileReader!=null){
                try {
                    fileReader.close();
                } catch (IOException e) {
                    throw new RuntimeException(e);
                }
            }
        }
    }

}
```



## FileWriter

![image-20230422152413409](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222319725.png)

1. new FileWriter(File/String):覆盖模式，相当于流的指针在首端
2. new FileWriter(File/String,true):追加模式，相当于流的模式在尾端
3. write(int):写入单个字符
4. write(char[]):写入指定数组
5. write(char[],off,len):写入指定数组的指定部分
6. write(string):写入整个字符串
7. write(string,off,len):写入字符串的指定部分

相关API：String类：toCharArray:将String转换成char[]

注意：FileWriter使用后，必须要关闭（close）或刷新（flush），否则写入不到指定文件

```java
import java.io.FileWriter;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        String filePath = "E:\\test.txt";
        //创建fileReader对象
        FileWriter fileWriter = null;
        char[] ch = {'a','b','c'};
        try {
            fileWriter = new FileWriter(filePath);
//            1. write(int):写入单个字符
            fileWriter.write('H');
//            2. write(char[]):写入指定数组
            fileWriter.write(ch);
//            3. write(char[],off,len):写入指定数组的指定部分
            fileWriter.write("abnb".toCharArray(),0, ch.length);
//            4. write(string):写入整个字符串
            fileWriter.write("aba");
//            5. write(string,off,len):写入字符串的指定部分
            fileWriter.write("aba",0,3);

        } catch (IOException e) {
            throw new RuntimeException(e);
        } finally {
            if (fileWriter!=null){
                try {
                    fileWriter.close();
                } catch (IOException e) {
                    throw new RuntimeException(e);
                }
            }
        }
    }

}
```

## 节点流 处理流

1. 节点流：节点流可以从一个特定的数据源读写数据，如FileReader,FileWriter
2. 处理流：（也叫包装流）是连接已经存在的流（节点流或处理流）之上，为程序提供更为强大的读写功能，如BufferedReder,BufferedWriter

区别：

1. 节点流是底层流 / 低级流，直接跟数据源相关。
2. 处理流（包装流）包装节点流，既可以消除不同节点流的实现差异，也可以提供更方便的方法来完成输入输出
3. 处理流（包装流）对节点流进行包装，使用了修饰器设计模式，会直接和数据源相连

处理流的功能主要体现在以下两个方面：

1. 性能的提高：主要以增加缓冲的方式来提高输入输出的效率
2. 操作的便捷：处理流肯提供一系列便捷的方法来一次输入输出大批的数据，使得操作更加灵活方便

## BufferedReader

```java
import java.io.BufferedReader;
import java.io.FileReader;

public class Main {
    public static void main(String[] args) throws Exception {
        String filePath = "E:\\test.txt";
        //创建BufferedReader
        BufferedReader bufferedReader = null;
        bufferedReader = new BufferedReader(new FileReader(filePath));
        //读取
        String line;//按行读取
        while ((line = bufferedReader.readLine())!=null){
            System.out.println(line);
        }
        //关闭流，只需要关闭处理流，系统会自动关闭节点流
        bufferedReader.close();
    }

}
```



## BufferedWriter

```java
import java.io.BufferedWriter;
import java.io.FileWriter;

public class Main {
    public static void main(String[] args) throws Exception {
        String filePath = "E:\\test.txt";
        //创建BufferedWriter
        //如果需要以追加的方式写入，在FileWriter加入true
        BufferedWriter bufferedWriter = null;
        bufferedWriter = new BufferedWriter(new FileWriter(filePath));
        bufferedWriter.write('a');
        //插入和系统相关的换行符
        bufferedWriter.newLine();
        bufferedWriter.write("dfghjkl");
        bufferedWriter.close();
    }

}
```

## Buffered拷贝

```java
import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.FileReader;
import java.io.FileWriter;

public class Main {
//  BufferedWriter和BufferedReader是处理字符的
//  操作二进制文件可能会造成文件损坏
    public static void main(String[] args) throws Exception {
        String srcPath = "E:\\test.txt";
        String destPath = "E:\\test1.txt";
        BufferedReader bufferedReader = null;
        bufferedReader = new BufferedReader(new FileReader(srcPath));
        BufferedWriter bufferedWriter = null;
        bufferedWriter = new BufferedWriter(new FileWriter(destPath));
        String line;
        while ((line = bufferedReader.readLine())!=null){
            bufferedWriter.write(line);
            bufferedWriter.newLine();
        }
        bufferedReader.close();
        bufferedWriter.close();
    }

}
```

## Buffered字节处理

```java
import java.io.BufferedInputStream;
import java.io.BufferedOutputStream;
import java.io.FileInputStream;
import java.io.FileOutputStream;

public class Main {

    public static void main(String[] args) throws Exception {
        String srcPath = "C:\\Users\\17946\\Pictures\\微信图片_20230413222042.jpg";
        String destPath = "E:\\1.jpg";
        BufferedInputStream bufferedInputStream = null;
        bufferedInputStream = new BufferedInputStream(new FileInputStream(srcPath));
        BufferedOutputStream bufferedOutputStream = null;
        bufferedOutputStream = new BufferedOutputStream(new FileOutputStream(destPath));
        byte[] bytes = new byte[1024];
        int datalen =0;
        while ((datalen = bufferedInputStream.read(bytes))!=-1){
            bufferedOutputStream.write(bytes,0,datalen);
        }
        bufferedInputStream.close();
        bufferedOutputStream.close();
    }

}
```

## 对象处理流

1. 序列化：保存值和数据类型

2. 反序列化：将保存在文件的值和数据类型恢复成对象

3. 需要让某个对象支持序列化机制，必须让这个类可序列化，则必须实现如下两个接口

   1. Serialized
   2. Externalizable该接口需要实现，一般使用第一种

   

![image-20230422191417691](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222319905.png)

![image-20230422191529621](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222319804.png)

## ObjectOutputStream

```java
import java.io.FileOutputStream;
import java.io.ObjectOutputStream;

public class Main {

    public static void main(String[] args) throws Exception {
        //在进行序列化时，按照自己的格式进行，文件名后缀没有实际意义
        String filePath = "e:\\a.txt";
        ObjectOutputStream oos = null;
        oos = new ObjectOutputStream(new FileOutputStream(filePath));
        //序列化对象到文件中
        //int -> Integer(Integer实现了serialized接口)
        oos.writeInt(100);
        oos.writeBoolean(true);//boolean -> Boolean
        oos.writeChar('a');
        oos.writeUTF("asdfgh");
        oos.writeObject(new Dog("旺财"));
        oos.close();
        System.out.println("序列化完成");
    }

}

```

```java
import java.io.Serializable;

public class Dog implements Serializable {
    private String name;

    public Dog(String name) {
        this.name = name;
    }

    @Override
    public String toString() {
        return "Dog{" +
                "name='" + name + '\'' +
                '}';
    }
}
```



## ObjectInputStream

```java
import java.io.FileInputStream;
import java.io.ObjectInputStream;

public class Main {

    public static void main(String[] args) throws Exception {
        //指定进行反序列化的文件
        String filePath = "e:\\a.txt";
        ObjectInputStream ois = null;
        ois = new ObjectInputStream(new FileInputStream(filePath));
        //读取的顺序和序列化的顺序一致
//        oos.writeInt(100);
//        oos.writeBoolean(true);//boolean -> Boolean
//        oos.writeChar('a');
//        oos.writeUTF("asdfgh");
//        oos.writeObject(new Dog("旺财"));
        System.out.println(ois.readInt());
        System.out.println(ois.readBoolean());
        System.out.println(ois.readChar());
        System.out.println(ois.readUTF());
        Object dog = ois.readObject();
        System.out.println(dog);
        ois.close();
        System.out.println("反序列化完成");
    }

}


```

**重点细节：**

在调用Dog方法时需要向下转型，因此我们需要将Dog类的定义放在可以引用的位置

**细节：**

1. 读写顺序一致
2. 要求序列化或反序列化对象，需要实现Serizlizable
3. 序列化的类中建议添加SerialVersionUID，为了提高版本的jianrx
4. 序列化对象时，默认将里面的所有属性都进行序列化，但是除了static或transient修饰的成员
5. 序列化对象时，要求里面的属性也需要实现序列化接口
6. 序列化具备可继承性，如果某类实现了序列化，则其子类也默认实现了序列化

## 标准输入输出流



|                     | 类型        | 默认设备 |
| :-----------------: | ----------- | :------: |
| System.in 标准输入  | InputStream |   键盘   |
| System.out 标准输出 | PrintStream |  显示器  |

## 转换流

1. **InPutStreamReader**:Reader的子类，可以将InPutStream(字节流)包装成Reader(字符流)
2. **OutPutStreamWriter**:Writer的子类，可以将OutPutStream(字节流)包装成Writer(字符流)
3. 当处理纯文本文件时，如果使用字符流的效率更高，并且可以有效地解决中文问题，所以建议将字节流转换成字符流
4. 可以在使用时指定编码格式（比如utf-8,gbk,gb2312,ISO8859-1等）

## InPutStreamReader

![](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222320499.png)

```java
import java.io.BufferedReader;
import java.io.FileInputStream;
import java.io.InputStreamReader;

public class Main {

    public static void main(String[] args) throws Exception {
        String filePath = "e:\\test.txt";
        InputStreamReader isr = null;
        //将FileInputStream转换成InputStreamReader
        //指定编码utf-8
        isr = new InputStreamReader(new FileInputStream(filePath),"utf-8");
        //传入BufferedReader
        BufferedReader br = new BufferedReader(isr);
        String line;
        while ((line = br.readLine())!=null){
            System.out.println(line);
        }
        br.close();
    }

}


```



## OutPutStreamWriter

![image-20230422214905914](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222320597.png)

```java
import java.io.FileOutputStream;
import java.io.OutputStreamWriter;

public class Main {

    public static void main(String[] args) throws Exception {
        String filePath = "e:\\test.txt";
        OutputStreamWriter outputStreamWriter = new OutputStreamWriter(new FileOutputStream(filePath),"utf-8");
        outputStreamWriter.write("dfghj");
        outputStreamWriter.close();
    }

}


```

## 打印流

只有输出，没有输入

### PrintStream

![image-20230422220921597](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222320411.png)

```java
import java.io.PrintStream;

public class Main {

    public static void main(String[] args) throws Exception {
        PrintStream out = System.out;
        //在默认情况下，PrintStream的标准输出在显示器
        out.println("out");
        //因为PrintStream的底层实现为writer，所以可以直接使用writer
        out.write("ghhg".getBytes());
        out.close();
        //可以修改打印位置
        //修改到e:\test.txt
        System.setOut(new PrintStream("e:\\test.txt"));
        System.out.println("sgsgsg");
    }

}


```

### PrintWriter

![image-20230422221027415](https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222320358.png)

```java
import java.io.PrintWriter;

public class Main {

    public static void main(String[] args) throws Exception {
        PrintWriter printWriter = new PrintWriter(System.out);
        printWriter.print("dfghj");
        printWriter.close();
        PrintWriter printWriter1 = new PrintWriter(new PrintWriter("e:\\test.txt"));
        printWriter1.print("adaad");
        //flush/关闭流 才会将数据写入文件
        printWriter1.close();
    }

}


```

## Properties

1. 专门用来读写配置文件的集合类

   配置文件的格式：

   键  = 值

   键  = 值

2. 键值对不需要有空格，值不需要用引号包裹，默认类型是String

3. 常用方法

   1. load:加载配置文件的键值到Properties对象
   2. list:将数据显示到指定设备
   3. getProperty(Key)：根据键取值
   4. setProperty(Key,value):设置键值对到Properties对象
   5. store:将Properties中的键值对储存到配置文件，在idea中，保存信息到配置文件，如果有中文，会存储为unicode码

   ```java
   import java.io.FileReader;
   import java.util.Properties;
   
   public class Main {
   
       public static void main(String[] args) throws Exception {
           //创建Properties对象
           Properties properties = new Properties();
           //加载指定配置文件
           properties.load(new FileReader("src\\Mysql.properties"));
           //将k-v显示在控制台
           properties.list(System.out);
           //根据键获取相应的值
           String user = properties.getProperty("user");
           System.out.println(user);
       }
   
   }
   
   
   ```

   


