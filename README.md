# JavaScript NaN Comparison Bug

This repository demonstrates a common, yet subtle, error in JavaScript related to comparing NaN (Not a Number) values.

## The Problem

In JavaScript, NaN is a special value that represents the result of an invalid numerical operation (e.g., dividing by zero, taking the square root of a negative number).  The peculiarity is that NaN is never equal to itself, regardless of whether you use loose comparison (`==`) or strict equality (`===`).

The `bug.js` file contains a function that attempts to compare two numbers for equality.  This function incorrectly returns `false` when both inputs are NaN.

## The Solution

The solution involves using the `Number.isNaN()` function to reliably check if a value is NaN. This function correctly handles the special case of NaN.

The `bugSolution.js` file demonstrates the corrected approach.

## How to Reproduce

1. Clone this repository.
2. Run `node bug.js` to observe the incorrect behavior.
3. Run `node bugSolution.js` to see the corrected behavior.
