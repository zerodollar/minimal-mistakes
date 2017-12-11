---
title: "JAVA300集视频教程"
categories:
  - java
tags:
  - 初级
comments: true
---
北京尚学堂高淇出品，比较老，主要是Java6、7  
# 1.如何学习JAVA
学习习惯：内存结构／JDK源码
java：服务器／安卓
手把手，代码一行码出来
工具先了解常见功能，不常见的用到再说。80-20法则

# 2.JAVA三版本区别
JAVAEE Enterprise Edition 企业版，开发服务器端应用，非常广泛
JAVASE Standard Edition标准版，开发个人计算机上应用，较少
JAVAME Micro Edition 微型版，消费性电子产品，消亡中，被安卓取代，和安卓没有任何关系，安卓用JAVA写

# 3.JDK下载安装
JDK包含JRE，JRE包含JVM，JVM跨平台
配置PATH、JAVA_HOME， 不用再配置CLASS_PATH了，1.5后JVM自动找
# 4.HelloWorld
类名和文件名一致，首字母大写。javac编译生成class字节码文件，java执行
# 5.HelloWorld深化
大小写敏感，一个源文件可以有多个class，至多只能有一个public的类声明（与文件名一致），其它类的个数不限，每个类生成独立的字节码文件。
`//单行注释`，`/*多行注释*/`
UTF8编码乱码，可以转换为ANSI编码


# 6.各种字符集关系
标识符支持字母／_/$

- ISO8859-1  西欧字符集
- BIG5   台湾大五码，繁体汉字
- GB2312 最早的简体字符
- GBK    GB2312的扩展，可以表示繁体中文
- GB18030   最新的GBK扩展，所有非手持／嵌入设备强制实行标准，可以表示汉字／维吾尔／藏文等中华民族字符
- Unicode（UTF-8，UTF-16） 国际通用字符集

# 7.整形类型
byte/short/int/long/BigInteger/BigDecimal   0b二 0八  0x十六
float/double
char
boolean
Integer.toBinaryString(int)  
Integer.toOctalString(int)  
Integer.toHexString(int)  

# 8.浮点误差
浮点有误差，不能直接比较，精确可以用BigDecimal
# 9.char 字符串
char 类型用来表示在Unicode编码表中的字符，可以大于255
'a'／'中'／’\u0061’

# 10.类型提升问题
自动／强制转换，注意溢出

# 11.JDK7特性
整形支持下划线分隔
# 12.变量
变量是最基本存储单元：变量名／变量类型／作用域

- 实例变量／成员变量／属性
- 局部变量，初始化后才能用
- Final常量只能初始化一次

命名：变量／方法首字母小写驼峰，类名首字母大写驼峰，常量下划线分隔大写
# 13. 算术运算符
浮点数也可以取余%
instanceof 对象是否是特定类的一个实例
# 14.字符串连接
4+“5”
# 15.eclipse开发环境
开源、基于Java的可扩展开发平台
包视图／控制台／大纲视图outline
# 16.eclipse运行程序
设置断点，Debug as调试，通过Debug／Java视图切换
# 17.if
# 18.switch
case穿透
# 19.增强switch
支持String
# 20.while

# 21.for
# 22.练习
遇到问题，先想能干，再简化，补充调整
# 23.带标签的break／continue
goto保留字但无功能
# 24.方法
功能块，一个方法只完成1个功能。
基本类型传递的是该数据值本身。
引用类型传递的是对象的引用，而不是对象本身。
JAVA中只有值传递。
# 25.递归
递归结构包括两个部分：
    1.递归头。解答：什么时候不调用自身方法。如果没有头，将陷入死循环。
    2.递归体。解答：什么时候需要调用自身方法。
# 26.API文档 -- 相当于字典，用时查，不用背
包->接口／类 -> 具体说明
不要使用默认包。
com.pa和com.pa.pb是2个独立的包
java.lang／awt／net/io/util
package 解决类之间的重名问题

export -> Java -> Javadoc  文档代码统一
- @Author 作者  默认是计算机用户名
- @version 版本
- @param  参数
- @return  返回值的含义
- @throws 抛出异常描述
- @deprecated 废弃。建议用户不再使用该方法
# 27.键盘输入
Scanner
# 28.面向对象01 和面向过程的本质区别
- 类：
  - 完全抽象：接口
  - 抽象+实行：抽象类
  - 管理：package／import／JDK中包
  - 包含：属性／方法／构造方法／重载
- 对象：
  - 引用类型
  - this／static
  - 内存结构 
- 三大特征：
  - 封装：public／private／protected
  - 继承：Object/super/重写／组合
  - 多态 

# 29.面向对象的思维
面向过程的思维模式是简单的线性思维，思考问题首先陷入第一步做什么、第二步做什么的细节中。

面向对象的思维模式说白了就是分类思维模式。思考问题首先会解决问题需要哪些分类，然后对这些分类进行单独思考。最后，才对某个分类下的细节进行面向过程的思索。

