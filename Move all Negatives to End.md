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

### Accepted Solutions (2)

#### Solution 1 (C++)

- **Submitted:** 2026-10-04 15:20:52
- **Status:** Correct
- **Marks:** 0

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


// #include <iostream>
// #include <vector>
// using namespace std;

// // Function to move all -ve element to end of array
// // in same order.
// void segregateElements(vector<int> &arr)
// {
//     int n = arr.size();

//     // Create an empty array to store result
//     vector<int> temp(n);
//     int idx = 0;

//     // First fill non-negative elements into the
//     // temporary array
//     for (int i = 0; i < n; i++)
//     {
//         if (arr[i] >= 0)
//             temp[idx++] = arr[i];
//     }

//     // Now fill negative elements into the
//     // temporary array
//     for (int i = 0; i < n; i++)
//     {
//         if (arr[i] < 0)
//             temp[idx++] = arr[i];
//     }

//     // copy the elements from temp to arr
//     arr = temp;
// }

// int main()
// {
//     vector<int> arr = {1, -1, -3, -2, 7, 5, 11, 6};
//     segregateElements(arr);

//     for (int i = 0; i < arr.size(); i++)
//         cout << arr[i] << " ";

//     return 0;
// }
```

#### Solution 2 (C++)

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

*Generated on: 10/4/2026, 3:21:51 PM*