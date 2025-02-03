# React 19 useEffect Bug

This repository demonstrates a common bug encountered in React 19 related to the `useEffect` hook. The issue arises when the `useEffect` hook lacks a dependency array, causing it to re-run after every render, which can lead to performance degradation and unexpected behavior. 

## Bug Description

The provided `bug.js` file contains a component that uses `useEffect` without a dependency array. As a result, the effect runs after every render, repeatedly logging the current count to the console. In larger applications, this can lead to performance issues, as the effect is unnecessarily re-executed.  Additionally, it can lead to unexpected behavior if the effect interacts with state or other components.

## Solution

The `bugSolution.js` file demonstrates how to correctly fix the issue by providing a dependency array to `useEffect`. By listing the `count` variable in the dependency array, the effect will only run when `count` changes, preventing unnecessary re-renders.

## How to Reproduce

1. Clone the repository.
2. Navigate to the repository directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server. 
5. Observe the console output and the behavior of the component.