老毛的分类。
# 30.类和对象的关系
以类的方式组织代码，以对象的组织(封装)数据。
对象是具体的事物。
类，是抽象的，是对对象的抽象。是抽出象的部分。
# 31/32.程序运行的内存分析
堆（new对象）、栈（局部变量）、方法区（也是堆，包括代码、static变量、常量池）
java中，除了基本数据类型之外的其他类型称之为引用类型。
java中的对象是通过引用来操作的。
属性的默认初始化：如果不对其初始化，Java使用默认的值对其初始化。
# 33.JVM内存管理
JAVA的内存管理实际上指的就是对象的管理，其中包括对象空间的分配和释放。

- 1.程序员无权调用垃圾回收器。
- 2.程序员可以通过System.gc()。通知GC运行，但是JAVA规范并不能保证立刻运行。
- 3.finalize方法，是JAVA提供给程序员用来释放对象或资源的方法，但是尽量少用。

# 34.构造方法
# 35.方法重载
类中可以定义有相同的名字，但参数不同的多个方法。调用匹配离得最近的类型。
# 36.Static
类的公用变量，属于类，被该类的所有实例共享，在类被载入时被显式初始化，该类的所有对象共享
# 37.this
普通方法中，this总是指向调用该方法的对象。
构造方法中，this总是指向正要初始化的对象。
# 38.继承
继承的本质在于抽象。继承是对某一批类的抽象。
# 39.方法的重写（override）
重写方法必须和被重写方法具有相同方法名称、参数列表和返回类型。
重写方法不能使用比被重写方法更严格的访问权限。
# 40.Object类
所有Java类的根基类，提供：

* toString方法，默认`getClass().getName() + "@" + Integer.toHexString(hashCode())`，可以重写
* equals方法，对象是否相等

# 41.继承
super是直接父类对象的引用。除了Object类之外其他所有类的构造方法第一句总是super(…)，编译器会默认添加。
# 42.组合
has-a关系：使用组合
# 43. final
- 修饰变量
    被final修饰的变量不可改变。即初始化一次后，就不能再次被赋值！即，变为常量！
- 修饰方法：
    被final修饰的方法不可以被子类重写！
- 修饰类：
    被final修饰的类不能被继承!

# 44.封装、隐藏
encapsulation 需要让用户知道的暴露出来，不需要让用户了解的全部隐藏起来。
白话：该露的露，该藏的藏
专业：高内聚，低耦合
低耦合便于调用者调用，高内聚便于修改内部代码，提高可维护性。可进行数据完整性检测，保证数据的有效性。
# 45.多态
polymorphism
编译时类型（模糊一点，一般是一个父类）由声明时的类型决定。
运行时类型（运行时，具体是哪个子类就是哪个子类）由实际对应的对象类型决定。
多态：如果编译时类型和运行时类型不一致，就会造成多态。
静态绑定：在编译期完成，可以提高代码执行速度。
动态绑定：通过对象调用的方法，采用动态绑定机制。除final类、方法，static方法外都是动态绑定，是慢的主要原因。
多态的存在要有3个必要条件：要有继承，要有方法重写，父类引用指向子类对象
子类的对象可以当作基类的对象来使用称作向上转型（upcasting），反之称为向下转型（downcasting）
# 46/47.多态内存分析
# 48.抽象类
# 49.接口
从接口的实现者角度看，接口定义了可以向外部提供的服务。
从接口的调用者角度看，接口定义了实现者能提供那些服务。

https://www.bwh1.net/pwreset.php
https://www.bwh1.net/pwreset.php?key=9bfebab34c204c2572912c9919f9d49e
# 50.回调的实现
CallBack   Hook函数  模板方法
调用注入的对象的方法（该方法支持多态）
# 51.内部类
组合
内部类提供了更好的封装。只能让外部类直接访问，不允许同一个包中的其他类直接访问。
内部类可以直接访问外部类的私有属性，内部类被当成其外部类的成员。 但外部类不能访问内部类的内部属性。

内部类在只为所在外部类提供服务的情况下优先使用。
类文件：外部类$内部类.class
- 非静态内部类
 OuterObject.new Inner()
 外部类名.this.变量名
- 静态内部类
 一个静态内部类对象存在，并不一定存在对应的外部类对象。
 new  OuterClass.Inner()
- 匿名内部类
 适合那种只需要使用一次的类.比如：键盘监听操作等
- 局部内部类
 定义在方法内部。 
# 52/53.数组
array是对象，元素类似对象的成员变量

- 默认初始化   int[] a = new int[4]
- 动态初始化   a[0] = 1
- 静态初始化   int[] a = {1,2,3,4}
# 54/55. String 分析 （JDK源码）
  循环 str+='c'  会导致创建很多临时对象
# 56/57/58. 可变字符序列对比、扩容
StringBuffer 线程安全，效率低
StringBuilder 线程不安全，效率高
通过return this实现方法链
# 59.数组_模拟ArrayList容器的底层实现
# 60/61/62.多维数组，矩阵运算,JDK的Array方法，增强的for循环
# 63.包装类
基本类型转换为对象，比如Byte、Boolean、Integer、Character。。。
# 64.auto-boxing/unboxing/缓存处理
auto-boxing  基本类型->对象
unboxing     对象->基本类型
缓存[-128,127]范围内数值缓存，按照简单类型处理 
```
Integer a=123;
Integer b=123;
System.out.println(a==b)  //输出的是true
```
# 65.时间Date相关类
java.util
Timezone
Date      特定的瞬间，精确到毫秒
Calendar  日期计算
  GregorianCalendar  公历
