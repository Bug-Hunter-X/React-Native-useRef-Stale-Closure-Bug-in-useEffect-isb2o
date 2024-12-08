# React Native useRef Stale Closure Bug

This repository demonstrates a common error encountered when using the `useRef` hook in React Native functional components. The problem stems from accessing the `current` value of a ref inside a callback function (like `useEffect` or an event handler), which may lead to stale closure issues.

The `bug.js` file shows the buggy code, where the ref is not correctly handled within the useEffect, often leading to unpredictable behavior, such as failing to correctly focus an input.

The `bugSolution.js` provides a solution by introducing a state variable to ensure the ref is properly accessed only when the component is mounted and the ref is available. 

## How to reproduce:

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run the application.
4. Observe that input focusing might not function correctly in the `bug.js` example.