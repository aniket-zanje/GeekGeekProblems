## 01. Min and Max in Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/find-minimum-and-maximum-element-in-an-array4428/1)

### Problem Description

**Task:** Given an array arr[]. Your task is to find the minimum and maximum elements in the array.Examples:Input: arr[] = [1, 4, 3, 5, 8, 6]

#### Examples

##### Example 1

- **Output:**
```text
[3, 15]Explanation: minimum and maximum element of array are 3 and 15.
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (3)

#### Solution 1 (C++)

- **Submitted:** 2026-10-02 21:59:19
- **Status:** Correct
- **Marks:** 0

```cpp
class Solution {
  public:
    vector<int> getMinMax(vector<int> &arr) {
        // code here
        int mi = INT_MAX;
        int ma = INT_MIN;
        
        vector<int> result;
        for(int i : arr){
            mi = min(mi,i);
            ma = max(ma,i);
        }
        
        result.push_back(mi);
        result.push_back(ma);
        return result;
    }
};
```

#### Solution 2 (C++)

- **Submitted:** 2026-10-02 21:58:50
- **Status:** Correct
- **Marks:** 0

```cpp
class Solution {
  public:
    vector<int> getMinMax(vector<int> &arr) {
        // code here
        int mi = INT_MAX;
        int ma = INT_MIN;
        
        vector<int> result;
        for(int i : arr){
            mi = min(mi,i);
            ma = max(ma,i);
        }
        
        result.push_back(mi);
        result.push_back(ma);
        return result;
    }
};
```

#### Solution 3 (C++)

- **Submitted:** 2026-10-02 21:57:04
- **Status:** Correct
- **Marks:** 1

```cpp
class Solution {
  public:
    vector<int> getMinMax(vector<int> &arr) {
        // code here
        int mi = INT_MAX;
        int ma = INT_MIN;
        
        vector<int> result;
        for(int i : arr){
            mi = min(mi,i);
            ma = max(ma,i);
        }
        
        result.push_back(mi);
        result.push_back(ma);
        return result;
    }
};
```

*Generated on: 10/2/2026, 9:59:56 PM*