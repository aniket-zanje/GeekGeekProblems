## 01. Floor and Ceil in Unsorted

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/ceil-the-floor2802/1)

### Problem Description

**Task:** Given an unsorted array arr[] of integers and an integer x, find the floor and ceiling of x in arr[].Floor of x is the largest element which is smaller than or equal to x. Floor of x doesn’t exist if x is smaller than smallest element of arr[].Ceil of x is the smallest element which is greater than or equal to x. Ceil of x doesn’t exist if x is greater than greatest element of arr[].Return an array of integers denoting the [floor, ceil]. Return -1 for floor or ceiling if the floor or ceiling is not present.Examples:Input: x = 7 , arr[] = [5, 6, 8, 9, 6, 5, 5, 6]

#### Examples

##### Example 1

- **Output:**
```text
6, 8
```
- **Explanation:** Floor of 7 is 6 and ceil of 7 is 8.

##### Example 2

- **Input:**
```text
x = 10 , arr[] = [5, 6, 8, 8, 6, 5, 5, 6]
```
- **Output:**
```text
8, -1
```
- **Explanation:** Floor of 10 is 8 but ceil of 10 is not possible.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-03 11:13:21
- **Status:** Correct
- **Marks:** 2

```cpp
class Solution {
  public:
    vector<int> getFloorAndCeil(int x, vector<int> &arr) {
        // code here
        int floor = -1,ceil = INT_MAX;
        
        for(int i : arr){
            if(i<=x){
                floor = max(floor,i);
            }
            if(i>=x){
                ceil = min(ceil,i);
            }
        }
        if(ceil == INT_MAX){
            ceil = -1;
        }
       
        return {floor,ceil};
    }
};
```

*Generated on: 10/3/2026, 11:13:58 AM*