# Node.js Server Unresponsiveness: Blocking Event Loop

This repository demonstrates a common Node.js issue: blocking the event loop with a long-running synchronous operation in a request handler.  This can lead to unresponsive servers and poor performance.

## Bug Description
The `bug.js` file contains a simple HTTP server that simulates a long-running task (5-second delay) within the request handler.  During this time, the server is unresponsive to new requests, resulting in timeouts and a negative user experience.

## Solution
The `bugSolution.js` file demonstrates how to solve this issue using asynchronous programming techniques, preventing the event loop from being blocked. This ensures the server remains responsive even during lengthy operations.

## How to Run
1. Clone the repository.
2. Navigate to the directory.
3. Run `node bug.js` to observe the unresponsive behavior.
4. Run `node bugSolution.js` to see the improved responsiveness.