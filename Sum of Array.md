## 01. Sum of Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/sum-all-array-elements/1)

### Problem Description

**Task:** Given an integer array arr[], return the sum of all elements of arr.Examples:Input: arr[] = [1, 2, 3, 4]

#### Examples

##### Example 1

- **Output:**
```text
10
```
- **Explanation:** 1 + 2 + 3 + 4 = 10.

##### Example 2

- **Input:**
```text
arr[] = [1, 3, 3]
```
- **Output:**
```text
7
```
- **Explanation:** 1 + 3 + 3 = 7.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-03 11:18:37
- **Status:** Correct
- **Marks:** 1

```cpp
class Solution {
  public:
    int arraySum(vector<int>& arr) {
        // code here
        int sum = 0;
        for(int i : arr){
            sum += i;
        }
        return sum;
    }
};
```

*Generated on: 10/3/2026, 11:19:19 AM*