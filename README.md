# React useEffect Cleanup Function Missing

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include a cleanup function.  This can lead to memory leaks or unexpected behavior if the component unmounts while the effect is still active.

## Problem

The provided code registers a `keydown` event listener in the `useEffect` hook without a cleanup function.  This means that when `MyComponent` unmounts, the event listener remains attached to the document, potentially causing memory leaks or unexpected behavior in other parts of the application.

## Solution

The solution involves adding a return statement to the `useEffect` hook that removes the event listener when the component unmounts. This ensures proper cleanup and prevents resource leaks.
