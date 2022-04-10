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
  else if (!p1 && !p2)
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
