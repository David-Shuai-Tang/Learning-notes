# <center>Markdown学习笔记
## 1.标题
一级标题（# 一级标题）
二级标题（## 二级标题）
ps：注意空格

## 2.字体
正常体
*斜体*（ctrl+i）
**粗体**(ctrl+b)      
==高亮==
选中行（ctrl+l）
<center>居中</center>
<br/><br/><br/>
空行 
 
`<br/>`

## 3.引用
>这是一个引用
>>b站：https://www.bilibili.com/

## 4.链接
### 4.1
b站：<https://www.bilibili.com/>
### 4.2
[这里是b站](https://www.bilibili.com/)

## 5.图片
- 直接cv(无法按调整大小)
 ![alt text](image.png)
- 利用html语法`<img src = "图片路径" width = "50%">)`(可以调整图片大小)
  <img src = "image.png" width = "30%">

## 6.列表
+ 无序列表
  * 无序列表
    - 无序列表
1. 有序列表
   1. 有序列表

ps：控制层级使用tab键

## 7.分割线
这是一行测试语句

---
ps：空一行，再---。否则字体会放大

## 8.删除线
~~这是被删除的文字~~

## 9.代码块
### 9.1单行引用
`hello world`
### 9.2代码块引用
```cpp
#include <iostream>
int main(){
    printf("Hello world");
}
```
```java
public static void main(String[] args) {
        System.out.println("helloworld");
    }
```
ps：语法格式：(\```+语言名称+代码块+```)

## 10.表格
使用`|`分割不同单元格，使用`-`分割表头以及其他行。

+ `:-`左对齐
+ `-:`右对齐
+ `:-:`居中对齐

| 左对齐 | 居中对齐 | 右对齐 | 
| :--- | :---: | ---:|
| a | b | c |

## 11.注释
[^1]:第一条注释
[^2]:第二条注释
ps：注释自动排版到文末

## 12.特殊符号
对于markdown语法符号，前面+反斜杠`\`即可显示符号本身。

## 13.待办
- [ ] 第一条待办
- [x] 第二条待办

## 14.高级用法
数学公式、甘特图、流程图、时序图等等
<https://www.runoob.com/markdown/md-advance.html>


一个小小的修改

再一次小小的修改

这是main分支的源文件
