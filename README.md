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
                  */ 通过javadoc.exe生成帮助文档

        public class HelloWorld{//类体中不直接写java
          public static void main(String[] args){//main 方法名 表示定义一个公开的静态的主方法(程序入口)
            System.out.println("Hello World!");//方法体
            System.out.println("I am Andrew");  
          }//公开的类名必须和源文件一致
   }

        classA{
          public static void main(String[] args){
            System.out.println("run this main");
          } 
  }//一个java源文件可以有多个class 并可以没有public class 每一个class都可以有main方法

  - 标识符\可以自己命名 数字字母_$,不以数字开头  
    类名、方法（main）、常量、接口
    命名规范：类名 接口名  首大写 后单词大写
    变量名 方法名 首小写 后单词大写
    常量名 全部大写
- 关键字
- 字面值(数据) 字符串型字面值 "" 字符型'' 整数 浮点 布尔
- 变量 命名一块空间，包含数据类型 名称 字面值 （类型 字面值一致）
  int housePrice,a,b；a并未初始化也并未开辟空间
  housePrice = 1；//运算右边赋值左边   int housePrice = 1；获取(get) 修改(set)
- 数据类型 指导程序运行阶段分配多少空间
- 作用域 变量的有效范围 同作用域只能有一个变量  
  局部变量 方法体中声明  
  成员变量 方法体外类体内声明
- 
  














