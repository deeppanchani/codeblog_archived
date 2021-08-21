# CP blog - Day 1
## Number of Problems Solved: 2/5

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
#### [Problem Statement](https://www.codechef.com/LTIME98C/problems/REDALERT)
#### Though Process:
We will use a variable **temp** to store the city water level. We would have a loop for N times to take input of rainfall data of N days, we have an variable D which is to be reduced from **temp** if we dont have rainfall and if the outpur of this is negative we would return 0. Finally we have H the max amount of water level, So we will check if **temp**>H if so then we would break out of the loop and print YES. Else we would print NO. We can also use a flag variable to chech how many times the **temp** > H.
#### Related Topics:
#### Code:
```c++
#include <iostream>
#include <bits/stdc++.h>
using namespace std;

int main() {
	int t;
	cin >> t;
	while(t--){
	    int N,H,D;
	    int temp=0,x;
	    cin >> N >> D >> H;
	    for(int i=0;i<N;i++){
	        if(temp>H){
	            cout << "YES\n";
	            break;
	        }
            cin >> x;
            if(x>0){
                temp = temp +x;
            }
            else if (0==x){
                if(temp>D){
                    temp = temp -D;
                }
                else 
                    temp = 0;
            }
	    }
	    cout<<"NO\n";
	}
	return 0;
}
// wrong out puts all came out no
```
```c++
#include <iostream>
#include <bits/stdc++.h>
using namespace std;

int main() {
	int t;
	cin >> t;
	while(t--){
	    int N,H,D;
	    int temp=0,x,y=0;
	    cin >> N >> D >> H;
	    for(int i=0;i<N;i++){
            cin >> x;
            if(x>0){
                temp = temp +x;
            }
            else if (0==x){
                if(temp>D){
                    temp = temp -D;
                }
                else 
                    temp = 0;
            }
            if(H<temp){
                y++;
            }
	    }
	    
	    if(y==1){
	        cout << "YES\n";
	    }
	    else
	        cout<<"NO\n";
	}
	return 0;
}
// again a silly mistake
```
In above code I am checking for y==1 instead of y!=0.
```c++
#include <iostream>
#include <bits/stdc++.h>
using namespace std;

int main() {
	int t;
	cin >> t;
	while(t--){
	    int N,H,D;
	    int temp=0,x,y=0;
	    cin >> N >> D >> H;
	    for(int i=0;i<N;i++){
            cin >> x;
            if(x>0){
                temp = temp +x;
            }
            else if (0==x){
                if(temp>D){
                    temp = temp -D;
                }
                else 
                    temp = 0;
            }
            if(H<temp){
                y++;
            }
	    }
	    
	    if(y!=0){
	        cout << "YES\n";
	    }
	    else
	        cout<<"NO\n";
	}
	return 0;
}
```
#### Time Taken: 20min

### Problem #3 Beautiful Pairs 
#### [Problem Statement](https://www.codechef.com/LTIME98C/problems/BUTYPAIR)
#### Though Process:
I had some hard time understanding the question but the question was simple. It can be solved easyly once we get all the data regarding the repetation and total number of number presents.
So we will know the total number of numbers from the input now we have to find number of duplicates.
#### Related Topics:
#### Code:
```c++
#include <iostream>
#include <bits/stdc++.h>
using namespace std;

int main() {
	int t;
	cin >> t;
	while(t--){
	    int N;
	    cin >> N;
	    
	    long arr[N];
	    
	    for(int i=0;i<N;i++){
	        cin >> arr[i];
	    }
	    
	    int count=0;
	    
	    for(int i=0; i<N; i++)
        {
            for(int j=i+1; j<N; j++)
            {
                if(arr[i] == arr[j])
                {
                    count++;
                    break;                
                }
            }
        }
        if(count>0){
            count++;
        }
        int ans =(N*(N-1));
        cout << ans-count << endl;
	}
	return 0;
}

```

Using above code I am getting TLE. So I need a better storage option than array. One thing I can think of is Hash Table or Maps. I Haven't Implemented them in C++. So will attemt this after learning more.
#### Time Taken: 15min(TBC)