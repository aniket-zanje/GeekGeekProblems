## 01. Third Largest

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/third-largest-element/1)

### Problem Description

**Task:** Given an array, arr[] of positive integers. Find the third largest element in it. Return -1 if the third largest element is not found.Examples:Input: arr[] = [2, 4, 1, 3, 5]Output: 3Explanation: The third largest element in the array [2, 4, 1, 3, 5] is 3.Input: arr[] = [10, 2]Output: -1Explanation: There are less than three elements in the array, so the third largest element cannot be determined.Input: arr[] = [5, 5, 5]Output: 5Explanation: In the array [5, 5, 5], the third largest element can be considered 5, as there are no other distinct elements.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-02 13:18:25
- **Status:** Correct
- **Marks:** 2

```cpp
class Solution {
  public:
    int thirdLargest(vector<int> &arr) {
        // code here
        
        int l1,l2= INT_MIN,l3 = INT_MIN;
        if(arr.size()<3){
            return -1;
        }
        l1 = arr[0];
        for(int i = 1;i<arr.size();i++){
            
            if(l1<arr[i]){
                l3 = l2;
                l2 = l1;
                l1 = arr[i];
            }else if(l2 < arr[i]){
                l3 = l2;
                l2 = arr[i];
            }else if (l3 < arr[i]) {
                 l3 = arr[i];
             }
            
        }
        return l3;
    }
};
```

*Generated on: 10/2/2026, 1:19:03 PM*