DateFormat
  SimpleDateFormat
# 66.DateFormat和SimpleDateFormat类 
G 公元前后
y年M月w年周W月周d月天D年天E周天F月周a上下午Hk24时hK12时m分s秒S毫秒zZ时区
SimpleDateFormat.format(Date) 转成String
# 67/68/69.时刻、日期计算Calendar 日历类，
注意一月为0、周日为1
可视化日历： 能，先做简单，后想办法解决问题
# 70/71.File类、递归
以pathname为路径创建File对象，File(File,String)
# 72/73/74.异常、异常处理
设计良好的程序应该在异常发生时提供处理这些错误的方法，使得程序不会因为异常的发生而终断或产生不可预见的结果。 
没有异常，逻辑代码和错误处理代码混在一起.

- Error类
描述了Java运行时系统内部错误和资源耗尽错误。这类错误是我们无法控制的。
- RuntimeException
一定是你的问题，可以不捕获，因为小心点这些异常是可以避免的。
- Checked Exception
不是RuntimeException，通常由外界因素造成的，为了预防这些异常产生时，造成程序的中断或得到不正确的结果，一定要去做异常的处理。

异常处理方法：

- try-catch    
执行顺序：执行try，catch ， 给返回值赋值； 执行finally；return
- 再把异常Throws出去。
- 手动抛出异常，throw子句
# 75/76.自定义异常
从Exception类或者它的子类派生一个子类即可 

- 1.要避免使用异常处理代替错误处理，这样会降低程序的清晰性，并且效率低下。 使用异常机制建议
- 2.处理异常不可以代替简单测试--- 只在异常情况下使用异常机制 
- 3.不要进行小粒度的异常处理---应该将整个任务包装在一个Try语句块中 
- 4.异常往往在高层处理
# 77.坐标
# 78/79.图片加载、实现动画
URL u = GameUtil.class.getClassLoader().getResource(path);  
BufferedImage img =ImageIO.read(u);
Graphics g.drawImage(img,x,y,null)

启动线程完成重画，坐标持续变化
# 80/81/82/83.移动，游戏项目
判断边界，修改方向，变化坐标
# 84/85/86/87.Star类,太阳系
# 88~97.飞机射击
键盘监听
```
class KeyMonitor extends KeyAdapter
addKeyListener(new KeyMonitor());
```
awt简单，需要使用双缓冲解决闪烁问题， 新版本swing默认支持双缓冲

