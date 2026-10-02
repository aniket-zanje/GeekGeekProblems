## 01. Alternate Positive Negative

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/array-of-alternate-ve-and-ve-nos1401/1)

### Problem Description

**Task:** Given an unsorted array arr containing both positive and negative numbers. Your task is to rearrange the array and convert it into an array of alternate positive and negative numbers without changing the relative order.Note: Resulting array should start with a positive integer (0 will also be considered as a positive integer). If any of the positive or negative integers are exhausted, then add the remaining integers in the answer as it is by maintaining the relative order.Examples:Input: arr[] = [9, 4, -2, -1, 5, 0, -5, -3, 2]

#### Examples

##### Example 1

- **Output:**
```text
[9, -2, 4, -1, 5, -5, 0, -3, 2]
```
- **Explanation:** The positive numbers are [9, 4, 5, 0, 2] and the negative integers are [-2, -1, -5, -3]. Since, we need to start with the positive integer first and then negative integer and so on (by maintaining the relative order as well), hence we will take 9 from the positive set of elements and then -2 after that 4 and then -1 and so on.

##### Example 2

- **Input:**
```text
arr[] = [-5, -2, 5, 2, 4, 7, 1, 8, 0, -8]
```
- **Output:**
```text
[9, -2, 5, -1, 5, -5, 0, -3, 2]
```
- **Explanation:** The positive numbers are [9, 5, 5, 0, 2] and the negative integers are [-2, -1, -5, -3]. Since, we need to start with the positive integer first and then negative integer and so on (by maintaining the relative order as well), hence we will take 9 from the positive set of elements and then -2 after that 5 and then -1 and so on.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-02 18:43:53
- **Status:** Correct
- **Marks:** 0

```cpp
class Solution {
public:
    void rearrange(vector<int> &arr) {

        vector<int> p;
        vector<int> n;

        
        for (int x : arr) {
            if (x >= 0)
                p.push_back(x);
            else
                n.push_back(x);
        }

        arr.clear();

        int pI = 0;
        int nI = 0;

        
        while (pI < p.size() && nI < n.size()) {

            if (arr.size() % 2 == 0)
                arr.push_back(p[pI++]);
            else
                arr.push_back(n[nI++]);
        }

      
        while (pI < p.size()) {
            arr.push_back(p[pI++]);
        }

        
        while (nI < n.size()) {
            arr.push_back(n[nI++]);
        }
    }
};
```

*Generated on: 10/2/2026, 6:44:20 PM*