## 01. Rotate Array by One

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/cyclically-rotate-an-array-by-one2614/1)

### Problem Description

**Task:** Given an array arr[], rotate the array by one position in clockwise direction.Examples:Input: arr[] = [1, 2, 3, 4, 5]

#### Examples

##### Example 1

- **Output:**
```text
[3, 9, 8, 7, 6, 4, 2, 1]Explanation: After rotating clock-wise 3 comes in first position.
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-02 22:07:23
- **Status:** Correct
- **Marks:** 0

```cpp
class Solution {
  public:
    void rotate(vector<int> &arr) {
        // code here
        int n = arr.size();
        int last = arr[n-1];
        
        for(int i = n-1 ;i>0; i--){
            arr[i] = arr[i-1];
        }
        arr[0] = last;
    }
};
```

*Generated on: 10/2/2026, 10:09:19 PM*