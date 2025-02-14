# React setInterval Memory Leak
This example demonstrates a common mistake when using `setInterval` within a React component's `useEffect` hook, leading to a memory leak.  The solution shows how to correctly implement cleanup to avoid this issue.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it fails to include a cleanup function within the `useEffect` hook to stop the interval when the component unmounts. This results in the interval continuing to run, even after the component is no longer needed, causing a memory leak.

## Solution
The `bugSolution.js` file demonstrates the correct way to handle `setInterval` within `useEffect`.  A cleanup function is returned from the `useEffect` hook to clear the interval when the component is unmounted. This ensures that no memory leaks occur.
