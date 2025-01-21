# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook.  The bug occurs when a dependency is omitted from the `useEffect` hook's dependency array, leading to an infinite render loop.  This example showcases the issue and provides a solution.

## Bug Description

The provided `MyComponent` uses `useEffect` to log a message to the console after every render. However, because `count` is not in the dependency array, the effect runs after every state update, triggering another render, and creating an infinite loop. 

## Solution

The solution involves adding `count` to the dependency array.  This ensures that the effect only runs when `count` changes, preventing the infinite loop.