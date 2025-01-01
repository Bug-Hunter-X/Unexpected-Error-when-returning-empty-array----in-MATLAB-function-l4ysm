# Unexpected Error when returning empty array [] in MATLAB function

This repository demonstrates a bug in MATLAB where returning an empty array from a function causes unexpected errors in the calling functions.  The problem arises specifically when the empty array is passed on to another function that does not handle the empty array correctly.

## Bug Description
The function `myFunction.m` returns an empty array [] under a certain condition. When this empty array is used as an input in another function, it causes an error, possibly due to size mismatch or an attempt to access an element of an empty array. This behavior is not intuitive and may be unexpected for developers.

## Solution
The solution involves adding checks to handle the empty array case gracefully. For example, we can add a check before using the output of `myFunction.m` to see if it is empty. Alternatively, we can modify the other function that receives this output so that it handles empty arrays as a special case.

## How to Reproduce
1. Clone this repository.
2. Open the files `bug.m` and `bugSolution.m` in MATLAB.
3. Run `bug.m` to observe the error.
4. Run `bugSolution.m` to see how the bug is fixed.