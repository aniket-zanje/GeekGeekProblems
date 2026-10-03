## 01. Binary Search

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/who-will-win-1587115621/1)

### Problem Description

**Task:** Given an array arr[], sorted in ascending order and an integer k. Return true if k is present in the array, otherwise, false.Examples:Input: arr[] = [1, 2, 3, 4, 6], k = 6

#### Examples

##### Example 1

- **Output:**
```text
false1 ≤ arr[i] ≤ 10⁶
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-03 12:15:55
- **Status:** Correct
- **Marks:** 1

```cpp
class Solution {
  public:
    bool binarySearch(vector<int>& arr, int k) {
        // code here
        
        int mid;
        int low = 0;
        int high = arr.size()-1;
        bool found = false;
        
        while(low<=high){
            
            mid = (low + high) / 2;
            if(arr[mid] == k){
                found = true;
                break;
            }
            
            if(arr[mid] > k){
                high = mid - 1;
            }else{
                low = mid + 1;
            }
        }
        
        return found;
    }
};
```

*Generated on: 10/3/2026, 12:17:11 PM*