# 98. 课程复习，对前面的知识的一个回顾
# 99/100. 容器
Collection
LinkedList、ArrayList 线程不安全，效率低
Vector 线程安全，效率低
# 101~104 非泛型的ArrayList/LinkedList实现
Q：transient关键字能实现什么？
A：当对象被序列化时（写入字节序列到目标文件）时，transient阻止实例中那些用此关键字声明的变量持久化；当对象被反序列化时（从源文件读取字节序列进行重构），这样的实例变量值不会被持久化和恢复。
# 105~107 非泛型的Map/HashMap/HashTable实现
HashTable线程安全、效率低  HashMap效率高
# 108  equals/hashcode分析
可以通过IDE辅助生成equals代码
equals相等，则hashcode必相等。 反之不一定。
# 109 List/Map源码分析
List在node时，根据index决定从first、last开始检索
# 110~111 Set/HashSet实现
# 112 JavaBean
JavaBean 实体类，存储数据：表/类、字段/私有属性、数据/测试类
只有属性和get、set方法
# 113 使用一个Map保存一条表记录
# 114~115 迭代器遍历List、Set、Map
# 116 自定义泛型、泛型类、泛型接口、泛型方法
类型转换错误运行时错误，需要instanceof检查类型是否对
泛型在编译时检查，安全（检查）、省心（自动转换）
T类型、KV键值、E元素、？不确定， 只能是引用类型(不能基本类型）
泛型类T不能使用静态属性、静态方法：运行时绑定，静态在编译时确定

泛型方法：  修饰 <T> 返回类型，只能访问对象信息、不能修改。
# 117 泛型擦除
```
class Father<T>
class child extends Father<String>
class child2<T,T1> extends Father<T>
class child3<T1> extends Father  父类泛型擦除 T是Object
class child4 extends Father      子、父类都擦除
```
不可以子类擦除、父类不擦除。
方法中T由父类定， 属性在父类中由父类定、子类中由子类定
编译器告警：指定T为Object。 擦除不会进行类型检查。
泛型没有多态，声明类型、方法使用<？ extends/super 父类>： 类型不定、使用时确定
没有泛型数组
# 117 jdkfa泛型
# 118 iterator
implements Iterator<T>
增强for使用java.lang.Iterable接口
# 119~121  HashMap存储
# 122~123 冒泡排序
print中计算pirnt("  "+(1+2)+" ")
# 124~126 Comparable接口   Comparator对象
public int compareTo(Object obj);
Comparator比较器独立于实体的比较接口（比如实体无法扩展/多比较方法）
public int compare(Object o1, Object o2)
新版java建议使用lamda表达式
jdk提供Collections类
```
public class NewsItem implements java.lang.Comparable<NewsItem>{
       @Override
       public int compareTo(NewsItem o) {...}
}
Collections.sort(news);

public class GoodsPriceComp implements java.util.Comparator<Goods>{
       @Override
       public int compare(Goods o1, Goods o2) {...}
}
Collections.sort(list,new GoodsPriceComp());
```
# 127 TreeSet/TreeMap
TreeSet：元素不可以重复，元素可以排序，添加数据时自动进行排序，更改不影响顺序，TreeSet存储数据尽量不要修改（重复、顺序不对）
空构造使用Comparable接口，否则构造传入Comparator对象(可以是匿名内部类）
可以将节点中成员修改成final

TreeMap的Key可以排序：使用Comparable接口或Comparator对象
# 128 Collections工具类常见方法
binarySearch、sort、reverse、shuffle洗牌、swap、
# 129 自定义堆栈
队列单向Queue,双向Deque： 异常/返回值， 增/删/取， 首/尾
# 130 Enumeration接口
1.5前使用，之后使用增强版Iterator
hasMoreElement、nextElement     
  
- Vector的elements
- StringTokenizer子类

# 131 Hashtable
- 主要：Hashtable线程安全，同步，效率低下    
       HashMap线程不安全，非同步，效率相对高。
- 父类：Hashtable 是Dictionary,HashMap是AbstractMap
- null:Hashtable键与值不能为null
        HashMap键最多一个null,值可以多个null.
HashTable子类Properties，读写资源配置文件（.property/.xml），键与值只能为字符串

不给src，只给字节码，在bin目录下
类相对路径   xxx.class.getResourceAsStream("/com/....") ""表示bin，类所在的根路径
Thread.currentThread().getContextClassLoader().getResourceAsStream("/com/....")
# 132 WeakHashMap、IdentityHashMap与EnumMap
引用的分类：（强，软，弱，虚）：

- Strong强：gc不回收，比如常量池对象
- Soft软：gc可能回收，内存不足时回收
- Weak弱：gc立即回收
- Phantom虚：跟踪回收状态，不单独使用，与引用队列联合使用

IdentityHashMap中key只比较地址
EnumMap中key是Enum类型

# 133 容器同步控制、只读控制
collections.synchronizedXXX()
c.emptyXxx()       和EMPTY_xxx配合，调用者不需要判空，类似OptionXxxx
c.singletonXxx()   只包含一个元素
c.unmodifiableXxx()  只读
# 134~135 google的Guava 只读、约束
Guava的collection   
函数编程
ImmutableList 只读链表
Collection2.filter用Predicate
Collection2.transform用Function，Function支持组合

Constraint约束：非空、长度验证
集合计算：Sets.intersection/difference/union
# 136~137 MultiSet,MultiMap,BiMap
Multiset 元素可以重复出现,count(E) 计数
实现有HashMultiset/TreeMultiset/LinkedHashMultiset/ConcurrentHashMultiset/ImmutableMultiset

Multimap  一个键映射到多个值
BiMap  键值都不能重复
Table  双键的MAP  Table<rowkey, colkey, val>
   rowKeySet()返回”行”的集合Set<R>

# 138  Apache Commons Collections   和guava非常类似
 
- 函数式编程 之 Predicate 断言
 封装条件或判别式  if..else替代
  1、 new EqualPredicate<类型>(值) 
     EqualPredicate.equalPredicate(值);
  2、NotNullPredicate.INSTANCE 
  3、UniquePredicate.uniquePredicate()
  4、自定义
     new Predicate() +evaluate  
    PredicateUtils.allPredicate  andPredicate anyPredicate
    PredicatedXxx.predicatedXxx(容器,判断)

- 解耦，业务处理与判断进行分类
 函数式编程 Transformer 类型转化
 1、new Transformer() +transform
 2、SwitchTransformer   类似switch/Predicate/Transformer
 CollectionUtils.collect(容器,转换器)

# 139 闭包
封装特定的业务功能

-  1、Closure<T> 实现接口 execute(T)修改T对象, collections.forAllOn(容器，闭包）
- 2、IfClosure  IfClosure.ifClosure(断言,功能1,功能2)
- 3、WhileClosure WhileClosure.whileClosure(断言,功能,标识) 
- 4、ChainedClosure.chainedClosure(功能列表);
CollectionUtils.forAllDo(容器,功能类对象);
# 140 交集，并集，差集

- 1、并集 CollectionUtils.union();
- 2、交集 CollectionUtils.intersection();
  CollectionUtils.retainAll();
- 3、差集
   CollectionUtils.subtract();
   
- 1、循环队列:CircularFifoQueue
- 2、只读队列:不可改变队列  UnmodifiableQueue
- 3、断言队列:PredicatedQueue.predicatedQueue()

# 141 对迭代器的扩展
1、MapIterator 以后不再使用map.keySet.iterator访问
  IterableMap  HashedMap
 2、UniqueFilterIterator 去重迭代器 
 3、FilterIterator 自定义过滤 +Predicate
 4、LoopingIterator 循环迭代器
 5、ArrayListIterator 数组迭代器

双向Map 要求键与值都不能重复
 BidiMap  inverseBidiMap()
 1、DualTreeBidiMap :有序
 2、DualHashBidiMap :无序

Bag 包 允许重复， 支持getcount
 1、HashBag 无序
 2、TreeBag 有序
# 142 集合 
- 1，一张图                                                  
Collection->Set/List -> HashSet/LinkedList/ArrayList
Map->HashMap
- 3，三个知识点：
  - 1）迭代器
            1）Itarator接口
                boolean hasNext();
                   next();
                boolean remove();
            2)foreach:java.lang.Iterable+iterator();
  - 2）比较器:
            1)实体类可以排序java.lang.Comparable+compareTo
            2)排序比较器（解耦，多种排序规则）Comparator+compare
                list+Collection.sort();
                TreeSet
                TreeMap
  - 3）泛型：<>
            泛型类，泛型方法，泛型接口，泛型的擦除，通配符？extends,super,泛型的嵌套
