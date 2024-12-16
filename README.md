# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug causes an infinite loop due to a missing dependency in the `useEffect` hook's dependency array.

## Bug Description
The `useEffect` hook is used to perform side effects after every render.  In this example, the `useEffect` hook logs the current count to the console. However, because the `count` variable is not included in the dependency array, the effect runs after every render, causing `setCount` to be called again, triggering another render, and creating an infinite loop.

## Bug Solution
The solution is to include the `count` variable in the dependency array. This ensures that the effect only runs when the `count` variable changes.

## How to Reproduce
1. Clone this repository.
2. Navigate to the repository directory in your terminal.
3. Run `npm install` to install the necessary dependencies.
4. Run `npm start` to start the development server.
5. Observe the infinite loop in the browser's console.

## Solution
The solution involves adding `count` to the dependency array of the useEffect hook, ensuring it only runs when `count` changes. 