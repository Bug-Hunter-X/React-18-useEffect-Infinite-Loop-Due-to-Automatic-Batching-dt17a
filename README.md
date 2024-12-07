# React 18 useEffect Infinite Loop Bug

This repository demonstrates a subtle bug that can occur in React 18 due to automatic batching of state updates within the `useEffect` hook.  The bug manifests as an infinite loop.

## Bug Description
The `useEffect` hook in the `MyComponent` component lacks `count` in its dependency array.  This leads to the effect running on every render, causing the state `count` to update continuously, triggering the effect again and again.