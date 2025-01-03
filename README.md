# React useEffect Hook: Incorrect Dependency Array

This repository demonstrates a common error in React's `useEffect` hook: an incorrect dependency array.  The example shows a counter that continues incrementing even after the component unmounts, leading to a memory leak.

The issue arises because the `useEffect` hook doesn't properly clean up the interval when the component is unmounted. This is because the dependency array `[]` is empty, meaning that the effect runs only once after the initial render. The solution shows how to fix this issue by adding the `count` state variable to the dependency array.