- 6.六个接口
       Collection ,Set, List,Map,Iterator,Comparable     - 9,九常用类：增删查+遍历
  - 1）ArrayList
  - 2)LinkedList
  - 3)HashSet
  - 4)TreeMap
  - 5)hashMap
  - 6)Properties
  - 7)Hashtable
  - 8)Stack:栈
  - 9）Collections:工具类。

# 143~145 IO入门之File类
pathSeparator、separator
getName() 文件名、路径名
getPath()路径名
getAbsoluteFile() 绝对路径所对应的File对象
getAbsolutePath() 绝对路径名
getParent() 父目录 ,相对路径的父目录，可能为null 如. 删除本身后的结果
2、判断信息
exists()
canWrite()
canRead()
isFile()
isDirectory()
isAbsolute()：消除平台差异，ie以盘符开头，其他以/开头
3、长度 字节数  不能读取文件夹的长度
length()
4、创建、删除
createNewFile() 不存在创建新文件,存在返回false
delete() 删除文件
static createTempFile(前缀3个字节长，后缀默认.temp) 默认临时空间
staticcreateTempFile(前缀3个字节长，后缀默认.temp,目录)
deleteOnExit() 退出虚拟机删除,常用于删除临时文件
5、操作目录
mkdir() 创建目录，必须确保 父目录存在，如果不存在，创建失败
mkdirs() 创建目录，如果父目录链不存在一同创建
list() 文件|目录 名字符串形式
listFiles()
static listRoots() 根路径

# 146  IO流
二进制 字节流：InputStream、OutputStream  一切文件
文本 字符流：Reader、Writer             纯文本
节点流：包裹源头，
处理流：增强功能、提高性能
# 147 文件读写追加
1、建立联系   File对象
       2、选择流     文件输入流  InputStream FileInputStream
       3、操作  : byte[] car =new byte[1024];  +read+读取大小
              输出
       4、释放资源 :关闭

# 148 文件拷贝
- 1、建立联系   File对象   源头 目的地
- 2、选择流       
文件输入流  InputStream FileInputStream
文件输出流  OutputStream FileOutputStream
- 3、操作  :  拷贝   

```
byte[] flush =new byte[1024];     
int len =0;
while(-1!=(len=输入流.read(flush))){  
  输出流.write(flush,0,len)
}
输出流.flush
```

- 4、释放资源 :关闭 两个流

# 149~150 文件夹拷贝、工具， 健壮性
1、文件 赋值  copyFile
2、文件 创建 mkdirs()
3、递归查找子孙级
# 151 字符流,只能处理纯文本
FileReader
FileWriter(File, 追加模式)
# 152~154 处理流
- 缓冲流：
  - 字节缓冲流    
  BufferedInputStream
  BufferedOutputStream
  - 字符缓冲流    
  BufferedReader.readLine
  BufferedWriter.newLine
- 转换流:
  - 字节流转为字符流:  处理乱码(编码集、解码集)    
  编码：字符->二进制  解码：二进制->字符
  乱码：编解码字符集不一致，  长度丢失、字节缺少， 
InputStreamReader(字节输入流,"解码集")
OutputStreamWriter(字符输出流,"编码集")

#155 流总结
步骤： 创建源 选择流 操作(读取|写出)释放
节点流:离数据源|程序最近的流
处理流:装饰模式 提高性能增强功能

- 1、 字节流:可以处理一切(纯文本、音频、视频等)
  - 1)、输入流
InputStream  FileInputStream ByteArrayInputStream
操作:read(字节数组)
    
     - a)、中间容器 byte[] flush=new byte[长度]
     - b)、接收长度 int len =0;
     - c)、循环读取while(-1!=(len=流.read(flush))){}
     - d)、操作:输出、拷贝

  - 2)、输出流   
OutputStream FileOutputStream ByteArrayOutputStream
操作:write(字节数组,0,长度)  输出

