# React useEffect Missing Dependency Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The example shows how forgetting to include a state variable in the dependency array leads to unexpected re-renders and, in some cases, an infinite render loop.

## Bug Description

The `useEffect` hook is designed to perform side effects after a component renders. However, if a state variable used within the effect is not included in the dependency array, the effect will run after every render, regardless of whether the state variable has actually changed. This can lead to unexpected behavior, performance issues, and infinite loops.

## Solution

The solution is simple: include all state variables used within the effect in the dependency array.  This ensures that the effect only runs when those variables change.