<h1>java代码规范</h1>
<ol>
<li><p>对于类，方法的注释，要以javadoc的方式来写。</p>
</li>
<li><p>非java doc的注释，是写给代码的维护者来看的。</p>
</li>
<li><p>使用tab操作，实现缩进默认向右移动，使用shift+tab可使代码整体向左移。</p>
</li>
<li><p>运算符和 = 两边习惯性各加一个空格。</p>
</li>
<li><p>源代码使用utf - 8的编码。</p>
</li>
<li><p>行宽度不要超过80字符。</p>
</li>
<li><p>代码编写需要次行风格和行尾风格（推荐）。</p>
<p>&nbsp;</p>
</li>

</ol>
<h1>路径详解</h1>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345563.png" referrerpolicy="no-referrer" alt="image-20230307232130533"></p>
<h2>相对路径</h2>
<p>从当前目录开始定位，形成的一个路径</p>
<h2>绝对路径</h2>
<p>从顶级目录d，开始定位，形成的路径</p>
<h2>需求</h2>
<p>从abc\test100访问abc2\test200\hello.txt</p>
<h2>方法</h2>
<p><strong>相对路径</strong>：..\..\abc2\test200\hello.txt</p>
<p><strong>绝对路径</strong>：d:\abc2\test200\hello.txt</p>
<h2>常用的dos命令</h2>
<ol>
<li><p>查看当前目录有什么内容 dir dir d:\abc2\test200</p>
</li>
<li><p>切换到其他盘下：cd:change directory</p>
<p>cd /D c: </p>
</li>
<li><p>切换到当前盘的其他目录下（使用相对路径和绝对路径分别演示）</p>
<p>cd d:\abc2\test200 cd ..\..\abc2\test200</p>
</li>
<li><p>切换到上一级：cd..</p>
</li>
<li><p>切换到根目录 ：cd\ </p>
</li>
<li><p>查看指定目录下的所有自己目录</p>
<p>tree d:</p>
</li>
<li><p>清屏cls</p>
</li>
<li><p>退出指令 exit</p>
</li>

</ol>
<h1>java API文档</h1>
<p>API(Application Programming Interface,应用程序编程接口)是Java提供的基本编程接口。</p>
<p>中文在线文档：<a href='http://www.matools.com' target='_blank' class='url'>http://www.matools.com</a></p>
<p>Java类的组织形式</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345650.png" referrerpolicy="no-referrer" alt="image-20230309172646567"></p>
<p>使用方法：</p>
<ol>
<li>包&gt;类&gt;方法</li>
<li>直接搜索</li>

</ol>
<h1>字符型本质</h1>
<h2>本质：</h2>
<p>字符型存储到计算机中，需要将字符对应的码值（整数）找出来，比如&#39;a&#39;</p>
<p>存储：&#39;a&#39;&gt;码值97&gt;二进制（110 0001）&gt;存储</p>
<p>读取：二进制（110 0001）&gt;97&gt;&#39;a&#39;&gt;显示</p>
<h2>字符编码表</h2>
<p>ASCII(一个字节表示，一个128个字符，实际上一个字节可以表示256个字符，只用128个)</p>
<p>Unicode（固定的编码，使用两个字节来表示字符，字母和汉字统一都是占用两个字节）</p>
<p>utf-8（大小可变的编码，字母使用1个字节，汉字使用3个字节）</p>
<p>gbk（可以表示汉字，范围广，字母使用1个字节，汉字使用2个字节）</p>
<p>big5码（繁体中文，台湾，香港）</p>
<h1>String和基本类型转化</h1>
<h2>基本数据类型转Sting类型</h2>
<p>语法：将基本类型的值+&quot;&quot;即可实现自动转换</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345546.png" referrerpolicy="no-referrer" alt="image-20230309181204762"></p>
<p>&nbsp;</p>
<h2>String类型转基本数据类型</h2>
<p>语法：通过基本类型的包装类调用parseXX方法即可实现转换</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345261.png" referrerpolicy="no-referrer" alt="image-20230309181331052"></p>
<p>怎么把字符串转换成字符char &gt; 将字符串的第一个字符得到</p>
<pre><code class='language-java' lang='java'>String s5 = &quot;123&quot;;
System.out.println(s5.charAt(0));
</code></pre>
<p>输出为1</p>
<h2>补充</h2>
<p>将String 类型进行转换时，要确保其可以转换成一个有效的数据，比如可以将&quot;123&quot;转换成一个整数，但不会把&quot;hello&quot;转换成一个整数。</p>
<h1>逻辑运算符</h1>
<h2>介绍</h2>
<p>&nbsp;</p>
<ol>
<li>短路与&amp;&amp;，短路或||，取反！</li>
<li>逻辑与&amp;，逻辑或|，逻辑异或^<img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345062.png" referrerpolicy="no-referrer" alt="image-20230309184955245"></li>

</ol>
<p>a&amp;&amp;b:当a和b同时为true时，结果为ture，否则为flase</p>
<p>a&amp;b:当a和b同时为true时，结果为ture，否则为flase</p>
<p>a|b:当a和b，有一个为true，结果为true，否则为flase</p>
<p>a||b:当a和b，有一个为true，结果为true，否则为flase</p>
<p>!a:当a为true，结果为flase，当a为flase，结果为true</p>
<p>a^b:当a和b不同时，结果为true，否则为flase</p>
<h2>区别</h2>
<p>短路与（&amp;&amp;）和逻辑与（&amp;）</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345564.png" referrerpolicy="no-referrer" alt="image-20230309190049724"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345213.png" referrerpolicy="no-referrer" alt="image-20230309190230675"></p>
<p>短路或（||）和逻辑或（|）</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345576.png" referrerpolicy="no-referrer" alt="image-20230309190451233"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345532.png" referrerpolicy="no-referrer" alt="image-20230309190517759"></p>
<p>因此在开发中基本使用短路或（||）和短路与（&amp;&amp;），效率更高。</p>
<h1>标识符</h1>
<h2>标识符规则</h2>
<ol>
<li><p>由26个英文字母大小写，0-9，——或&amp;组成。</p>
</li>
<li><p>数字不可以开头</p>
</li>
<li><p>不可以使用关键字和保留字，但可以包含。</p>
</li>
<li><p>java严格区分大小写，长度无限制。</p>
</li>
<li><p>标识符不能包含空格。</p>
<p>&nbsp;</p>
</li>

</ol>
<h2>标识符规范</h2>
<ol>
<li><p>包名：多单词组成时所有字母都小写：aaa.bbb.ccc//比如 com.yzd.com</p>
</li>
<li><p>类名，接口名：多单词组成时，所有单词首字母大写：XxxYyyZzz[大驼峰]</p>
<p>比如：ThankShotGame</p>
</li>
<li><p>变量名，方法名：多单词组成时，第一个的单词小写，第二个但那次开始首字母大写：xxxYyyZzz[小驼峰]</p>
<p>比如：thankShotGame</p>
</li>
<li><p>常量名：所有单词都要大写，多单词之间每个单词都用下划线连接：XXX_YYY_ZZZ</p>
<p>比如：定义一个所得税率TAX_RATE</p>
<p>代码规范可以参照<a href='[前言 · GitBook (1994.github.io)](https://1994.github.io/p3c/)'>阿里巴巴java开发手册</a></p>
</li>

</ol>
<h1>进制</h1>
<h2>介绍</h2>
<ol>
<li><p>二进制：0，1，满2进1，以0b或0B开头</p>
</li>
<li><p>十进制：0-9，满10进1</p>
</li>
<li><p>八进制：0-7，满8进1，以数字0开头</p>
</li>
<li><p>十六进制：0-9及A（10）-F（15），满16进1，以0x或0X开头表示，此处的A-F不区分大小写</p>
<p>&nbsp;</p>
</li>

</ol>
<p>举例：</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171345885.png" referrerpolicy="no-referrer" alt="image-20230309231123642"></p>
<h2>进制转换</h2>
<h3>十进制转化</h3>
<h4>二进制转十进制</h4>
<p>从最低位（右边）开始，将每位的数提取出来，乘以2的（位数-1）次方，然后求和</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346832.png" referrerpolicy="no-referrer" alt="image-20230309233119963"></p>
<h4>八进制转十进制</h4>
<p>从最低位（右边）开始，将每位的数提取出来，乘以8的（位数-1）次方，然后求和</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346907.png" referrerpolicy="no-referrer" alt="image-20230309233205015"></p>
<h4>十六进制转十进制</h4>
<p>从最低位（右边）开始，将每位的数提取出来，乘以16的（位数-1）次方，然后求和</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346642.png" referrerpolicy="no-referrer" alt="image-20230309233435529"></p>
<h4>十进制转二进制</h4>
<p>将该数不断地除以2，直到商为0为止，然后将每步得到的余数倒过来，就是对应的2进制。</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346027.png" referrerpolicy="no-referrer" alt="image-20230309233803291"></p>
<h4>十进制转八进制</h4>
<p>将该数不断地除以8，直到商为0为止，然后将每步得到的余数倒过来，就是对应的8进制。</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346301.png" referrerpolicy="no-referrer" alt="image-20230309233936505"></p>
<h4>十进制转十六进制</h4>
<p>将该数不断地除以16，直到商为0为止，然后将每步得到的余数倒过来，就是对应的16进制。</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346673.png" referrerpolicy="no-referrer" alt="image-20230309234101466"></p>
<h3>二进制转化</h3>
<h4>八进制转二进制</h4>
<p>将八进制每一位，转化成对应的一个三位的二进制数</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346630.png" referrerpolicy="no-referrer" alt="image-20230310194658449"></p>
<h4>十六进制转二进制</h4>
<p>将十六进制每一位，转化成对应的一个四位的二进制数</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346745.png" referrerpolicy="no-referrer" alt="image-20230310194803004"></p>
<h4>二进制转八进制</h4>
<p>从低位开始，每三位一组，转成对应的八进制数</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346087.png" referrerpolicy="no-referrer" alt="image-20230310194414831"></p>
<h4>二进制转其十六进制</h4>
<p>从低位开始，每四位一组，转成对应的十六进制数</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346189.png" referrerpolicy="no-referrer" alt="image-20230310194514926"></p>
<h2>原码，反码，补码</h2>
<ol>
<li><p>二进制的最高位是符号位，0代表正数，1代表负数。</p>
</li>
<li><p>正数的原码，反码，补码都一样。</p>
</li>
<li><p>负数的反码=原码符号位不变，其余位取反。</p>
</li>
<li><p>负数的补码=反码+1。</p>
</li>
<li><p>0的反码，补码都是0。</p>
</li>
<li><p>Java中的数都是有符号的。</p>
</li>
<li><p>计算机在运算的时候，是以补码的方式进行运算的。</p>
</li>
<li><p>当我们要看结果时需要看它的原码。</p>
<p>&nbsp;</p>
</li>

</ol>
<h2>位运算符</h2>
<p>按位与&amp;：两位全为1，结果为1，否则为0。</p>
<p>按位或|：两位中有一位为1，结果为1，否则为0。</p>
<p>按位异或^:两位中一个为0，一个为1，结果为1，否则为0.</p>
<p>按位取反：0-&gt;1,1-&gt;0。</p>
<p>算数右移&gt;&gt;：低价溢出，符号位不变，并且用符号位补溢出的高位。</p>
<p>算数左移&lt;&lt;:符号位不变，低位补0。</p>
<p>逻辑右移&gt;&gt;&gt;:低位溢出，高位补0。</p>
<p>补充：没有&lt;&lt;&lt;符号</p>
<h1>数组</h1>
<h2>数组赋值</h2>
<p>基本数据类型的赋值为值传递。</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171346978.png" referrerpolicy="no-referrer" alt="image-20230313202506512"></p>
<p>数组在默认情况下是引用传递，赋的是地址的值</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347020.png" referrerpolicy="no-referrer" alt="image-20230313202729355"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347842.png" referrerpolicy="no-referrer" alt="image-20230313203441679"></p>
<h2>数组拷贝</h2>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347153.png" referrerpolicy="no-referrer" alt="image-20230313203817984"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347447.png" referrerpolicy="no-referrer" alt="image-20230313203938938"></p>
<p>&nbsp;</p>
<h1>对象内存分布</h1>
<p>示例图</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347838.png" referrerpolicy="no-referrer" alt="image-20230313221151419"></p>
<p><strong>注意：</strong></p>
<p>cat仅仅是对象名（对象引用）</p>
<p>new Cat()创建的对象空间（数据）才是真正的对象</p>
<p><strong>结构分析：</strong></p>
<ol>
<li>栈：一般存放基本数据类型（局部能量）</li>
<li>堆：存放对象（Cat cat,数组）</li>
<li>方法区：常量池（常量，比如字符串），类加载信息</li>

</ol>
<p><strong>流程分析：</strong></p>
<ol>
<li>先加载Cat类信息（属性和方法信息，只加载一次）</li>
<li>在堆中分配空间，进行默认初始化</li>
<li>进行对象初始化，先默认初始化，接着进行指定初始化，最后完成构造器初始化</li>
<li>把地址付给cat，cat指向对象</li>

</ol>
<h1>方法调用机制</h1>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347615.png" referrerpolicy="no-referrer" alt="image-20230313231243571"></p>
<h1>递归</h1>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347320.png" referrerpolicy="no-referrer" alt="image-20230315172045420"></p>
<h1>可变参数</h1>
<p><strong>定义：</strong></p>
<p>java中允许将同一个类中多个同名同功能但参数个数不同的方法，封装成一个方法，可通过可变参数实现。</p>
<p><strong>基本语法:</strong></p>
<p>访问修饰符 返回类型 方法名（数据类型...形参名）{
}</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347119.png" referrerpolicy="no-referrer" alt="image-20230316163745830"></p>
<p><strong>细节注意：</strong></p>
<ol>
<li>可变数组的实参可以为0个或任意多个。</li>
<li>可变数组的实参可以为数组。</li>
<li>可变参数的本质就是数组。</li>
<li>可变参数和普通类型的参数一起放在形参列表中，但必须保证可变参数在最后。</li>
<li>一个形参列表只能出现一个可变参数</li>

</ol>
<h1>IDEA快捷键</h1>
<ol>
<li>删除当前行ctrl+Y</li>
<li>复制当前行ctrl+D</li>
<li>补全代码alt+/</li>
<li>自动导入包或者自动实例化对象alt+enter</li>
<li>快速格式化代码ctrl+alt+L</li>
<li>生成构造器alt+insert(还有其他用法)</li>
<li>查看一个类的层级关系，ctrl+H</li>
<li>将光标放在一个方法上，输入ctrl+B,可以定位到方法</li>
<li>自动分配变量名，加.var</li>

</ol>
<h1>包</h1>
<ol>
<li>区分相同名字的类</li>
<li>当类很多时，可以很好的管理类[看java API文档]</li>
<li>控制访问范围</li>

</ol>
<p><strong>包基本语法：</strong></p>
<p>package com.yzd</p>
<ol>
<li><p>package 关键字，表示打包</p>
</li>
<li><p>com.yzd表示包名</p>
<p>&nbsp;</p>
</li>

</ol>
<p><strong>包的本质：</strong></p>
<p>实质上就是创建不同的的文件夹/目录来保存类文件，</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347713.png" referrerpolicy="no-referrer" alt="image-20230316215243186"></p>
<p><strong>命名规则：</strong></p>
<p>只能包含数字，字母，下划线，小圆点，但不可以用数字开头，不可以是关键字或保留字</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171347864.png" referrerpolicy="no-referrer" alt="image-20230316220402923"></p>
<p><strong>命名规范：</strong></p>
<p>一般是小写字母+小圆点</p>
<p>com.公司名.项目名.业务模块名</p>
<p>列如com.yzd.oa.model</p>
<p>举例：</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171348570.png" referrerpolicy="no-referrer" alt="image-20230316220647513"></p>
<p><strong>常用的包：</strong></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171348419.png" referrerpolicy="no-referrer" alt="image-20230316220903599"></p>
<h1>访问修饰符</h1>
<ol>
<li>公开级别：public,对外公开</li>
<li>受保护级别：protected，对子类和同一个包中的类公开</li>
<li>默认级别：对同一个包的类公开</li>
<li>私有级别：private，只有类本身可以访问</li>

</ol>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171348081.png" referrerpolicy="no-referrer" alt="image-20230316222347115"></p>
<p><strong>注意：</strong></p>
<p>只有public和默认的可以修饰类</p>
<h1>继承</h1>
<h2>细节</h2>
<p>&nbsp;</p>
<ol>
<li>子类继承了所有的属性和方法，但是私有属性和方法不可以在子类直接访问，要通过公共类方法访问。</li>
<li>子类必须调用父类的构造器，完成父类的初始化</li>
<li>java是单继承，一个子类只可以有一个父类，一个父类可以有多个子类</li>

</ol>
<h2>本质</h2>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171740109.png" referrerpolicy="no-referrer" alt="image-20230317174027556"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303171742782.png" referrerpolicy="no-referrer" alt="image-20230317174237468"></p>
<h1>方法重写</h1>
<ol>
<li><p>子类方法的参数，方法名称，要和父类方法的参数，方法名称一致。</p>
</li>
<li><p>子类方法的返回类型要和父类的一致，或者是父类返回类型的子类</p>
<p>父类的返回类型为Obiect,子类的返回方法可以为String</p>
</li>
<li><p>子类方法不能缩小父类方法的访问权限</p>
<p>&nbsp;</p>
</li>

</ol>
<h1>多态</h1>
<h2>方法的多态</h2>
<ol>
<li><p>方法重载</p>
</li>
<li><p>方法重写</p>
<p>&nbsp;</p>
</li>

</ol>
<h2>对象的多态</h2>
<ol>
<li>一个对象的编译类型和运行类型可以不一致</li>
<li>编译类型在定义对象时已经确定，无法改变</li>
<li>运行类型是可以改变的</li>
<li>编译类型看 = 号的左边，运行类型看 = 号的右边</li>

</ol>
<p>&nbsp;</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303172209586.png" referrerpolicy="no-referrer" alt="image-20230317220946420"></p>
<h2>向上转型</h2>
<p><strong>本质：</strong></p>
<p>父类引用指向子类的对象</p>
<p><strong>语法：</strong></p>
<p>父类类型   引用名 = new 子类类型（）;</p>
<p><strong>特点：</strong></p>
<p>编译类型看左边，运行类型看右边。</p>
<p>可以调用父类的所有成员（遵循访问权限）</p>
<p>不可以调用子类的特有成员;</p>
<p>最终的运行效果看子类的具体实现</p>
<p><strong>总结：</strong></p>
<p>可以调用那些成员看编译类型，具体方法的运行结果先看运行类型</p>
<h2>向下转型</h2>
<ol>
<li>子类类型  引用名 = （子类类型）父类引用</li>
<li>只能强制转换父类的引用，不可以强转父类的对象</li>
<li>要求父类的引用必须指向的是当前对象目标类型的对象</li>
<li>可以调用子类类型中所有的对象</li>

