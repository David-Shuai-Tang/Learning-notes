# <center>Java学习笔记

## 一、Java 特性
### 1. java版本
java se（标准版）：桌面应用开发
java me（移动版）：移动应用开发
Java ee（企业版）：企业应用开发，web应用开发。
>JavaEE并不是一个软件产品，它更多的是一种软件架构和设计思想。我们可以把JavaEE看作是在JavaSE的基础上，开发的一系列基于服务器的组件、API标准和通用架构。
>>JavaEE最核心的组件就是基于Servlet标准的Web服务器，开发者编写的应用程序是基于Servlet API并运行在Web服务器内部的

- JDK：Java Development Kit
- JRE：Java Runtime Environment
  ![alt text](image.png)





### 2. java跨平台性
java的跨平台性，是由于每个os都装有不同版本的java虚拟机（jvm），从而做到运行只依赖于java虚拟机，而与os无关。（一处编译，处处运行）

### 3. 环境变量

Path环境变量是让系统程序的路径，方便程序员在命令行窗口的 %任意目录% 下启动程序；

### 4. 工程嵌套 
java中的工程嵌套：
project(项目) → module(模块) → package(包) → class(类)

即：最终在每一个类文件中编写代码。
ps：Java中最基本的组成单位为类



### 5.Tips

1. **src:** 在 Java 项目中，src 是 source 的缩写，表示源代码文件夹。这个文件夹主要用于存放项目的源文件，即以 .java 为后缀的文件和一些配置文件
   > (src 文件夹将源代码与其他类型的文件（如模板文件、Web 文件等）区分开来。这有助于保持项目结构的清晰和整洁)


2. 




---

## 二、Java 语法
### 1.程序基础
#### 1.1 基础结构
Java是面向对象的语言，一个程序的**基本单位就是class**，class是关键字，这里定义的class名字就是Hello

类名要求：
- 类名必须以英文字母开头，后接字母，数字和下划线的组合
- 习惯以**大写字母开头**

```public class Hello {
    public static void main(String[] args) {
        // 向屏幕输出文本:
        System.out.println("Hello, world!");
        /* 多行注释开始
        注释内容
        注释结束 */
    }
} // class定义结束 
``` 

> 注意到**public是访问修饰符**，表示该class是公开的。
不写public，也能正确编译，但是这个类将无法从命令行执行。
在class内部，可以定义若干方法（method）：
```
public class Hello {
    public static void main(String[] args) { // 方法名是main
        // 方法代码...
    } // 方法定义结束
}
```
>这里的**方法名是main**，返回值是void，表示没有任何返回值。
我们注意到public除了可以修饰class外，**也可以修饰方法**。而关键字**static是另一个修饰符，它表示静态方法**
>>ps：Java入口程序规定的方法必须是静态方法，方法名必须为main，括号内的参数必须是String数组

方法名也有命名规则，命名和class一样，但是**首字母小写**


```
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello, world!"); // 语句
    }
}
```
> 在方法内部，语句才是真正的执行代码。Java的每一行语句必须**以分号结束**

#### 1.2 数据类型
Java定义了以下几种**基本数据**类型：
- 整数类型：byte，short，int，long
- 浮点数类型：float，double
- 字符类型：char
- 布尔类型：boolean
byte恰好就是一个字节，而long和double需要8个字节

**常量：**
定义变量的时候，如果加上**final**修饰符，这个变量就变成了常量：
```
final double PI = 3.14; // PI是一个常量
double r = 5.0;
double area = PI * r * r;
PI = 300; // compile error!
```
常量在定义时进行初始化后就**不可再次赋值**，再次赋值会导致编译错误。
为了和变量区分开来，根据习惯，常量名通常**全部大写**

定义变量时，要遵循作用域最小化原则，尽量将变量定义在**尽可能小的作用域**，并且，**不要重复使用**变量名


#### 1.2 运算
**运算优先级**
在Java的计算表达式中，运算优先级从高到低依次是：
- ()
- ! ~ ++ --
- \* / %
- \+ -
- << >> >>>
- &
- |
- += -= *= /=

**三元运算符**
Java还提供一个三元运算符`b ? x : y`，它根据第一个布尔表达式的结果，分别返回后续两个表达式之一的计算结果
三元运算`b ? x : y`会首先计算b，如果b为true，则只计算x，否则，只计算y。此外，x和y的类型必须相同，因为返回值不是boolean，而是x和y之一

**字符串连接**
Java的编译器对字符串做了特殊照顾，可以使用+连接任意字符串和其他数据类型，这样极大地方便了字符串的处理。如果用+连接字符串和其他数据类型，会将其他数据类型先自动转型为字符串，再连接。

字符串可以用"""..."""表示**多行字符串**（Text Blocks）


Java的字符串除了是一个**引用类型**外，还有个重要特点，就是字符串**不可变**。
> ps：引用数据类型是Java中两大数据类型之一，区别于基本数据类型。引用数据类型包括类、接口、数组、枚举、注解和字符串等







---
## 三、web 开发
web开发通常指开发**服务器端**的web应用




---
## 四、Spring
>Spring是一个支持快速开发Java EE应用程序的**框架**，它提供了一系列底层容器和基础设施，并可以和大量常用的开源框架无缝集成

### 4.1 Springmvc

> Spring MVC 是 Spring 框架中专门处理Web请求的**模块**，采用经典的 MVC（Model-View-Controller）架构：
> - Controller：处理用户请求，返回逻辑结果
> - View：渲染界面（如JSP、Thymeleaf模板）
> - Model：传递数据给视图




---
## 五、spring boot
> Spring Boot是一个**基于Spring**的套件，它帮我们预组装了Spring的一系列组件，以便以**尽可能少的代码和配置**来开发基于Spring的Java应用程序。核心理念是“约定大于配置”，通过以下特性提升效率：
> - 内嵌 Tomcat/Jetty 服务器（无需手动部署）
> - 自动配置依赖（如添加 spring-boot-starter-web 一键配置Web开发环境）
> - 提供 Actuator 监控模块



---
## 六、spring cloud
> Spring Cloud顾名思义是跟云相关的，云程序实际上就是指分布式应用程序，所以Spring Cloud就是为了让分布式应用程序编写更方便，更容易而提供的一组基础设施，它的核心是Spring框架，利用Spring Boot的自动配置，力图实现最简化的**分布式应用程序开发**。




---

## 七、Javascript
> 一种**脚本语言**，主要在浏览器中运行，负责网页的动态交互（如表单验证、动画效果）。随着 Node.js 的出现，也可以在服务端运行。java与JavaScript二者名字相似但无血缘关系，JavaScript 更多**用于前端**（尽管Node.js能在服务端运行），而 Java 是**编译型语言**。


---


## 八、资源网址
1.java学习博客：https://liaoxuefeng.com/books/java/introduction/index.html
<br/>
2.Idea官方中文文档：https://intellijidea.com.cn/help/idea/getting-started.html 
<br/>
3.
