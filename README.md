# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug where an infinite loop is created within the `useEffect` hook.

## Bug Description
The `useEffect` hook is used to perform side effects after the component renders. However, if the `useEffect` function modifies the state that triggers the rerender, this creates an infinite loop. This is particularly true when the dependency array is empty, causing the effect to run continuously.

## Bug Reproduction
Clone the repository and run the application using `npm start` or `yarn start`. The count will increment continuously.

## Solution
The solution involves correctly managing the dependencies of the `useEffect` hook. In this case, the dependency array should include the state variable that the effect function depends on to prevent re-rendering continuously.