</ol>
<h2>细节</h2>
<p>属性没有重写，属性的结果直接看编译类型</p>
<p>instanceOf 用于判断对象的运行类型是否为XX类型或XX类型的子类型</p>
<h2>动态绑定机制</h2>
<ol>
<li>当调用对象方法时，该方法会和该对象的内存地址/运行类型绑定</li>
<li>属性没有动态绑定机制，哪里声明，就在那里使用</li>

</ol>
<h1>Object类详解</h1>
<h2>equals</h2>
<p><strong>==</strong>是一个比较运算符</p>
<ol>
<li>既可以判断基本类型，也可以判断引用类型</li>
<li>判断基本类型时，判断的是值是否相等</li>
<li>判断引用类型时，判断的是地址是否相等</li>

</ol>
<p><strong>equals</strong>是Object类中的方法，只可以判断引用类型，默认判断地址是否相等，但Integer,String重写了父类方法，用于判断内容是否相等</p>
<h2>hashCode</h2>
<ol>
<li>提高具有哈希结构的容器的效率</li>
<li>两个引用，指向的是同一个对象，哈希值是一样的</li>
<li>两个引用，指向的不是同一个对象，哈希值是不一样的</li>
<li>哈希值主要根据地址号来的，不可以将其完全等价成地址</li>

</ol>
<h2>toString</h2>
<p><strong>默认返回：</strong></p>
<p>全类名+@+哈希值的十六进制</p>
<p>子类往往重写toString方法，用于返回对象的属性信息</p>
<p>直接输出一个对象时，等价于调用它的toString方法</p>
<h1>代码块</h1>
<p>没有方法名，没有返回，没有参数，只有方法体，不用通过对象或类显式调用，而是加载类时，或创建对象是隐式调用</p>
<h2>基本语法</h2>
<p>[修饰符]{
代码</p>
<p>}；</p>
<p><strong>注意：</strong></p>
<ol>
<li>修饰符可选，要写的话，只可以写static</li>
<li>代码块分为两类，使用static修饰的是静态代码块，没有修饰的为普通代码块</li>
<li>逻辑语句可以为任意逻辑语句</li>
<li>;号可以有，也可以省略</li>

</ol>
<p><strong>好处：</strong></p>
<ol>
<li>相当于另一种形式的代码块，对构造器的一种补充形式，可以进行初始化的操作</li>
<li>如果多个构造器中都有重复的语句，可以抽取到初始化代码块中，提高代码的重用性</li>

</ol>
<h2>细节</h2>
<ol>
<li><p>static代码块也叫做静态代码块，作用是进行类的初始化，随着类的加载而执行，并且只执行一次，如果是普通代码块，每创建一个对象，就执行一次</p>
</li>
<li><p>类什么时候进行加载：</p>
<ol>
<li>创建对象实例化时</li>
<li>创建子类对象时，父类也会被加载</li>
<li>使用类的静态成员时</li>

</ol>
</li>
<li><p>普通的代码块创建一次就会被隐式调用一次，如果只是调用类的静态成员，则不会调用普通代码块</p>
</li>
<li><p>创建一个对象时，在一个类的调用顺序</p>
<ol>
<li>调用静态代码块和静态属性初始化（静态代码块和静态属性初始化的优先级一样，如果有多个，则按照他们定义的顺序调用）</li>
<li>调用普通代码块和普通属性初始化（普通代码块和普通属性初始化的优先级一样，如果有多个，则按照他们定义的顺序调用）</li>
<li>调用构造器初始化</li>

</ol>
</li>
<li><p>构造器的最前面隐含了super()和调用普通代码块，新写一个类时，静态相关的代码块，属性初始化，在类加载时就已经完成，因此是优先于构造器和普通代码块的<img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303201623440.png" referrerpolicy="no-referrer" alt="image-20230320162335021"></p>
</li>
<li><p>创建一个子类对象时，他们的静态代码块，静态属性初始化，普通代码块，普通属性初始化，构造方法的调用顺序</p>
<ol>
<li><p>父类的静态代码块和静态属性</p>
</li>
<li><p>子类的静态代码块和静态属性</p>
</li>
<li><p>父类的普通代码块和普通属性</p>
</li>
<li><p>父类的构造方法</p>
</li>
<li><p>子类的普通代码块和普通属性</p>
</li>
<li><p>子类的构造方法</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303201636893.png" referrerpolicy="no-referrer" alt="image-20230320163648816"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303201638608.png" referrerpolicy="no-referrer" alt="image-20230320163816400"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303201638336.png" referrerpolicy="no-referrer" alt="image-20230320163853266"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303201639106.png" referrerpolicy="no-referrer" alt="image-20230320163926024"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303201640384.png" referrerpolicy="no-referrer" alt="image-20230320164000304"></p>
</li>

</ol>
</li>
<li><p>静态代码块只可以直接调用静态成员，普通代码块可以调用任意成员</p>
<p>&nbsp;</p>
</li>

</ol>
<h1>单例模式</h1>
<h2>饿汉式</h2>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303201900101.png" referrerpolicy="no-referrer" alt="image-20230320190039714"></p>
<h2>懒汉式</h2>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303201914923.png" referrerpolicy="no-referrer" alt="image-20230320191453615"></p>
<p><strong>区别：</strong></p>
<p>饿汉式和懒汉式的创建时机不同，饿汉式是类加载时创建，懒汉式是使用时才创建</p>
<p>饿汉式：存在资源浪费问题</p>
<p>懒汉式：存在线程安全问题</p>
<h1>final</h1>
<ol>
<li><p>final修饰的属性又叫做常量，一般用XX_XX_XX命名</p>
</li>
<li><p>final修饰的属性在定义时必须赋初值，并且不可以修改，可以在以下位置</p>
<ol>
<li>定义时</li>
<li>在构造器中</li>
<li>在代码块中</li>

</ol>
</li>
<li><p>如果final修饰的属性是静态的，则初始化的位置只可以是定义时和在代码块时，不可以在构造器中</p>
</li>
<li><p>final类不可以继承，但是可以进行实例化对象</p>
</li>
<li><p>如果类不是final类，但是含有final方法，该方法不可以重写，但是可以被继承</p>
</li>
<li><p>final 和static往往搭配使用，效率更高，不会导致类加载，底层编译进行了优化处理</p>
</li>
<li><p>包装类都是final类型，不可以被继承</p>
</li>
<li><p>构造器不可以用final修饰</p>
</li>

</ol>
<h1>抽象类</h1>
<p>当父类中一些方法不能确定时，可以使用abstract关键字来修饰，该方法也就成为了抽象方法，用abstract修饰的该类也就是抽象类</p>
<h2>细节</h2>
<ol>
<li>抽象类不可以被实例化</li>
<li>抽象类中可以没有抽象方法，还可以有实现方法</li>
<li>类中一旦有抽象方法，该类必须时抽象类</li>
<li>abstract只可以修饰类和方法</li>
<li>抽象类可以有任意成员（本质还是类）</li>
<li>抽象类不可以有实体</li>
<li>一个类继承了抽象类，则必须实现抽象类的方法，或者本身也是抽象类</li>
<li>抽象方法不可以用privite,final,static来修饰</li>

</ol>
<h1>接口</h1>
<h2>基本介绍</h2>
<p>语法：</p>
<pre><code class='language-java' lang='java'>intterface 接口名{
	//属性
	//方法（1.抽象方法 2.默认实现方法 3。静态方法）
}

class 类名 implements 接口{
	自己属性
	自己方法
	必须实现的接口的抽象方法
}
</code></pre>
<p><strong>小结：</strong></p>
<ol>
<li><p>在jdk7.0 之前接口中所有的方法都没有方法体</p>
</li>
<li><p>在jdk8.0之后接口可以有静态方法，默认方法，也就是接口中可以有方法的具体实现</p>
<p>&nbsp;</p>
</li>

</ol>
<h2>细节</h2>
<ol>
<li>接口不可以被实例化</li>
<li>接口中的所有方法都是public方法，接口中抽象方法，可以不用abstract修饰</li>
<li>一个普通类实现接口，就必须实现接口的所有方法</li>
<li>抽象类实现接口，可以不用实现接口的方法</li>
<li>一个类可以同时实现多个接口</li>
<li>接口中的属性都是final的，而且是public static final 修饰</li>
<li>接口中属性的访问形式：接口名.属性名</li>
<li>接口不可以继承别的类，但是可以继承别的多个接口</li>
<li>接口的修饰符只可以是public和默认的，和类一样</li>

</ol>
<h2>接口 VS 继承</h2>
<p>当子类继承了父类，就自动拥有了父类的功能</p>
<p>如果子类需要扩展功能，可以通过实现接口的方式扩展</p>
<p>可以理解为，实现接口是对于java 单继承机制的一种补充</p>
<h2>接口的多态特性</h2>
<ol>
<li>多态参数（接口引用可以指向实现了接口的类的对象实例）</li>

</ol>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303211929401.png" referrerpolicy="no-referrer" alt="image-20230321192902785"></p>
<ol start='2' >
<li><p>多态数组</p>
</li>
<li><p>接口的多态传递</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303211935335.png" referrerpolicy="no-referrer" alt="image-20230321193537270"></p>
</li>

</ol>
<h1>内部类</h1>
<p>一个类的内部有完整的嵌套了另一个类结构，被嵌套的类称为内部类，属于类的第五大成员，<strong>类的成员包含{属性，方法，构造器，代码块，内部类}</strong></p>
<p><strong>基本语法：</strong></p>
<pre><code>class Outer{//外部类
	class Inner{
	//内部类
	}
}
class Other{
//外部其他类
}
</code></pre>
<h2>局部内部类</h2>
<p><strong>定义：</strong></p>
<p>定义在外部类的局部位置，通常在方法中，并且有类名</p>
<ol>
<li>可以直接访问外部类的所有成员，包括私有的</li>
<li>不可以添加访问修饰符，因为它的地位就是一个局部变量，局部变量不可以使用修饰符，但是可以用final修饰，因为局部变量中也含有final</li>
<li>作用域：仅仅在定义它的方法或代码块中</li>
<li>局部内部类--访问---&gt;&gt;外部类的成员（直接访问）</li>
<li>外部类--访问---&gt;局部内部类的成员（创建对象，再进行访问，必须在作用域中）</li>
<li>外部其他类不可以访问局部内部类（因为局部内部类的地位是一个局部变量）</li>
<li>如果外部类和局部内部类的成员重名时，默认遵循就近原则，如果想要访问外部类的成员，则可以使用（外部类名.this.成员）访问</li>

</ol>
<h2>匿名内部类</h2>
<h3>介绍</h3>
<p><strong>定义：</strong></p>
<ol>
<li>本质是类</li>
<li>内部类</li>
<li>该类没有名字</li>
<li>同时还是一个对象</li>

</ol>
<p><strong>基本语法：</strong></p>
<p>new 类和接口（参数列表）{</p>
<p>	类体</p>
<p>}；</p>
<p><strong>方法匿名内部类：</strong></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303231849523.png" referrerpolicy="no-referrer" alt="image-20230323184903937"></p>
<p><strong>接口匿名内部类：</strong></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303231853215.png" referrerpolicy="no-referrer" alt="image-20230323185341098"></p>
<h3>细节</h3>
<p><strong>1.基于类调用</strong></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303231901621.png" referrerpolicy="no-referrer" alt="image-20230323190114944"></p>
<p><strong>2.直接调用</strong></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303231859438.png" referrerpolicy="no-referrer" alt="image-20230323185957404"></p>
<ol start='3' >
<li>可以调用外部类的所有成员，包括私有的</li>
<li>不可以添加访问修饰符，因为它的地位就是一个局部变量</li>
<li>作用域：仅仅在定义它的方法或代码块中</li>
<li>匿名内部类--访问---外部类成员（直接访问）</li>
<li>外部其他类不可以访问内部类（本质就是一个局部变量）</li>
<li>如果外部类和匿名内部类的成员重名时，匿名内部类访问的时候，遵循就近原则，如果想要访问外部类成员，则可以使用（外部类名.this.成员）访问</li>

</ol>
<h3>内部类使用</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303231940540.png" referrerpolicy="no-referrer" alt="image-20230323194009442"></p>
<h2>成员内部类</h2>
<ol>
<li><p>可以访问外部类的所有成员，包括私有的</p>
</li>
<li><p>可以添加任意访问修饰符（public,protected,默认,private），因为它的地位就是一个成员</p>
</li>
<li><p>和外部类的其他成员一样</p>
</li>
<li><p>成员内部类访问外部类，直接访问</p>
</li>
<li><p>外部类访问内部类，创建成员内部类的对象，使用相关的属性</p>
</li>
<li><p>外部其他类访问内部类：</p>
<ol>
<li>外部类.内部类 XXX = 外部类.new.内部类（）;</li>
<li>在外部类中编写一个方法，返回内部类对象</li>

</ol>
</li>
<li><p>如果外部类和匿名内部类的成员重名时，匿名内部类访问的时候，遵循就近原则，如果想要访问外部类成员，则可以使用（外部类名.this.成员）访问</p>
</li>

</ol>
<h2>静态内部类</h2>
<p>静态内部类是定义了在外部类的成员变量，并且有static修饰</p>
<ol>
<li><p>可以直接访问外部类的所有静态变量，包括私有的，但是不可访问非静态成员</p>
</li>
<li><p>可以添加任意访问修饰符（public,protected,默认,private），因为它的地位就是一个成员</p>
</li>
<li><p>作用域:为一个类体</p>
</li>
<li><p>外部类访问内部类，创建成员内部类的对象，使用相关的属性</p>
</li>
<li><p>外部其他类访问内部类</p>
<ol>
<li>外部类.内部类 XXX = new 外部类.内部类（）;</li>
<li>在外部类中编写一个方法，返回内部类对象</li>

</ol>
<p>&nbsp;</p>
</li>
<li><p>如果外部类和匿名内部类的成员重名时，匿名内部类访问的时候，遵循就近原则，如果想要访问外部类成员，则可以使用（外部类名.this.成员）访问,如果是静态成员变量，则不用this</p>
</li>

</ol>
<h1>枚举</h1>
<h2>自定义枚举</h2>
<ol>
<li>将构造器私有化，目的防止直接new</li>
<li>去掉setXxx方法，防止属性被修改</li>
<li>在Season内部，直接创建固定的对象</li>
<li>优化，可以加入 final 修饰符</li>
<li>枚举对象名通常全部大写</li>

</ol>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303232157363.png" referrerpolicy="no-referrer" alt="image-20230323215658225"></p>
<h2>关键字实现枚举</h2>
<ol>
<li>使用关键字enum替代class</li>
<li>使用SPRING(&quot;春天&quot;，&quot;温暖&quot;)，常量名（实参列表）</li>
<li>如果有多个常量，使用,号间隔</li>
<li>使用enum来实现枚举时，先定义常量，写在前面</li>

</ol>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303251508296.png" referrerpolicy="no-referrer" alt="image-20230325150843436"></p>
<h3>注意</h3>
<ol>
<li><p>在使用enum关键字实现枚举时，默认会继承Enum类，而且是final类</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303251520490.png" referrerpolicy="no-referrer" alt="image-20230325152054204"></p>
</li>
<li><p>如果使用的是无参构造器，则实参列表和小括号可以省略</p>
</li>
<li><p>枚举对象必须放在枚举类的行首</p>
</li>
<li><p>enum类不可以在继承其他类，但是可以实现接口</p>
</li>

</ol>
<h3>常用方法</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303251527031.png" referrerpolicy="no-referrer" alt="image-20230325152701078"></p>
<h1>注解</h1>
<h2>Override </h2>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303251546369.png" referrerpolicy="no-referrer" alt="image-20230325154612873"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202303251548411.png" referrerpolicy="no-referrer" alt="image-20230325154805696"></p>
<ol>
<li>@Override 只可以修饰方法，不可以修饰别的属性</li>
<li>查看@Override的注解源码为@Target(ElementType.METHOD),说明其只可以修饰方法</li>
<li>@Target是修饰注解的注解，称为元注解</li>

</ol>
<h2>Deprecated</h2>
<ol>
<li>@Deprecated 修饰某个元素，表明该元素已经过时，但仍然可以使用</li>
<li>可以修饰方法，类，字段，包，参数等</li>
<li>@Deprecated 可以用作版本升级过渡使用</li>

</ol>
<h2>SuppressWarnings</h2>
<ol>
<li><p>当我们不希望看到一些警告时，可以使用@SuppressWarings来隐藏警告</p>
</li>
<li><p>在{&quot;&quot;}中，可以填入希望抑制的警告信息 </p>
</li>
<li><p>关于SuppressWarnings作用范围和放的位置有关</p>
<p>&nbsp;</p>
</li>

</ol>
<h2>元注解</h2>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201645002.png" referrerpolicy="no-referrer" alt="image-20230325161127812"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201645630.png" referrerpolicy="no-referrer" alt="image-20230325161412614"></p>
<h1>异常处理</h1>
<h2>概念</h2>
<p>选中代码块 --&gt; 使用ctrl + alt + t -&gt; 选中 try catch</p>
<p>异常分类：</p>
<ol>
<li>error(错误)：Java无法解决的严重问题，比如JVM系统内部错误，资源耗尽</li>
<li>Exception：因为编程问题或者偶然的外在因素造成的一般性问题，可以使用针对性的代码进行处理，Exception又分为两大类，运行时异常，编译时异常</li>

</ol>
<h2>异常体系图</h2>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646499.png" referrerpolicy="no-referrer" alt="image-20230325164022033"></p>
<h2>五大运行时异常</h2>
<p>NullPointerException(空指针异常)</p>
<p>ArithmeticExpection(算术异常)</p>
<p>ArrayIndexOutOfBoundsExpection(数组下标越界异常)</p>
<p>ClassCastException(类转换异常)</p>
<p>NumberFormatExpection(数字格式异常)</p>
<h2>异常处理机制</h2>
<p><strong>try-catch-finally</strong></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646918.png" referrerpolicy="no-referrer" alt="image-20230325165439950"></p>
<p><strong>throws</strong></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646469.png" referrerpolicy="no-referrer" alt="image-20230325165809784"></p>
<h2>try-catch</h2>
<pre><code class='language-java' lang='java'>try{
	//可疑代码
	//将异常生成的对应异常对象，传递给catch块
}catch(异常){
	//对异常的处理
}
//如果没有finally也是可以的
</code></pre>
<h3>细节</h3>
<ol>
<li>如果异常发生了，则异常发生后面的代码不会进行，直接进入到catch语句</li>
<li>如果没有异常，则顺序执行try代码块，不会进入catch代码块</li>
<li>如果希望无论是否发生异常，都执行某段代码（比如关闭连接，释放资源等），可以使用finall代码块</li>
<li>可以有多个catch代码块，要求子类异常写在前面，父类异常写在后面</li>
<li>也可以使用try-finally配合使用，相当于没有捕获异常，因此程序会直接崩溃/退出</li>

</ol>
<h2>throws</h2>
<ol>
<li>对于编译异常，必须用throws或者try-catch处理</li>
<li>对于运行异常，如果没有处理，默认用throws处理</li>
<li>子类重写父类方法时，对抛出异常的规定：子类抛出的异常类型要和父类的异常一致，或者是父类抛出异常的子类型</li>
<li>如果在throws过程中，如果有try-catch，则认为异常已经处理</li>

