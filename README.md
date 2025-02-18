# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid input.  Specifically, the example shows a route that retrieves a user by ID but fails to handle cases where the provided ID is not a valid integer.

## Bug

The `bug.js` file contains the buggy code.  The route attempts to parse the user ID as an integer using `parseInt()`, but doesn't handle the case where `parseInt()` returns `NaN` (Not a Number).  This leads to errors when an invalid ID is provided.

## Solution

The `bugSolution.js` file provides a corrected version of the code.  It includes error handling to check if `parseInt()` returns `NaN` and sends an appropriate error response if so.