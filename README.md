# Search method<br>
Java stars>1000 pushed>2021 language:Java<br>
- 在线编辑 https://www.zhihu.com/question/389505292/answer/2472686098?utm_psn=1709268661565505536  
# Java路线 
- https://www.bilibili.com/video/BV1mM411x7Z6/?spm_id_from=333.999.0.0&vd_source=b94ed34e56dd4e10593fb925ded770a2
- Javase 杜
- Mysql 黑马 第一遍基础
- JDBC 链接Java Mysql 杜  
- web前端 后端程序员看懂前端 杜 HTMl CSS JavaScript 
- Javaweb 杜
- SSM 黑马 Spring 轻量级容器 和项目结合
- Springboot 黑马 （结合黑马外卖项目）
- JVM 黑马 Java跑在虚拟机上 结合周知名 java虚拟机
- java并发编程 黑马 **
- Springcloud 黑马
- Redis 黑马（结合缓存项目）
# JavaSE-java EE
### 标识符-运算符 p55
### p135
### P148
class 类{
静态代码块;
实例代码块

静态变量;
实例变量;

构造方法;

静态方法；
实例方法；

this
}
### p151
- this
### p159

## java 基础
- program files(X86) 32位系统
-  注释 只在源文件不会被编译到字节码  
  单行 //  
  多行 /*  
*/  
  javadoc注释 /**  
               *  
                  */ 通过bin下 javadoc.exe生成帮助文档 鼠标停留有信息
- **根目录***在文件系统建立时即已被创建，其目的就是存储子目录
### DOS命令
dir  
cd Desktop （change direcroty）  
cd.. 上级目录  
cd. 当前目录  
cd \ 跟目录  
cls  
java -version / javac -version  //java和javac命令版本
exit  
del *class
### java特性
- 垃圾回收机制（GC） 没有引用指向对象
- 可移植性（跨平台） 一次编译 到处运行（从windows到linux）  java代码运行在JVM（java虚拟机），而不和操作系统追鹅交互
### java加载和运行
-  .java(源文件，在硬盘)-.class(编译通过则使用javac编译为字节码，检查是否符合java语法，非纯二进制不然操作系统能处理而不用JVM) .class 可拷贝到其他操作系统执行   //javac Hw.java
-  编译只检查语法不运算 byte b = i（int 10 / 3 (错) 
-  java.exe 运行 // A.class - java A  // JVM 类加载器(ClassLoader)-操作系统-硬件平台 \操作系统执行二进制和底层硬件平台交互
#### javac启动编译器，java启动JVM
-  JRE(包括JVM)  java runtime envoronment 运行环境
-  JDK(自带JRE)给开发 JRE给客户（内存小）
-  JDK > JRE >JVM
### JDK目录  
- java/bin 存放命令 包括javac java.exe

## java环境搭建
- 不配置环境 javac只能在bin目录下使用，不是内部或外部命令，不能在计算机任何位置直接使用
- windows/System32/ipconfig.exe 在administrator下可使用
- windows操作系统会从当前目录再从环境变量path下搜索
- 在环境变量path指定的路径中设置（我的电脑-属性-高级）**path环境变量属于操作系统**
- path中增加一个javac所在目录（java/bin），封号相隔
- javac可以采用绝对路径（admin下cmd+绝对路径）也可采用相对路径（java文件目录下cmd+java文件名）
- java + 文件名（HelloWorld）
- 配置classpath 帮助类加载器找到HelloWorld字节码文件 **classpath环境变量属于java语言中的环境变量**
- classpath=.; classpath不用配置，默认从当前目录查找


~~~java
public class HelloWorld{//类体中不直接写java 除声明变量外
  public static void main(String[] args){
 
  //public 公开的，在任何位置都可以方位
  //static 静态的，类名.访问
  //main 方法名 表示定义一个公开的静态的主方法(程序入口) main方法也可以重载
  //string[]是一种引用数据类型 args是局部变量，可以随意命名

  System.out.println("Hello World!");//方法体
  }
  //public class 和class区别 
  //公开的类名必须和文件名一致 一个文件一个公开类
  //一个java源文件可以有多个class 并可以没有public class 每一个class都可以有main方法
}

class A{
  public static void main(String[] args){
    System.out.println("run this main");//println换行 print不换
  } 
}
~~~

