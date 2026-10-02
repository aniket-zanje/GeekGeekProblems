## 01. Largest in Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/largest-element-in-array4009/1)

### Problem Description

**Task:** Given an array arr[]. The task is to find the largest element and return it.Examples:Input: arr[] = [1, 8, 7, 56, 90]

#### Examples

##### Example 1

- **Output:**
```text
10
```
- **Explanation:** There is only one element which is the largest.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-02 21:49:05
- **Status:** Correct
- **Marks:** 1

```cpp
class Solution {
  public:
    int largest(vector<int> &arr) {
        // code here
        int largest=INT_MIN;
        for(int i=0; i<arr.size();i++){
            largest = max(largest,arr[i]);
        }
        return largest;
    }
};
```

*Generated on: 10/2/2026, 9:49:40 PM*