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
### 
- program files(X86) 32位
- DOS命令
- dir  
  cd Desktop （change direcroty）  
  cd.. 上级目录  
  cd \ 跟目录  
  cls  
  java -version  
  exit  
  del *class
- 垃圾回收机制（GC）
- 可移植性（跨平台） 一次编译 到处运行  JVM（java虚拟机）
- java加载和运行
-  .java(源文件，在硬盘)-.class(使用javac编译为字节码，检查是否符合java语法，非纯二进制不然操作系统能处理) .class 可拷贝到其他操作系统执行   \javac 路径
-  编译只检查语法不运算 byte b = i（int 10） / 3 (错) 
-  java.exe 运行 \ A.class - java A  \ JVM 类加载器(ClassLoader)-操作系统-硬件平台 \操作系统执行二进制和底层硬件平台交互
-  JRE(包括JVM)  java runtime envoronment 运行环境（运行JDK）
-  JDK目录
  java/bin :存放命令 包括javac java.exe  
  Windows/System32 ipconfig.exe 在环境变量path指定的路径中设置（属性-高级） classloader: classpath=.;XX(当前目录) 用户变量
-  注释 只在源文件不会被编译到字节码
   单行 //  
  多行 /* */  
  javadoc注释 /**  
               *  
                  */ 通过javadoc.exe生成帮助文档 鼠标停留有信息

        public class HelloWorld{//类体中不直接写java 除声明变量外
          public static void main(String[] args){//main 方法名 表示定义一个公开的静态的主方法(程序入口) string[]是一种饮用数据类型 args是局部变量，可以随意命名
            System.out.println("Hello World!");//方法体
            System.out.println("I am Andrew");  
          }//公开的类名必须和源文件一致
   }

        classA{
          public static void main(String[] args){
            System.out.println("run this main");//println换行 print不换
          } 
  }//一个java源文件可以有多个class 并可以没有public class 每一个class都可以有main方法

## 标识符
    可以自己命名 数字字母_$,不以数字开头  
    类名、方法（main）、常量、接口
    命名规范：类名 接口名  首大写 后单词大写
    变量名 方法名 首小写 后单词大写
    常量名 全部大写
## 关键字 
SUN提前设置 全小写
## 字面值(数据)
字符串型字面值 "" 字符型'' 整数 浮点 布尔
## 变量
  命名一块空间，包含数据类型 变量名 字面值 （类型 字面值一致）
  int housePrice,a,b；a并未初始化也并未开辟空间
  housePrice = 1；//运算右边赋值左边   int housePrice = 1；获取(get) 修改(set)
- 作用域 变量的有效范围 同作用域只能有一个变量  
  局部变量 方法体中声明  
  成员变量 方法体外**类体**内声明 **就近原则** 有默认值(0) char-\u0000(\u0020是空格)
## 数据类型 指导程序运行阶段分配多少空间
  基本数据类型 整数型(byte,short,int,long) 浮点型(float,double) 布尔型(boolean) 字符型(cahr)  12484812byte
- 取值范围  源码补码反码
- 以补码存储
- 正数补码相同 负数将正数取反+1
- int 2147483647
- 补码 1000000
- 减一 01111111
- 反码 10000000 —— -128


  
  引用数据类型   类 接口 数组 (字符串) 
- 1byte(字节) = 8 bit(字节位) 1KB = 8byte 第一位表正负
- ASCII码 字符码 用二进制表示文字（解码）  文字表二进制 (编码)
  'a' --> 97 按照ASCII 解码 [0110 0001]
  'A' --> 65
  '0' --> 48
- 简中编码 GB2312 < GBK < GB18030
- 统一所有 unicode utf-8（.） utf-16 utf-32 java标识符可以用中文 public class 学生{}
- char K = '我' 双字节可存储中文
- 转义字符\
  char c2 = '\n' 换行符  '\t'制表符<br>
  char k = '\\'   char k ='\'(\将‘转义为普通‘,错)  char k = ''Hello''(前两个单引号配对，错)
