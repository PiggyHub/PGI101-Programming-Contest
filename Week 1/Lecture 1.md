# Lecture 1 Programming Basic
## Introduction to Luogu
OJ（Online Judge）是指在线判题系统，将代码提交给OJ后， OJ会在线检测程序源代码的正确性，并返回结果。

IDE（Integrated Development Environment）是一种辅助程序开发人员开发软件的应用软件，在开发工具内部就可以辅助编写源代码文本、并编译打包成为可用的程序。

常见状态术语

AC （Accepted = 答案正确）

WA （WrongAnswer = 答案错误）

TLE （Time Limit Exceeded = 运⾏超时）

CE （Compile Error =编译错误）

RE （Runtime Error = 运⾏时出错）

MLE （Memory Limit Exceeded = 内存超限）

PE （Presentation Error = 格式错误）
## 1.1 Sequential Structure
### Example 1 Welecome to Piggy Island
```c++
#include<iostream> //头文件
using namespace std; //命名空间
int main(){
    cout<< "Welecome to Piggy Island"<<endl; //输出语句并换行
    cout<< 2022 << "/" << 4 << "/" <<10;
    return 0;
    /*
    忘记Return 0可能会造成运行错误（RE）
    */
}
```
输出结果
```
Welecome to Piggy Island
2022/4/10
```
### Example 2 Variable & Calculator
```c++
//基本运算符：+ - * /
#include<iostream> 
#include<cmath> //数学函数库
using namespace std;
int main(){
    int balance = 100;
    balance += 10; //balance = balance + 10
    cout<< balance <<endl;
    
    cout<< 1314/520; //整数除法得整数
    cout<< 1314.0/520; //浮点数除法得浮点数
    cout<< pow(3,2); // 幂函数
    cout<< sqrt(9); //开平方根
    cout<< abs(-10); //绝对值
    cout<< ceil(2.1); //向上取整
    cout<< floor(2.9); //向下取整
    cout<< round(3.5); //四舍五入
    
    return 0;
}
```
输出结果
```
10
2
2.52692
9
3
10
3
2
4
```
### Example 3 Data Type & I/O 
``` c++
#include<iostream> 
#include<cstdio>
using namespace std;
int main(){
    int ans1;
    char ans2;
    ans1 = 'M' - 'A' + 1; //ASCII
    ans2 = 'A' + 1
    cout<< ans1 << endl;
    cout<< ans1 << endl;
    cout<< int('A') <<endl<<endl; //强制类型转换
    
    int x; cin>> x; cout<< x << endl; //基本输入输出
    char a,b,c,d,str[10]={"Hello"};
    scanf("%c%c%c.%c", &a, &b, &c, &d); //123.4
    printf("%c.%c%c%c\n", &d, &c, &b, &a);
    printf("%02d %.2f %s", 2, 3.14159, str);
    return 0;;    
}
```
输出结果
```
13
B
65

4.321
02 3.14 Hello
```





















