# Lecture 1 Programming Basic (Full)
## Example 1 Branch Structure
逻辑运算符：&& || ! ^（异或，两个条件恰好一个成立）

```c++
#include<iostream> 
using namespace std;
int main(){
    int a=10;
    if(a > 0){
        cout<<"a > 0"<<endl;
    } else{
        cout<<"a <= 0"<<endl;
    }
    a > 0 ? a = 1 : a = -1;
    cout<<a;
    return 0;
}
```

Result

```
a > 0
1
```
### Exercise P1909, P1055
## Example 2 Loop Structure
```c++
#include<iostream> 
using namespace std;
int main(){
    for(int i=1; i<=10; i++){
        cout<< i <<" ";
    }

    cout<<endl;

    int i=10;
    while(i>=1){
        cout<< i <<" ";
        i--;
    }

    // break, continue
    
    return 0;
}
```
Result
```
1 2 3 4 5 6 7 8 9 10 
10 9 8 7 6 5 4 3 2 1 
```

### Exercise P2669, P5723
## Example 3 Array 
```c++
#include<iostream> 
using namespace std;
int main(){
    int a[100]={0};
    
    for(int i=1; i<=5; i++){
        cin>>a[i];
    }

    for(int i=1; i<=10; i++){
        cout<<a[i]<<" ";
    }

    return 0;
}
```
Input
```
1 2 3 4 5
```
Output
```
1 2 3 4 5 0 0 0 0 0 
```
### Exercise P1428, P2550
## Example 4 String
```c++
#include<iostream> 
#include<string>
using namespace std;
int main(){
    string s; getline(cin, s);
    cout<< s[1]<<endl;
    cout<< s.append("!") <<endl; //拓展字符串
    cout<< s.length() <<endl; //增加字符串长度
    cout<< s.substr(2,2) <<endl; //截取从第2个位置，长度为2的字符串
    cout<< s.insert(3,"?") <<endl; //在第三个字符前，插入字符串
    cout<< (int)s.find("lo",0) <<endl; //返回从第0个位置开始，第一次出现该字符串位置，未出现则为-1
    return 0;
}
```
Input
```
Hello
```
Output
```
e
Hello World!
12
ll
Hel?lo World!
4
```
### Exercise P5733, P1308
## Example 5 Function & Struct





























