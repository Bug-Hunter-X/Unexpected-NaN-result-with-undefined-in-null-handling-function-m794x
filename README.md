# Unexpected NaN result with undefined in null-handling function

This repository demonstrates a common JavaScript error related to how the language handles `null` and `undefined` values.  The original code attempts to gracefully handle `null` inputs, returning `null` if either parameter is `null`. However, it fails to account for `undefined`, resulting in `NaN` instead of the expected `null`. This is a subtle bug that can be difficult to spot in larger codebases. 

The solution shows a more robust approach that explicitly checks for both `null` and `undefined`.

## How to reproduce

1. Clone this repository.
2. Open `bug.js` and `bugSolution.js` to view the original buggy code and the corrected version respectively.
3. Run the `bug.js` file in a JavaScript environment (e.g., Node.js) to see the unexpected `NaN` output.
4. Run the `bugSolution.js` file to see the corrected output.

## Lessons learned

- Always explicitly check for both `null` and `undefined` when handling potential missing or invalid values in JavaScript.
- Be aware of the differences between `null`, `undefined`, and how they behave in arithmetic operations.
- Comprehensive testing, especially edge case testing, helps prevent such unexpected behaviour.
