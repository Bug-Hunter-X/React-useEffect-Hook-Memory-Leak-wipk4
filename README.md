# React useEffect Hook Memory Leak

This example demonstrates a common error in React's `useEffect` hook: forgetting to include a return statement for cleanup.  This can lead to memory leaks if the component unmounts before cleanup actions are completed.

## Bug
The `bug.js` file contains a component with a `useEffect` hook that logs a message when the component mounts.  However, it lacks a return statement, meaning any cleanup function (like setting timers, event listeners, etc.) won't be executed when the component unmounts.