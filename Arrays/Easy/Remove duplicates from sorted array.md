### Link: [26. Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)

## Problem Statement:
Given an integer array `nums` sorted in **non-decreasing order**, remove the duplicates [**in-place**](https://en.wikipedia.org/wiki/In-place_algorithm) such that each unique element appears only **once**. The **relative order** of the elements should be kept the **same**. Then return _the number of unique elements in_ `nums`.

Consider the number of unique elements of `nums` to be `k`, to get accepted, you need to do the following things:

- Change the array `nums` such that the first `k` elements of `nums` contain the unique elements in the order they were present in `nums` initially. The remaining elements of `nums` are not important as well as the size of `nums`.
- Return `k`.

## Approach:
- We initialize new index and traverse the whole array
- Check the condition that the current element is not equal to the previous element 
- We put the array of new index value to the previous repeated element and increase the new index.
- After traversing return the new index.

## Code
```cpp
class Solution {
public:
    int removeDuplicates(vector<int>& nums) {
        
        int k = 1;
        
        for(int i=1; i<nums.size(); i++) {

            if(nums[i] != nums[i-1]){
                nums[k] = nums[i];
                k++;
            }
            
        }

        return k;
    }
};
```