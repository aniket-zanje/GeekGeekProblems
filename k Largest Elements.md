## 01. k Largest Elements

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/k-largest-elements4206/1)

### Problem Description

**Task:** Given an array arr[] of positive integers and an integer k, Your task is to return k largest elements in decreasing order. Examples:Input: arr[] = [12, 5, 787, 1, 23], k = 2

#### Examples

##### Example 1

- **Output:**
```text
[787, 23]
```
- **Explanation:** 1st largest element in the array is 787 and second largest is 23.

##### Example 2

- **Input:**
```text
arr[] = [1, 23, 12, 9, 30, 2, 50], k = 3
```
- **Output:**
```text
[23]
```
- **Explanation:** 1st Largest element in the array is 23.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** k+(n-k)*logkAuxiliary Space: k+(n-k)*logk
- **Expected Auxiliary Space Complexity:** k+(n-k)*logk

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-03 12:04:01
- **Status:** Correct
- **Marks:** 0

```cpp
class Solution {
public:
    vector<int> kLargest(vector<int>& arr, int k) {

        sort(arr.begin(), arr.end(), greater<int>());

        vector<int> v(arr.begin(), arr.begin() + k);

        return v;
    }
};
```

*Generated on: 10/3/2026, 12:04:50 PM*