# Infinite Re-renders in React Component

This repository demonstrates a common React bug: infinite re-renders caused by a missing dependency in the `useEffect` hook.

## Bug Description
The `MyComponent` component uses the `useEffect` hook without specifying any dependencies.  This means the effect runs after every render, leading to an infinite render loop.  The `console.log` statement will show the component re-rendering continuously.

## Solution
The solution involves adding the `count` variable to the dependency array of the `useEffect` hook. This ensures the effect only runs when the `count` value changes.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console output showing infinite re-renders.
5. Uncomment the corrected code in `bugSolution.js` to see the fixed version.