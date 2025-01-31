# React 19 useEffect Performance Issue

This repository demonstrates a common performance issue in React 19 applications related to the `useEffect` hook.  The problem stems from an incorrectly configured dependency array, leading to unnecessary re-renders and potential performance bottlenecks. The solution involves correctly specifying dependencies to optimize the effect's execution.

## Bug Description
The `useEffect` hook is used to perform side effects after a component renders.  However, if the dependency array is missing or incomplete, the effect will run more frequently than intended, potentially leading to performance degradation, especially in complex applications.  This example showcases this issue and offers a solution.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console output; you'll see the effect runs after every click, even though it only needs to run when the count changes.

## Solution
The solution is to accurately specify the dependencies in the useEffect hook's dependency array.  In this case, the `count` state variable is what triggers changes that warrant the effect's execution.