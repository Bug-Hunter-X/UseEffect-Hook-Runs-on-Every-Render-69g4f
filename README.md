# React useEffect Hook Runs on Every Render

This repository demonstrates a common issue with the React `useEffect` hook where it runs after every render instead of only once after the initial render.  This can lead to performance problems and unexpected behavior.

## Problem

The provided `MyComponent` uses `useEffect` without specifying dependencies. This means it will run after every render, causing the `console.log` to print on each render. In larger applications, this behavior can significantly impact performance.

## Solution

The solution involves specifying an empty dependency array `[]` as the second argument to `useEffect`. This ensures that the effect runs only once after the initial mount and not on subsequent renders.