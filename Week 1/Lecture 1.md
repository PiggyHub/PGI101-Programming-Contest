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
### Exercise P1001, P5708, P5707
## 3. Branch Structure
### Example 4 if & switch
``` c++
#include<iostream>
using namespace std;
int main() {
  // 浅学 if 句 (if, else if, else)
  bool p1 = 1, p2 = 0;
  if ( p1 ^ p2 ) //两个性质刚好一个成立 
    cout << "异或" <<endl;
  else if (!p1 && !p2)a
    cout << "同时不成立"<<endl;
  else 
    cout << "其他情况";
  
  // 浅学 switch case 句
  int a = 2, b = 3;
  int m = a * b > 10 ? 66 : 88;  //三目运算符 (S1?S2:S3) 如果S1成立，则值为S2，否则值为S3
  switch (m) {
     case 1: case 66: cout << "6"; //多重case均为一种结果时
     case 88: cout << "8";
    }
}
```
输出结果
```
异或
8
```

## 4. Loop Structure
### Example 5 for & while & nested loop
``` c++
#include<iostream>
#include<algorithm> // 头文件

//与随机数有关的头文件
#include<ctime>
#include<cstdlib>

using namespace std;
int main() {

    //函数比较
    int a = 5,b = 10;
    int ans = max(a,b); //取ab间较大值
    int s = min(a,b);//取ab间较小值
    int temp;
    cout<<ans<<" "<<s<<endl;

    //随机数: 从a到b中产生一个随机数
    srand(time(0));
    int x = rand() % (a-b+1) +a;
    cout<<x<<endl;
    
    //for的嵌套循环
    for (int i = 0; i < 3; i++) {
        if(i ==1)
            continue; //跳过本次循环中未执行的语句
        for (temp = 0;;temp++){ // 不设终止条件
            if(temp == ans){ // 循环终止条件
                cout<<temp+i<<" ";
                break; //跳出该层循环
                              
            }    
        }
        
    }
    cout<<"\n";
    //while的循环
    while (temp--) // 先判断temp是否为0再减；若写成 --temp 则先将temp减1再判断是否为0
        cout<<"1 ";
    cout<<"\n";

    // 逗号表达式，没有循环体; x = x+1; ans = ans/2;
    for (int x = 0; x < 2; x+=1, ans/=2);
    cout<<ans<<endl;
    
    // do...while (先做后判断)
    do{
            ans *= 8;
        } while (ans < 30);
    cout<<ans;    
}
```
输出结果
```
10 5
6
10 12 
1 1 1 1 1 1 1 1 1 1 
2
128
```






















