# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation blocks the event loop, causing the server to become unresponsive.  The `bug.js` file shows the problematic code. The solution is provided in `bugSolution.js`.

## Problem

Node.js is single-threaded.  A long-running operation in the main thread blocks the event loop, preventing it from processing other requests and events (like handling incoming connections).

## Solution

The solution involves refactoring the long-running task to be asynchronous using promises, async/await, or other asynchronous patterns. This allows the event loop to continue processing other requests even while the long-running task is in progress.