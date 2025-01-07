# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common error in JavaScript related to closures and the `setTimeout` function within a loop.

The `bug.js` file contains code that exhibits this issue.  The loop iterates 10 times, scheduling a `setTimeout` function for each iteration.  The intention is to print the value of `i` at each iteration, but due to the closure nature of `setTimeout`, an unexpected result is obtained.

The solution, found in `bugSolution.js`, uses an immediately invoked function expression (IIFE) to create a new scope for each iteration, ensuring that the correct value of `i` is captured.