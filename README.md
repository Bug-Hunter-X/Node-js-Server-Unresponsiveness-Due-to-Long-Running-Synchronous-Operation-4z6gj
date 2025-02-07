# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a server becomes unresponsive due to a long-running synchronous operation blocking the event loop.  The `bug.js` file contains the problematic code. The solution is provided in `bugSolution.js`.

## Problem

The server uses a `while` loop to simulate a long-running task. This blocks the event loop, preventing the server from handling subsequent requests.  This results in the server appearing to hang or become unresponsive.

## Solution

The solution involves using asynchronous operations or offloading long-running tasks to worker threads to avoid blocking the event loop. The `bugSolution.js` file provides an example using asynchronous operations with `setTimeout`.