## 01. First and Second Smallests

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/find-the-smallest-and-second-smallest-element-in-an-array3226/1)

### Problem Description

**Task:** Given an array, arr[] of integers, your task is to return the smallest and second smallest element in the array. If the smallest and second smallest do not exist, return -1.Examples:Input: arr[] = [2, 4, 3, 5, 6]

#### Examples

##### Example 1

- **Output:**
```text
[-1]
```
- **Explanation:** Only element is 1 which is smallest, so there is no second smallest element.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-02 22:28:31
- **Status:** Correct
- **Marks:** 2

```cpp
class Solution {
public:
    vector<int> minAnd2ndMin(vector<int> &arr) {

        int sm1 = INT_MAX;
        int sm2 = INT_MAX;

        for (int i : arr) {

            if (i < sm1) {
                sm2 = sm1;
                sm1 = i;
            }
            else if (i > sm1 && i < sm2) {
                sm2 = i;
            }
        }

        if (sm2 == INT_MAX) {
            return {-1};
        }

        return {sm1, sm2};
    }
};
```

*Generated on: 10/2/2026, 10:30:07 PM*