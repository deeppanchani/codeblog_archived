# CP blog - Day 1
## Number of Problems Solved: 1/5

### Problem #1 Chef and Spells
#### [Problem Statement](https://www.codechef.com/LTIME98C/problems/CHFSPL)
#### Though Process:

After reading the question we can tell that we need to use the spell with highes powers. For doing so we will use an array of size 3 and then apply sorting algorithm and then add the last two elements of the array as we will sort the array in accending order.

Took help of internet for using STL sort function.
#### Related Topics:
Array, Sorting
#### Code:
```c++
#include <iostream>
#include <bits/stdc++.h>
using namespace std;

int main() {
	int t;
	cin >> t;
	while(t--){
	    long arr[3];
	    for(int i=0;i<3;i++){
	        cin >> arr[i];
	    }
	    sort(arr, arr + 3);
	    
	    cout << arr[1]+arr[2] << "\n";
	}
	return 0;
}
```
#### Time Taken: 8 mins

### Problem #2
#### Problem Statement
#### Though Process:
#### Related Topics:
#### Code:

### Problem #3
#### Problem Statement:
#### Though Process:
#### Related Topics:
#### Code: