# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving an infinite loop caused by the `useEffect` hook.  The bug occurs when the `useEffect` hook lacks a dependency array, leading to it running after every render, creating an infinite loop.

## Bug Description
The component `MyComponent` uses `useState` to manage a count. The `useEffect` hook logs the count to the console after every render. Because there's no dependency array, the effect runs repeatedly, causing an infinite loop and filling the console with log messages. 

## Solution
The solution involves adding a dependency array to the `useEffect` hook. This ensures that the effect only runs when the specified dependency (in this case, `count`) changes.