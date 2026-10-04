## 01. Array Leaders

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/leaders-in-an-array-1587115620/1)

### Problem Description

**Task:** My SubmissionsRefresh Time (IST)StatusMarksLangTest CasesCode2026-10-04 15:03:56Correct0cpp1111 / 1111View2026-10-04 15:03:42Wrong0cpp2 / 1111View2026-10-04 15:02:36Compilation Error0cpp0 / 1111View2026-10-04 15:02:32Compilation Error0cpp0 / 1111View2026-10-04 14:58:25Correct2cpp1111 / 1111ViewDiscussions ( Threads )Most Recent💡Discussion Guidelines×Please avoid posting complete solutions or full code in the comments.Ask questions, share hints, discuss approaches, or report any issues. Let's help everyone learn together.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** Not found
- **Expected Auxiliary Space Complexity:** Not found

### Accepted Solutions (2)

#### Solution 1 (C++)

- **Submitted:** 2026-10-04 15:03:56
- **Status:** Correct
- **Marks:** 0

```cpp
class Solution {
  public:
    vector<int> leaders(vector<int>& arr) {
        // code here
        vector<int> res;
        int largest = INT_MIN;
        
        for(int i = arr.size()-1; i>=0;i--){
            
            if(largest <= arr[i]){
                // res.insert(res.begin(),arr[i]);
                res.push_back(arr[i]);
                
            }
            largest = max(largest , arr[i]);
        }
        
        // return res;
        reverse(res.begin(), res.end());
        return res;
    }
};
```

#### Solution 2 (C++)

- **Submitted:** 2026-10-04 14:58:25
- **Status:** Correct
- **Marks:** 2

```cpp
class Solution {
  public:
    vector<int> leaders(vector<int>& arr) {
        // code here
        vector<int> res;
        int largest = INT_MIN;
        
        for(int i = arr.size()-1; i>=0;i--){
            
            if(largest <= arr[i]){
                res.insert(res.begin(),arr[i]);
                
            }
            largest = max(largest , arr[i]);
        }
        
        return res;
    }
};
```

*Generated on: 10/4/2026, 3:04:30 PM*