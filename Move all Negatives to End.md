## 01. Move all Negatives to End

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/move-all-negative-elements-to-end1813/1)

### Problem Description

**Task:** Given an unsorted array arr[ ] having both negative and positive integers. Place all negative elements at the end of the array without changing the order of positive elements and negative elements.Note: Don't return any array, just in-place on the array.Examples:Input : arr[] = [1, -1, 3, 2, -7, -5, 11, 6 ]

#### Examples

##### Example 1

- **Output:**
```text
[7, 9, 10, 11, -5, -3, -4, -1]
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-04 15:17:20
- **Status:** Correct
- **Marks:** 2

```cpp
class Solution {
  public:
    void segregateElements(vector<int>& arr) {
        // code here
        vector<int> p;
        vector<int> n;
        
        for(int i : arr){
            if(i>=0){
                p.push_back(i);
            }else{
                n.push_back(i);
            }
        }
        
        arr.clear();
        
        for(int i : p){
            arr.push_back(i);
        }
        for(int i : n){
            arr.push_back(i);
        }
        
    }
};
```

*Generated on: 10/4/2026, 3:20:11 PM*