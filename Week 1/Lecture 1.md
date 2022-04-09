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
## 1.1 Basic I/O
### Example 1 欢迎来到猪猪岛
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
