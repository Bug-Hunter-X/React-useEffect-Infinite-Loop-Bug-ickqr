# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array.

## Bug Description
The `useEffect` hook in `bug.js` is intended to log the current count to the console after every render. However, because `count` is not included in the dependency array, the effect runs on every render, causing `count` to update, which triggers another render, creating an infinite loop.

## Bug Solution
The solution in `bugSolution.js` adds `count` to the dependency array, ensuring that the effect only runs when `count` changes.