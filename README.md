# Unhandled Promise Rejection in Express.js Route Handler

This repository demonstrates a common error in Express.js applications: unhandled promise rejections in route handlers.  The bug occurs when fetching user data from a database without proper error handling.  If the database query fails, the application will crash or exhibit unexpected behavior.

The `bug.js` file contains the problematic code. The `bugSolution.js` file provides a corrected version with robust error handling.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `npm install` to install Express.js.
4. Run `node bug.js` (or `node bugSolution.js` to see the fix). 

## Solution

The solution involves using `.catch()` to handle potential errors during the database query. This prevents unhandled promise rejections and allows for graceful error handling, such as returning an appropriate HTTP status code to the client.