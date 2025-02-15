# Uncommon React useEffect Bug: Infinite Loop

This repository demonstrates a subtle but common bug in React's `useEffect` hook that can lead to an infinite rendering loop. The issue arises when the effect's dependency array is missing or improperly defined.

## Bug Description
The `MyComponent` uses the `useEffect` hook to log the current count value.  However, because the `count` variable is not included in the dependency array, the effect runs on every render, which updates the count, which in turn causes another render. This creates a vicious cycle.