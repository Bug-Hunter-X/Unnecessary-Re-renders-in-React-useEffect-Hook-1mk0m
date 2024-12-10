# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common React bug: unnecessary re-renders caused by a missing dependency in the `useEffect` hook.  The `useEffect` hook should only run when the values in its dependency array change.  In this example, the component re-renders on every render because the dependency array is incorrect.

## Bug

The `MyComponent` uses the `useEffect` hook to log the count to the console. However, the dependency array `[count]` isn't correctly specified, causing unnecessary re-renders. 

## Solution

The solution involves correctly specifying the dependency array within the useEffect hook. If the useEffect hook should only execute after the initial render, pass an empty array `[]` as the dependency array.