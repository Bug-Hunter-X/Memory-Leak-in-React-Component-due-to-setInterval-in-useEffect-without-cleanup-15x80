# React useEffect setInterval Memory Leak
This example demonstrates a common mistake in React: using setInterval within useEffect without proper cleanup. This can lead to memory leaks because the interval continues to run even after the component unmounts.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second.  However, it fails to clear the interval when the component is unmounted, causing a memory leak.

## Solution
The `bugSolution.js` file provides a corrected version. It uses the return value of `useEffect` to clear the interval with `clearInterval` before the component unmounts, preventing the memory leak.