# Daily Leetcode

## 374 - Guess Number Higher or Lower: 11/16/2022

![](374-guess-number/guess-number.png)
![](374-guess-number/guess-number-code.png)

### Problem

I pick a number from 1 to n. You have to guess which number I picked.
Every time you guess wrong, I will tell you whether the number I picked is higher or lower than your guess.
You call a pre-defined API int guess(int num), which returns three possible results:

- -1: Your guess is higher than the number I picked (i.e. num > pick).
- 1: Your guess is lower than the number I picked (i.e. num < pick).
- 0: your guess is equal to the number I picked (i.e. num == pick).

Return the number that I picked.

### Assumptions

- Searching for an unknown number by one number at a time is inefficient.
- Introducing a third number (middle) for comparison will allow us to remove numbers lower or higher than the third number.
- When the unknown number is lower or higher than the middle number, the middle number needs to be shifted as the unknown number cannot equal the middle number.

### Optimizations

Solution is:

- Binary search
- O(log(n)) time: The range of the input is halved each iteration, therefore the runtime is reduced.
- O(1) space: No extra space is allocated that cannot be determined at runtime.

_Since_ `pick` _is namespaced,_ `__pick__` _can be used to make the solution O(1) time :wink:_

## 1480 - Running Sum of 1D Array: 11/15/2022

![](1480-running-sum/running-sum.png)
![](1480-running-sum/running-sum-code.png)

### Problem

Given an array `nums`. We define a running sum of an array as `runningSum[i] = sum(nums[0]…nums[i])`.

Return the running sum of `nums`.

### Assumptions

- An array can be modified in place.
- The first number of the input array does not change, therefore it can be skipped in iteration.
- Indexes 1...n is where the addition takes place, start the iteration at index 1 until index _n_.

### Optimizations

Solution is:

- O(n) time: The loop has to run through each element in the array.
- O(1) space: The array is modified in place and extra space is not created based on the input size.
