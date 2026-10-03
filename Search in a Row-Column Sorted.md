## 01. Search in a Row-Column Sorted

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/search-in-a-matrix17201720/1)

### Problem Description

**Task:** Given a 2D integer matrix mat[][] of size n x m, where every row and column is sorted in increasing order and a number x, return true if the element x is present in the matrix. Otherwise, return false.Examples:Input: mat[][] = [[3, 30, 38], [20, 52, 54], [35, 60, 69]], x = 62

#### Examples

##### Example 1

- **Output:**
```text
true
```
- **Explanation:** 3 is present in the matrix.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n + m)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-03 12:22:42
- **Status:** Correct
- **Marks:** 2

```cpp
class Solution {
  public:
    bool matSearch(vector<vector<int>> &arr, int x) {
        // code here
        
        
        for(vector<int> i : arr){
                int mid;
                int low = 0;
                int high = i.size()-1;
                bool found = false;

                while(low<=high){

                    mid = (low + high) / 2;
                    if(i[mid] == x){
                       return true;
                    }

                    if(i[mid] > x){
                        high = mid - 1;
                    }else{
                        low = mid + 1;
                    }
                }
        }
        return false;
    }
};
```

*Generated on: 10/3/2026, 12:23:23 PM*