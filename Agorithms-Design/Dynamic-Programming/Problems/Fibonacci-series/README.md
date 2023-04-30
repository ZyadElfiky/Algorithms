# Fibonacci Series
## this is an implementation of dynamic programming approach using memoization to find the Fibonacci series up to a given number.
```cpp
#include <iostream>
#include<bits/stdc++.h>
using namespace std;
int N=1000;
vector<int>F(10,-1);

int fib(int N){

    if(N<=1)return F[N]=1;
    if(F[N]!=-1)
        return F[N];
    else
        return F[N]=fib(N-1)+fib(N-2);

}
int main() {

    fib(5);
    for(int i=0;i<F.size();i++)cout<<F[i]<<endl;

    return 0;
}
```
## Solution Explanation
- The algorithm first initializes an integer N to 1000 and creates a vector F of size 10, where each element is initialized to -1. The vector F is used to store the intermediate results of the Fibonacci series calculated so far.

- The function "fib" takes an integer parameter N and returns the value of the Nth element in the Fibonacci series. If N is less than or equal to 1, then the function directly returns 1 as per the base case for the Fibonacci series. Otherwise, it checks whether the value of the Nth element is already present in the vector F. If yes, then it directly returns that value from the vector without calculating it again. If not, then it recursively calls the "fib" function for (N-1)th and (N-2)th elements of the series and stores their sum in the vector F at the Nth index before returning the result.

- In the main function, the "fib" function is called with the argument 5 to calculate the first five numbers in the Fibonacci series, and then the vector F is printed to display the entire series up to the length of the vector.

## Solution Analyses
- the time complexity of this solution is O(N), which is much better than the traditional recursive approach of O(2^N). This improvement in time complexity is achieved by storing intermediate results in the vector F using memoization, which helps to avoid redundant calculations. The space complexity of this solution is also O(N), due to the use of the vector F to store the intermediate results.