- jdk native2ascii.exe 中 '\u4e2d' \转义u-unicode
- 整数型 byte short int long
- int a = 10; 10默认int
- 三种表示方式
- int a = 10 / 3; 整数/整数=整数
- int b = 010; //8进制
- int c = 0x10; //16进制
- system.out.println(c);
- long z = 2147483648L //整数型字面值默认为int类型处理 添加L作为long 自动类型转换-小容量转换为大容量 int-long
- 大容量-小容量 强制类型转换符 强制删去左侧二进制位
- Long x = 100;
- int y = (int)x;
- byte b = 50； byte不超过127可以不用强制类型转换符  包括short char
- 浮点型 float double 存储近似值 
- 引用数据类型 java.math.BigDecimal
- Java SE 类库 jre\lib\rt.jar  //JavaSE自带的类 String System
- 类库源码 src.zip
- double d = 3.0; 浮点型默认float
- float f = 3.0f;   float f = (float)3.0;
- 布尔型 boolean
- 只有 true false 两个值 底层用01存储
- boolean login = true;
- 转换规则
- 除bool数据类型都能互相转换 char c = 97;
- 任意浮点型都比整数型容量大
- 多种数据类型混合运算 先转换成容量最大的类型再运算
- byte short char 先转换成int运算
# 运算符
- 算数运算符 + - * / %(取余) ++(自加一) --
- 优先级 加()
- ++x/x++ 单目运算符
- int b = a ++ 先赋值 再a+1
- int b = ++ a 先➕1再赋值
- system.out.println(s--);  x=s-- 打印s再s=s-1
- 关系运算符 > >= == !=       =是赋值运算符<br>
  运算结果bool型
- 逻辑(bool)运算符
- & | !(单目 !false) ^(异或 两边算子不一样就是真) &&(短路与 和与结果相同但存在短路现象) ||(短路或)
- 两边算子bool，最终结果bool
- system.oyt.println((5 > 3) | (5 > 6)); //true
- int x = 10;
- int Y = 8;
- system.out.println( x < Y && ++x < Y); //短路与 第一个出现false则第二个表达式不执行
- 两边算子都要执行要用逻辑与
- system.out.println(X); // 10
- || 短路或
## 赋值运算符
- 基本赋值运算符 =
- 扩展运算符 不改变运算结果类型
- +=(累进)  /=  %=(取余)
- byte x =10;
- x += 5;  //等同于x = (byte)(x+5) 不等于x = x + 5(int 赋值到 byte 不通过)
## 字符串连接运算符 +
- +两边是数字 加法运算
- +两边有一个字符串 字符串连接 返回字符串结果
- system.out.println(a "+"+b+"="+(a+b));
## 三元(条件)运算符
- char c = bool表达式 ? 表达式1 : 表达式2； c的类型和表达式类型一致
- boolen sex = false;
- char c = sex ? '男' : '女'；
## 控制语句
## 选择结构
- if、if else

- if(bool表达式){
  };
- if(bool表达式){
  }else{
  };
- if(bool表达式){
  }else if{
  }else if{
  }else{
  };<br>
- else if一个分支执行剩下的不执行  全是if分支全部执行
~~~
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
    String userInputContent = s.next();
  //以字符串的形式接受
    int age = s.nextInt();//以整数的形式接收
  
  //判断年龄 幼儿少年 青少年 青年 中年
    String str = "老年";
    if(age < 0 || age > 150){
      str = "年龄不合法";
    }else if(age <= 5){
      str = "幼儿"；
    }else if(ag  e <= 35){
    str = "青年"；
  }
  System.out.pringln(str);
  
  }
}
~~~
- if中一条语句不加大括号 可以只有if,没有else 不能相反
~~~
boolean sex = true;
if(sex) System.out.println("男"); else System.out.println("女")；
~~~


- 第一步：java.util.Scanner S = new java.util.Scanner(System.in);
- 第二步：string str = s.next();  int num = s.nextInt();

## swich
    switch(int/string){//也可以是byute short char 因为可以自动类型转换
      case i:
        java语句；
        break；//到break终止 没有break直接进行下一个分支执行(不进行匹配，case穿透)
      default :
        java语句；//都不匹配则default
    }
### case 可以合并
    int i  = 10;
    switch(i){
      case 1 : case 2: case 10；:
      system.out.println("hw");
    }
