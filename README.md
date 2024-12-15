# Express.js Route Handler Bug: Missing Error Handling

This repository demonstrates a common bug in Express.js route handlers: missing error handling for invalid input.  The `bug.js` file contains a route that retrieves a user by ID.  However, it lacks proper error handling for cases where the user ID is not a valid number.

The `bugSolution.js` file provides a corrected version with comprehensive error handling to address this issue. 

## Bug
The original code attempts to parse the user ID as an integer without any validation.  If the ID is not a number (e.g., a string or undefined), `parseInt(userId)` will return `NaN`, causing errors later in the code.  This can lead to unexpected behavior or crashes.

## Solution
The solution implements error handling to address the following scenarios:

1. **Invalid User ID:** Checks if `userId` is a valid number before attempting to access user data.
2. **User Not Found:** Handles the case where a user with the given ID does not exist.

By adding these checks, the route handler becomes more robust and prevents crashes due to invalid input.