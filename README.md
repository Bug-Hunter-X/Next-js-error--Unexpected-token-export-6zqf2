# Next.js Unexpected Token Export Bug

This repository demonstrates a common but easily overlooked bug in Next.js applications when using functional components as default exports in the `pages/index.js` file. The error message may be unclear, making it challenging to debug.  This repository provides a clear example of the problem and its solution.

## Bug Description

The primary issue stems from an incorrect configuration or file structure. When Next.js attempts to parse the `pages/index.js` file, it encounters an unexpected token (the `export` keyword) if not correctly structured within a module.

## Solution

The solution involves ensuring that the functional component is the default export within an immediately invoked function expression (IIFE).  This allows the component to be defined as the default export while maintaining compatibility with Next.js's routing mechanism.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install`
3. Run `npm run dev`
4. Observe the error message on the browser console.
5. Refer to `bugSolution.js` for the corrected code.