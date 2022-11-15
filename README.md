# Daily Leetcode

## 1480 - Running Sum of 1D Array: 11/15/2022

![](1480-running-sum/running-sum.png)
![](1480-running-sum/running-sum-code.png)

### Assumptions

- An array can be modified in place.
- The first number of the input array does not change, therefore it can be skipped in iteration.
- Indexes 1...n is where the addition takes place, start the iteration at index 1 until index _n_.

### Optimizations

Solution is:

- O(n) time: The loop has to run through each element in the array.
- O(1) space: The array is modified in place and extra space is not created based on the input size.
