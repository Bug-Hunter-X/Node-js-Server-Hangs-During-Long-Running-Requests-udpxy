# Node.js Server Hang Issue

This repository demonstrates a common issue in Node.js applications where long-running requests can cause the server to hang or become unresponsive.  The problem arises from blocking the event loop, preventing other requests from being processed. The solution showcases how to utilize asynchronous operations and non-blocking methods to avoid this issue. 

## Bug

The `server.js` file contains a simple HTTP server.  However, it includes a `while` loop that simulates a long-running task which blocks the event loop.  This prevents the server from responding to other requests during the execution of the long task leading to a hang.

## Solution

The `serverSolution.js` file demonstrates how to fix the problem by using asynchronous operations.  Instead of blocking the event loop with a `while` loop, it employs techniques to handle the long-running task concurrently, keeping the server responsive.