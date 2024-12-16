# React useEffect Infinite Loop Bug
This repository demonstrates a common bug in React applications involving the `useEffect` hook: an infinite loop caused by a missing dependency.

## Description
The `MyComponent` function uses the `useEffect` hook to log the current count to the console.  However, the dependency array `[]` is empty, meaning the effect runs after every render. This causes an infinite loop of renders, as each render triggers the effect, which causes another render, and so on.

## Solution
The solution is to include `count` in the dependency array. This ensures the effect only runs when the `count` value changes.  The cleanup function is also included to demonstrate proper effect cleanup which is often overlooked.