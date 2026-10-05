## 01. Next Prime Number

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/next-prime-number/1)

### Problem Description

**Task:** Given an integer n. Write a program to find the first prime number greater than n.

#### Examples

##### Example 1

- **Input:**
```text
n = 15
```
- **Output:**
```text
17
```
- **Explanation:** 17 is next prime number.

##### Example 2

- **Input:**
```text
n = 7
```
- **Output:**
```text
11
```
- **Explanation:** 11 is the prime number next to 7.

#### Constraints

- **1.** `1 <= n <= 500`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-05 14:19:10
- **Status:** Correct
- **Marks:** 0

```cpp
int nextPrime(int n) {

    // code here to find next prime number
    // return next prime number
    n++;
   while(true){
        int number = n++;
        bool isPrime = true;
        for(int i = 2;i<number ; i++){
            if(number % i == 0){
                isPrime = false;
                break;
            }
        }
        if(isPrime){
            return number;
        }
        
   }
}
// PAIYSX
```

*Generated on: 10/5/2026, 2:19:39 PM*