</ol>
<h2>自定义异常</h2>
<ol>
<li>自定义异常名继承Exception或者RuntimeException</li>
<li>如果继承Exception,属于编译异常</li>
<li>如果继承RuntimeException,属于运行异常（一般继承RuntimeException）</li>

</ol>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646859.png" referrerpolicy="no-referrer" alt="image-20230325190748732"></p>
<p><strong>实例演示：</strong></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646405.png" referrerpolicy="no-referrer" alt="image-20230325191211875"></p>
<p>[更加具体的异常问题参照于锦泉的备忘笔记]（<a href='https://arthurjq.com/2021/06/01/java/throw/'>try-catch,throw和throws的使用 | 锦泉<sup>-</sup> (arthurjq.com)</a>）</p>
<h1>常用类</h1>
<h2>包装类</h2>
<h3>概念</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646573.png" referrerpolicy="no-referrer" alt="image-20230325195659858"></p>
<p> <strong>示例图：</strong><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646141.png" referrerpolicy="no-referrer" alt="image-20230325200413396"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646687.png" referrerpolicy="no-referrer" alt="image-20230325200442761"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201646198.png" referrerpolicy="no-referrer" alt="image-20230325200509466"></p>
<h3>装箱与拆箱</h3>
<pre><code class='language-java' lang='java'>演示int &lt;--&gt; Integer 的装箱与拆箱
//jdk5之前是手动装箱和拆箱
//手动装箱int --&gt;integer
int n1 =100;
Integer integer = new Integer(n1);
//在jdk9之后在使用会报错显示下面语句
&#39;Integer(int)&#39; is deprecated and marked for removal
//或者
Integer integer1 = Integer.valueOf(n1);

//手动拆箱
//Integer -&gt;int
int i = integer.intValue();

//jdk5之后可以实现自动装箱和拆箱
int n2 = 200;
//自动装箱 Int -&gt;Integer
Integer integer2 = n2;
 //自动拆箱
int n3 = integer2;
</code></pre>
<p>其余包装类均可以参照int类型</p>
<h3>包装类方法</h3>
<p><strong>类型转化</strong></p>
<pre><code class='language-java' lang='java'>//包装类（Integer）-&gt;String
        Integer i = 100;
        //方式一
        String str1 = i + &quot;&quot;;
        //方式二
        String str2 = i.toString();
        //方式三
        String str3 = String.valueOf(i);

        //String 转包装类（Integer）
        String str4 = &quot;123456&quot;;
        //方式一
        Integer i2 = Integer.parseInt(str4);
        //方式二
        Integer i3 = new Integer(str4);
        //该方法已经被弃用
		&#39;Integer(java.lang.String)&#39; is deprecated and marked for removal
</code></pre>
<p>可以直接查找某个包装类的方法</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201647279.png" referrerpolicy="no-referrer" alt="image-20230325223335476"></p>
<p>一些常用方法</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201647583.png" referrerpolicy="no-referrer" alt="image-20230325223413125"></p>
<h3>Integer面试题</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201647980.png" referrerpolicy="no-referrer" alt="image-20230325224114390"></p>
<pre><code class='language-java' lang='java'>//Integer.valueOf源码如下
 @IntrinsicCandidate
    public static Integer valueOf(int i) {
        if (i &gt;= IntegerCache.low &amp;&amp; i &lt;= IntegerCache.high)
            return IntegerCache.cache[i + (-IntegerCache.low)];
        return new Integer(i);
    }
</code></pre>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201647746.png" referrerpolicy="no-referrer" alt="image-20230325225251402"></p>
<h2>String</h2>
<h3>概念</h3>
<ol>
<li><p>String 对象用于保存字符串</p>
</li>
<li><p>字符串的字符使用的是Unicode字符编码，一个字符占两个字节</p>
</li>
<li><p>字符串的字符有许多构造器，实现了构造器重载</p>
</li>
<li><p>String类实现了 接口 Serializable[String 可以串行化：可以在网络中传输]</p>
<p>							接口 Comparable [String 对象可以比较大小]</p>
</li>
<li><p>String 是final 类， 不可以被其他类继承</p>
</li>
<li><p>String 有属性 private final char value[];用于存放字符串内容</p>
</li>
<li><p>注意:value 是一个final类型，不可以被修改（不可以修改地址，不代表是值）</p>
</li>

</ol>
<h3>创建机制</h3>
<pre><code class='language-java' lang='java'>		//方式一:直接赋值
        String s = &quot;yzd&quot;;
        //方式二：调用构造器
        String yzd = new String(&quot;yzd&quot;);
        //方式一：先从常量池中查看是否有“yzd”，如果有，则直接指向，如果没有则重新创建，然后指向，s最终指向的是常量池中的空间地址
        //方式二：先在堆中创建空间，里面维护了value属性，指向常量池的yzd空间，如果常量池没有“yzd”，重新创建，如果有通过value指向，最终指向的是堆中的空间地址
        
</code></pre>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201647196.png" referrerpolicy="no-referrer" alt="image-20230326205743749"></p>
<h3>字符串特性</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201647559.png" referrerpolicy="no-referrer" alt="image-20230326214107268"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201647128.png" referrerpolicy="no-referrer" alt="image-20230326214039327"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201647568.png" referrerpolicy="no-referrer" alt="image-20230326214003483"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201648082.png" referrerpolicy="no-referrer" alt="image-20230326214238349"></p>
<h3>Srtring常用方法</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201648458.png" referrerpolicy="no-referrer" alt="image-20230326215218828"></p>
<h2>StringBuffer</h2>
<h3>概念</h3>
<ol>
<li><p>StringBuffer的直接父类是AbstractStringBulider</p>
</li>
<li><p>StringBuffer 实现了Serialzable,即SttringBuffer的对象可以串行化</p>
</li>
<li><p>在父类 AbstractStringBulider 有属性char[] value,但不是final，该value数组存放字符串内容，因此存放在堆中</p>
</li>
<li><p>StringBuffer是final类，不可以被继承</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201648317.png" referrerpolicy="no-referrer" alt="image-20230326222322461"></p>
</li>

</ol>
<h3>转换</h3>
<p><strong>构造器使用：</strong></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201648425.png" referrerpolicy="no-referrer" alt="image-20230326222825282"></p>
<p><strong>类型转化：</strong></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201648266.png" referrerpolicy="no-referrer" alt="image-20230326223254775"></p>
<h3>常用方法</h3>
<ol>
<li><p>增：append</p>
</li>
<li><p>删：delete(m,n)</p>
<p>删除[m,n)的字符</p>
</li>
<li><p>改：replace(m,n,S)</p>
<p>修改[m,n)的字符改为S</p>
</li>
<li><p>查：indexOf</p>
<p>查找指定字符在字符串第一次出现的位置，如果找不到就返回-1</p>
</li>
<li><p>插：insert(m,S)</p>
<p>在原来索引为m的位置插入S字符，原来m位置的字符往后面移动</p>
<p>&nbsp;</p>
</li>

</ol>
<h2>StringBulider</h2>
<h3>概念</h3>
<p>一个可变的字符序列，提供了一个StringBuffer兼容的API，但不可保证同步（不是线程安全的），用在字符串缓冲区被单个线程使用的时候，在可能的情况下，建议优先使用该类</p>
<p>在StringBulider上经常使用的时append,insert</p>
<ol>
<li>StringBulider的直接父类是AbstractStringBulider</li>
<li>StringBulider 实现了Serialzable,即SttringBulider的对象可以串行化</li>
<li>在父类 AbstractStringBulider 有属性char[] value,但不是final，该value数组存放字符串内容，因此存放在堆中</li>
<li>StringBulider是final类，不可以被继承</li>
<li>StringBulider中的方法，没有做互斥的处理，即没有synchronized关键字，因此在单线程情况下使用</li>

</ol>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201649293.png" referrerpolicy="no-referrer" alt="image-20230327195349006"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201649904.png" referrerpolicy="no-referrer" alt="image-20230327195658857"></p>
<h2>Math</h2>
<h3>常用方法</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201649615.png" referrerpolicy="no-referrer" alt="image-20230327200551812"></p>
<h2>Arrays</h2>
<h3>sort 排序</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201649818.png" referrerpolicy="no-referrer" alt="image-20230327202146313"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201649635.png" referrerpolicy="no-referrer" alt="image-20230327202312553"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201649826.png" referrerpolicy="no-referrer" alt="image-20230327202423833"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201649644.png" referrerpolicy="no-referrer" alt="image-20230327202500729"></p>
<h3>binarySearch查找</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201650891.png" referrerpolicy="no-referrer" alt="image-20230327203300551"></p>
<h3>copyOf拷贝</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201650590.png" referrerpolicy="no-referrer" alt="image-20230327203521337"></p>
<h3>fill填充</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201650569.png" referrerpolicy="no-referrer" alt="image-20230327203612757"></p>
<h3>asList</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201650342.png" referrerpolicy="no-referrer" alt="image-20230327203939433"></p>
<h2>System</h2>
<h3>exit</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201650238.png" referrerpolicy="no-referrer" alt="image-20230327205124141"></p>
<h3>arraycopy</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201650659.png" referrerpolicy="no-referrer" alt="image-20230327205438349"></p>
<h3>currentTimeMillens</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201650377.png" referrerpolicy="no-referrer" alt="image-20230327205642350"></p>
<h2>大数处理</h2>
<h3>BigInteger</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201650720.png" referrerpolicy="no-referrer" alt="image-20230327210342977"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201651735.png" referrerpolicy="no-referrer" alt="image-20230327210354375"></p>
<h3>BigDecimal</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201651786.png" referrerpolicy="no-referrer" alt="image-20230327210506144"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201651070.png" referrerpolicy="no-referrer" alt="image-20230327211016497"></p>
<h2>Date</h2>
<h3>第一代日期类</h3>
<ol>
<li>Date:精确到毫秒，代表特定的瞬间</li>
<li>SimpleDateFormat：格式和解析日期的类，它允许进行格式化（日期-&gt;文本）和解析(文本-&gt;日期)和规范化</li>

</ol>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201651680.png" referrerpolicy="no-referrer" alt="image-20230327220025982"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201651965.png" referrerpolicy="no-referrer" alt="image-20230327220045778"></p>
<h3>第二代日期类Calendar</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201651582.png" referrerpolicy="no-referrer" alt="image-20230327220550019"></p>
<h3>第三代日期类</h3>
<p><strong>获取时间</strong></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201651310.png" referrerpolicy="no-referrer" alt="image-20230327221116195"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201651206.png" referrerpolicy="no-referrer" alt="image-20230327221500230"></p>
<p><strong>格式化</strong></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652211.png" referrerpolicy="no-referrer" alt="image-20230327221920088"></p>
<p><strong>时间戳</strong></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652063.png" referrerpolicy="no-referrer" alt="image-20230327222047457"></p>
<h1>集合</h1>
<ol>
<li><p>可以动态的保存任意多个元素</p>
</li>
<li><p>提供了一系列方便的操作对象的方法：add,remove,set,get等</p>
</li>
<li><p>使用集合删除，增加元素更加简单明了</p>
<p>&nbsp;</p>
</li>

</ol>
<h2>集合体系图</h2>
<ol>
<li>集合主要是两组（单列集合，双列集合）</li>
<li>Collection接口有两个重要的子接口List Set，他们的实现子类都是单列集合</li>
<li>Map接口的实现子类是双列集合，存放的K-V</li>

</ol>
<p><strong>单列集合</strong></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652008.png" referrerpolicy="no-referrer" alt="image-20230328191004490"></p>
<p><strong>双列集合</strong></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652696.png" referrerpolicy="no-referrer" alt="image-20230328191253680"></p>
<h2>Collection方法</h2>
<pre><code class='language-java' lang='java'> List list = new ArrayList();//使用List接口进行接收
        //add添加单个元素
        list.add(&quot;tom&quot;);
        list.add(10);
        list.add(&quot;jack&quot;);
        System.out.println(&quot;list=&quot;+list);
        //remove删除指定元素
        list.remove(0);//删除第一个元素
        list.remove(&quot;jack&quot;);//删除某个指定元素
        System.out.println(&quot;list=&quot;+list);
        //contains查询元素是否存在
        System.out.println(list.contains(&quot;jack&quot;));
        //size获取元素的个数
        System.out.println(list.size());
        //isEmpty判断是否为空
        System.out.println(list.isEmpty());
        //clear清空
        list.clear();
        //addAll添加多个元素
        ArrayList list1 = new ArrayList();
        list1.add(&quot;123&quot;);
        list1.add(&quot;abc&quot;);
        list.addAll(list1);
        //containsALL查找多个元素
        System.out.println(list.containsAll(list1));
        //removeAll三处多个元素
        list.removeAll(list1);
</code></pre>
<h2>迭代器遍历</h2>
<h3>介绍</h3>
<ol>
<li>Iterator对象称为迭代器，主要用于遍历Collection集合中的元素</li>
<li>实现了Collection接口的集合类都有一个Iterator()方法，用于返回一个实现了Iterator接口的对象，即返回一个迭代器</li>
<li>Iterator结构</li>

</ol>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652240.png" referrerpolicy="no-referrer" alt="image-20230328195852604"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652984.png" referrerpolicy="no-referrer" alt="image-20230328201214868"></p>
<p><strong>实现迭代器的快捷键--&gt;itit</strong></p>
<p><strong>增强for实现遍历</strong></p>
<ol>
<li>使用增强for，在Collection集合</li>
<li>增强for，底层依旧是迭代器</li>

</ol>
<pre><code class='language-java' lang='java'>for(Object book: col){
	System.out.println(&quot;book=&quot;+book);
}
</code></pre>
<p>快捷键方式 I</p>
<h3>实例演示</h3>
<pre><code class='language-java' lang='java'>import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