- 
## 循环结构
- for | while | do while
- 循环体(要反复执行的代码) 计算器
### 变量的作用域
- 
~~~
for(初始化表达式；布尔表达式；更新表达式){
  循环体；
}
初始化表达式(仅一次)-bool(true-循环体-更新 false-结束)
public static void main(String[] args){
  int i; //先定义再声明
  for(i = 1; i<=10; i++){
    System.out.println(i);
  }
  System.out.println(i);//i的作用域，此时是11
}
~~~
- for + if 找出1-100的奇数
## while
~~~
while(bool表达式){
  循环体；
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
- 含static时 调用 类名.方法名(实参) 调用的方法和被调用的方法在同一个类，类名可省略 最好一个java源文件一个class
- 定义方法时不执行，调用时执行
- 不返回任何数据是void可以return;（此时所在方法结束） 否则return A(返回值类型，8种)；
- 返回值可以接收也可以不接收 **用变量接收** 用赋值运算符先计算右边 int c = divide(10,3);
- 形参 局部变量 逗号相隔 重要的是数据类型不是形参名字
- 实参 调用方法时传递的真实数据 和形参必须数量 类型相同 **方法调用时传递的是值浅拷贝？**
- 公开的类名和源文件名相同 类体内不直接写java语句
- main方法程序入口 由jvm调用 最先开始**最后结束** 符合栈结构
## 方法执行过程中jvm内存分配
- 定义方法时不执行，不调用执行，JVM中也不分配内存
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
- class 文件装载到jvm后 最先给方法代码片段存放在方法区
- 代码片段只有一份 调用一次方法 给方法在栈内存中分配一块空间(为局部变量(在方法体中声明)) 此时压栈(先调用方法在栈底部、) 方法结束后方法的内存空间全部释放 此时弹栈 这也是局部变量其他方法无法调用的原因
## 方法重载 overload
- 同一个类中 功能相似 参数列表不同(数量 顺序 类型) 和修饰符,返回值类型无关
- 调用方法不依赖方法名依赖实参类型
## 方法的递归调用
- 方法自身调用自身 耗费栈内存 不断压栈 可能栈内存溢出错误 stack overflow error
~~~java
//1-N 的和
public static void sumN(int n){
  if(n == 1){
    return 1;
  }
  return n + sum(n-1);
}
~~~
![递归方法调用内存图](/pic/递归1.png"递归")
## 面向对象
- 面向过程 步骤间因果关系实现模块/系统 没有独立体
- 面向对象 关注对立的个体实现的功能 集成显卡和独立显卡
- 特征 封装 继承 多态
- 面向对象的方式
- 面向对象的分析  OOA
- 面向对象的设计  OOD
- 面向对象的开发  OOP
### 类和对象
类是对象的共同特征 描述状态和动作
对象(instance)是实际存在的个体
- 类-实例化--对象
- 对象--抽象--类

### 类的语法结构
~~~
[修饰符列表] class 类名{
  属性；//状态 成员变量 默认值向0看齐
  int no；//实例变量，通过对象调用而不是类 不创建对象，no变量的内存空间不存在，创建后默认是0
  static int no；//静态变量，存储在方法区内存中
  方法；//动作 
}
~~~
### 对象的创建和使用
- new 类名();
- new 是一个运算符 作用是创建对象 在JVM堆内存中开辟新的内存空间 
- student s = new student();
- s 是一个局部变量，**保存对象的内存地址** (通过赋值)【保存内存地址指向对象/等号左边 可以是局部变量(main内)也可以是实例变量(address类内)】，叫引用。堆内存中开的内存空间叫对象 **java没指针 赋值时的内存变化方法 传递内存地址 浅拷贝？** **赋值时右边内存地址赋值给左边**
- 通过引用访问堆内存中的对象内部的实例变量 不同于C语言用指针操作内存空间
- 读取 s.no 修改 s.no = 1
- 修改实例变量不影响下一次调用对象的实例变量 实例变量在堆内存的java对象内部存储
![对象内存图](/pic/类和对象.png "对象")
- u.address.city
- ![引用](/pic/类2.png "引用详解")
### JVMM内存管理
- ![JVM内存管理](/pic/JVM内存管理.png "内存")
- 空指针异常 java.lang.NullPointerException 可以编译不能运行
- 空引用访问实例香港的数据
- customer.c = new customer();
- c = null;
- System.out.println(c);
## Java集成开发环境 IDE
- 没有IDE需要安装JDK，配置环境变量，手动编译，没有错误提示
- eclipse
-  workspace 工作区 存放java代码(src)和编译.class(output/bin)
- 打开软件生成 .metadata 保存工作区状态(窗口)
- 右上角切换布局(语言)
- package/navigator/project 源代码窗口
- console 控制台窗口
- P125 project配置 包(package)机制
### 封装
- 对外提供简单的操作入口
- 封装后产生真正的对象，独立体
- 安全级别高 否则随意读取修改
#### 属性私有化
- private int age; //只能在本类访问 外部无法 对象.属性 访问
#### 对外提供简单操作入口
~~~
public void setAge(int a){age = a;}
public int setAge(int a){
  //安全过滤
  if(a < 0 || a >150){
    System.out.println("不合法");
    return;
  }
  this.age = age
}
~~~
- 没有static修饰的方法调用: **引用.方法名(实参);** CP类.方法
### 构造方法
- 构造方法/函数/构造器/Constructor
- [修饰符列表] 构造方法名 (形参){构造方法体} //构造方法名和类名一致
- 没有返回值类型 有了变为普通方法 因为返回值类型就是类本身
- 用来创建对象
- 方法调用 new 构造方法名 (实参)
- ctrl + (shift) +/ 多行注释
- 类中没构造方法有默认构造方法 缺省构造器
- 无参数 有参数构造方法都要写 用到重载 public user(){}; public user(int i){}




















