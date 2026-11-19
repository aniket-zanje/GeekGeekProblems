## 01. Peak in Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/peak-element/1)

### Problem Description

**Task:** Given an array arr[] where no two adjacent elements are same, find the index of a peak element. An element is considered to be a peak if it is greater than its adjacent elements (if they exist). If there are multiple peak elements, Return index of any one of them. The output will be "true" if the index returned by your function is correct; otherwise, it will be "false".Note: Consider the element before the first element and the element after the last element to be negative infinity.Examples :Input: arr = [1, 2, 4, 5, 7, 8, 3]

#### Examples

##### Example 1

- **Output:**
```text
true
```
- **Explanation:** Element 20 at index 1 is a peak since 10 < 20 > 15. Index 5 (value 90) is also a peak, but returning any one peak index is valid.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (C++)

- **Submitted:** 2026-11-19 08:09:05
- **Status:** Correct
- **Marks:** 0

```cpp
class Solution {
  public:
    int peakElement(vector<int> &arr) {
        // code here
        int index = -1;
        
        if(arr.size() == 1){
                return 0;
        }
            
        if(arr[0] > arr[1]){
            return 0;
        }
        else if(arr[arr.size()-1] > arr[arr.size()-2]){
                return arr.size()-1;
        }
            
        for(int i=1;i<arr.size()-1;i++){
            if(arr[i] > arr[i-1] && arr[i] >arr[i+1]){
                return i;
            }
        }
    }
};
```

#### Solution 2 (C++)

- **Submitted:** 2026-11-19 08:03:09
- **Status:** Correct
- **Marks:** 4

```cpp
class Solution {
  public:
    int peakElement(vector<int> &arr) {
        // code here
        int index = -1;
        for(int i=0;i<arr.size();i++){
            if(arr.size() == 1){
                return 0;
            }
            if(i == 0){
                if(arr[i] >arr[i+1]){
                    index = i;
                    break;
                }
            }
            else if(i == arr.size()-1){
                if(arr[i] > arr[i-1]){
                    index = i;
                    break;
                }
            }
            else if(arr[i] > arr[i-1] && arr[i] >arr[i+1]){
                index = i;
                break;
            }
        }
        return index;
    }
};
```

*Generated on: 11/19/2026, 8:09:34 AM*