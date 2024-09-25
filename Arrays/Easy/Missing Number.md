## Intiution
Given an array **arr** of size **n−1** that contains distinct integers in the range of 1 to n (inclusive), find the missing element. The array is a permutation of size n with one element missing. Return the missing element.

**Examples:**

**Input:** n = 5, arr[] = [1,2,3,5]
**Output:** 4
**Explanation :** All the numbers from 1 to 5 are present except 4.

**Input:** n = 2, arr[] = [1]
**Output:** 2
**Explanation :** All the numbers from 1 to 2 are present except 2.

**Expected Time Complexity:** O(n)  
**Expected Auxiliary Space:** O(1)

**Constraints:**  
1 ≤ n ≤ 105  
1 ≤ arr[i] ≤ n

### Solution
```java
class Solution {

    // Note that the size of the array is n-1
    int missingNumber(int n, int arr[]) {

        // Your Code Here
        
        Arrays.sort(arr);
        
        if(arr[0] == 1 && n == 1) {
            return 2;
        }
        
        if(arr[0] == 2 && n == 1) {
            return 1;
        }
        
        int k = 1;
        for(int i=0; i<arr.length; i++) {
            if(arr[i] != k) return k;
            k++;
        }
        
        return k;
    }
}
```