## 标识符
- 可以自己命名 数字字母_$,不以数字开头  
- 类名、方法（main）、常量、接口
- 命名规范：类名 接口名  首大写 后单词大写
- 变量名 方法名 首小写 后单词大写
- 常量名 全部大写
## 关键字 
SUN提前设置 全小写
## 字面值(数据)
字符串型字面值 "" 字符型'' 整数 浮点 布尔
## 变量
- 变量是内存中一块空间，包含数据类型 变量名 字面值 （类型 字面值一致）
- int housePrice,a,b；变量并未初始化也并未开辟空间，此时无法访问
- java中变量必须先声明再赋值才能访问
### 变量的定义，声明，初始化
- https://worktile.com/kb/ask/37730.html
- https://www.cnblogs.com/bigbigbird/p/11382561.html
- https://www.zhihu.com/question/27639400/answer/489853106
- 获取(get) println System.out.println()
- 修改(set) housePrice = 1；//运算右边赋值左边   int housePrice = 1；
- 作用域 变量的有效范围 同作用域只能有一个变量  
  局部变量 方法体中声明  
  成员变量 方法体外**类体**内声明 **就近原则** **有默认值**(0) char-\u0000(\u0020是空格)
## 数据类型 
- 指导程序运行阶段分配多少空间
### 基本数据类型(Primitive Data Types)
- 整数型(byte,short,int,long) 浮点型(float,double) 布尔型(boolean) 字符型(cahr)  12484812byte(字节)
- 取值范围
- 以补码存储
- 正数补码相同 负数将正数取反+1
- int 2147483647
- 补码 1000000
- 减一 01111111
- 反码 10000000 —— -128
- 【-128 ～ 127】
- https://zhuanlan.zhihu.com/p/673611096

  
### 引用数据类型(Reference Data Types)
- 类 接口 数组(字符串)
- 1byte(字节) = 8 bit(字节位) 1KB = 8byte 第一位表正负
#### ASCII码
- 让计算机显示现实中的文字 单字节
- 字符码 用二进制表示文字（解码）  文字表二进制 (编码)  
  'a' --> 97 按照ASCII 解码 [0110 0001]  
  'A' --> 65  
  '0' --> 48
  大小写字符差32
- 简中编码 GB2312 < GBK < GB18030
- 统一所有 unicode utf-8（.） utf-16 utf-32 java标识符可以用中文 public class 学生{}
- char K = '我' 双字节可存储中文 '\u4e2d' - 中

#### 字符型字面值
- 单字符  
  字符数据类型的范围为0到65535(2^16-1) (FFFF/ffff)
  char c = 'A';  
  char c = '\101';  //八进制
  char c = '\u0041';  //ASCII字符占据Unicode字符集中前127个值
  char c = 0x41; //十六进制，等海于0x0041  
  char c = 65;
- char-int 类型转换
- char c = '\u0041';  
  int f = c;  
  结果 f=65
  
- 字符转义序列  
  char c2 = '\n' 换行符  '\t'制表符  '\r'回车  '\\'反斜杠  '\f'换页  '\b'退格  
  char k ='\'(\将‘转义为普通‘,错)  char k = ''Hello''(前两个单引号配对，错)  
  jdk native2ascii.exe  \转义u-unicode

### 整数型 byte short int long
- int a = 10; 10默认int
- 三种表示方式  
int a = 10 / 3; 整数/整数=整数  
int b = 010; //8进制  
int c = 0x10; //16进制
#### 自动类型转换
- 小容量-大容量 **隐式**
- byte b = 3;  
  int x = b;
- 整数型之间转换
- 整数型-浮点型

#### 强制类型转换
- 大容量-小容量 强制类型转换符 强制删去左侧二进制位
- 数字前加上**括号**，括号中写上要转换的类型  
  Long x = 100;  
  int y = (int)x;
- 数字的后面直接加上要转换的类型的第一个**字母**  
  long z = 2147483648L //**整数型字面值默认为int类型处理** 添加L作为long
- byte b = 50； byte不超过127可以不用强制类型转换符  包括short char
- 浮点型 float double 存储近似值 
- 引用数据类型 java.math.BigDecimal  
  Java SE 类库 jre\lib\rt.jar  类的字节码文件 //JavaSE自带的类 String System  
  类库源码 src.zip
- double d = 3.0; **浮点型默认double**
- float f = 3.0f;   float f = (float)3.0;
  
#### 布尔型 boolean
- 只有 true false 两个值 底层用01存储
- boolean login = true;

#### 总结
- 除bool数据类型都能互相转换 char c = 97;
- 任意浮点型都比整数型容量大
- 多种数据类型混合运算 先转换成容量最大的类型再运算
- byte chort char 类型会参与运算时，结果会自动转化为int类型
  
## 运算符
### 算数运算符
- + - * / %(取余) ++(自加一) --
- 优先级 加()
- ++x/x++ 单目运算符
- int b = a ++ 先赋值 再a+1
- int b = ++ a 先➕1再赋值
- system.out.println(s--);  x=s-- 打印s再s=s-1
  
