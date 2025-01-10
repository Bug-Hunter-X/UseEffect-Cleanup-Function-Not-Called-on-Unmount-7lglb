# React useEffect Cleanup Function Issue

This repository demonstrates a common issue with React's `useEffect` hook where the cleanup function isn't called as expected during component unmount. The problem stems from a misunderstanding of how the dependency array works and how cleanup functions are handled in React's lifecycle.

## Problem
The `bug.js` file contains a component that uses `useEffect` to log the current count and perform a cleanup action. However, the cleanup function (`console.log('cleanup');`) doesn't execute when the component is unmounted. This is because the useEffect runs on every render as no dependency array is specified.

## Solution
The `bugSolution.js` file provides a corrected version that addresses this issue by providing a correct dependency array which ensures that the cleanup function is correctly executed when the component is unmounted.

## How to reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console output. Note that the cleanup function doesn't print. This is the bug.
5. Open `bugSolution.js`. Note that the cleanup function now correctly runs.