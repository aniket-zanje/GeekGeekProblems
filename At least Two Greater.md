## 01. At least Two Greater

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/at-least-two-greater-elements4625/1)

### Problem Description

**Task:** Given an array arr of distinct elements, the task is to return an array of elements that have at least two greater elements.Examples:Input: arr[] = [2, 8, 7, 1, 5]

#### Examples

##### Example 1

- **Output:**
```text
[1, 2, 5]
```
- **Explanation:** Here we return an array contains 1, 2, 5 and we leave two greatest elements 7 & 8. Input: arr[] = [7, -2, 3, 4, 9, -1]Output: [-2, -1, 3, 4]Explanation: Here we return an array contains -2 , -1, 3, 4 and we leave two greatest elements 7 & 9.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n log n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-03 12:43:38
- **Status:** Correct
- **Marks:** 1

```cpp
class Solution {
  public:
    vector<int> findElements(vector<int> arr) {
        // code here
       sort(arr.begin(), arr.end());
        vector<int> v(arr.begin(),arr.end()-2);
        return v;
    }
};
```

*Generated on: 10/3/2026, 12:44:10 PM*