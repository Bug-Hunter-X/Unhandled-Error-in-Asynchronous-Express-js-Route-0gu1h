# Unhandled Error in Asynchronous Express.js Route

This repository demonstrates a common error in Node.js applications where an unhandled error in an asynchronous operation can cause the server to crash.  The `bug.js` file contains the problematic code.  The `bugSolution.js` provides a corrected version with proper error handling.

## Problem

The original code simulates an asynchronous operation (using `setTimeout`) that can either succeed or fail randomly. If the operation fails, an unhandled `Error` is thrown, causing the Node.js process to terminate.

## Solution

The solution implements proper error handling using a `try...catch` block within the asynchronous operation.  This prevents the server from crashing and allows for graceful handling of errors, such as sending an error response to the client.