# React useEffect Hook Not Updating State Correctly
This repository demonstrates a common issue encountered when using the `useEffect` hook in React: the dependency array is missing the state variable that the effect depends on.  This can lead to unexpected behavior and stale closures.

## Bug Description
The provided `MyComponent` uses the `useEffect` hook to log the current count to the console after every render. However, if we omit the count from the dependency array, the effect will only run once during the initial render, not after every state change.