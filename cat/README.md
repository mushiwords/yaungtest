hrllo ! its cst !
hello ! it's cat !
it's the right answer
Sorry, user oracle is not allowed to execute'/usr/bin/passwd' as root 


/*
*程序名称：CppPriavteType
*程序描述：C++自定义数据类型
*编写时间：20121219
*/
#include <iostream>
using namespace std;

/**************************************************************************************
*创建新的数据类型可以使用类、联合和结构，使用关键字class、union和struts
*结构：一种数据类型、它 定义了一种特殊类型的对象
* 1.使用关键字struct；
* 2.必需以分号(;) 结尾 ； 
* 3.结构中数据成员可以是任何类型，但不能是所定义的结构类型(可以使用所定义结构类型的指针)；
* 4.结构类型的定义一般放到头文件中
* 5.没有初始值的成员会被初始化为0
*
*联合：一种数据类型，允许使用同一个内存块在不同时间存储不同类型的值。
* 1.联合实际上是一种结构，只是所有的成员都占用相同的内存空间
* 2.联合的声明使用关键字union,跟结构的语法类似
*
**************************************************************************************/

struct Client{
 char client_name[20];
 char mobile_phone[12];
 char address[100]; 
 //定义成员函数
 int getClientInfo(){
  cout << client_name << ":" << mobile_phone << ":" << address;
 }
}; //定义结构必需以分号(;) 结尾
//可以在定义结构时定义变量
//}c01,c02;
 
int main(){
 //定义结构变量
 Client c01;      //对象
 Client* pc02;  //指针
 Client c03[10];  //数组
 struct Client c04;  //可以指定struct
 //也可以使用如下方式定义
 //Client c01,*pc02,c03[10];

 //1.定义时初始化
 Client c05 = {
  "张三",
  "18636663666",
  "中国11" 
 };
 //2.定义数组并初始化
 Client c06[] = {
  //注意里面用花括号
  {
   "张三",
   "18636663666",
   "中国" 
  },  //注意此处的逗号
  {
   "李四",
   "18636663665",
   "中国" 
  }
   
 };
 
 //访问结构中的成员，使用成员访问运算符(英文句点.) 
 cout << c05.client_name << "----" << c05.mobile_phone;
 cout << "\n";
 cout << c05.getClientInfo();
 cout << "\n"; 
}
分享到：
上一篇：C++程序文件和预处理器
下一篇：C++类


