# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing or incorrect dependency array.  The `useEffect` hook, while powerful, requires careful management of its dependencies to avoid unexpected behavior.

## The Problem

The `bug.js` file contains a component with a `useEffect` hook that logs the current count to the console.  Because the dependency array is missing, the effect runs after every render, leading to an infinite loop and performance degradation.  The browser console will fill rapidly with log messages.

## The Solution

The `bugSolution.js` file provides the corrected code.  By including `[count]` as the dependency array, the effect now only runs when the `count` state variable changes, solving the infinite loop problem.

## How to Reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the infinite logging in your browser's console (in `bug.js`).
6.  Modify the code to match `bugSolution.js` to fix the issue.