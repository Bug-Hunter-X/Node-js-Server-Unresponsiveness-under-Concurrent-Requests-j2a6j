# Node.js Server Unresponsiveness under Concurrent Requests

This repository demonstrates a common issue in Node.js servers where they become unresponsive or throw errors when handling multiple concurrent requests.  The provided code showcases the problem and offers a solution using asynchronous request handling.

## Problem

The initial `bug.js` file demonstrates a server created using `http.createServer`.  When many requests hit this server simultaneously, it may fail to respond to some or all of them, potentially leading to errors or a complete server freeze. This is due to Node.js's single-threaded nature; blocking operations in request handling can block other requests.

## Solution

The solution, found in `bugSolution.js`, uses asynchronous operations to prevent blocking. This ensures the server can handle multiple requests efficiently without freezing.