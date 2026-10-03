## 01. class Solution { public static int maxProduct(int[] arr) { int max1 = -1; int max2 = -1;

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/maximum-product-of-two-numbers2730/1)

### Problem Description

**Task:** Given an array arr[] of non-negative integers, find the maximum product of any two elements present in the array.

#### Examples

##### Example 1

- **Input:**
```text
arr[] = [1, 4, 3, 6, 7, 0]
```
- **Output:**
```text
42Explanation: 6 and 7 have the maximum product.
```

##### Example 2

- **Input:**
```text
arr[] = [1, 100, 42, 4, 23]
```
- **Output:**
```text
4200Explanation: 42 and 100 have the maximum product.
```

#### Constraints

- **1.** `2 ≤ arr.size ≤ 10⁷⁰ ≤ arr[i] ≤ 10⁹`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-03 11:48:55
- **Status:** Correct
- **Marks:** 1

```cpp
class Solution {
  public:
    int maxProduct(vector<int>& arr) {
        // code here
        int m1 = INT_MIN, m2 = INT_MIN;
        for(int i : arr){
            if(m1 < i){
                m2 = m1;
                m1 = i;
            }
            else if(m2<i && i <= m1){
                m2 = i;
            }
        }
        return m1*m2;
    }
};
```

*Generated on: 10/3/2026, 11:49:57 AM*