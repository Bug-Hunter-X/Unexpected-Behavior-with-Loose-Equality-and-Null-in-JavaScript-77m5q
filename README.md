# JavaScript Loose Equality Bug

This repository demonstrates a common error in JavaScript related to loose equality (==) and null checks.  The `bug.js` file contains a function that uses loose equality to check for null values. This can lead to unexpected behavior, particularly when dealing with values that might be implicitly type-coerced.

The `bugSolution.js` file provides a corrected version of the function using strict equality (===), ensuring correct handling of null values and preventing unexpected type coercion issues.

## How to reproduce

1. Clone this repository.
2. Run `bug.js` using a JavaScript runtime (e.g., Node.js).  Observe the output.
3. Compare the output with the expected behavior.  Note that the loose equality comparison may produce incorrect results.
4. Run `bugSolution.js`. Observe the corrected output. 

## Discussion

Loose equality (==) performs type coercion before comparing values.  This can lead to unexpected results, particularly when comparing null or undefined values to other types.  Strict equality (===) does not perform type coercion, providing more reliable comparisons.

Always prefer strict equality (===) over loose equality (==) in JavaScript to avoid these common pitfalls.