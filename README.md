# Silent Failure in Express.js Route Handler

This repository demonstrates a common but easily missed error in Express.js applications: failing to send a response in a route handler.  When a route handler doesn't explicitly send a response using `res.send()`, `res.json()`, etc., the request might hang, leading to unexpected behavior.

## Bug
The `bug.js` file contains an Express.js application with a route handler that lacks a response.  This results in the server seemingly working but not responding to requests to the root path (`/`).

## Solution
The `bugSolution.js` file fixes the issue by adding a `res.send()` call in the route handler to send a simple response.