- 2、 字符流:只能处理纯文本 1)、输入流:Reader FileReader 操作:read(字符数组)
a)、中间容器 char[] flush=new char[长度] b)、接收长度 int len =0; c)、循环读取while(-1!=(len=流.read(flush))){} d)、操作:输出、拷贝 2）、输出流:Writer FileWriter
操作:write(字符数组,0,长度)  输出
1、 转换流:解码与编码字符集问题
1)、输入流:InputStreamReader 解码
2)、输出流:OutputStreamWriter—>编码

2、缓冲流:提高性能    1)、输入流:BufferedInputStream BufferedReader    2)、输出流:BufferedOutputStream BufferedWriter

- 3、处理数据+类型 1)、基本+字符串：必须存在才能读取 读取与写出顺序一致
a)、输入流:DataInputStream readXxx
b)、输出流:DataOutputStream writeXxx 2）、引用类型:Serializable transient    a)、反序列化:ObjectInputStream readObject    b)、序列化:ObjectOutputStream writeObject

- 4、打印流: PrintStream 
- 5、System.in out err  setIn setOut 以下流使用新增方法不能发生多态 1、ByteArrayOutputStream:  toByteArray() 2、BufferedReader: readLine() 3、BufferedWriter:newLine() 4、DataInputStream DataOutputStream 5、ObjectInputStream ObjectOutputStream 6、PrintStream 

#159 对象处理流
- 1、基本类型+String  保留数据+类型    
  输入流:DataInputStream    readXxx
  输出流:DataOutputStream  writeXxx
- 2、引用类型 (对象) 保留数据+类型    
反序列化 输入流:ObjectInputStream  readObject() 
序列化  输出流:ObjectOutputStream  writeObject()
注意:
1)、先序列化后反序列化；反序列化顺序必须与序列化一致
2)、不是所有的对象都可以序列化， java.io.Serializable
不是所有的属性都需要序列化，transient

# 160 关闭
1.7以后版本支持：   try(自动关闭的资源){}
# 161 打印流
PrintStream  system.in
Scanner  system.out/err
System.setOut(PrintStream)
FileDescriptor.in/out/err
# 162 IO流模式： 装饰
- 依赖：形参，局部变量
- 关联：属性，构造注入
   - 聚合：属性 整体与部分 不一致的生命周期 人与手
   - 组合: 属性 整体与部分 一致的生命周期 人与大脑
- 继承：父子类
- 实现：接口、实现类
# 163 超长文件夹
- 不要把父目录拷贝到子目录当中
dst.getAbsolute().contains()
- robocopy 删除超长目录
# 164~167 RandomAccessFile 文件分割、合并
多个流加入vector，作为SequenceInputStream的构造，多个流合并
# 168 IO总结
# 169~173 多线程
main主线程，gc线程，异常线程
调用start方法，不是run方法（阻塞、串行）

静态代理 设计模式
 - 1、真实角色
 - 2、代理角色： 持有真实角色的引用（构造注入）
 - 3、二者 实现相同的接口
 
一、继承Thread + run() 启动:创建子类对象+对象.start() 二、实现Runnable +run() 启动:使用静态代理   1、创建真实角色   2、创建代理角色Thread(真实角色引用）x   3、代理角色.start() 推荐使用接口: 1、避免单继承局限性 2、便于共享资源，一个真实角色传递给多个thread
三、实现Callable<T>接口
有返回值、可以抛出异常,但使用代码麻烦
ExecutorService  ser=Executors.newFixedThreadPool(xx);
Future<T> result1 =ser.submit(Callable<T> a) ;
a.setFlag(false);
result1.get();
ser.shutdownNow();
# 174~177 线程状态
创建、就绪、阻塞、运行、终止 
不可以stop（废弃),通过flag通知
join :合并线程，等待对应线程的终止
yield:暂停自己的线程 静态方法
sleep:休眠，不释放锁， 与时间相关、模拟延时
isAlive/setName/getName/setPriority概率、没有先后顺序
# 178~181 同步与锁
同步、并发：多个线程访问同一个资源
加锁  synchronized方法
synchronized块(引用类型|this|类.class){...}  注意锁定范围、锁定资源
同步:并发 多个线程访问同一份资源 确保资源安全 -->线程安全

死锁:过多的同步容易造成死锁
   相同顺序锁定
   生产者、消费者模式， 信号灯法：  wait会释放锁
   
# 182~183 任务调度
Time定时器类
TimeTask定时任务类
JUC  QUARTZ
# 184~194 网络编程、聊天室
- InetAddress 地址、DNS   
getHostAddress/getHostName
- InetSocketAddress 包含端口
getAddress/getHostName/getPort
- URL
绝对路径、相对路径  getProtocol/getHost/getFile/getPath/getQuery/openStream
- TCP
服务端ServerSocket  客户端Socket   getOutputStream/getInputStream
- UDP
都用DatagramSocket，服务端、客户端的DatagramPacket不同
# 195~207 HTTP server
   httpwatch  firebug
   StringTokenizer
   java.net.URLDecoder
   反射：Obj.getClass/类.class/Class.forName("完整类名")
   XML：DOM/SAX/DOM4J/JDOM
   getResourceAsStream
   
   
# 208~210 注解，反射读取注解
JDK5引入，对程序做解释，被其他程序读取
package/class/method/field 上添加

