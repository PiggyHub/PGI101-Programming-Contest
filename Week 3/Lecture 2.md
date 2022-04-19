# Lecture 2 Introduction to Algorithm
## Example 1 Imitation
```
Follow your heart.
```
### Exercise P1601, P2670
## Example 2 Sort
```c++
#include<iostream>
#include<algorithm>
using namespace std;

bool cmp(int a, int b){
	return a>b;
}

int main(){
	int a[10]={1,5,2,3,4};
	sort(a,a+5,cmp);
	for(int i=0; i<=4; i++) cout<<a[i]<<" ";
	return 0;
}
```
Output
```
5 4 3 2 1
```
### Exercise P1059, P1093

## Example 3 Greedy
```
Make the locally optimal choice at each stage
```
### Exercise P1223, P1090

## Example 4 Recursion & Recurrence
```
Recursion: A function which calls itself.
Recurrence: An equation that describes a function in terms of its value on smaller inputs
```
### Exercise P1059, P1093








