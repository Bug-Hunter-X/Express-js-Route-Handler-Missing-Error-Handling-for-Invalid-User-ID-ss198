# Express.js Route Handler Missing Error Handling

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid input.  Specifically, the `/users/:id` route fails if the `id` parameter is not a valid number.

## Bug

The `bug.js` file shows an Express.js route handler that fetches a user by ID.  It fails silently if the user ID is not a number, throwing a runtime error.

## Solution

The `bugSolution.js` file demonstrates the correct approach: adding explicit error handling to check if the `userId` is a valid number before accessing the `users` array. This prevents errors and provides a graceful response to the client when an invalid ID is provided.