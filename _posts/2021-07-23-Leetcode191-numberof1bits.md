---
title: "Leetcode 191. Number of 1 Bits"
categories:
  - Leetcode
tags:
  - Coding
---
URL: [https://leetcode.com/problems/number-of-1-bits/](https://leetcode.com/problems/number-of-1-bits/)  
So I had the idea of writing about my thought process and solutions to programming problems on sites such as Leetcode and Hackerrank. The goal is to improve my ability to explain code, motivate me to program more in general, and keep my skills sharp. This problem interests me as I majored in computer engineering and a lot of the programming I had to do involved bit manipulation and detecting the value of individual bits.  
My solution:
```java
public class Solution {
    // you need to treat n as an unsigned value
    public int hammingWeight(int n) {
        int cnt = 0;
        
        while(n != 0) {

            if ((n & 1) == 1) {  
                ++cnt;
            }
            n = n >>> 1;
        }
        return cnt;
    }
}
```
Explanation:  
Before line 16 is executed, "cnt" is equal to the total number of 1 digits counted so far.  
On line 18, "(n & 1)" will return a 1 if the least significant digit is a 1 or 0 otherwise.  If it returns 1, then increment "cnt".  
On line 21, "n >>> 1" performs an unsigned right shift on "n" by one place. This will remove the least significant digit.  
On Line 16, it checks if "n != 0" is true. If it is true, then all of the 1 bits have been counted, otherwise continue looping.


