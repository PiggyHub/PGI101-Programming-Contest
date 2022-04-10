## 3. Branch Structure
### Example 4 if
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
