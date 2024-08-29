
### Link: [1752. Check if Array Is Sorted and Rotated](https://leetcode.com/problems/check-if-array-is-sorted-and-rotated/)
## Problem Statement
Given an array `nums`, return `true` _if the array was originally sorted in non-decreasing order, then rotated **some** number of positions (including zero)_. Otherwise, return `false`.

There may be **duplicates** in the original array.

**Note:** An array `A` rotated by `x` positions results in an array `B` of the same length such that `A[i] == B[(i+x) % A.length]`, where `%` is the modulo operation.

## Approach
- Iterate from the first(1) index to last and check
- Whether the current element is smaller than the previous element then we increase our break count. 
- And after traversing the array we will check some conditions 
- If the break count will be equal to 0 if yes then return true.
- Else if the break count is equal to 1 and also the last element is smaller than or equal to the first element then also we return true
- Else return false.

## Code
```c++
// Online C++ compiler to run C++ program online
#include <iostream>
#include <vector>

using namespace std;

bool check(vector<int> &nums) {
    int breakCount = 0;
    for(int i=1; i<nums.size(); i++) {

        if(nums[i] < nums[i-1]) breakCount++;

    }

    if(breakCount == 0) return true;
    else if(breakCount == 1 && nums[nums.size()-1] <= nums[0]) return true;
    else return false;
}

int main() {
    int n; 
    
    cout<<"Enter the size of the array"<<endl;
    cin>> n;
    
    vector<int> nums(n);
    
    for(int i=0; i<n; i++) {
        cin>>nums[i];
    }
    
    bool ans = check(nums);
  
    cout<<boolalpha<<ans<<endl;
}

```