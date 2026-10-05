## 01. Last Digit of Number

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/last-digit-of-a-number--145429/1)

### Problem Description

**Task:** Given an integer n. Write a program to print the last digit of n.

#### Examples

##### Example 1

- **Input:**
```text
n = 10
```
- **Output:**
```text
0
```

##### Example 2

- **Input:**
```text
n = 9768
```
- **Output:**
```text
8
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(1)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-05 14:05:30
- **Status:** Correct
- **Marks:** 1

```cpp
#include <cstdlib>
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    // code here
    cout<<abs(n%10);

    return 0;
}
```

*Generated on: 10/5/2026, 2:06:27 PM*