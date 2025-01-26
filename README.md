# React useEffect setInterval Memory Leak

This repository demonstrates a common error in React applications involving the `useEffect` hook and the `setInterval` function.  Improperly using `setInterval` without a cleanup function can lead to memory leaks.

## The Problem

The `bug.js` file shows a component that uses `setInterval` to update a counter every second.  However, it fails to provide a cleanup function in the `useEffect` hook. This means the interval continues to run even after the component is unmounted, leading to a memory leak.

## The Solution

The `bugSolution.js` file corrects the issue by adding a cleanup function. This function clears the interval when the component unmounts, preventing the memory leak.

## How to run

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.