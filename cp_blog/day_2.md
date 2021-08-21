# CP blog - Day 2
## Number of Problems Solved: 1/5

## Problem #1 Young Physicist
### [Problem Statement](http://codeforces.com/problemset/problem/69/A)
### Though Process:
Simple question we will check if the sum of forces in x,y,z direction are 0 or not.
### Related Topics:
Maths
### Code:
```c++
#include <iostream>
 
using namespace std;
 
int main(){
    int N=0;
    cin >> N;
    int arr[N][3];
    for(int i=0;i<N;i++){
        cin >> arr[i][0] >> arr[i][1] >> arr[i][2];
    }
    int x=0,y=0,z=0;
    for(int i=0;i<N;i++){
        x = x + arr[i][0] ;
        y = y + arr[i][1] ;
        z = z + arr[i][2] ;
    }
    
    if((0==x)&&(0==y)&&(0==z)){
        cout << "YES";
    }
    else{
        cout << "NO";
    }
}
```
## Problem #1 Beautiful Matrix
### [Problem Statement](http://codeforces.com/problemset/problem/263/A)
### Though Process:
### Related Topics:
### Code: