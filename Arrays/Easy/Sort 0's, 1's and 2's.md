## Initution
Given an array arr containing only 0s, 1s, and 2s. Sort the array in ascending order.

Examples:

Input: arr[]= [0, 2, 1, 2, 0]
Output: 0 0 1 2 2
Explanation: 0s 1s and 2s are segregated into ascending order.
Input: arr[] = [0, 1, 0]
Output: 0 0 1
Explanation: 0s 1s and 2s are segregated into ascending order.
Expected Time Complexity: O(n)
Expected Auxiliary Space: O(1)

Constraints:
1 <= arr.size() <= 106
0 <= arr[i] <= 2

### Solution
```java
class Solution {
    // Function to sort an array of 0s, 1s, and 2s
    public void sort012(ArrayList<Integer> arr) {
        // code here
        
    //   Collections.sort(arr);
        
        int zeroCount = 0, oneCount = 0, twoCount = 0;
        int index = 0;
        
        for(int i=0; i<arr.size(); i++) {
            if(arr.get(i) == 0) zeroCount ++;
            if(arr.get(i) == 1) oneCount ++;
            if(arr.get(i) == 2) twoCount ++;
        }
        
        int i=1, j=1, k=1;
        while(i <= zeroCount) {
            arr.set(index, 0);
            index++;
            i++;
        }
        
        while(j <= oneCount) {
            arr.set(index, 1);
            index++;
            j++;
        }
        
        while(k <= twoCount) {
            arr.set(index, 2);
            index++;
            k++;
        }
    }
}
```