# JavaScript setTimeout Loop Closure Issue

This repository demonstrates a common issue encountered when using `setTimeout` within a loop in JavaScript.  Due to the asynchronous nature of `setTimeout`, the loop variable `i` is not captured correctly by the closure, leading to unexpected behavior.

The `bug.js` file contains code exhibiting the problem. The `bugSolution.js` file provides a corrected version of the code.

## Problem:
The expected output would be 0 through 9, but instead it produces 10 repeated 10 times.

## Solution:
Use `let` inside the loop to create a new variable scope for each iteration, or use an immediately-invoked function expression (IIFE).