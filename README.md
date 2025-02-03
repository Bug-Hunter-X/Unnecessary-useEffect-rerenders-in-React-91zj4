# Unnecessary useEffect rerenders in React

This repository demonstrates a common React bug where the `useEffect` hook runs on every render due to a missing or incorrect dependency array.  This can lead to performance issues and unexpected behavior.

The `bug.js` file contains the buggy code, while `bugSolution.js` shows the corrected version.

## Bug

The `useEffect` hook in `bug.js` is intended to log the count whenever it changes. However, because the dependency array is missing or incorrect, the effect runs on every render, flooding the console and impacting performance.

## Solution

The `bugSolution.js` file demonstrates the correct usage of `useEffect`.  The dependency array `[count]` ensures the effect runs only when the `count` value changes.