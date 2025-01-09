# Express.js: Handling Empty or Invalid JSON Request Bodies
This repository demonstrates a common issue in Express.js applications where handling empty or invalid JSON request bodies isn't done robustly.  The application should gracefully handle these situations by returning appropriate error responses (e.g., 400 Bad Request) instead of silently failing.

## Bug
The provided `bug.js` file shows an Express.js application that accepts a POST request to `/data`. It logs the request body using `console.log(req.body)`. When an empty or malformed JSON request is sent, the application logs an empty object `{}` instead of throwing an error.

## Solution
The `bugSolution.js` file provides a corrected version. It uses a try-catch block to gracefully handle potential errors during JSON parsing, responding with a 400 Bad Request if parsing fails.