# 211~214 反射
动态语言： 程序运行时，可以改变程序结构或变量类型
运行时动态加载、探知、编译器未知的类
getFields 获取public，  getDeclareFields获取所有的
可以访问私有变量、方法， setAccessable
支持获取泛型的具体类型   

# 215 javaScript脚本引擎
# 216~217 javassist 字节码操作
反射：性能低于字节码操作
字节码操作：动态生成类、改变类（增删改属性、方法）
- BCEL
- ASM  需要JVM指令
- CGLIB 基于ASM
- javassist：支持bytecode、source级别

XJAD反编译
导入外部jar包
增加方法、修改方法，在反射中调用增加的方法
这样可以实现 AOP、动态代理
#219 JVM核心机制
类加载过程
- 加载：class字节码到内存，静态数据转换成方法区运行时数据结构，堆中生成Class对象，作为方法区类数据的访问入口
- 链接：类的二进制代码合并到JVM的运行态
  - 验证：确保符合规范、没有安全问题
  - 准备：为类变量（static）分配内存、设置类变量初始值，方法区中分配
  - 解析：VM常量池内的符号引用替换为直接引用（包括类名、方法名、变量名、常量值）
- 初始化：
  - 执行类构造器clinit：类变量自动赋值、静态语句块
  - 初始化化父类
  - clinit多线程安全

栈:   函数栈
堆：  java.lang.Class对象， 具体类对象
方法区（堆）：类运行时数据，静态变量、静态方法、常量池（类名、常量）、类代码

父类静态块、子类静态块、main、父类构造、子类构造
被动引用不会初始化：比如final常量，数组定义类引用，仅使用声明静态域的类

# 220~222 类加载器
- 引导类加载器（bootstrap class loader);
  java.lang.ClassLoader:加载类，加载资源（比如图片、配置文件）
- 扩展类加载器(extensions class loader);
  sun.misc.Launcher$ExtClassLoader
- 应用类加载器(application class loader);
  sun.misc.Launcher$AppClassLoader
- 自定义类加载器(从java.lang.ClassLoader);
  同类+同加载器  就是同一个类

依次组合， 
双亲委托： 先父类加载、再自己加载， 最终导致都是从引导类开始。 安全机制：防止自定义类和语言内置的类冲突。
#223 线程上下文类加载器
线程上下文类加载器： 
   - 一个类及其关联类应该由同一个加载器加载
   - 接口（ext）、实现（app）不同厂商提供，
   - 可选的加载器：应用、当前、当前线程类加载器
Tomcat类加载：app独立，为了安全， 先子类、再父类
OSGI：Open Service Gateway Initative 面向java的动态模块系统，比如Eclipse，每个模块有一个自己的类加载器，使用其他模块由对应模块导出
	Equinox 一个OSGI实现

# 224~225 内部类
Swing:AWT的基础上构建的一套新的图形界面系统
SWT:Standard WidgetToolkit,IBM构建的一个新的GUI库,解决AWT和swingw问题
AWT:Abstract Window Toolkit（抽象窗口工具包）,Sun不推荐使用的工具集	

- 静态内部类：包含静态、非静态成员，不能调用外部类普通成员、方法
- 成员内部类：使用外部类所有成员，仅供外部类使用。先创建外部类对象、再通过之创建内部类对象。不能有静态成员
- 方法/局部内部类：不能有静态成员， 不可以引用方法中的非final变量（栈、堆对象生命周期不一致）
- 匿名内部类：
new InterfaceOrClass(){...};
使用方式： 继承式，接口式、参数式

# 226~228 单例模式
保证一个类只能产生一个对象

- 饿汉式（线程安全，调用效率高，但是不能延迟加载）
  private static CC obj= new CC(); 
- 懒汉式（线程安全，调用效率不高，但是可以延迟加载） 
  public static  synchronized CC getInstance
- 双重检测锁式（JVM内部原因[优化、模型]，偶尔出错，不建议用）
- 静态内部类（线程安全，调用效率高，可以延时加载）
  private static class CCInstance {
       private static final CC obj = new CC();
  }
- 枚举单例（枚举天然单例，线程安全，效率高，无延迟加载，无反射、序列化漏洞）
public enum CC{
  INSTANCE;
  public void operation(){...}
}

常见场景：    

- windows任务管理器
- 回收站
- 读取配置文件的类
- 计数器
- 日志应用
- Servlet
- SpringMVC的控制器对象

破解单例（不包含枚举）

- 反射
 私有构造中判断obj不为null时，抛出异常
- 反序列化
 private Object  readResolve(){return instance;}
 
 多线程测试辅助类 CountDownLatch
 UML插件：
 http://download.eclipse.org/release/helios
 AmaterasUML
 http://marketplace.eclipse.org/search/site/uml?page=1
 http://www.umlet.com/umlet_14_2/com.umlet.plugin-14.2.zip
 
# 229~231 工厂模式
oop设计原则
ocp:对源码关闭，对扩展开发原则
dip:依赖翻转原则
迪米特法则：

