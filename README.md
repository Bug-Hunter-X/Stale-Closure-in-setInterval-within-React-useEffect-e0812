# Stale Closure in setInterval within React useEffect

This example demonstrates a common error in React when using `setInterval` within a `useEffect` hook.  The problem arises from a stale closure over the `count` state variable.  The callback function passed to `setInterval` captures the initial value of `count`, leading to incorrect updates.

## How to reproduce

1. Run the `bug.js` file. The counter will not increment correctly due to the stale closure.

## Solution

The solution in `bugSolution.js` utilizes a functional update to ensure `setCount` receives the latest value of `count`.