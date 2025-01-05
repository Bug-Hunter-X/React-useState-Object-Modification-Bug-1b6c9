# React useState Object Modification Bug

This repository demonstrates a common error when using the `useState` hook in React with object states.  Directly modifying the object state does not trigger a re-render because the object reference remains unchanged. The solution involves creating a new object with the updated values using the spread operator or other methods to ensure the reference changes, triggering re-rendering.

## Bug Description
The bug occurs when directly modifying an object in the state using `useState` without using the setter function correctly. This prevents the component from re-rendering. 

## How to Reproduce
Clone this repo and run `npm install` to install the dependencies. Then, run `npm start` to start the development server. You will see that clicking the button will not increment the counter because of the incorrect state update method in `bug.js`.

## Solution
The solution is provided in `bugSolution.js`. It shows the correct way to update the state by creating a new object using the spread operator.