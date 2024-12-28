# Unhandled Exception in Asynchronous Node.js Server

This repository demonstrates a common error in Node.js where an uncaught exception in an asynchronous operation can cause the server to crash. The `bug.js` file shows the problematic code, while `bugSolution.js` provides a solution using error handling.

## Problem

The server in `bug.js` uses `setTimeout` to simulate an asynchronous task.  If the request URL is '/error', an exception is thrown. Without proper error handling, this uncaught exception crashes the server.

## Solution

The solution in `bugSolution.js` uses a `try...catch` block within the asynchronous operation to handle potential errors. This prevents the server from crashing and allows for graceful error handling, such as logging the error or returning an appropriate error response to the client.

## Running the Code

1. Clone this repository.
2. Navigate to the repository's directory in your terminal.
3. Run `node bug.js` and then visit `http://localhost:3000` and `http://localhost:3000/error` in your browser to see the problem.
4. Run `node bugSolution.js` and repeat step 3 to observe the solution.  The '/error' route will now return an error message without crashing the server.