public class Main {
    @SuppressWarnings({&quot;all&quot;})
    public static void main(String[] args) {
        List list = new ArrayList();
        list.add(new Dog(&quot;小黑&quot;, 18));
        list.add(new Dog(&quot;小白&quot;,16));

        for(Object dog:list){
            System.out.println(dog);
        }
        System.out.println(&quot;++++++++++++++++++++++&quot;);
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
        return &quot;Dog{&quot; +
                &quot;name=&#39;&quot; + name + &#39;\&#39;&#39; +
                &quot;, age=&quot; + age +
                &#39;}&#39;;
    }
}
</code></pre>
<h2>List接口</h2>
<ol>
<li>List集合类的元素是有序的（添加顺序和取出顺去是一致的），且可以重复</li>
<li>List集合的每个元素都有其对应的顺序索引，即支持索引</li>
<li>List容器中的元素都有一个整数型的序号记录其在容器中的位置，可以根据序号存取容器中的元素</li>

</ol>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652456.png" referrerpolicy="no-referrer" alt="image-20230328205056613"></p>
<h3>常用方法</h3>
<pre><code class='language-java' lang='java'> List list = new ArrayList();
        list.add(&quot;张三丰&quot;);
        list.add(&quot;贾宝玉&quot;);
        //void add(int index,Object ele):在index位置插入ele元素
        //在index = 1的位置插入一个对象
        list.add(1,&quot;tom&quot;);
        System.out.println(&quot;list=&quot;+list);
        //boolean addAll(int index,Collection eles):从index位置开始将eles中所有元素添加进来
        List list1 = new ArrayList();
        list1.add(&quot;jack&quot;);
        list1.add(&quot;tom&quot;);
        list.addAll(1,list1);
        System.out.println(&quot;list:&quot;+list);
        //Object get(int index)获取index位置上的元素
        System.out.println(list.get(0));
        //int indexOf(Object obj)返回obj在集合中首次出现的位置
        System.out.println(list.indexOf(&quot;tom&quot;));
        //int lastIndexOf(Object  obj):返回obj在当前集合中最后出现的位置
        System.out.println(list.lastIndexOf(&quot;tom&quot;));
        //Object remove(int index):移除指定index位置的元素，并返回该元素
        list.remove(0);
        //Object set(int index,Object ele):设置指定位置上index位置的元素为ele，相当于时替换
        list.set(1,&quot;AAA&quot;);
        //List subList(int fromIndex,int toIndex):返回从fromIndex到toIndex位置的子集合
        //注意返回的子集合为 fromIndex&lt;=subList&lt;toIndex
        List returnlist = list.subList(0,2);
</code></pre>
<h3>遍历方式</h3>
<pre><code class='language-java' lang='java'>import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;
@SuppressWarnings({&quot;all&quot;})
public class Main {
    public static void main(String[] args) {
        //List的实现子类ArrayList,LinkedList,Vector的使用相同
        List list = new ArrayList();
        list.add(&quot;张三丰&quot;);
        list.add(&quot;贾宝玉&quot;);
        list.add(&quot;jack&quot;);
        //遍历
        //1.迭代器
        Iterator iterator = list.iterator();
        while (iterator.hasNext()) {
            Object obj =  iterator.next();
            System.out.println(obj);
        }
        System.out.println(&quot;-------------------------&quot;);
        //2.增强for循环
        for (Object obj:list) {
            System.out.println(obj);
        }
        System.out.println(&quot;-------------------------&quot;);
        //3.普通for循环
        for (int i = 0; i &lt; list.size(); i++) {
            System.out.println(list.get(i));
        }
        }


    }

</code></pre>
<h2>ArrayList</h2>
<h3>注意事项</h3>
<ol>
<li>ArrayList可以加入null，并且可以加入多个</li>
<li>ArrayList是由数组来实现数据储存的</li>
<li>ArrayList基本等同于Vector，除了ArrayList是线程不安全的（执行效率高），在多线程的情况下不建议使用ArrayList</li>

</ol>
<h3>扩容机制</h3>
<ol>
<li><p>ArrayList中维护了一个Object类型的数组elementData</p>
<p>transient Object[] elementData;//transient 表示瞬间，短暂的，表示该属性不会被序列化</p>
</li>
<li><p>当创建ArrayList对象时，如果使用的为无参构造器，则初始elementData的容量为0，第一次添加，则扩容为10，如需要再次扩容，则扩容为1.5倍</p>
</li>
<li><p>如果使用的为指定大小的构造器，则构造器elementData的容量为指定大小，如需扩容，则直接扩容为1.5倍</p>
</li>

</ol>
<h3>底层分析</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652126.png" referrerpolicy="no-referrer" alt="image-20230401192227488"></p>
<hr />
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652795.png" referrerpolicy="no-referrer" alt="image-20230401192802815"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652809.png" referrerpolicy="no-referrer" alt="image-20230401194346452"></p>
<h2>Vector</h2>
<h3>注意事项</h3>
<ol>
<li><p>类型说明</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652279.png" referrerpolicy="no-referrer" alt="image-20230401201807348"></p>
</li>
<li><p>Vector底层也是一个对象数组，protected Object[] elementData</p>
</li>
<li><p>Vector是线程同步的，即线程安全，操作方法带有synchronized</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652439.png" referrerpolicy="no-referrer" alt="image-20230401202014813"></p>
</li>
<li><p>在开发时需要考虑线程安全时，使用Vector</p>
</li>

</ol>
<h2>LinkedList</h2>
<h3>底层结构</h3>
<ol>
<li>LinkedList底层实现了双向链表和双端队列特点</li>
<li>可以添加任意元素，包括null</li>
<li>线程不安全，没有实现同步</li>

</ol>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652463.png" referrerpolicy="no-referrer" alt="image-20230401203940457"></p>
<h2>List集合选择</h2>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201652771.png" referrerpolicy="no-referrer" alt="image-20230401213715518"></p>
<h2>Set接口</h2>
<p><strong>基本介绍：</strong></p>
<ol>
<li>无序（添加和取出的顺序不一致），没有索引</li>
<li>不允许重复元素，所以最多包含一个null</li>

</ol>
<p><strong>常用方法：</strong></p>
<p>和List接口一样，Set接口也是Collection的子接口，因此，常用方法和Collection接口一样</p>
<p><strong>遍历方法：</strong></p>
<ol>
<li>迭代器</li>
<li>增强for</li>

</ol>
<p><strong>注意：</strong>但是无法使用索引的方式获取</p>
<h2>HashSet</h2>
<ol>
<li><p>HashSet实现了Set接口</p>
</li>
<li><p>HashSet实质上是HashMap</p>
<pre><code class='language-java' lang='java'>public HashSet(){
	map = new HashMap&lt;&gt;();
}
</code></pre>
<p>&nbsp;</p>
</li>
<li><p>可以存放null值，但是只可以有一个null</p>
</li>
<li><p>HashSet不保证元素是有序的，取决于hash后，在确认索引的结果</p>
</li>
<li><p>不可以有重复的元素/对象</p>
</li>

</ol>
<h3>底层分析</h3>
<ol>
<li>先获取元素的哈希值（hashcode方法）</li>
<li>对哈希值进行运算，得到一个索引值为要存放在哈希表中的位置号</li>
<li>如果该位置没有其他元素，则直接存放，如果位置有其他元素，则需要进行equals判断（并非一定要比较内容），如果相等，则不用添加，如不相等，则以链表的形式添加</li>
<li>HashSet的底层是HashMap，第一次添加时，table数组扩容到16，临界值(threshold)是16*0.75（加载因子）=12</li>
<li>如果table数组到了临界值12，就会扩容到32，新的临界值就是32*0.75=24，以此类推</li>
<li>在java8中，如果一条链表的元素个数到达TREEIFY_THRESHOLD(默认为8)，并且table的大小&gt;=MIN_TREEIFY_CAPACITY(默认为64)，就会进行树化（红黑树），否则仍会进行数组扩容机制</li>

</ol>
<h2>LinkedHashSet</h2>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201653891.png" referrerpolicy="no-referrer" alt="image-20230405150120866"></p>
<ol>
<li>LinkedHashSet是HashSet的子类</li>
<li>LinkedHashSet底层是LinkedHashMap，底层维护了一个数组+双向链表</li>
<li>LinkedHashSet根据元素的hashCOde值来决定元素的储存位置,同时使用链表维护元素的次序，是的元素看起来是以插入顺序保证的</li>
<li>LinkedHashSet不允许添加重复元素</li>

</ol>
<h2>TreeSet</h2>
<ol>
<li><p>当我们使用无参构造器时，创建的TreeSet，仍然是无序的</p>
</li>
<li><p>使用TreeSet提供的一个构造器，可以传入一个比较器(Comparator)并指定排序规则</p>
<pre><code class='language-java' lang='java'>public static void main(String[] args) {
        TreeSet treeSet = new TreeSet(new Comparator() {
            @Override
            public int compare(Object o1, Object o2) {
                return ((String)o1).compareTo((String) o2);
            }
        });
        treeSet.add(&quot;tom&quot;);
        treeSet.add(&quot;jack&quot;);
        treeSet.add(&quot;jreey&quot;);
        System.out.println(treeSet);
    }
</code></pre>
<p>&nbsp;</p>
</li>

</ol>
<h2>Map接口</h2>
<ol>
<li>Map与Collection并列存在，用于保存具有映射关系的数据：Key-Value（双列元素）</li>
<li>Map中的key和value可以是任何引用类型的数据，会封装到HAshMap$Node对象中</li>
<li>Map中的key不允许重复，当有相同的key时，相当于替换value</li>
<li>Map中的Value可以重复</li>
<li>Map中的key可以为null,value也可以为null，但是注意key有且仅有一个null,value可以有多个null</li>
<li>常用String类作为Map的key</li>
<li>key和value之间存在单向一对一关系，通过key总可以找到对应的value</li>
<li>Map存放数据的key-value示意图，一对k-v是放在HashMap$Node中，因为Node实现了Entry接口，有的书也称一堆k-v就是一个Entry</li>

</ol>
<h3>常用方法</h3>
<pre><code class='language-java' lang='java'>public static void main(String[] args) {
        Map map = new HashMap();
        //put:添加
        map.put(&quot;张三&quot;,&quot;李四&quot;);
        map.put(&quot;tom&quot;,&quot;jack&quot;);
        map.put(null,null);
        map.put(&quot;liming&quot;,null);
        //remove:根据键删除映射关系
        map.remove(null);
        //get:根据键获取值
        Object peo = map.get(&quot;张三&quot;);
        Object peo1 = map.get(&quot;张&quot;);
        System.out.println(peo);//李四
        System.out.println(peo1);//null
        //size:获取元素个数
        System.out.println(map.size());
        //isEmpty:判断个数是否为0
        System.out.println(map.isEmpty());
        //clear:清除
        map.clear();
        //containsKey:查找键是否存在
        System.out.println(map.containsKey(&quot;tom&quot;));
    }
</code></pre>
<h3>遍历方法</h3>
<pre><code class='language-java' lang='java'> public static void main(String[] args) {
        Map map = new HashMap();
        map.put(&quot;张三&quot;,&quot;李四&quot;);
        map.put(&quot;tom&quot;,&quot;jack&quot;);
        map.put(null,null);
        map.put(&quot;liming&quot;,null);
        //第一组:先取出所有的Key,通过Key取出对应的Value
        Set keyset = map.keySet();
        //1.增强for
        for (Object key:keyset) {
            System.out.println(key + &quot;-&quot;+ map.get(key));
        }
        //2.迭代器
        Iterator iterator = keyset.iterator();
        while (iterator.hasNext()) {
            Object key =  iterator.next();
            System.out.println(key + &quot;-&quot; +map.get(key));
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
        Set entrySet = map.entrySet();//使用EntrySet&lt;Map.Entry&lt;K,V&gt;&gt;
        //1.增强for
        for (Object entry:entrySet) {
            Map.Entry m = (Map.Entry)entry;
            System.out.println(m.getKey()+&quot;-&quot;+m.getValue());
        }
        //迭代器
        Iterator iterator2 = entrySet.iterator();
        while (iterator2.hasNext()) {
            Object next =  iterator2.next();
            Map.Entry m = (Map.Entry)next;
            System.out.println(m.getKey()+&quot;-&quot;+m.getValue());
        }
    }
</code></pre>
<p><strong>练习</strong></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201653710.png" referrerpolicy="no-referrer" alt="image-20230405174709382"></p>
<pre><code class='language-java' lang='java'>package demo;

import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;
import java.util.Set;

@SuppressWarnings({&quot;all&quot;})
class Test{
    public static void main(String[] args) {
        Map map = new HashMap();
        map.put(&quot;00001&quot;,new employee(&quot;tom&quot;,10000,&quot;00001&quot;));
        map.put(&quot;00002&quot;,new employee(&quot;jerry&quot;,20000,&quot;00002&quot;));
        map.put(&quot;00003&quot;,new employee(&quot;jack&quot;,30000,&quot;00003&quot;));
        Set keySet = map.keySet();
        System.out.println(&quot;第一种&quot;);
        for (Object key:keySet) {
            employee em = (employee)map.get(key);
            if(em.getSalary()&gt;18000)
            System.out.println(em);
        }
        System.out.println(&quot;第二种&quot;);
        Iterator iterator = keySet.iterator();
        while (iterator.hasNext()) {
            Object key =  iterator.next();
            employee em = (employee)map.get(key);
            if(em.getSalary()&gt;18000)
            System.out.println(em);
        }
        System.out.println(&quot;第三种&quot;);
        Set entrySet = map.entrySet();
        for (Object set:entrySet) {
            Map.Entry m = (Map.Entry)set;
            employee em = (employee) m.getValue();
            if(em.getSalary()&gt;18000)
            System.out.println(em);
        }
        System.out.println(&quot;第四种&quot;);
        Iterator iterator1 = entrySet.iterator();
        while (iterator1.hasNext()) {
            Object next =  iterator1.next();
            Map.Entry m = (Map.Entry)next;
            employee em = (employee) m.getValue();
            if(em.getSalary()&gt;18000)
            System.out.println(em);
        }
    }
}
@SuppressWarnings({&quot;all&quot;})
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

        return &quot;employee{&quot; +
                &quot;name=&#39;&quot; + name + &#39;\&#39;&#39; +
                &quot;, salary=&quot; + salary +
                &quot;, id=&#39;&quot; + id + &#39;\&#39;&#39; +
                &#39;}&#39;;
        }


}
</code></pre>
<h3>小结</h3>
<ol>
<li>Map接口的常用实现类：HashMap,HAshtable和Properties</li>
<li>HashMap是Map接口使用频率最高的实现类</li>
<li>HashMap是以Key-val对的方式来储存数据的</li>
<li>Key不可以重复，但是Value可以重复，允许使用null</li>
<li>如果添加1相同的Key，会覆盖原来的Key-val等于修改</li>
<li>和HashSet相同，不会保证映射的顺序，因为底层是以hash表的方式进行储存</li>
<li>HashMap没有实现同步，因此线程是不安全的</li>

</ol>
<h2>Hashtable</h2>
<ol>
<li>存放的元素是键值对：K-V</li>
<li>Hashtable的键和值都不能为null否则会抛出NullPointerException</li>
<li>HashTable的使用方法基本上和HashMap一致</li>
<li>HashTable是线程安全的，HashMap是线程不安全的</li>

</ol>
<p><strong>底层分析：</strong></p>
<ol>
<li>底层有数组Hashtable$Entry[] 初始化大小为11</li>
<li>临界值 threshold 8 = 11*0.75</li>
<li>扩容机制：当数量大于临界值时，按照*2+1的方式进行扩容</li>

</ol>
<h2>Properties</h2>
<ol>
<li>Properties类继承Hashtable类并且实现了Map接口，也是使用键值对的形式进行数据储存</li>
<li>使用特点与Hashtable相似</li>
<li>Properties还用于从xxx.Properties文件中，加载数据到Properties类对象，并进行读取与修改</li>

</ol>
<pre><code class='language-java' lang='java'>public static void main(String[] args) {
        Properties properties = new Properties();
        //添加
        properties.put(&quot;john&quot;,100);
        properties.put(&quot;lucy&quot;,100);
        properties.put(&quot;lic&quot;,100);
        //修改
        properties.put(&quot;lic&quot;,88);
        //查找
        System.out.println(properties.get(&quot;lic&quot;));
        //删除
        properties.remove(&quot;lic&quot;);
    }
</code></pre>
<h2>TreeMap</h2>
<ol>
<li><p>当我们使用无参构造器时，创建的TreeMap，仍然是无序的</p>
</li>
<li><p>使用TreeMap提供的一个构造器，可以传入一个比较器(Comparator)并指定排序规则</p>
<pre><code class='language-java' lang='java'>    public static void main(String[] args) {
        TreeMap treeMap = new TreeMap(new Comparator() {
            @Override
            public int compare(Object o1, Object o2) {
                return ((String)o1).compareTo((String)o2);
            }
        });
        treeMap.put(&quot;tom&quot;,&quot;300&quot;);
        treeMap.put(&quot;jack&quot;,&quot;200&quot;);
        treeMap.put(&quot;areey&quot;,&quot;100&quot;);
        System.out.println(treeMap);
    }
</code></pre>
<p>&nbsp;</p>
</li>

</ol>
<h2>集合选择</h2>
<ol>
<li><p>判断储存类型（一组对象[单列]或一组键值对[双列]）</p>
</li>
<li><p>一组对象[单列]：collection接口</p>
<p>允许重复：List</p>
<p>		增改多：LinkedList[底层维护了一个双向链表]</p>
<p>		改查多：ArrayList[底层维护 Object类型的可变数组]</p>
<p>不允许重复：Set</p>
<p>		无序：HashSet[底层是HashMap,维护了一个哈希表（数组+链表+红黑树）]</p>
<p>		排序：TreeSet</p>
<p>		插入和取出顺序一致：LinkedHashSet，维护数组+双向链表</p>
</li>
<li><p>一组键值对：Map</p>
<p>键无序：HashMap[底层是哈希表 jdk7:数组+链表，jdk8:数组+链表+红黑树]</p>
<p>键排序：TreeMap</p>
<p>键插入和取出顺序一致:LinkedHashMap</p>
<p>读取文件:Propreties</p>
<p>&nbsp;</p>
</li>

</ol>
<h2>Collections工具类</h2>
<h3>排序</h3>
<pre><code class='language-java' lang='java'>public static void main(String[] args) {
        List list = new ArrayList();
        list.add(&quot;tom&quot;);
        list.add(&quot;smith&quot;);
        list.add(&quot;jack&quot;);
        list.add(&quot;miss&quot;);
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
</code></pre>
<h3>查找替换</h3>
<pre><code class='language-java' lang='java'> public static void main(String[] args) {
        List list = new ArrayList();
        list.add(&quot;tom&quot;);
        list.add(&quot;smith&quot;);
        list.add(&quot;jack&quot;);
        list.add(&quot;miss&quot;);
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
        System.out.println(Collections.frequency(list,&quot;tom&quot;));
        //void copy(List dest,List src):将src中的元素拷贝到dest上
        List list1 = new ArrayList();
        //为了完成一次拷贝需要先给list1赋值，避免下标越界
        for (int i = 0; i &lt; list.size(); i++) {
            list1.add(&quot;&quot;);
        }
        Collections.copy(list1,list);
        System.out.println(list);
        //boolean replaceAll(List list,Object oldVal,Object newVal)
        Collections.replaceAll(list,&quot;tom&quot;,&quot;汤姆&quot;);
        System.out.println(list);
    }
</code></pre>
<p>&nbsp;</p>
<h1>泛型</h1>
<ol>
<li>泛型又称为参数化类型，是jdk5.0以后出现的新特性，解决数据类型的安全性问题</li>
<li>在类声明或实例化时只需要指定好需要的具体类型即可</li>
<li>java泛型可以保证如果程序在编译时没有发生警告，运行就不会产生ClassCastException异常，同时代码更加简洁，健壮</li>
<li>作用：可以在类声明时通过一个标识表示类中某个属性的类型，或者某个方法的返回值类型，或者是参数类型</li>

</ol>
<pre><code class='language-java' lang='java'>public class Test {
    public static void main(String[] args) {
        person&lt;String&gt; stringperson = new person&lt;String&gt;(&quot;123&quot;);
    }
}
class person&lt;E&gt;{
    E s;

    public person(E s) {
        this.s = s;
    }
    public E getS(){
        return s;
    }
}
</code></pre>
<h2>语法</h2>
<p> <strong>声明：</strong></p>
<p>interface接口<T>{}和class类&lt;K,V&gt;{}</p>
<ol>
<li><p>其中，T，K，V不代表值，表示类型</p>
</li>
<li><p>任意字母都可以，常用T表示，是Type的缩写</p>
<p>&nbsp;</p>
</li>

</ol>
<p>实例化:</p>
<p>在类名后面指定类型参数的值（类型）</p>
<pre><code class='language-java' lang='java'>List&lt;String&gt; strlist = new ArrayList&lt;String&gt;();
Iterator&lt;Customer&gt; iterator = customers.iterator();
</code></pre>
<h2>注意事项</h2>
<ol>
<li><p>T,K,V只能是引用类型，不能是基本数据类型</p>
</li>
<li><p>在给泛型指定了类型后，可以传入该类型或者子类型</p>
</li>
<li><p>泛型的定义形式</p>
<pre><code class='language-java' lang='java'>第一种
ArrayList&lt;Integer&gt; list1 = new ArrayList&lt;Integer&gt;();
在实际开发中往往会简写，编译器会进行类型推断
ArrayList&lt;Integer&gt; list = new ArrayList&lt;&gt;();
</code></pre>
</li>
<li><pre><code class='language-java' lang='java'>ArrayList arrayList = new ArrayList();
相当于
ArrayList&lt;Object&gt; objects = new ArrayList&lt;&gt;();
</code></pre>
<p>&nbsp;</p>
<p>&nbsp;</p>
</li>

</ol>
<h1>自定义泛型</h1>
<h2>自定义泛型类</h2>
<p><strong>基本语法</strong></p>
<p>class 类名 &lt;T,R...&gt;{//...表示可以有多个泛型成员}</p>
<p><strong>注意细节</strong></p>
<ol>
<li>普通成员可以使用泛型（属性，方法）</li>
<li>使用泛型的数组，不能进行初始化</li>
<li>静态方法中不能使用类的泛型</li>
<li>泛型类的类型，是在创建对象是确定的</li>
<li>如果在创建对象时，没有指定类型，默认为Object</li>

</ol>
<pre><code class='language-java' lang='java'>public class Test {

}
//1. Tiger后面具有泛型，一般将Tiger称为自定义泛型类
//2. T,R,M 为泛型的标识符
//3. 泛型的标识符可以有多个
//4. 普通成员可以使用泛型(属性，方法)
//5. 使用泛型的数组不可以初始化（数组在new时无法确定空间大小）
//6. 静态方法无法使用泛型（在类加载时，类仍未创建，JVM无法完成初始化）

class Tiger&lt;T,R,M&gt;{
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
</code></pre>
<h2>自定义泛型接口</h2>
<p><strong>基本语法</strong></p>
<p>interface接口名&lt;T,R...&gt;{</p>
<p>}</p>
<p><strong>注意细节</strong></p>
<ol>
<li><p>接口中，静态成员也不能使用泛型</p>
</li>
<li><p>泛型接口的类型，在继承接口或者实现接口时确定</p>
</li>
<li><p>没有指定类型，默认为Object</p>
<p>&nbsp;</p>
</li>

</ol>
<h2>自定义泛型方法</h2>
<p><strong>基本语法</strong></p>
<p>修饰符 &lt;T,R...&gt; 返回类型 方法名（参数列表）{</p>
<p>}</p>
<p><strong>注意细节</strong></p>
<ol>
<li>泛型方法，可以定义在普通类中，也可以定义在泛型类中</li>
<li>当泛型方法调用时，类型便会确定</li>
<li>public void eat(E e){},修饰符后没有&lt;T,R...&gt; eat方法不是泛型方法，而是使用了泛型</li>

</ol>
<h1>泛型的继承与通配符</h1>
<ol>
<li><p>泛型不具备继承性</p>
<pre><code class='language-java' lang='java'>List&lt;Object&gt; list = new ArraryList&lt;String&gt;();
//该代码不正确
</code></pre>
</li>
<li><p>&lt;?&gt;:支持任意泛型类型</p>
</li>
<li><p>&lt;? extends A&gt;:支持A类以及A类的子类，规定了泛型的上限</p>
</li>
<li><p>&lt;?super A&gt;:支持A类以及A类的子类，不限于父类，规定了泛型的下限</p>
</li>

</ol>
<h1>JUnit使用</h1>
<p>在测试对象前加上@Test，在按下alt+enter,选择添加5.8版本</p>
<h1>绘图机制</h1>
<pre><code class='language-java' lang='java'>import javax.swing.*;
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
        Image image = Toolkit.getDefaultToolkit().getImage(Mypanel.class.getResource(&quot;Snipaste_2022-11-04_17-36-21.png&quot;));
        g.drawImage(image,10,10,252,168,this);
        //画字符串 drawString
        g.setColor(Color.BLUE);
        g.setFont(new Font(&quot;隶书&quot;,Font.BOLD,50));
        g.drawString(&quot;中国&quot;,100,100);
    }
}
</code></pre>
<h1>事件处理机制</h1>
<p>java事件处理是采用的“委派事件模型”，当事件发生时，产生事件的对象，会把“信息”传递给“事件的监听者”处理，这里所说的“信息”实质上就是java.awt.event事件库里某个类所创建的对象，把它称为事件的对象。</p>
<ol>
<li>事件源：事件源是一个产生事件的对象，比如按钮，窗口</li>
<li>事件：事件就是承载事件源状态改变的对象，比如当键盘事件，鼠标事件，窗口事件等等，会生成一个事件对象，该对象保存着当前事件很多信息，比如KeyEvent对象有含有被按下键的Code值，java.awt.event包和javax.swing.event包中定义了各种事件类型</li>

</ol>
<h1>多线程</h1>
<ol>
<li>线程是由进程创建的，是进程的一个实体</li>
<li>一个进程可以拥有多个线程</li>
<li>单线程：同一时刻，只允许执行一个线程</li>
<li>多线程：同一时刻，可以执行多个线程</li>
<li>并发：同一时刻，多个任务交替执行，造成一种“貌似同时”的错觉，单核cpu实现的多任务就是并发</li>
<li>并行：同一个时刻，多个任务同时进行，多核cpu可以实现并行</li>

</ol>
<h2>继承Thread</h2>
<p><strong>简单演示：</strong></p>
<pre><code class='language-java' lang='java'>public class Main {
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
            System.out.println(&quot;喵喵，我是小猫咪&quot;+(++times));
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
</code></pre>
<h3>多线程机制</h3>
<pre><code class='language-java' lang='java'>public class Main {
    public static void main(String[] args) throws InterruptedException {
        //创建一个Cat对象，可以当作线程使用
        Cat cat = new Cat();
        cat.start();//启动线程-&gt;最终会执行Cat的run方法
        /*
            public void start() {
            synchronized (this) {
                // zero status corresponds to state &quot;NEW&quot;.
                if (holder.threadStatus != 0)
                    throw new IllegalThreadStateException();
                start0();
            }
        }
        真正实现多线程的是start0方法
         */
        //当main线程启动一个子线程Thread-0,主线程不会阻塞，继续进行
        for (int i = 0; i &lt; 60; i++) {
            System.out.println(&quot;主线程进行&quot;+i);
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
            System.out.println(&quot;喵喵，我是小猫咪&quot;+(++times));
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
</code></pre>
<h2>实现Runnable</h2>
<pre><code class='language-java' lang='java'>public class Test {
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
            System.out.println(&quot;汪，小狗汪汪叫&quot;+(++count)+&quot; 线程名称:&quot;+Thread.currentThread().getName());
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

</code></pre>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201653152.png" referrerpolicy="no-referrer" alt="image-20230408215451325"></p>
<h2>线程终止</h2>
<ol>
<li>当线程完成任务后，会自动退出</li>
<li>还可以通过使用变量来控制run()方法退出的方式停止线程，即通知方式</li>

</ol>
<pre><code class='language-java' lang='java'>public class Test {
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
            System.out.println(&quot;汪，小狗汪汪叫&quot;+(++count)+&quot; 线程名称:&quot;+Thread.currentThread().getName());
            //休眠一秒
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                throw new RuntimeException(e);
            }
            }
        }
    }
</code></pre>
<h2>常用方法</h2>
<p><strong>第一组：</strong></p>
<ol>
<li>setName：设置线程名称</li>
<li>getName: 返回该线程的名称</li>
<li>start: 使该线程开始执行，java虚拟机底层调用该线程的start0方法</li>
<li>run:调用该线程对象的run方法</li>
<li>setPriority:更改线程的优先级</li>
<li>getPriority: 获取线程的优先级</li>
<li>sleep: 在指定的毫秒数内让当前执行的线程休眠</li>
<li>interrupt:中断线程</li>

</ol>
<p><strong>第二组：</strong></p>
<ol>
<li><p>yield:线程的礼让，让出cpu，让其他线程执行，但礼让的时间不一定确定，所以礼让不一定成功。</p>
</li>
<li><p>join：线程的插队，插队的线程一旦成功，则先执行完插入的线程的所有任务。</p>
<pre><code class='language-java' lang='java'>public class Test {
    public static void main(String[] args) throws InterruptedException {
        Dog dog = new Dog();
        //dog.start();无法调用start
        //创建Thread对象，把dog对象(实现了Runnable)放入Thread
        Thread thread = new Thread(dog);
        thread.start();
        //输出五次hello后中断
        for (int i = 0; i &lt; 20; i++) {
            Thread.sleep(1000);
            System.out.println(&quot;主线程吃包子&quot;+i);
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
            for (int i = 0; i &lt; 20; i++) {
                try {
                    Thread.sleep(1000);
                } catch (InterruptedException e) {
                    throw new RuntimeException(e);
                }
                System.out.println(&quot;子线程吃包子&quot;+i);
            }
        }
    }
</code></pre>
<p>&nbsp;</p>
</li>

</ol>
<h2>守护线程</h2>
<ol>
<li>用户线程：也称为工作线程，当线程的任务执行完或通知方式结束</li>
<li>守护线程：一般是为工作线程服务，当所有的用户线程结束，守护线程自动结束</li>
<li>常见的守护线程：垃圾回收机制</li>

</ol>
<pre><code class='language-java' lang='java'>public class Test {
    public static void main(String[] args) throws InterruptedException {
        Dog dog = new Dog();
        //dog.start();无法调用start
        //创建Thread对象，把dog对象(实现了Runnable)放入Thread
        Thread thread = new Thread(dog);
        //将子线程设置为守护线程，当主线程结束时随之结束
        thread.setDaemon(true);
        thread.start();
        for (int i = 0; i &lt; 10; i++) {
            Thread.sleep(1000);
            System.out.println(&quot;主线程吃包子&quot;+i);
        }
    }
}
class Dog implements Runnable{
    int count;

    @Override
    public void run() {
            for (int i = 0; i &lt; 20;i++ ) {
                try {
                    Thread.sleep(1000);
                } catch (InterruptedException e) {
                    throw new RuntimeException(e);
                }
                System.out.println(&quot;子线程吃包子&quot;+i);
            }
        }
    }
</code></pre>
<h2>线程的七大状态</h2>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201653002.png" referrerpolicy="no-referrer" alt="image-20230409184114472"></p>
<h2>线程同步机制</h2>
<ol>
<li>在多线程编程中，一些敏感数据不允许被多个线程同时访问，此时就使用同步访问技术，保证数据在任意同一时刻，最多有一个线程访问，以保证数据的完整性</li>
<li>当有一个线程在对内存进行操作时，其他线程都不可以对这个内存地址进行操作，直到该线程完成操作，其他线程才可以对该内存地址进行操作</li>

</ol>
<p><strong>实现方法：</strong></p>
<ol>
<li><p>同步代码块</p>
<pre><code class='language-java' lang='java'>synchronized(对象){//得到对象的锁，才能操作同步代码
	//需要被同步的代码
}
</code></pre>
</li>
<li><p>synchronized还可以放在方法声明中，表示整个方法为同步方法</p>
<pre><code class='language-java' lang='java'>public synchronized void m(String name){
	//需要同步的代码
}
</code></pre>
<p>&nbsp;</p>
</li>

</ol>
<h2>互斥锁</h2>
<ol>
<li>java语言中，引入了对象互斥锁的概念，来保证共享数据的完整性</li>
<li>每一个对象都对应一个可称为&quot;互斥锁&quot;的标记，这个标记用来保证在任意时刻，只能有一个线程来访问该对象</li>
<li>关键字synchronized来与对象的互斥锁联系，当某个对象用synchronized修饰时，表明该对象在任一时刻只能有一个线程访问</li>
<li>同步的局限性：导致程序的执行效率要降低</li>
<li>同步方法（非静态的）的锁可以是this，也可以是其他对象（要求是同一个对象）</li>
<li>同步方法（静态的）的锁为当前类本身</li>

</ol>
<h2>线程死锁</h2>
<pre><code class='language-java' lang='java'>public class Test {
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
                    System.out.println(&quot;1&quot;);
                    synchronized (o2){
                        System.out.println(&quot;2&quot;);
                    }
                }
            }else {
                synchronized (o2){
                    System.out.println(&quot;3&quot;);
                    synchronized (o1){
                        System.out.println(&quot;4&quot;);
                    }
                }
            }
        }
    }
</code></pre>
<h2>释放锁</h2>
<ol>
<li>当代码块的同步方法，同步代码块执行结束</li>
<li>当前线程在同步方法，同步代码块中遇到break,return </li>
<li>当前线程在同步方法，同步代码块中出现了未处理的Error或Exception，导致异常结束</li>
<li>当前线程在同步方法，同步代码块中执行了线程对象的wait()方法，当前线程暂停，并且释放锁</li>

</ol>
<p><strong>不会释放锁的情况：</strong></p>
<ol>
<li>线程在执行同步方法，同步代码块中，程序调用了Thread.sleep(),Thread.yield()方法1暂停线程的执行，不会释放锁</li>
<li>线程在执行同步代码块时，其他线程调用了该线程的suspend()方法将线程挂起，该线程不会释放锁（尽量避免使用suspend()和resume()来控制线程，方法不再推荐使用）</li>

</ol>
<h1>IO流</h1>
<p>流：数据在数据源（文件）和程序（内存）之间经历的路径</p>
<p>输入流：数据从数据源（文件）到程序（内存）的路径</p>
<p>输出流：数据从程序（内存）到数据源（文件）的路径</p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304201653996.png" referrerpolicy="no-referrer" alt="image-20230417210408674"></p>
<h2>创建文件</h2>
<pre><code class='language-java' lang='java'>import java.io.File;
import java.io.IOException;
public class Main {

    public static void main(String[] args) {
        //方式一：new File(String pathname)
        //根据路径构建一个File对象
        String filePath = &quot;e:\\test.txt&quot;;
        File file = new File(filePath);
        try {
            file.createNewFile();
            System.out.println(&quot;创建成功&quot;);
        } catch (IOException e) {
            throw new RuntimeException(e);
        }
        //方法二；new File(File parent,String child)
        //根据父目录文件+子路径构建
        File parenrfile = new File(&quot;e:\\&quot;);
        String filename1 = &quot;test1.txt&quot;;
        //此处的file仅仅是一个对象，只有进行下面的creatNewFile才会有文件产生
        File file1 = new File(parenrfile, filename1);
        try {
            file1.createNewFile();
            System.out.println(&quot;创建成功&quot;);
        } catch (IOException e) {
            throw new RuntimeException(e);
        }
        //方法三：new File(String parent,String child)//根据父母录+子路径构建
        String parentPath = &quot;e:\\&quot;;
        String filename2 = &quot;test2.txt&quot;;
        File file2 = new File(parentPath, filename2);
        try {
            file2.createNewFile();
            System.out.println(&quot;创建成功&quot;);
        } catch (IOException e) {
            throw new RuntimeException(e);
        }
    }
}

</code></pre>
<h2>获取文件信息</h2>
<pre><code class='language-java' lang='java'>import java.io.File;

public class Test {

    public static void main(String[] args) {
        new Test().info();
    }
    //获取文件信息
    public void info(){
        //创建文件对象
        File file = new File(&quot;E:\\teat.txt&quot;);
        //调用相应的方法，得到对应信息
        System.out.println(&quot;文件名:&quot;+file.getName());
        System.out.println(&quot;文件绝对路径:&quot;+file.getAbsoluteFile());
        System.out.println(&quot;文件父级目录:&quot;+file.getParent());
        System.out.println(&quot;文件大小(字节):&quot;+file.length());
        System.out.println(&quot;文件是否存在:&quot;+file.exists());
        System.out.println(&quot;是否为一个文件:&quot;+file.isFile());
        System.out.println(&quot;是否为一个目录:&quot;+file.isDirectory());
    }
}

</code></pre>
<h2>目录操作</h2>
<pre><code class='language-java' lang='java'>import java.io.File;

public class Test {

    public static void main(String[] args) {
        new Test().m();
        new Test().m2();
        new Test().m3();
    }
    //判断文件e:\test.txt是否存在，存在就删除
    public void m(){
        String filePath = &quot;e:\\test.txt&quot;;
        File file = new File(filePath);
        if (file.exists()){
            if(file.delete()){
                System.out.println(filePath+&quot;删除成功&quot;);
            }
            else {
                System.out.println(filePath+&quot;删除失败&quot;);
            }
        }else {
            System.out.println(&quot;该文件不存在&quot;);
        }
    }
    //判断目录d:\demo1是否存在，存在就删除
    public void m2(){
        String filePath = &quot;d:\\demo1&quot;;
        File file = new File(filePath);
        if (file.exists()){
            if(file.delete()){
                System.out.println(filePath+&quot;删除成功&quot;);
            }
            else {
                System.out.println(filePath+&quot;删除失败&quot;);
            }
        }else {
            System.out.println(&quot;该目录不存在&quot;);
        }
    }
    //判断目录e:\\demo\\a\\b,是否存在，没有就创建
    public void m3(){
        String filePath = &quot;e:\\demo\\a\\b&quot;;
        File file = new File(filePath);
        if (file.exists()){
            System.out.println(&quot;该目录存在&quot;);
        }else {
            //使用mkdirs创建多级目录，使用mkdir创建一级目录
                if(file.mkdirs()){
                    System.out.println(filePath+&quot;创建成功&quot;);
                }
                else {
                    System.out.println(filePath+&quot;创建失败&quot;);
                }
        }
    }
}

</code></pre>
<h2>IO流原理</h2>
<p>分类：</p>
<ol>
<li>按操作数据单位不同分为：字节流二进制文件，字符流文本文件</li>
<li>按数据流的流向不同分为：输入流，输出流</li>
<li>按流的角色不同分为：节点流，处理流/包装流</li>

</ol>
<figure class='table-figure'><table>
<thead>
<tr><th>抽象基类</th><th>字节流</th><th>字符流</th></tr></thead>
<tbody><tr><td>输入流</td><td>InputStream</td><td>Reader</td></tr><tr><td>输出流</td><td>OutputStream</td><td>Writer</td></tr></tbody>
</table></figure>
<ol>
<li>java IO流的共涉及40多个类，实际上非常规则，都是从如上4个抽象基类派生的</li>
<li>由着四个类派生的子类名称都是以其父类名作为子类后缀</li>

</ol>
<h2>FileInputStream</h2>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222319800.png" referrerpolicy="no-referrer" alt="image-20230420193357077"></p>
<pre><code class='language-java' lang='java'>import java.io.FileInputStream;
import java.io.IOException;

public class Test {

    public static void main(String[] args) {

    }
    //使用read()读取
    @org.junit.jupiter.api.Test
    public void readFile(){
        String filePath = &quot;e:\\test.txt&quot;;
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
        String filePath = &quot;e:\\test.txt&quot;;
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

</code></pre>
<h2>FileOutputStream</h2>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222319928.png" referrerpolicy="no-referrer" alt="image-20230420200653426"></p>
<pre><code class='language-java' lang='java'>import java.io.FileOutputStream;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {

    }
    @org.junit.jupiter.api.Test
    public void writeFile(){
        //创建FileOutPutStream
        String filePath = &quot;e:\\test.txt&quot;;
        FileOutputStream fileOutputStream = null;
        try {
            // 得到fileOutputStream对象
            // 1.new FileOutputStream(filePath)会覆盖原来内容
            // 2.new FileOutputStream(filePath,true)会追加原来内容
            fileOutputStream = new FileOutputStream(filePath);
            //写入一个字节
            fileOutputStream.write(&#39;a&#39;);
            //写入一个字符串
            String str = &quot;hello word&quot;;
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
</code></pre>
<h2>文件拷贝</h2>
<pre><code class='language-java' lang='java'>import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        //文件拷贝 将C:\\Users\\17946\\Pictures\\1.png拷贝到E:\\
        //1.创建文件的输入流，将文件输入到程序
        //2.创建文件的输出流，将程序输出到文件
        FileInputStream fileInputStream = null;
        FileOutputStream fileOutputStream = null;
        String srcFilePath = &quot;C:\\Users\\17946\\Pictures\\1.png&quot;;
        String destFilePath = &quot;E:\\1.png&quot;;

        try {
            fileInputStream = new FileInputStream(srcFilePath);
            fileOutputStream = new FileOutputStream(destFilePath);
            //定义一个字节数组
            byte[] bytes = new byte[1024];
            int readLen = 0;
            while ((readLen = fileInputStream.read(bytes))!=-1){
                fileOutputStream.write(bytes,0,readLen);//一定要使用这个方法
            }
            System.out.println(&quot;拷贝成功&quot;);
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
</code></pre>
<h2>FileReader</h2>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222319048.png" referrerpolicy="no-referrer" alt="image-20230422145209611"></p>
<p><strong>相关方法：</strong></p>
<ol>
<li>new FileReader(File/String)</li>
<li>read:每次读取单个字符，返回该字符，如果读到文件末尾返回-1</li>
<li>read(char[]):批量读取多个字符到数组，返回读取到的字符数，如果到文件末尾返回-1</li>

</ol>
<p>相关API：</p>
<ol>
<li>new String(char[]):将char[]转换成String</li>
<li>new String(char[],off,len):将char[]指定部分转换成String</li>

</ol>
<pre><code class='language-java' lang='java'>//单个字符读取文件
import java.io.FileReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        String filePath = &quot;E:\\test.txt&quot;;
        //创建fileReader对象
        FileReader fileReader = null;
        int data = &#39; &#39;;
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
</code></pre>
<pre><code class='language-java' lang='java'>//字符数组读取
import java.io.FileReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        String filePath = &quot;E:\\test.txt&quot;;
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
</code></pre>
<p>&nbsp;</p>
<h2>FileWriter</h2>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222319725.png" referrerpolicy="no-referrer" alt="image-20230422152413409"></p>
<ol>
<li>new FileWriter(File/String):覆盖模式，相当于流的指针在首端</li>
<li>new FileWriter(File/String,true):追加模式，相当于流的模式在尾端</li>
<li>write(int):写入单个字符</li>
<li>write(char[]):写入指定数组</li>
<li>write(char[],off,len):写入指定数组的指定部分</li>
<li>write(string):写入整个字符串</li>
<li>write(string,off,len):写入字符串的指定部分</li>

</ol>
<p>相关API：String类：toCharArray:将String转换成char[]</p>
<p>注意：FileWriter使用后，必须要关闭（close）或刷新（flush），否则写入不到指定文件</p>
<pre><code class='language-java' lang='java'>import java.io.FileWriter;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        String filePath = &quot;E:\\test.txt&quot;;
        //创建fileReader对象
        FileWriter fileWriter = null;
        char[] ch = {&#39;a&#39;,&#39;b&#39;,&#39;c&#39;};
        try {
            fileWriter = new FileWriter(filePath);
//            1. write(int):写入单个字符
            fileWriter.write(&#39;H&#39;);
//            2. write(char[]):写入指定数组
            fileWriter.write(ch);
//            3. write(char[],off,len):写入指定数组的指定部分
            fileWriter.write(&quot;abnb&quot;.toCharArray(),0, ch.length);
//            4. write(string):写入整个字符串
            fileWriter.write(&quot;aba&quot;);
//            5. write(string,off,len):写入字符串的指定部分
            fileWriter.write(&quot;aba&quot;,0,3);

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
</code></pre>
<h2>节点流 处理流</h2>
<ol>
<li>节点流：节点流可以从一个特定的数据源读写数据，如FileReader,FileWriter</li>
<li>处理流：（也叫包装流）是连接已经存在的流（节点流或处理流）之上，为程序提供更为强大的读写功能，如BufferedReder,BufferedWriter</li>

</ol>
<p>区别：</p>
<ol>
<li>节点流是底层流 / 低级流，直接跟数据源相关。</li>
<li>处理流（包装流）包装节点流，既可以消除不同节点流的实现差异，也可以提供更方便的方法来完成输入输出</li>
<li>处理流（包装流）对节点流进行包装，使用了修饰器设计模式，会直接和数据源相连</li>

</ol>
<p>处理流的功能主要体现在以下两个方面：</p>
<ol>
<li>性能的提高：主要以增加缓冲的方式来提高输入输出的效率</li>
<li>操作的便捷：处理流肯提供一系列便捷的方法来一次输入输出大批的数据，使得操作更加灵活方便</li>

</ol>
<h2>BufferedReader</h2>
<pre><code class='language-java' lang='java'>import java.io.BufferedReader;
import java.io.FileReader;

public class Main {
    public static void main(String[] args) throws Exception {
        String filePath = &quot;E:\\test.txt&quot;;
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
</code></pre>
<p>&nbsp;</p>
<h2>BufferedWriter</h2>
<pre><code class='language-java' lang='java'>import java.io.BufferedWriter;
import java.io.FileWriter;

public class Main {
    public static void main(String[] args) throws Exception {
        String filePath = &quot;E:\\test.txt&quot;;
        //创建BufferedWriter
        //如果需要以追加的方式写入，在FileWriter加入true
        BufferedWriter bufferedWriter = null;
        bufferedWriter = new BufferedWriter(new FileWriter(filePath));
        bufferedWriter.write(&#39;a&#39;);
        //插入和系统相关的换行符
        bufferedWriter.newLine();
        bufferedWriter.write(&quot;dfghjkl&quot;);
        bufferedWriter.close();
    }

}
</code></pre>
<h2>Buffered拷贝</h2>
<pre><code class='language-java' lang='java'>import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.FileReader;
import java.io.FileWriter;

public class Main {
//  BufferedWriter和BufferedReader是处理字符的
//  操作二进制文件可能会造成文件损坏
    public static void main(String[] args) throws Exception {
        String srcPath = &quot;E:\\test.txt&quot;;
        String destPath = &quot;E:\\test1.txt&quot;;
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
</code></pre>
<h2>Buffered字节处理</h2>
<pre><code class='language-java' lang='java'>import java.io.BufferedInputStream;
import java.io.BufferedOutputStream;
import java.io.FileInputStream;
import java.io.FileOutputStream;

public class Main {

    public static void main(String[] args) throws Exception {
        String srcPath = &quot;C:\\Users\\17946\\Pictures\\微信图片_20230413222042.jpg&quot;;
        String destPath = &quot;E:\\1.jpg&quot;;
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
</code></pre>
<h2>对象处理流</h2>
<ol>
<li><p>序列化：保存值和数据类型</p>
</li>
<li><p>反序列化：将保存在文件的值和数据类型恢复成对象</p>
</li>
<li><p>需要让某个对象支持序列化机制，必须让这个类可序列化，则必须实现如下两个接口</p>
<ol>
<li>Serialized</li>
<li>Externalizable该接口需要实现，一般使用第一种</li>

</ol>
<p>&nbsp;</p>
</li>

</ol>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222319905.png" referrerpolicy="no-referrer" alt="image-20230422191417691"></p>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222319804.png" referrerpolicy="no-referrer" alt="image-20230422191529621"></p>
<h2>ObjectOutputStream</h2>
<pre><code class='language-java' lang='java'>import java.io.FileOutputStream;
import java.io.ObjectOutputStream;

public class Main {

    public static void main(String[] args) throws Exception {
        //在进行序列化时，按照自己的格式进行，文件名后缀没有实际意义
        String filePath = &quot;e:\\a.txt&quot;;
        ObjectOutputStream oos = null;
        oos = new ObjectOutputStream(new FileOutputStream(filePath));
        //序列化对象到文件中
        //int -&gt; Integer(Integer实现了serialized接口)
        oos.writeInt(100);
        oos.writeBoolean(true);//boolean -&gt; Boolean
        oos.writeChar(&#39;a&#39;);
        oos.writeUTF(&quot;asdfgh&quot;);
        oos.writeObject(new Dog(&quot;旺财&quot;));
        oos.close();
        System.out.println(&quot;序列化完成&quot;);
    }

}

</code></pre>
<pre><code class='language-java' lang='java'>import java.io.Serializable;

public class Dog implements Serializable {
    private String name;

    public Dog(String name) {
        this.name = name;
    }

    @Override
    public String toString() {
        return &quot;Dog{&quot; +
                &quot;name=&#39;&quot; + name + &#39;\&#39;&#39; +
                &#39;}&#39;;
    }
}
</code></pre>
<p>&nbsp;</p>
<h2>ObjectInputStream</h2>
<pre><code class='language-java' lang='java'>import java.io.FileInputStream;
import java.io.ObjectInputStream;

public class Main {

    public static void main(String[] args) throws Exception {
        //指定进行反序列化的文件
        String filePath = &quot;e:\\a.txt&quot;;
        ObjectInputStream ois = null;
        ois = new ObjectInputStream(new FileInputStream(filePath));
        //读取的顺序和序列化的顺序一致
//        oos.writeInt(100);
//        oos.writeBoolean(true);//boolean -&gt; Boolean
//        oos.writeChar(&#39;a&#39;);
//        oos.writeUTF(&quot;asdfgh&quot;);
//        oos.writeObject(new Dog(&quot;旺财&quot;));
        System.out.println(ois.readInt());
        System.out.println(ois.readBoolean());
        System.out.println(ois.readChar());
        System.out.println(ois.readUTF());
        Object dog = ois.readObject();
        System.out.println(dog);
        ois.close();
        System.out.println(&quot;反序列化完成&quot;);
    }

}


</code></pre>
<p><strong>重点细节：</strong></p>
<p>在调用Dog方法时需要向下转型，因此我们需要将Dog类的定义放在可以引用的位置</p>
<p><strong>细节：</strong></p>
<ol>
<li>读写顺序一致</li>
<li>要求序列化或反序列化对象，需要实现Serizlizable</li>
<li>序列化的类中建议添加SerialVersionUID，为了提高版本的jianrx</li>
<li>序列化对象时，默认将里面的所有属性都进行序列化，但是除了static或transient修饰的成员</li>
<li>序列化对象时，要求里面的属性也需要实现序列化接口</li>
<li>序列化具备可继承性，如果某类实现了序列化，则其子类也默认实现了序列化</li>

</ol>
<h2>标准输入输出流</h2>
<p>&nbsp;</p>
<figure class='table-figure'><table>
<thead>
<tr><th style='text-align:center;' >&nbsp;</th><th>类型</th><th style='text-align:center;' >默认设备</th></tr></thead>
<tbody><tr><td style='text-align:center;' >System.in 标准输入</td><td>InputStream</td><td style='text-align:center;' >键盘</td></tr><tr><td style='text-align:center;' >System.out 标准输出</td><td>PrintStream</td><td style='text-align:center;' >显示器</td></tr></tbody>
</table></figure>
<h2>转换流</h2>
<ol>
<li><strong>InPutStreamReader</strong>:Reader的子类，可以将InPutStream(字节流)包装成Reader(字符流)</li>
<li><strong>OutPutStreamWriter</strong>:Writer的子类，可以将OutPutStream(字节流)包装成Writer(字符流)</li>
<li>当处理纯文本文件时，如果使用字符流的效率更高，并且可以有效地解决中文问题，所以建议将字节流转换成字符流</li>
<li>可以在使用时指定编码格式（比如utf-8,gbk,gb2312,ISO8859-1等）</li>

</ol>
<h2>InPutStreamReader</h2>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222320499.png" referrerpolicy="no-referrer"></p>
<pre><code class='language-java' lang='java'>import java.io.BufferedReader;
import java.io.FileInputStream;
import java.io.InputStreamReader;

public class Main {

    public static void main(String[] args) throws Exception {
        String filePath = &quot;e:\\test.txt&quot;;
        InputStreamReader isr = null;
        //将FileInputStream转换成InputStreamReader
        //指定编码utf-8
        isr = new InputStreamReader(new FileInputStream(filePath),&quot;utf-8&quot;);
        //传入BufferedReader
        BufferedReader br = new BufferedReader(isr);
        String line;
        while ((line = br.readLine())!=null){
            System.out.println(line);
        }
        br.close();
    }

}


</code></pre>
<p>&nbsp;</p>
<h2>OutPutStreamWriter</h2>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222320597.png" referrerpolicy="no-referrer" alt="image-20230422214905914"></p>
<pre><code class='language-java' lang='java'>import java.io.FileOutputStream;
import java.io.OutputStreamWriter;

public class Main {

    public static void main(String[] args) throws Exception {
        String filePath = &quot;e:\\test.txt&quot;;
        OutputStreamWriter outputStreamWriter = new OutputStreamWriter(new FileOutputStream(filePath),&quot;utf-8&quot;);
        outputStreamWriter.write(&quot;dfghj&quot;);
        outputStreamWriter.close();
    }

}


</code></pre>
<h2>打印流</h2>
<p>只有输出，没有输入</p>
<h3>PrintStream</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222320411.png" referrerpolicy="no-referrer" alt="image-20230422220921597"></p>
<pre><code class='language-java' lang='java'>import java.io.PrintStream;

public class Main {

    public static void main(String[] args) throws Exception {
        PrintStream out = System.out;
        //在默认情况下，PrintStream的标准输出在显示器
        out.println(&quot;out&quot;);
        //因为PrintStream的底层实现为writer，所以可以直接使用writer
        out.write(&quot;ghhg&quot;.getBytes());
        out.close();
        //可以修改打印位置
        //修改到e:\test.txt
        System.setOut(new PrintStream(&quot;e:\\test.txt&quot;));
        System.out.println(&quot;sgsgsg&quot;);
    }

}


</code></pre>
<h3>PrintWriter</h3>
<p><img src="https://raw.githubusercontent.com/yzd11/yzd.github.io/master/img/202304222320358.png" referrerpolicy="no-referrer" alt="image-20230422221027415"></p>
<pre><code class='language-java' lang='java'>import java.io.PrintWriter;

public class Main {

    public static void main(String[] args) throws Exception {
        PrintWriter printWriter = new PrintWriter(System.out);
        printWriter.print(&quot;dfghj&quot;);
        printWriter.close();
        PrintWriter printWriter1 = new PrintWriter(new PrintWriter(&quot;e:\\test.txt&quot;));
        printWriter1.print(&quot;adaad&quot;);
        //flush/关闭流 才会将数据写入文件
        printWriter1.close();
    }

}


</code></pre>
<h2>Properties</h2>
<ol>
<li><p>专门用来读写配置文件的集合类</p>
<p>配置文件的格式：</p>
<p>键  = 值</p>
<p>键  = 值</p>
</li>
<li><p>键值对不需要有空格，值不需要用引号包裹，默认类型是String</p>
</li>
<li><p>常用方法</p>
<ol>
<li>load:加载配置文件的键值到Properties对象</li>
<li>list:将数据显示到指定设备</li>
<li>getProperty(Key)：根据键取值</li>
<li>setProperty(Key,value):设置键值对到Properties对象</li>
<li>store:将Properties中的键值对储存到配置文件，在idea中，保存信息到配置文件，如果有中文，会存储为unicode码</li>

</ol>
<pre><code class='language-java' lang='java'>import java.io.FileReader;
import java.util.Properties;

public class Main {

    public static void main(String[] args) throws Exception {
        //创建Properties对象
        Properties properties = new Properties();
        //加载指定配置文件
        properties.load(new FileReader(&quot;src\\Mysql.properties&quot;));
        //将k-v显示在控制台
        properties.list(System.out);
        //根据键获取相应的值
        String user = properties.getProperty(&quot;user&quot;);
        System.out.println(user);
    }

}


</code></pre>
<p>&nbsp;</p>
</li>

</ol>
<h1>网络编程</h1>
<h2>相关概念</h2>
<p>网络通信：</p>
<ol>
<li>概念：两台设备之间通过网络实现数据传输</li>
<li>将数据通过网络从一台设备传输到另一台设备</li>
<li>java.net包下提供了一系列的类或接口，供程序员使用，完成网络通信</li>

</ol>
<p>网络：</p>
<ol>
<li><p>概念：两台或多台设备通过一定的物理设备连接起来构成网络</p>
</li>
<li><p>分类</p>
<ol>
<li>局域网：覆盖范围最小，仅仅覆盖一个教室或一个机房</li>
<li>城域网：覆盖范围较大，可以覆盖一个城市</li>
<li>广域网：覆盖范围最大，可以覆盖全国，甚至全球，万维网是广域网的代表</li>

</ol>
<h2>IP地址</h2>
<ol>
<li>概念：用于唯一标识网络中每台计算机/主机</li>
<li>查看ip地址：ipconfig</li>
<li>ip表示形式：点分十进制 xx.xx.xx.xx</li>
<li>每一个十进制数的范围：0-255</li>
<li>ip地址的组成=网络地址+主机地址，比如：192.168.16.69</li>
<li>IPv6是互联网工程任务组设计的用于替代Ipv4的下一代IP协议，其地址数量号称可以为全世界的每一粒沙子编写一个地址</li>
<li>由于IPv4最大的问题在于网络地址资源有限，严重制约了互联网的应用和发展。IPv6的使用，不仅可以解决网络资源数量的问题，而且也可以解决多种设备连入互联网的障碍</li>

</ol>
</li>

</ol>
<p><img src="../AppData/Roaming/Typora/typora-user-images/image-20230423235508750.png" referrerpolicy="no-referrer" alt="image-20230423235508750"></p>
<h2>域名和端口</h2>
<p>域名：</p>
<ol>
<li>概念：将ip地址映射成域名</li>
<li>优点：方便记忆，解决记ip的问题</li>
<li>列如:<a href='http://www.baidu.com' target='_blank' class='url'>www.baidu.com</a></li>

</ol>
<p>端口：</p>
<ol>
<li><p>概念：用于标识计算机上某个特定的网络程序</p>
</li>
<li><p>表示形式：以整数形式，范围0~65535</p>
</li>
<li><p>0-1024已被占用，比如ssh 22, ftp 21, smtp 25, http 80</p>
</li>
<li><p>常见的网络程序端口号：</p>
<p>tomcat:8080</p>
<p>mysql:3306</p>
<p>oracle:1521</p>
<p>sqlserver:1433</p>
</li>

</ol>
<h2>网络协议</h2>
<p>协议：</p>
<p>TCP/IP协议（Transmission Control Protocol/Internet Protocol）</p>
<p>中文译名为传输控制协议/因特网互联协议，又叫做网络通讯协议，这个协议是Internet最基本的协议，Internet国际互联网的基础，简单将，就是由网络层的IP协议和传输层的TCP协议组成的</p>
<p><img src="../AppData/Roaming/Typora/typora-user-images/image-20230424183505894.png" referrerpolicy="no-referrer" alt="image-20230424183505894"></p>
<p>TCP协议:传输控制协议</p>
<ol>
<li>在使用TCP协议前，必须先建立TCP连接，形成传输数据通道</li>
<li>传输前，采用“三次握手”方式，是可靠的</li>
<li>在连接过程中可进行大数据量的传输</li>
<li>传输完毕，需要释放建立的连接，效率低</li>

</ol>
<p>UDP协议：用户数据协议</p>
<ol>
<li>将数据，源，目的封装成数据包，不需要建立连接</li>
<li>每个数据包的大小限制在64K内，不适合传输大量数据</li>
<li>因为无需连接，故此是不可靠的</li>
<li>发送数据结束时无需释放资源（因为不是面向连接的），速度快</li>

</ol>
<h2>InetAddress</h2>
<pre><code class='language-java' lang='java'>import java.net.InetAddress;
import java.net.UnknownHostException;

public class Main {
    public static void main(String[] args) throws UnknownHostException {
        //获取本机的InetAddress 对象
        InetAddress localHost = InetAddress.getLocalHost();//LAPTOP-RTGA2J39/10.62.116.128
        System.out.println(localHost);
        //根据指定主机名，获取InetAddress对象
        InetAddress byName = InetAddress.getByName(&quot;LAPTOP-RTGA2J39&quot;);
        System.out.println(byName);
        //根据域名，获取InetAddress对象
        InetAddress byName1 = InetAddress.getByName(&quot;www.baidu.com&quot;);
        System.out.println(byName1);
        //根据InetAddress对象，获取地址
        String hostAddress = byName1.getHostAddress();
        System.out.println(hostAddress);
        //根据InetAddress对象，获取主机名/域名
        String hostName = byName1.getHostName();
        System.out.println(hostName);
    }
}
</code></pre>
<h2>Socket</h2>
<ol>
<li>套接字（Socket）开发网络应用程序被广泛采用，以至于成为事实上的标准</li>
<li>通信的两端都要有Socket，是两台机器间通信的端点</li>
<li>网络通信其实就是Socket间的通信</li>
<li>Socket允许程序把网络连接当成一个流，数据在两个Socket间通过IO传输</li>
<li>一般主动发起通信的应用程序属于客户端，等待通信请求的为服务端</li>

</ol>
<h2>TCP字节流编程</h2>
<pre><code class='language-java' lang='java'>import java.io.IOException;
import java.io.InputStream;
import java.io.OutputStream;
import java.net.ServerSocket;
import java.net.Socket;

public class SocketTCP01Server {
    public static void main(String[] args) throws IOException {
        //1.在本机的9999端口监听，等待连接
        //要求在本机没有其他服务监听9999端口
        //serverSocket可以通过accept返回多个socket
        ServerSocket serverSocket = new ServerSocket(9999);
        System.out.println(&quot;服务端在9999端口监听，等待连接&quot;);
        //2.当客户端没有连接9999端口时，程序会阻塞，等待连接
        //如果有客户段来连接，就会返回一个Socket对象
        Socket socket = serverSocket.accept();
        System.out.println(&quot;服务端Socket连接完成&quot;);
        //3.通过socket.getInputStream()读取客户端写入的数据，显示
        InputStream inputStream = socket.getInputStream();
        //4.IO输入
        byte[] bytes = new byte[1024];
        int readLen = 0;
        while ((readLen = inputStream.read(bytes))!=-1){
            System.out.println(new String(bytes,0,readLen));
        }
        //5.获取socket相关的输出流
        OutputStream outputStream = socket.getOutputStream();
        outputStream.write(&quot;hello Client&quot;.getBytes());
        //设置结束标记
        socket.shutdownOutput();
        //6.关闭流和资源
        outputStream.close();
        inputStream.close();
        socket.close();
        System.out.println(&quot;服务端退出&quot;);
    }
}

</code></pre>
<pre><code class='language-java' lang='java'>import java.io.IOException;
import java.io.InputStream;
import java.io.OutputStream;
import java.net.InetAddress;
import java.net.Socket;

/**
 * @author 禹治东
 * @version 1.0
 */
public class SocketTCP01Client {
    public static void main(String[] args) throws IOException {
        //1.连接服务器（ip,端口）
        //连接本机的9999端口，如果成功返回Socket对象
        Socket socket = new Socket(InetAddress.getLocalHost(),9999);
        System.out.println(&quot;客户端Socket连接完成&quot;);
        //2.连接以后，生产Socket,通过
        //得到Socket对象关联的输出流对象
        OutputStream outputStream = socket.getOutputStream();
        //3.通过输出流写入数据到数据通道
        outputStream.write(&quot;hello Server&quot;.getBytes());
        //设置结束标记
        socket.shutdownOutput();
        //4.获取socket相关的输入流
        InputStream inputStream = socket.getInputStream();
        byte[] bytes = new byte[1024];
        int readLen = 0;
        while ((readLen = inputStream.read(bytes))!=-1){
            System.out.println(new String(bytes,0,readLen));
        }
        //5.关闭相关的流和资源
        inputStream.close();
        outputStream.close();
        socket.close();
        System.out.println(&quot;客户端退出&quot;);
    }
}

</code></pre>
<h2>TCP字符流编程</h2>
<pre><code class='language-java' lang='java'>import java.io.*;
import java.net.ServerSocket;
import java.net.Socket;

public class SocketTCP01Server {
    public static void main(String[] args) throws IOException {
        //1.在本机的9999端口监听，等待连接
        //要求在本机没有其他服务监听9999端口
        //serverSocket可以通过accept返回多个socket
        ServerSocket serverSocket = new ServerSocket(9999);
        System.out.println(&quot;服务端在9999端口监听，等待连接&quot;);
        //2.当客户端没有连接9999端口时，程序会阻塞，等待连接
        //如果有客户段来连接，就会返回一个Socket对象
        Socket socket = serverSocket.accept();
        System.out.println(&quot;服务端Socket连接完成&quot;);
        //3.通过socket.getInputStream()读取客户端写入的数据，显示
        InputStream inputStream = socket.getInputStream();
        //4.IO输入
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(inputStream));
        String s = bufferedReader.readLine();
        System.out.println(s);
        //5.获取socket相关的输出流
        OutputStream outputStream = socket.getOutputStream();
        BufferedWriter bufferedWriter = new BufferedWriter(new OutputStreamWriter(outputStream));
        bufferedWriter.write(&quot;hello Client&quot;);
        bufferedWriter.newLine();
        bufferedWriter.flush();
        //6.关闭流和资源
        bufferedReader.close();
        bufferedWriter.close();
        socket.close();
        System.out.println(&quot;服务端退出&quot;);
    }
}

</code></pre>
<pre><code class='language-java' lang='java'>import java.io.*;
import java.net.InetAddress;
import java.net.Socket;

public class SocketTCP01Client {
    public static void main(String[] args) throws IOException {
        //1.连接服务器（ip,端口）
        //连接本机的9999端口，如果成功返回Socket对象
        Socket socket = new Socket(InetAddress.getLocalHost(),9999);
        System.out.println(&quot;客户端Socket连接完成&quot;);
        //2.连接以后，生产Socket,通过
        //得到Socket对象关联的输出流对象
        OutputStream outputStream = socket.getOutputStream();
        //3.通过输出流写入数据到数据通道
        BufferedWriter bufferedWriter = new BufferedWriter(new OutputStreamWriter(outputStream));
        bufferedWriter.write(&quot;hello Server&quot;);
        bufferedWriter.newLine();//插入换行符，表示结束，但要求对方也需要用readLine来读
        bufferedWriter.flush();//使用字符流需要手动刷新
        //4.获取socket相关的输入流
        InputStream inputStream = socket.getInputStream();
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(inputStream));
        String s = bufferedReader.readLine();
        System.out.println(s);
        //5.关闭相关的流和资源
        bufferedReader.close();
        bufferedWriter.close();
        socket.close();
        System.out.println(&quot;客户端退出&quot;);
    }
}
</code></pre>
<h2>网络上传文件</h2>
<pre><code class='language-java' lang='java'>import java.io.*;
import java.net.ServerSocket;
import java.net.Socket;

public class TCPFileUpLoadServer {
    public static void main(String[] args) throws IOException {
        //1.在本机的9999端口监听，等待连接
        //要求在本机没有其他服务监听9999端口
        //serverSocket可以通过accept返回多个socket
        ServerSocket serverSocket = new ServerSocket(9999);
        System.out.println(&quot;服务端在9999端口监听，等待连接&quot;);
        //2.当客户端没有连接9999端口时，程序会阻塞，等待连接
        //如果有客户段来连接，就会返回一个Socket对象
        Socket socket = serverSocket.accept();
        System.out.println(&quot;服务端Socket连接完成&quot;);
        //3.通过socket.getInputStream()读取客户端写入的数据，显示
        BufferedInputStream bis = new BufferedInputStream(socket.getInputStream());
        byte[] bytes = StreamUtils.readBytes(bis);
        //4.将得到的bytes写入指定路径
        String destFile = &quot;src\\1.jpg&quot;;
        BufferedOutputStream bos = new BufferedOutputStream(new FileOutputStream(destFile));
        bos.write(bytes);
        bos.close();
        //回复收到图片
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(socket.getOutputStream()));
        bw.write(&quot;收到图片&quot;);
        bw.flush();//刷新
        socket.shutdownOutput();
        //5.关闭相应的资源
        bw.close();
        bis.close();
        socket.close();
        serverSocket.close();
    }
}

</code></pre>
<pre><code class='language-java' lang='java'>import java.io.*;
import java.net.InetAddress;
import java.net.Socket;

public class TCPFileUpLoadClient {
    public static void main(String[] args) throws IOException {
        //1.连接服务器（ip,端口）
        //连接本机的9999端口，如果成功返回Socket对象
        Socket socket = new Socket(InetAddress.getLocalHost(),9999);
        System.out.println(&quot;客户端Socket连接完成&quot;);
        //2.创建读取磁盘文件的输入流
        String filePath = &quot;e:\\1.jpg&quot;;
        BufferedInputStream bis = new BufferedInputStream(new FileInputStream(filePath));
        //借用工具类转换成字节数组
        byte[] bytes = StreamUtils.readBytes(bis);
        //通过socket得到输出流
        BufferedOutputStream bos = new BufferedOutputStream(socket.getOutputStream());
        bos.write(bytes);//将对应的字节数组写入数据通道
        bis.close();
        socket.shutdownOutput();//设置写入标识
        //接受从Server收到的信息
        BufferedReader br = new BufferedReader(new InputStreamReader(socket.getInputStream()));
        System.out.println(br.readLine());
        //关闭相关的流
        br.close();
        bos.close();
        socket.close();
    }
}

</code></pre>
<pre><code class='language-java' lang='java'>import java.io.ByteArrayOutputStream;
import java.io.IOException;
import java.io.InputStream;

public class StreamUtils {
    public static byte[] readBytes(InputStream inputStream) throws IOException {
        ByteArrayOutputStream buffer = new ByteArrayOutputStream();
        int nRead;
        byte[] data = new byte[1024];
        while ((nRead = inputStream.read(data, 0, data.length)) != -1) {
            buffer.write(data, 0, nRead);
        }
        buffer.flush();
        return buffer.toByteArray();
    }
}

</code></pre>
<p>&nbsp;</p>
<h2>netstat</h2>
<ol>
<li>netstst -an 可以查看当前主机网络情况，包括端口监听情况和网络连接情况</li>
<li>netstst -an|more 可以分页显示</li>
<li>netstat -anb显示具体应用在监听</li>

</ol>
<h2>UDP网络通信编程</h2>
<p><strong>基本介绍：</strong></p>
<ol>
<li>类DatagramSocket 和 DatagramPacket[数据包/数据报]实现了基于UDP协议的网络程序</li>
<li>UDP数据报通过数据报套接字 DatagramSocket 发送和接受，系统不保证UDP数据报一定可以安全的送到目的地，也不能确定什么时候可以抵达</li>
<li>DatagramPacket 对象封装了UDP数据报，在数据报中包含了发送端的IP地址和端口号以及接收端的IP地址和端口号</li>
<li>UDP协议中每个数据报都给出了完整的地址信息，因此无需建立发送方和接受方的连接</li>

</ol>
<p><strong>说明：</strong></p>
<ol>
<li>没有明确的服务端和客户端，演变成数据的发送端和接收端</li>
<li>接受数据和发送数据是通过 DatagramSocket对象完成</li>
<li>将数据封装到DatagramPacket对象/装包</li>
<li>当接收到DatagramPacket对象，需要进行拆包，取出数据</li>
<li>DatagramSocket可以指定在那个端口接受数据</li>

</ol>
<pre><code class='language-java' lang='java'>import java.io.IOException;
import java.net.DatagramPacket;
import java.net.DatagramSocket;
import java.net.InetAddress;

public class UDPReceiver {
    public static void main(String[] args) throws IOException {
        //创建一个DatagramSocket接收数据
        DatagramSocket datagramSocket = new DatagramSocket(9999);
        //构建一个DatagramPacket对象接收数据
        byte[] bytes = new byte[1024];
        DatagramPacket datagramPacket = new DatagramPacket(bytes, bytes.length);
        //调用接受方法接收数据
        //填充到datagrampacket
        //当端口没有接收到数据包会产生阻塞
        System.out.println(&quot;接收端等待连接&quot;);
        datagramSocket.receive(datagramPacket);
        //把datagrampacket进行拆包
        int len = datagramPacket.getLength();
        byte[] data = datagramPacket.getData();//接收数据
        String s = new String(data, 0, len);
        System.out.println(s);
        //回复
        bytes = &quot;hello Sender&quot;.getBytes();
        datagramPacket = new DatagramPacket(bytes, bytes.length, InetAddress.getByName(&quot;10.62.116.128&quot;), 9998);
        datagramSocket.send(datagramPacket);
        //关闭资源
        datagramSocket.close();
        System.out.println(&quot;接收端退出&quot;);
    }
}

</code></pre>
<pre><code class='language-java' lang='java'>import java.io.IOException;
import java.net.DatagramPacket;
import java.net.DatagramSocket;
import java.net.InetAddress;

public class UDPSender {
    public static void main(String[] args) throws IOException {
        //创建DatagramSocket对象
        DatagramSocket datagramSocket = new DatagramSocket(9998);
        byte[] bytes = &quot;hello Receiver&quot;.getBytes();
        DatagramPacket datagramPacket = new DatagramPacket(bytes, bytes.length, InetAddress.getByName(&quot;10.62.116.128&quot;), 9999);
        datagramSocket.send(datagramPacket);
        //接收回复
        byte[] bytes1 = new byte[1024];
        datagramPacket = new DatagramPacket(bytes1, bytes1.length);
        datagramSocket.receive(datagramPacket);
        int len = datagramPacket.getLength();
        byte[] data = datagramPacket.getData();
        String s = new String(data, 0, len);
        System.out.println(s);
        datagramSocket.close();
        System.out.println(&quot;发送端退出&quot;);
    }
}

</code></pre>
<h2>TCP文件下载</h2>
<pre><code class='language-java' lang='java'>import java.io.*;
import java.net.ServerSocket;
import java.net.Socket;

public class TCPServer {
    public static void main(String[] args) throws IOException {
        //创建serverSocket监听9999端口
        ServerSocket serverSocket = new ServerSocket(9999);
        System.out.println(&quot;服务端在监听&quot;);
        //进行连接
        Socket socket = serverSocket.accept();
        InputStream inputStream = socket.getInputStream();
        byte[] bytes = new byte[1024];
        int len = 0;
        String s = &quot; &quot;;
        //使用while循环是为了将来现在的文件较大的情况
        while ((len = inputStream.read(bytes))!=-1){
            s += new String(bytes, 0, len);
        }
        System.out.println(&quot;客户端希望下载名:&quot;+s);
        String resFile = &quot;&quot;;
        //如果是1就返回1，否则返回默认的2
        if (s.equals(&quot;1&quot;) ){
            resFile = &quot;src\\1.txt&quot;;
        }
        else {
            resFile = &quot;src\\2.txt&quot;;
        }
        //创建输入流
        BufferedInputStream bis = new BufferedInputStream(new FileInputStream(resFile));
        //使用工具类，读取文件到字节数组
        byte[] bytes1 = StreamUtils.readBytes(bis);
        //得到一个和socket相关的输出流
        BufferedOutputStream bos = new BufferedOutputStream(socket.getOutputStream());
        //写入数据通道
        bos.write(bytes1);
        socket.shutdownOutput();
        //关闭相关资源
        inputStream.close();
        bis.close();
        bos.close();
        socket.close();
        serverSocket.close();
    }
}

</code></pre>
<pre><code class='language-java' lang='java'>import java.io.*;
import java.net.InetAddress;
import java.net.Socket;
import java.util.Scanner;

public class TCPClient {
    public static void main(String[] args) throws IOException {
        //接受用户输入
        System.out.println(&quot;请输入下载文件名&quot;);
        Scanner scanner = new Scanner(System.in);
        String downFile = scanner.nextLine();
        //客户端连接服务器
        Socket socket = new Socket(InetAddress.getLocalHost(), 9999);
        //获取输出流
        OutputStream outputStream = socket.getOutputStream();
        outputStream.write(downFile.getBytes());
        //设置结束标志
        socket.shutdownOutput();
        //读取服务端文件
        BufferedInputStream bis = new BufferedInputStream(socket.getInputStream());
        byte[] bytes = StreamUtils.readBytes(bis);
        //得到一个输出流
        String filePath = &quot;e:\\&quot;+downFile+&quot;.txt&quot;;
        BufferedOutputStream bos = new BufferedOutputStream(new FileOutputStream(filePath));
        bos.write(bytes);
        //关闭相关资源
        bos.close();
        bis.close();
        socket.close();
        outputStream.close();
    }
}
</code></pre>
<pre><code class='language-java' lang='java'>import java.io.ByteArrayOutputStream;
import java.io.IOException;
import java.io.InputStream;

public class StreamUtils {
    public static byte[] readBytes(InputStream inputStream) throws IOException {
        ByteArrayOutputStream buffer = new ByteArrayOutputStream();
        int nRead;
        byte[] data = new byte[1024];
        while ((nRead = inputStream.read(data, 0, data.length)) != -1) {
            buffer.write(data, 0, nRead);
        }
        buffer.flush();
        return buffer.toByteArray();
    }
}

</code></pre>
<h1>反射机制</h1>
<h2>入门案例</h2>
<pre><code class='language-java' lang='java'>package aaa.reflection.question;

import aaa.Cat;

import java.io.FileReader;
import java.lang.reflect.Method;
import java.util.Properties;

public class reflectionQuestion {
    public static void main(String[] args) throws Exception {
        Properties properties = new Properties();
        properties.load(new FileReader(&quot;src\\re.properties&quot;));
        String classfullpath = properties.get(&quot;classfullpath&quot;).toString();
        String methodName = properties.get(&quot;method&quot;).toString();
//        System.out.println(classfullpath);
        //加载类
        Class cls = Class.forName(classfullpath);
        //通过cls得到加载的类的对象实例
        Cat o = (Cat)cls.getDeclaredConstructor().newInstance();
        //通过cls得到加载的类可以得到 methodName 的方法对象
        //在反射机制中可以将方法视为对象
        Method method = cls.getMethod(methodName);
        //通过methed 调用方法，即通过方法对象来实现调用方法
        method.invoke(o);
    }
}

</code></pre>
<pre><code class='language-java' lang='java'>package aaa;

public class Cat {
     private String name = &quot;招财猫&quot;;
     public void hi(){
         System.out.println(&quot;hi&quot;+name);
     }
}

</code></pre>
<pre><code class='language-java' lang='java'>classfullpath = aaa.Cat
method = hi
</code></pre>
<h2>反射原理</h2>
<ol>
<li>反射机制允许程序在执行期间借助Reflectiopn API取得任何类的内部信息（比如成员变量，构造器，成员方法等等），并能操作对象的方法，反射在设计模式和框架底层都会用到</li>
<li>加载完成类以后，再堆中就产生了一个Class类型的对象（一个类只包含一个Class对象），这个对象包含了类的完整结构信息。通过这个对象得到这个类的结构，这个对象就像一面镜子，透过这个镜子可以看到类的结构，所以形象的称之为反射。</li>

</ol>
<p><img src="../AppData/Roaming/Typora/typora-user-images/image-20230426184200077.png" referrerpolicy="no-referrer" alt="image-20230426184200077"></p>
<h2>反射相关类</h2>
<ol>
<li>java.lang.Class: 代表一个类，Class对象表示某个类加载后在堆中生成的对象</li>
<li>java.lang.reflect.Method: 代表类的方法，Method对象表示某个类的方法</li>
<li>java.lang.reflect.Field: 代表类的成员变量，Field对象表示某个类的成员变量</li>
<li>java.lang.reflect.Constructor: 代表类的构造方法，Constructor对象表示构造器</li>

</ol>
<pre><code class='language-java' lang='java'>public class reflectionQuestion {
    public static void main(String[] args) throws Exception {
        Properties properties = new Properties();
        properties.load(new FileReader(&quot;src\\re.properties&quot;));
        String classfullpath = properties.get(&quot;classfullpath&quot;).toString();
        String methodName = properties.get(&quot;method&quot;).toString();
        //加载类
        Class cls = Class.forName(classfullpath);
        //通过cls得到加载的类的对象实例
        Cat o = (Cat)cls.getDeclaredConstructor().newInstance();
        //通过cls得到加载的类可以得到 methodName 的方法对象
        //在反射机制中可以将方法视为对象
        Method method = cls.getMethod(methodName);
        //通过methed 调用方法，即通过方法对象来实现调用方法
        method.invoke(o);
        //得到Field字段
//        getField无法得到私有属性
        Field field = cls.getField(&quot;age&quot;);
        System.out.println(field.get(o));
        //传统方法 对象.成员变量     反射 成员变量对象.get(对象)
        Constructor constructor = cls.getConstructor();//()可以指定参数类型
        System.out.println(constructor);
        Constructor constructor1 = cls.getConstructor(String.class);
        System.out.println(constructor1);//传入的为String类型的Class对象
    }
}
</code></pre>
<h2>反射调用优化</h2>
<ol>
<li>优点：可以动态的创建和使用对象（也是框架底层核心），使用灵活，没有反射机制，框架技术就失去底层支撑</li>
<li>使用反射基本是解释执行，对执行速度有影响</li>

</ol>
<pre><code class='language-java' lang='java'>package aaa.reflection.question;

import aaa.Cat;

import java.lang.reflect.Method;

public class Reflection {
    public static void main(String[] args) throws Exception {
        new Reflection().m1();
        new Reflection().m2();
        new Reflection().m3();
    }
    //使用传统方法
    public void m1(){
        long start = System.currentTimeMillis();
        Cat cat = new Cat();
        for (int i = 0; i &lt; 100000000; i++) {
            cat.hi();
        }
        long end = System.currentTimeMillis();
        System.out.println(&quot;传统方法时间:&quot;+(end-start));
    }
    //使用反射
    public void m2() throws Exception {
        long start = System.currentTimeMillis();
        Class cls = Class.forName(&quot;aaa.Cat&quot;);
        Object o = cls.getConstructor().newInstance();
        Method method = cls.getMethod(&quot;hi&quot;);
        for (int i = 0; i &lt; 100000000; i++) {
            method.invoke(o);
        }
        long end = System.currentTimeMillis();
        System.out.println(&quot;反射方法时间:&quot;+(end-start));
    }
    public void m3() throws Exception{
        long start = System.currentTimeMillis();
        Class cls = Class.forName(&quot;aaa.Cat&quot;);
        Object o = cls.getConstructor().newInstance();
        Method method = cls.getMethod(&quot;hi&quot;);
        //取消访问检查进行优化
        method.setAccessible(true);
        for (int i = 0; i &lt; 100000000; i++) {
            method.invoke(o);
        }
        long end = System.currentTimeMillis();
        System.out.println(&quot;优化方法时间:&quot;+(end-start));
    }
}



</code></pre>
<pre><code class='language-java' lang='java'>package aaa;

public class Cat {
     private String name = &quot;招财猫&quot;;
     public int age = 10;

    public Cat(String name) {
        this.name = name;
    }

    public Cat(){

    }
     public void hi(){
//         System.out.println(&quot;hi&quot;+name);
         for (int i = 0; i &lt; 100000; i++) {

         }
     }
}

</code></pre>
<h2>Class类分析</h2>
<pre><code class='language-java' lang='java'>public class Class01 {
    public static void main(String[] args) throws Exception {
        //1.Class也是类，因此继承Object类
        //2.Class对象不是new出来的，而是系统创建的
        //(1)传统new对象
        Cat cat = new Cat();
        //(2)反射方式
        /*
        Classloader类,仍然是通过ClassLoader类加载Cat类的Class对象
        public Class&lt;?&gt; loadClass(String name) throws ClassNotFoundException {
        return loadClass(name, false);
        }
         */
        Class cls = Class.forName(&quot;aaa.Cat&quot;);
        //3.对于某个类的Class对象，在内存中只有一份，因为类只加载一次
        //4.每个对象实例都知道自己是由那个Class对象生成的
        //5.通过Class对象，可以完整的得到一个类的完整结构，通过一系列API
        //6.Class对象存放在堆中
        //7.类的字节码二进制文件，是放在方法区的，有的地方称为类的元数据(包含方法代码，变量名，方法名，访问权限...)
    }
}
</code></pre>
<h2>Class相关方法</h2>
<pre><code class='language-java' lang='java'>package aaa.reflection.question;

import java.lang.reflect.Field;

public class Class02 {
    public static void main(String[] args) throws Exception {
        String classAllPath = &quot;aaa.Cat&quot;;
        //1.获取相应的Class对象
        Class cls = Class.forName(classAllPath);
        //2.输出cls
        System.out.println(cls);//显示cls对象，是哪个类的Class对象 aaa.Cat
        System.out.println(cls.getClass());//输出cls的运行类型
        //3.得到包名
        System.out.println(cls.getPackage().getName());
        //4.得到全类名
        System.out.println(cls.getName());
        //5.通过cls创建对象实例
        Object o = cls.getConstructor().newInstance();
        System.out.println(o.toString());
        //6.通过反射得到属性
        Field field = cls.getField(&quot;age&quot;);
        System.out.println(field.get(o));
        //7.通过反射给属性赋值
        field.set(o,20);
        System.out.println(field.get(o));
        //8.得到所有的属性字段
        Field[] fields = cls.getFields();
        for (Field f : fields) {
            System.out.println(f.getName());//名称
        }
    }
}

</code></pre>
<h2>获取Class对象的六种方式</h2>
<pre><code class='language-java' lang='java'>package aaa.reflection.question;

import aaa.Cat;

public class GetClass_ {
    public static void main(String[] args) throws Exception {
        //1.已知一个类的全类名，并且在类的路径下，可以通过Class类的静态方法forNmae()获取，可能会抛出ClassNotFoundExpection
        //多用于配置文件，读取全类名，加载类
        String classAllPath = &quot;aaa.Cat&quot;;//通过读取配置文件获取
        Class cls = Class.forName(classAllPath);
        System.out.println(cls);
        //2.通过类名.class
        //用于参数传递
        Class cls1 = Cat.class;
        System.out.println(cls1);
        //3.对象.getClass()
        //用于有对象实例
        Cat cat = new Cat();
        Class cls2 = cat.getClass();
        System.out.println(cls2);
        //4.通过类加载器[4种]获取到类的Class对象
        //(1)得到类加载器
        ClassLoader classLoader = cat.getClass().getClassLoader();
        //(2)通过类加载器得到class对象
        Class cls3 = classLoader.loadClass(classAllPath);
        System.out.println(cls3);
        //5.基本数据类型(int, char, boolean, float )
        Class&lt;Integer&gt; integerClass = int.class;
        System.out.println(integerClass);
        //基本数据类型对应的包装类，可以通过.TYPE得到Class对象
        Class&lt;Integer&gt; type = Integer.TYPE;
        System.out.println(type);
    }
}

</code></pre>
<h2>具有Class对象的类型</h2>
<pre><code class='language-java' lang='java'>package aaa.reflection.question;

import java.io.Serializable;

public class GetClass_ {
    public static void main(String[] args) throws Exception {
        Class&lt;String&gt; stringClass = String.class;//外部类
        Class&lt;Serializable&gt; serializableClass = Serializable.class;//接口
        Class&lt;Integer[]&gt; aClass = Integer[].class;//数组
        Class&lt;float[][]&gt; aClass1 = float[][].class;//二维数组
        Class&lt;Deprecated&gt; deprecatedClass = Deprecated.class;//注解
        Class&lt;Thread.State&gt; stateClass = Thread.State.class;//枚举
        Class&lt;Long&gt; longClass = long.class;//基本数据类型
        Class&lt;Integer&gt; type = Integer.TYPE;//包装类
        Class&lt;Void&gt; voidClass = void.class;//返回类型
        Class&lt;Class&gt; classClass = Class.class;//Class本身
    }
}

</code></pre>
<h2>动态加载和静态加载</h2>
<ol>
<li>静态加载: 编译时加载相关的类，如果没有则报错，依赖性太强</li>
<li>动态加载: 运行时加载需要的类，如果没有运行不需要加载，不会报错，降低了依赖性</li>

</ol>
<pre><code class='language-java' lang='java'>switch(key){
	case &quot;1&quot;:
		Dog dog = new Dog();
		dog.cry();
		break;
	case &quot;2&quot;:
    	Class cls = Class.forName(&quot;Person&quot;);
    	Object o = cls.getConstructor().newInstance();
    	Method m = cls.getMethod(&quot;hi&quot;);
    	m.invoke(o);
    	break;
    default:
    	System.out.println(&quot;do nothing&quot;)
}
</code></pre>
<p><strong>类加载时机:</strong></p>
<ol>
<li>当创建对象时(new)//静态加载</li>
<li>当子类被调用时，父类也加载//静态加载</li>
<li>调用类中的静态成员时//静态加载</li>
<li>通过反射//动态加载</li>

</ol>
<h2>类加载流程图</h2>
<p><img src="../AppData/Roaming/Typora/typora-user-images/image-20230426214749705.png" referrerpolicy="no-referrer" alt="image-20230426214749705"></p>
<p><img src="../AppData/Roaming/Typora/typora-user-images/image-20230426214947324.png" referrerpolicy="no-referrer" alt="image-20230426214947324"></p>
<h2>类加载五阶段</h2>
<p><strong>加载阶段</strong></p>
<p>JVM包在该阶段的主要目的是将字节码从不同的数据源(可能是class文件，也可能是jar包，甚至是网络)转换成二进制字节流加载到内存中，并生成一个代表该类的java.lang.Class对象</p>
<p><strong>连接阶段-验证</strong></p>
<ol>
<li>目的是为了确保Class文件的字节流中包含的信息符合当前虚拟机的要求，并不会危害虚拟机自身的安全</li>
<li>包括：文件格式验证（是否以魔数 oxcafebabe开），元数据验证，字节码验证和符号引用验证</li>
<li>可以考虑使用-Xverify:none参数关闭大部分的类验证措施，缩短虚拟机类加载的时间</li>

</ol>
<p><strong>连接阶段-准备：</strong></p>
<ol>
<li>JVM会在该阶段对静态变量，分配内存并进行默认初始化（对应数据类型的默认初始值，如0,OL,null,flase等）。这些变量所使用的内存都将在方法去进行分配</li>

</ol>
<p><strong>连接阶段-解析：</strong></p>
<p>虚拟机将常量池的符号引用替换成直接引用的过程</p>
<p><strong>初始化：</strong></p>
<ol>
<li>在初始化阶段，才真正开始执行类中定义的java代码，此阶段执行的是<clinit>()方法的过程</li>
<li><clinit>()方法是由编译器按照语句在源文件中出现的顺序，依次自动收集类中所有静态变量的赋值动作的静态代码块中的语句，并进行合并</li>
<li>虚拟机会保证一个类的<clinit>()方法在多线程环境中被正确的加锁，同步，如果多线程同时去初始化一个类，那么只有一个线程去执行这个类的<clinit>()方法，其他线程都需要阻塞等待，直到活动线程执行<clinit>()方法完毕</li>

</ol>
<h2>获取类结构信息</h2>
<pre><code class='language-java' lang='java'>package aaa.reflection.question;

import org.junit.jupiter.api.Test;

import java.lang.annotation.Annotation;
import java.lang.reflect.Constructor;
import java.lang.reflect.Field;
import java.lang.reflect.Method;

public class Class02 {
    public static void main(String[] args) throws Exception {

    }
    @Test
    //第一组api
    public void api_01() throws Exception {
        //得到class对象
        Class cls = Class.forName(&quot;aaa.reflection.question.People&quot;);
        //getName:得到全类名
        System.out.println(cls.getName());
        //getSimpleName:取得简单类名
        System.out.println(cls.getSimpleName());
//        getFields:获取public修饰的属性，包含本类和父类的
        Field[] fields = cls.getFields();
        for (Field field:fields) {
            System.out.println(field.getName());
        }
        //getDeclareFields:获取本类的所有属性
        Field[] declaredFields = cls.getDeclaredFields();
        for (Field field1:declaredFields) {
            System.out.println(field1.getName());
        }
        //getMethods:获取本类的所有方法，包含本类和父类的
        Method[] methods = cls.getMethods();
        for (Method method : methods) {
            System.out.println(method.getName());
        }
        //getDeclaredMethods:获取本类的所有方法
        Method[] declaredMethods = cls.getDeclaredMethods();
        for (Method declaredMethod : declaredMethods) {
            System.out.println(declaredMethod.getName());
        }
        //getConstructors:获取本类的所有所有public修饰的构造器，包含本类
        Constructor[] constructors = cls.getConstructors();
        for (Constructor constructor : constructors) {
            System.out.println(constructor.getName());
        }
        //getDeclaredConstructors:获取本类所有的构造器
        Constructor[] declaredConstructors = cls.getDeclaredConstructors();
        for (Constructor declaredConstructor : declaredConstructors) {
            System.out.println(declaredConstructor.getName());
        }
        //getPackage:以package的形式返回包信息
        System.out.println(cls.getPackage().getName());
        //getSuperClass:以Class形式返回父类
        System.out.println(cls.getSuperclass().getName());
        //getInterfaces:以Class[]的形式返回接口类型
        Class[] interfaces = cls.getInterfaces();
        for (Class anInterface : interfaces) {
            System.out.println(anInterface);
        }
        //getAnnotations:以Annotation[]形式返回注解信息
        Annotation[] annotations = cls.getAnnotations();
        for (Annotation annotation : annotations) {
            System.out.println(annotation);
        }
    }

}
class A{
    public int a;
    public void hi(){

    }
}
class People extends A{
    //属性
    public String name;
    protected int age;
    String job;
    private int sale;
    //方法
    private void m1(){

    }
    protected void m2(){

    }
    void m3(){

    }
    public void m4(){

    }
}

</code></pre>
<pre><code class='language-java' lang='java'>@Test
    //第二组api
    public void api_01() throws Exception {
        //得到class对象
        Class cls = Class.forName(&quot;aaa.reflection.question.People&quot;);
        Field[] declaredFields = cls.getDeclaredFields();
        //getModifiers:以int形式返回修饰符
        //默认修饰符为0，public为1，private为2，protected为4，static是8，final是16
        for (Field declaredField : declaredFields) {
            System.out.println(declaredField.getModifiers());
        }
        //getType:以Class形式返回类型
        for (Field declaredField : declaredFields) {
            System.out.println(declaredField.getType());
        }
        //getName:返回属性名
        for (Field declaredField : declaredFields) {
            System.out.println(declaredField.getName());
        }
    }
</code></pre>
<pre><code class='language-java' lang='java'>@Test
    //第三组api
    public void api_01() throws Exception {
        //得到class对象
        Class cls = Class.forName(&quot;aaa.reflection.question.People&quot;);
        Method[] declaredMethods = cls.getDeclaredMethods();
        //getModifiers:以int形式返回修饰符
        //默认修饰符为0，public为1，private为2，protected为4，static是8，final是16
        //getReturnType:以Class方式获取返回类型
        //getName:返回方法名
        //getParameterTypes:以Class[]返回参数类型数组
        for (Method declaredMethod : declaredMethods) {
            System.out.println(declaredMethod.getModifiers()+&quot; &quot;+declaredMethod.getReturnType()+&quot; &quot;
                    +declaredMethod.getName()+&quot; &quot;+declaredMethod.getParameterTypes());
        }
    }
</code></pre>
<pre><code class='language-java' lang='java'>   @Test
    //第四组api
    public void api_01() throws Exception {
        //得到class对象
        Class cls = Class.forName(&quot;aaa.reflection.question.People&quot;);
        Constructor[] declaredConstructors = cls.getDeclaredConstructors();
        //getModifiers:以int形式返回修饰符
        //默认修饰符为0，public为1，private为2，protected为4，static是8，final是16
        //getName:返回方法名
        //getParameterTypes:以Class[]返回参数类型数组
        for (Constructor constructor : declaredConstructors) {
            System.out.println(constructor.getModifiers()+&quot; &quot;
                    +constructor.getName()+&quot; &quot;+constructor.getParameterTypes());
        }
    }
</code></pre>
<h2>反射暴破</h2>
<h3>创建实例</h3>
<pre><code class='language-java' lang='java'>package aaa.reflection.question;

import org.junit.jupiter.api.Test;

import java.lang.reflect.Constructor;

public class Class02 {
    public static void main(String[] args) throws Exception {

    }
    @Test
    public void api_01() throws Exception {
        //得到class对象
        Class cls = Class.forName(&quot;aaa.reflection.question.People&quot;);
        //1.通过public的有参构造器
        Object a = cls.getConstructor(int.class, String.class, int.class).newInstance(10, &quot;a&quot;, 10);
        //2.通过public的无参构造器
        Object o = cls.getConstructor().newInstance();
        //3.通过非public的有参构造器
        Constructor declaredConstructor = cls.getDeclaredConstructor(String.class);
        //使用反射的暴破
        declaredConstructor.setAccessible(true);
        Object abc = declaredConstructor.newInstance(&quot;abc&quot;);
    }

}
class A{
    public int a;
    public void hi(){

    }
}
class People extends A{
    //属性
    public String name;
    protected int age;
    String job;
    private int sale;

    private People(String name) {
        this.name = name;
    }

    public People() {
    }

    public People(int age, String job, int sale) {
        this.age = age;
        this.job = job;
        this.sale = sale;
    }
}
</code></pre>
<h3>操作属性</h3>
<pre><code class='language-java' lang='java'>package aaa.reflection.question;

import org.junit.jupiter.api.Test;

import java.lang.reflect.Field;

public class Class02 {
    public static void main(String[] args) throws Exception {

    }
    @Test
    public void api_01() throws Exception {
        //得到class对象
        Class cls = Class.forName(&quot;aaa.reflection.question.People&quot;);
        //创建实例
        Object o = cls.getConstructor().newInstance();
        //使用反射得到name
        Field field = cls.getField(&quot;name&quot;);
        field.set(o,&quot;张三&quot;);
        //
        Field sale = cls.getDeclaredField(&quot;sale&quot;);
        //进行爆破可以设置private变量
        sale.setAccessible(true);
        sale.set(o,10000);
        //因为是static可以写为null
        sale.set(null,20000);
        System.out.println(o);
    }

}

class People {
    //属性
    public String name;
    protected int age;
    private static int sale;

    @Override
    public String toString() {
        return &quot;People{&quot; +
                &quot;name=&#39;&quot; + name + &#39;\&#39;&#39; +
                &quot;, age=&quot; + age +
                &quot;, sale=&quot; + sale +
                &#39;}&#39;;
    }

    public People() {
    }
}
</code></pre>
<h3>操作方法</h3>
<pre><code class='language-java' lang='java'>package aaa.reflection.question;

import org.junit.jupiter.api.Test;

import java.lang.reflect.Method;

public class Class02 {
    public static void main(String[] args) throws Exception {

    }

    @Test
    //第四组api
    public void api_01() throws Exception {
        //得到class对象
        Class cls = Class.forName(&quot;aaa.reflection.question.People&quot;);
        //创建实例
        Object o = cls.getConstructor().newInstance();
        //使用反射得到
        Method method = cls.getMethod(&quot;hi&quot;);
        method.invoke(o);
        //调用private static方法
        Method declaredMethod = cls.getDeclaredMethod(&quot;sum&quot;, int.class);
        declaredMethod.setAccessible(true);
        declaredMethod.invoke(o, 2);
        //因为是stastic可以使用null
        declaredMethod.invoke(null, 3);
        //如果有返回值统一用Object接受
    }
}
class People {
    //属性
    public String name;
    protected int age;
    private static int sale;

    public void hi(){
        System.out.println(&quot;hi&quot;);
    }
    private static void sum(int c){
        int a=5;
        int b=1;
        System.out.println(a+b+c);
    }

    public People() {
    }
}

</code></pre>
<p>&nbsp;</p>
