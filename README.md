# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common issue in JavaScript related to closures and the `setTimeout` function within loops.  The problem arises because the `setTimeout` callback function doesn't capture the value of `i` at the time it's defined, but rather captures a reference to the variable `i`. By the time the `setTimeout` function finally executes, the loop has already completed, and `i` holds its final value.

The `bug.js` file shows the buggy code, while `bugSolution.js` demonstrates the corrected version.

## How to Reproduce
1. Clone the repository.
2. Open `bug.js` in your browser's console or using Node.js.
3. Run the `myFunction()` function.
4. Observe that the console repeatedly logs the value '10', instead of the expected sequence from 0 to 9. 
5. Then run `bugSolution.js` to see the corrected output.