## 01. Sum Except First and Last

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/max-length-chain/1)

### Problem Description

**Task:** You are given an array arr of numbers. Return the sum of all the elements except the first and last elements.

#### Examples

##### Example 1

- **Input:**
```text
arr[] = [5, 24, 39, 60, 15, 28, 27, 40, 50, 90]
```
- **Output:**
```text
283
```
- **Explanation:** The sum of all the elements except the first and last element is 283.

##### Example 2

- **Input:**
```text
arr[] = [5, 10, 1, 11]
```
- **Output:**
```text
11
```
- **Explanation:** The sum of all the elements except the first and last element is 11.

##### Example 3

- **Input:**
```text
arr[] = [5, 10]
```
- **Output:**
```text
0
```
- **Explanation:** The sum of all the elements except the first and last element is 0.

#### Constraints

- **1.** `2 <= arr.size() <= 10⁵`
- **2.** `2 <= arr[i] <= 10⁵^`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-02 12:25:09
- **Status:** Correct
- **Marks:** 1

```cpp
class Solution {
  public:
    int sumExceptFirstLast(vector<int>& arr) {
        // code here
        int sum = 0;
        for(int i : arr){
            sum += i;
        }
        return sum - arr[0] - arr[arr.size()-1];
    }
};
```

*Generated on: 10/2/2026, 12:42:35 PM*