### 关系运算符 
- < <= == != （=是赋值运算符）
- 运算结果bool型
- == 对于基本类型来说是值比较，对于引用类型来说是比较的是引用；而**equals**默认情况下是引用比较，只是很多类重新了equals 方法，比如String、Integer 等把它变成了值比较
  
### 逻辑(bool)运算符
- & | !(单目 !false) ^(异或 两边算子不一样就是真) &&(短路与 和与结果相同但存在短路现象) ||(短路或)
- 两边算子bool，最终结果bool
- system.oyt.println((5 > 3) | (5 > 6)); //true
- int x = 10;  
  int Y = 8;  
  system.out.println( x < Y && ++x < Y); //短路与 第一个出现false则第二个表达式不执行  
- 两边算子都要执行要用逻辑与
  system.out.println(X); // 10

### 赋值运算符
- 基本赋值运算符 =
- 扩展运算符 不改变运算结果类型
- +=(累进)  /=  %=(取余)
- byte x =10;
- x += 5;  //等同于x = (byte)(x+5) 不等于x = x + 5(int 赋值到 byte 不通过)
  
### 字符串连接运算符 +
- +两边是数字 加法运算
- +两边有一个字符串 字符串连接 返回字符串结果
- system.out.println(a "+"+b+"="+(a+b));

### 三元(条件)运算符
- char c = bool表达式 ? 表达式1 : 表达式2； c的类型和表达式类型一致
- boolen sex = false;
- char c = sex ? '男' : '女'；

## 控制语句
### 选择结构
#### if
- if、if else
- if(bool表达式){  
  };
- if(bool表达式){  
  }else{  
  };
- if(bool表达式){  
  }else if(){  
  }else if(){  
  }else(){  
  };
~~~java
public class IfTest01
{
  public static void main(Stringp[]) args{
    double distance = 1.0;//单位KM
    if( distance < 5){
      System.println("去KFC");     
    }
  }
}
~~~
~~~java
public class Keyinputtest
{
  public static void main(String[] args){

  //第一步 创建键盘扫描器对象s
    java.util.Scanner s = new java.util.Scanner(System.in);

  //给出提示
    system.out.print("请输入你的年龄：");

  //第二步 调用Scanner对象的next方法开始接收用户的键盘输入
  //当程序执行到这里时会停下，等待用户输入
  //用户敲下回车键，输入的信息赋值给userInputContent
    String userInputContent = s.next();//以字符串的形式接受
  
    int age = s.nextInt();//以整数的形式接收
  
  //判断年龄 幼儿少年 青少年 青年 中年
    String str = "老年";
    if(age < 0 || age > 150){
      str = "年龄不合法";
    }else if(age <= 5){
      str = "幼儿"；
    }else if(age <= 35){
      str = "青年"；
  }
    System.out.pringln(str);
  
  }
}
~~~
#### 总结
- else if一个分支执行剩下的不执行  全是if分支全部执行
- if中一条语句不加大括号 可以只有if,没有else 不能相反
~~~java
boolean sex = true;
if(sex) System.out.println("男"); else System.out.println("女")；
~~~

#### swich
switch(int/string){//也可以是byute short char 因为可以自动类型转换  
  case i:  
    java语句；  
    break；//到break终止 没有break直接进行下一个分支执行(不进行匹配，case穿透)  
  default:  
    java语句；//都不匹配则default  
}
##### case 可以合并
- int i  = 10;
  switch(i){
    case 1 : case 2: case 10；:
    system.out.println("hw");
  }
  
### 循环结构
- for | while | do while
- 循环体(要反复执行的代码) 计算器
### 变量的作用域
#### for
~~~
for(初始化表达式；布尔表达式；更新表达式){
  循环体；
}
初始化表达式(仅一次)-bool(true-循环体-更新 false-结束)
public static void main(String[] args){
  int i; //先声明再定义(初始化) 声明在头文件，定义在源文件
  for(i = 1; i<=10; i++){
    System.out.println(i);
  }
  System.out.println(i);//i的作用域，此时是11
}
~~~
- 低一级可以访问高一级的变量
- 类级变量 static修饰 在类定义后就已经存在
- 对象实例级变量就是成员变量，实例化后才会分配内存空间
- 方法级变量就是在方法内部定义的变量-局部变量 作用域从它被声明的点开始，一旦出了自己的作用域马上从内存中消失
- 块级变量就是定义在一个块内部的变量，变量的生存周期就是这个块，出了这个块就消失了，比如 if、for 语句的块。块是指由大括号包围的代码
~~~java
public class Test{
    public static String name = "TEST"; // 类级变量
    public int i; // 对象实例级变量
    
    // 属性块，在类初始化属性时运行
    {
        int j = 2;// 块级变量
    }
    
