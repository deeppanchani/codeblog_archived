# CP blog - Day 2
## Number of Problems Solved: 2/5

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
We have to move 1 from any given position to middle of the matrix. By simple permutations we know that to move a given number from one position to another given position in a matrix we have to find absolute differnce of their corrdinate and it will give the number of steps one need to take in that direction.

While taking input I am also searching for 1 so that I can get its corrdinate.(To reduce time)
### Related Topics:
### Code:
```c++
#include <iostream>
#include <cstdlib>

using namespace std;

int main(){
    int arr[5][5];
    int x,y;
    for(int i=0;i<5;i++){
        for(int j=0;j<5;j++){
            cin >> arr[i][j];
            if(arr[i][j]==1){
                x=i;
                y=j;
            }
        }
    }
    x = abs(x-2);
    y = abs(y-2);
    cout << x+y;
}
```