简单工厂：单个工厂，违反开闭原则， 都是静态方法，又叫静态工厂方法
工厂方法：工厂接口，多个具体工厂
抽象工厂：多个具体工厂， 每个工厂生产产品族--多个产品接口

#232 建造者模式
Builder：子组件单独构造
Director：装配子组件成复杂的对象

#233~234 原型模式、克隆、拷贝
当使用New关键字实例化对象的时候，很复杂，可以考虑原型模式来实现！
再则就是New对象比较耗时,克隆（clone）比较节省时间！
 implements Cloneable   --》 Object.clone()浅克隆
 也可以使用序列化、反序列化实现。
 
# 235 适配器模式
Target 目标接口
Adaptee 需要（被）适配的类，
Adapter  适配器，通过继承或组合Adaptee实现Target接口

# 236~238 代理模式
安全、远程、延迟加载
静态代理
动态代理 dynamic proxy，代理类不需要写、由工具自动生成
  - JDK自带
  java.lang.reflect.Proxy/InvocationHandler
  可以在handler的invoke中集中控制
  - javaassist字节码操作
  - CGLIB
  - ASM（底层指令，可维护性差）

  拦截器、连接池关闭处理、AOP（日志、声明式事务处理）、AspectJ

#239 组合模式
树形结构表示部分、整体关系
GUI的组件、xml解析、Junit单元测试框架

# 240 装饰模式Decorator、包装器Wrapper、桥接模式
动态的为一个对象增加新的功能， 继承会导致类数量膨胀
IO流、Swing图形界面、request&response
桥接模式解决多继承问题：对象自身沿多个维度变化
# 241 门面模式、外观模式
核心：为了系统提供统一的入口，封装子系统的复杂性，便于客户端调用
# 242 FlyWeight 享元模式
共享的方式高效地支持大量细粒度对象的重用，比如围棋子
内部状态：可以共享，不会随环境变化而变化
外部状态：不可以共享，会随着环境变化而改变
线程池、DB连接池

# 243 责任链模式 chain of responsibility
同一类请求的对象连成一条链，所提交的请求将沿着链传递，链上的对象逐个判断是否有能力处理该请求，如果能则处理，如果不能则传递给链上的下一个对象。

异常机制、servlet过滤器链式处理、struct2拦截器调用
# 244 迭代器模式
提供一种遍历聚合对象的方式，又称游标、cursor
# 245 中介者模式（Mediator
中介、协调作用： 比如中台，网状->星型
# 246 命令模式（command）  使用概率低
将一个请求封装为一个对象，从而使我们可用不同的请求对客户进行参数化；对请求进行处理（排队、记录请求日志、撤销），也称之为：动作Action模式，事务transaction模式。
事务机制、action调用、命令撤销与恢复
# 247 解释器模式Interpreter  访问者模式 Visitor 使用概率极其低
开发一种新语言用： EL、正则表达式、SQL、数学表达式
尽量不用，可以考虑使用Groovy/js引擎

存储在一个集合中的对象，类型不同，可以使用访问者对象来访问。
XML解析、编译器设计、复杂集合对象处理
# 248 策略模式 strategy
算法剥离，通过配置等方法注入
# 249 模板方法模式（template method）
固定流程，子类覆盖特定步骤
# 250 状态模式（State）
用于解决系统中复杂对象状态转换以及不同状态下行为的封装问题
一个ConcreteState封装一个状态对应的行为
Context完成状态切换
# 251~252 观察者模式（Observer）
广播机制：用于1:N的通知, 通知方式：推、拉
多个订阅者、客户称为观察者Observer，订阅内容称为目标Object
java.util.Observable/Observer
# 253 备忘录模式（memento）  纪念章
保存某个对象内部状态的拷贝，这样以后就可以将该对象恢复到原先的状态。
源发器类Originator
备忘录类Memento
负责人类CareTake
将备忘录压栈，将多个备忘录对象，序列化和持久化。

# 254~262 正则表达式
RegexBuddy
.不包含换行，[\s\S]包含换行  \b单词边界  多行定位\A\Z   \1反向引用
（?:非捕获组表达式）  (?=后面匹配)  (?<=前面匹配)  (?!后面不匹配) (?<!前面不匹配)
默认贪婪模式，?表示非贪婪模式
Pattern.compile(r,int).matcher(string)/find()/group(int)/replaceAll()/split
#263~276 JDBC
Mysql的客户端软件Navicat

Driver/DriverManager/Connection
Statement/PrepareStatement/CallableStatement
ResultSet
- CLOB/BLOB/时间
  - java.sql.Date/Time/Timestamp
- 批处理
- 事务处理  ：原子、一致、隔离、持久
  -读取未提交（Read Uncommitted）
  -读取已提交（Read Committed）默认
  -可重复读（Repeatable Read）
  -序列化（Serializable）
properties存储JDBC连接信息
# 277~300 ORM简单框架设计
一条记录封装到数组、Map、JavaBean
Hibernate、myBatis的简化版
联合表查询结果使用xxxVO的bean来对应。
空构造便于给反射newInstance使用
模板方法+回调接口+匿名内部类
工厂+克隆
export  JAR file  导出jar包
export  Javadoc   导出API文档