    public void test1() {
        int j = 3; // 方法级变量
        if(j == 3) {
            int k = 5; // 块级变量
        }
        // 这里不能访问块级变量，块级变量只能在块内部访问
        System.out.println("name=" + name + ", i=" + i + ", j=" + j);
    }
 
    public static void main(String[] args) {
        // 不创建对象，直接通过类名访问类级变量
        System.out.println(Test.name);
        // 创建对象并访问它的方法
        Test t = new Test();
        t.test1();
    }
}
~~~

#### while
~~~
while(bool表达式){
  循环体；
}

public static void main(String[] args)
{
  int i = 1;
  while(i<=10)
  {
    System.out.println(i);
    i++;
  }
}

while(true){}//死循环

do{
  循环体；
}while(bool); //注意封号

~~~
## 控制循环语句
- break continue
- 关键字+封号构成java语句
- break 终止switch语句/循环语句 跳出最内层的循环
- for+if+break 找质数

~~~java
//每八个一行显示100以内质数

public static void main(String[] args){
  int count = 0;
  for(int i = 2; i<=100; i++){
    boolean issushu = true;//标记思想 放在第一个循环，保证每一个数更新一次状态
    for (int j = 2; j<i; j++){
      if(i%j==0){
        issushu = false;
        break;//仅为了不接着做除法，自动到下一个数，不用else
      }//这里可以不用else
  }

  if(issushu)
  {
    System.out.print(i+"\t");
    count++;
    if(count % 8 == 0)
    {
      System.out.print("\n");
    }
  }
}
~~~
  
### 总结
- break 结束所在循环
- continue 表示更新表达式跳到下一次循环
- for 循环中return终止方法
  
### continue + 循环名称（了解）

## 方法 method/function(c)
- 代码复用 调用 invoke
- 定义在类体中
- 【修饰符列表】 返回值类型 方法名（形参列表）{方法体;}
- 不同功能抽取到不同方法 不全写在main
  
### 修饰符 public static
- **含static时 调用 类名.方法名(实参)** 调用的方法和被调用的方法在同一个类，类名可省略 最好一个java源文件一个class
- 也可采用引用. 也和对象无关，也不会有空指针异常
- 定义方法时不执行，调用.时执行
- 不返回任何数据是void可以return;（此时所在方法结束） 否则return A(返回值类型，8种)；
- 返回值可以接收也可以不接收 **用变量接收** 用赋值运算符先计算右边 int c = divide(10,3);
- 形参 局部变量 逗号相隔 重要的是数据类型不是形参名字
- 实参 调用方法时传递的真实数据 和形参必须数量 类型相同 **方法调用时传递的是值浅拷贝？**
- 公开的类名和源文件名相同 类体内不直接写java语句
- main方法程序入口 由jvm调用 最先开始**最后结束** 符合栈结构

## 方法执行过程中jvm内存分配
- 定义方法时不执行，JVM中也不分配内存
### jvm主要内存空间：方法区内存 堆内存 栈内存
### 数据结构：数据的存储形态
- 常见：数组 队列 栈 链表 二叉树 哈希表/散列表
- 栈：stack
- 栈桢指向栈顶元素
- 栈顶活跃 其他元素静止
- 压栈/入栈 pop 弹栈/出栈 push
- 方法结束时弹栈
- 先进后出
- 队列 两头通 先进先出

### 方法执行内存分析
- class 文件装载到jvm后 最先将方法代码片段存放在方法区
- 代码片段只有一份 调用一次方法 给方法在栈内存中分配一块空间(为局部变量(在方法体中声明)) 此时压栈(先调用方法在栈底部) 方法结束后方法的内存空间全部释放 此时弹栈 这也是局部变量其他方法无法调用的原因
### 方法重载 overload
- 同一个类中 功能相似 参数列表不同(数量 顺序 类型) 和修饰符,返回值类型无关
- 调用方法不依赖方法名依赖实参类型
### 方法的递归调用
- 方法自身调用自身 耗费栈内存 不断压栈 可能栈内存溢出错误 stack overflow error
~~~java
//1-N 的和
public static int sumN(int n){
  if(n == 1){
    return 1;
  }
  return n + sum(n-1);
}

public static void main(String[] args) {
  int n = 4;
  System.out.println(sumN(n));
}

~~~
![递归方法调用内存图](/pic/递归1.png "递归")
## 面向对象
- 面向过程 步骤间因果关系实现模块/系统 没有独立体
- 面向对象 关注独立的个体实现的功能 集成显卡和独立显卡
- 特征 封装 继承 多态
- 面向对象的方式
- 面向对象的分析  OOA
- 面向对象的设计  OOD
- 面向对象的开发  OOP

## 类和对象
类是对象的共同特征 描述状态和动作
对象(instance)是实际存在的个体
- 类-实例化--对象
- 对象--抽象--类

### 类的语法结构
~~~
[修饰符列表] class 类名{
  属性；//状态 成员变量 默认值向0看齐

//实例变量，通过对象调用而不是类 不创建对象，no变量的内存空间不存在，创建对象后默认是0
  int no；
//静态变量，存储在方法区内存中
  static int no；

  方法；//动作 
}
~~~

#### 注意
- 成员变量具有默认值
- 实例变量创建对象后默认是0
- 静态变量直接具有默认值

### 对象的创建和使用
- new 类名();
- new 是一个运算符 作用是创建对象 在JVM堆内存中开辟新的内存空间 
- student s = new student();
- s 是一个局部变量，**保存对象的内存地址** (通过赋值)【可以是局部变量(main内)也可以是实例变量(address属性)】，叫**引用**。堆内存中开的内存空间叫对象 **赋值时右边内存地址赋值给左边**
- 通过引用访问堆内存中的对象内部的实例变量 不同于C语言用指针操作内存空间
- 读取 s.no 修改 s.no = 1
- 修改实例变量不影响下一次调用对象的实例变量 实例变量在堆内存的java对象内部存储
![对象内存图](/pic/类和对象.png "对象")
- u.address.city
- ![引用](/pic/类2.png "引用详解")
#### 注意
- 字符串是引用数据类型 创建了Srting对象将地址保存给name 和new作用相同
- 类里面的字符串属性都是引用
- 引用数据类型默认值是null(空值)，不同于void（返回值类型）
- null说明指针不指向任何数据，void指针实实在在地指向一块内存，只是不知道这块内存中是什么类型数据（void是返回值类型是空类型）
- char默认值 \u0000  boolean默认值 false

### JVMM内存管理
- ![JVM内存管理](/pic/JVM内存管理.png "内存")
- 空指针异常 java.lang.NullPonterException 可以编译不能运行
- 空引用访问实例变量的数据
- customer c = new customer();
- c = null;
- System.out.println(c);//如果一个对象为null，调用其方法或访问其字段就会产生NullPointerException
## Java集成开发环境 IDE
- Integrated Development Environment
- IDE是一种应用程序，它提供了一个统一的界面来编写(打包)、调试、编译和执行代码。
- 没有IDE需要安装JDK，配置环境变量，手动编译，没有错误提示
- eclipse
-  workspace 工作区 存放java代码(src)和编译.class(output/bin)
- 打开软件生成 .metadata 保存工作区状态(窗口)
- 右上角切换布局(语言)
- package/navigator/project 源代码窗口
- console 控制台窗口
- P125 project配置 包(package)机制

## 封装
- 对外提供简单的操作入口
- 封装后产生真正的对象，独立体
- 安全级别高 否则随意读取修改

#### 属性私有化
- private int age; //只能在本类访问，外部无法访问，对象.属性 访问
- 成员变量声明为private，通过public方法访问
  
#### 对外提供简单操作入口
- 项目是mavan可以导入jdr包实现属性的封装
~~~java
public int getAge(){
  return age;
}

public void setAge(int age){
  //安全过滤
  if(a < 0 || a >150){
    System.out.println("不合法");
    return;
  }
  this.age = age
}
~~~
#### super
- 没有static修饰的方法调用: **引用.方法名(实参);** CP类.方法
  
## 构造方法
- 构造方法/函数/构造器/Constructor
- [修饰符列表] 构造方法名 (形参){构造方法体} //构造方法名和类名一致
- 没有返回值类型 有了变为普通方法 因为返回值类型就是类本身
- 用来创建对象
- 方法调用 new 构造方法名 (实参)
#### ctrl + (shift) +/ (多行)注释
- 类中没构造方法有默认构造方法 缺省构造器
- 无参数 有参数构造方法都要写 用到重载 public User(){} public User(int i){}
### 构造对象的同时初始化实例变量
- **构造方法创建对象 同时初始化实例变量**（不在类加载的时候而在构造方法执行过程中）
#### eclipse 快捷键
- ctrl 鼠标移动到要查看的属性/方法
- ctrl + O 查看类中所有方法
- 块编辑

### 参数传递
- 方法调用时怎么传递数据
- 参数传递的是变量中保存的具体值 没有**引用传递**
![参数1](/pic/参数传递1.png)
![参数2](/pic/参数传递2.png)
![参数3](/pic/参数传递3.png)
![参数4](/pic/参数传递4.png)
- 第二个和堆内存有关
- int i = 10
- int j = i
- 传递了10，j是一块全新的内存空间

### this 关键字
- this 是一个引用，**保存当前对象的内存地址指向自身**，this 存储在JVM堆内存java对象内部
#### 可以出现在**实例方法**(main中没有this)中，表示当前的对象
- name是实例变量，要采用引用.访问 但是访问name在大括号中，**作用域**包括当前方法，一定是当前对象的name，this可省略
~~~
public class Customer{
  String name;
  public Customer(){
  }
  public void Shopping(){
    System.out.pringln(name + "在购物");
  }
  
}
~~~

#### 创建两个customer对象
- ![this1](/pic/this1.png)
- 一个对象一个this 
#### this使用在实例方法 可省略
- 没有static 的方法是实例方法，**必须有对象的参与** 引用.调用
- 带static的方法通过类名.访问 不能使用this 也不能调用实例变量（**带static方法不能访问 this.name**）
- static方法不能直接访问实例变量和实例方法，可以创建对象后访问
#### this用来区分实例变量和局部变量
~~~
public class Customer{
  private int id; //实例变量

  //构造方法
  public void SetId(int id){
    super();
    this.id = id;
  }
  public int GetId(){
    return id; //这里不用this 因为实例方法
  }

  //构造方法
  public Customer(int id){
    this.id = id;
  }
}
~~~
#### this使用在构造方法
- 通过当前构造方法调用其他的构造方法 this(实参) 只能出现在构造函数第一行
~~~
public Customer(int id, String name)
  {this.id = id;
  this.name = name;
  }

public Customer(){

//int id = 000001; String name = "张三"; 可以通过调用另一个构造方法完成
  this(00001,"张三")；

//new Customer(00001,"张三");  不能采用这种方法 因为当调用构造方法时会new两次
}
~~~


### static
- 实例变量 每个对象都保存这块内存空间 浪费内存
- 静态变量存储在方法区内存中 在**类加载**时初始化 不需要创建对象 内存就开辟了
- static String country(国籍)
- static修饰的元素 可以类名.也可以引用.  任何的实例都可以调用，因此静态方法中不能用this和super关键字
- static方法无法访问实例方法和实例对象
- 实例方法访问static方法可直接调用
- 大多数工具类的方法是静态方法(+ — * / print) 因为工具类是方便编程 不需要new对象
#### private static
- 如果你的私有函数没有访问类里面的其他参数和方法，又被频繁调用，那就把他设为private static
- 被private static修饰的属性只能被本类中的方法(可以是非静态的)调用，在外部创建这个类的对象或者直接使用这个类访问都是非法的(public static可以)

## static 代码块
- static{java语句；}
- **类加载时**执行（main方法前） 一个类中可编写多个 自上而下依次执行
- 静态代码块这种语法机制实际上是sun公司给我们java程序员的一个特殊的时刻/时机，这个时机叫：类加载时机。
- 类加载到JVM时记录日志
### 实例方法快
- 构造方法执行前执行(**对象初始化**时机) 在类中，构造函数外
- un公司为java程序员准备的一个特殊的时机，叫做对象构建时机。
- {java语句;}

#### 总结
- 静态代码块，在虚拟机加载类的时候就会加载执行，而且只执行一次;
- 非静态代码块，在创建对象的时候(即new一个对象的时候)执行，每次创建对象都会执行一次
- https://www.cnblogs.com/lukelook/p/11183155.html
- 一个程序可以有多个静态非静态代码区域。

## 继承
- 封装产生独立体
- 继承是为了代码复用 方法覆盖和多态机制
#### 通过继承，子类就可以获得了父类方法的地址信息并把这些信息保存到自己的方法区，这样就可以通过子类对象访问自己的方法区从而间接的访问父类的方法
#### 重写的话，就直接访问子类自己重写后的方法，方法表中原先存父类method01方法的引用被改写成子类的method01方法的引用
#### 静态方法的调用的是通过在编译器静态绑定的，而实例方法的调用是在运行时动态绑定的，2者的调用的方式不同，所以二者只能存在其一，否则会存在歧义！

### 继承机制
- 私有的数据(属性,方法)，构造方法不支持继承 其他数据都可以支持
- 语法格式：
~~~
[修饰符表] class 类名 extends 父类名{
  类体 = 属性 + 方法
}
//账户信息
public class Account{

private accountno;
private balance;

}

//信用账户
public class CreditAccount extends Account{

//继承private account，balance，通过继承的public get，set调用
  private double credit;

}

public static void main(String[] args){

CreditAccount act = new CreditAccount();
act.setAccountno("act-001");

}
~~~
- java只支持单继承 一个类不能继承很多类
- B继承A
- B 父类 基类 超类 superclass
- A 子类 派生类 subclass

### super
- super 指向离自己最近的一个父(超)类对象
- super.变量名 super.成员函数据名（实参）
- **构造方法 super(); / super(name)**
- 每个子类构造方法的第一条语句，都是隐含地调用 super()，如果父类没有这种形式的构造函数，那么在编译的时候就会报错。
- super() 和 this() 均不可以在 static 环境中使用，包括：static 变量,static 方法，static 语句块。
#### this 和 super 不能同时出现在一个构造函数里面，也必须在构造方法内第一行
- 子类是从父类继承而来，继承了父类的属性和方法，如果在子类中先不完成父类的成员的初始化，则子类无法使用，因为在java中不允许调用没初始化的成员。在构造器中是顺序执行的，也就是说必须在第一行进行父类的初始化。而super能直接完成这个功能。This()通过调用本类中的其他构造器也能完成这个功能。
- https://www.runoob.com/w3cnote/the-different-this-super.html


#### 间接继承多个类
- c extends B{}
- B extends A{}
- A extends T{}
- C直接继承B 间接继承T A
- 没有显示继承任何类则默认继承JDK javaSE库中的java.Lang.object类(所有类都继承这个类)
- Extendtest et = new Extendtest();  
  String s = et.toString();
#### 查找类型【open type】C+S+T 查找类
#### 查找资源【open resource】C+S+R 当前项目下(src)文件
### 方法覆盖 override (方法重写)
- 父类中方法无法满足子类的业务需求
- **返回值类型 方法名 形参列表**相同
- 访问权限不能更低 只能更高 public private protected
- 抛出异常不能更多只能更少 public void move() throws Exception{}

#### 注意
- 私有方法，构造方法没有继承 不能覆盖
- - 覆盖只针对方法不针对属性
#### 静态方法不存在覆盖(重写)，也就不存在多态
- 如果子类里面定义了同名静态方法和属性，那么这时候父类的静态方法或属性称之为"隐藏"
- 直接调用方法区中静态方法，无需经过方法表，这也就解释了静态方法的执行只看静态类型，而与实际类型无关，
#### static方法（变量）的内存空间子类也可操作
- Son s = new Son();  
  s.staticMethod();//输出：Parent staticMethod run

#### 声明为static的方法有以下几条限制：
- 它们只能直接访问static数据，非static创建对象 
- 它们不能以任何方式引用this 或super。
  
## 多态
- 多态就是指程序中定义的引用变量所指向的具体类型和通过该引用变量发出的方法调用在编程时并不确定，而是在程序运行期间才确定
- 这样，不用修改源程序代码，就可以让引用变量绑定到各种不同的类实现上，从而导致该引用调用的具体方法随之改变，即不修改程序代码就可以改变程序运行时所绑定的具体代码，让程序可以选择多个运行状态，这就是多态性。
  
#### 向上转型（upcasting）
- 子类型转换为父类型 自动类型转换（bool外七种都可）**必须有继承关系**
- - animl a = new cat(); **父类型引用指向子类型对象** cat is a animal
- a.catchMouse() ✖️ 只能访问animal中的方法 编译不通过
- **a.move()**
- Animal.class 字节码中有move方法，编译通过。这过程称为静态绑定，编译阶段绑定
- a的底层（堆内存）对象是cat 运行时调用cat的方法。这过程称为动态绑定，运行阶段绑定
- 无论有没有重写move，运行阶段都是调用cat对象的move
- 父类型引用指向子类型对象这种机制导致程序在编译阶段和运行阶段绑定两种不同的形态/状态 - 多态
  
#### 向下转型（downcasting）
- 父 - 子 强制类型转换 **必须有继承关系** 
#### 调用子类型中特有方法需要向下转型
-  Cat b = (Cat)a;//类似long x = 100L; int i = (int)x
-  b.catchMouse();
-  Animal a3 = new bird();Cat c3 = (Cat)a3; ✖️  
  **ClassCastException** 必须有继承关系 出现在向下转型  
  编译时通过 cat animal 继承关系，向下转型 运行行不通过 因为真实存在的对象是bird类型，而不是animal  
  java规范强制类型转换前 使用instanceof运算符避免异常
#### instanceof
- 引用 instanceof 数据类型名 执行结果布尔类型
- a instance of Animal; true - a这个引用指向的对象是一个Animal类型
- 测试它左边的对象是否是它右边的类的实例
- 当a3引用指向的对象是一个Cat时
~~~java

if(a3 instance of Cat){
  Cat c3 = (Cat)a3;//再做强制类型转换
}else if(a3 instanceof Bird){
  Bird b2 = (Bird)a3;
  Bird.fly();
}

~~~
## 解耦合
- 降低程序耦合度，提高程序扩展力
- master cat 新加dog类不对master类中方法有影响 master只和pet有联系，只面向抽象的pet
  
~~~java
public void Master{
  Public void feed(Pet pet){//相当于Pet pet = new cat()
    pet.eat();
  }
}

public void Test{
  public static void main(String[] args){
    Master Zhangsan = new Master();
    Zhangsan.feed(new Cat());//参数传递到feed方法相当于Pet pet = new cat()

//也就是父类型引用指向子类型变量 编译阶段调用pet的方法，运行阶段调用对象的方法
//Cat Tom = new Cat(); Zhangsan.feed(tom);

  }
}
~~~

## 断点调试 P153-38'
- 右键设置断点 debug as / java application
- 双击一行 设置断点(表示执行到这行上面，不包括这行)
- F5 step into 进入方法
- F6 step over 下一步
- F7 step return 退出方法
- F8 resume 下一个断点
- terminate 强行终止 关闭java虚拟机

### final
- P155 源码链接方法 类库：源码 字节码 帮助文档
- 最终的 不可变的
- final修饰的修饰的类无法继承
- final修饰的方法无法覆盖
- final修饰的变量赋值后不能重新赋值
- final修饰的实例变量要手动赋值，不能采用系统默认值
- final int age = 1;
#### 方法二
- final int age;
- public FinalTest(){
    this.age = 1
- }//两种方法都在构造方法执行时给实例变量赋值，时间相同
#### 常量
- final 修饰的变量不可变，一般与static联合使用(节约内存)，称为常量
- **public static final** GUO_JI = "中国";
- 常量名字全大写 下划线连接
- 类名.调用 Math.PI

- final修饰的引用不能指向新的对象 被指向的变量无法被垃圾回收
- final User u = new User(30);
- u = new User(50) ✖️
- 对象内部内存可以修改 u.id = 50;

#### 总结
- 父类中staitic修饰的静态方法，不能覆盖、不能继承，也无法表现出多态
- 父类中staitic修饰的变量或常量，能覆盖、不能继承
- 父类中final修饰的方法，不能覆盖，但可继承

## 包和import
- 不同功能的类放到不同的包
- 程序第一行(不包括注释)编写package语句
- Package 包名
- 包名：公司域名倒序 + 项目名 + 模块名 + 功能名//重名几率低 全小写
- package com.bjpowernode.oa.service;
- 一个包对应一个目录 这里四个
#### 如何编译运行这个包下的类？  
  在第一层目录下cmd(day11-2)  
  javac *.java  
  java com.bjpowernode.oa.service.day11.Test01  
（需要把Test101.class放在第四层目录下才能运行）
#### 另一种方式
javac -d 编译后存放的路径 java源文件的路径
- javac -d C:\ F:\Hello.java
- 将F:\Hello.java编译后放到C:\目录下
#### 在第一层目录下cmd javac -d . *.java
- 当前路径中 *.java编译后放到当前目录下
- 自动创建目录

~~~java

package com.bjpowernode.javase.day11;

public class Test01{}

public class Test02{
  public static void main(String[] args){
    com.bjpower.node.javase.day11.test01 t = new com.bjpower.node.javase.day11.test01();
    System.out.println(t);
    Test01 tt = new test01() //类在同一个包下 包名可省略
    //不同则import导入类 写在package语句下class语句上
    //import com.bjpowernode.javase.day11.test01;
    //import com.bjpowernode.javase.day11.*;
  }
}
javac -d . *.java
~~~

- java lang包是核心包不需要导入 包括String
- java.util.Date d = new java.util.Date();//工具类
- import java.util.*;
- Date d = new Date();

### 访问控制权限修饰符
- 控制元素的访问范围
- public      公开的 任何位置都可访问
- protected   同包 + 子类（包外子类可用父类不可）（包外子类继承了父类型的实例方法，但只能子类对象访问）
- 缺省         同包
- private     私有的，只能在本类访问
- private < 缺省 < proetcted < public
#### https://blog.csdn.net/qq_32907195/article/details/110631855
- 类只能public/缺省 【内部类除外】
#### 内部类
~~~java

//不使用static修饰内部类
//内部类没有使用static关键字，不能直接创建实例。
public class OuterClass {
    public class InnerClass{
        InnerClass(){}
    }
}

public class TestStaticClass {
    public static void main(String[] args) {
        // OutClass需要先生成一个实例
        OuterClass oc = new OuterClass();
        oc.new InnerClass();
    }
}


//使用static修饰内部类
public class OuterClass {
    public static class InnerClass{
        InnerClass(){}
    }
}

public class TestStaticClass {
    public static void main(String[] args) {
        // OutClass 不需要生成实例
        new OuterClass.InnerClass();
    }
}

~~~
- 




















