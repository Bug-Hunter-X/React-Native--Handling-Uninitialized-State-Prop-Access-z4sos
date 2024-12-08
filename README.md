# React Native: Handling Uninitialized State/Prop Access

This repository demonstrates a common error in React Native applications: accessing a state variable or prop before it has been initialized. The `bug.js` file shows the problematic code, where `this.state.data` is accessed before the asynchronous `fetch` call completes.  The `bugSolution.js` file provides a corrected version, handling the potential `null` or `undefined` value.

## Problem

Attempting to access `this.state.data` before the data has been fetched from the API results in a runtime error because `this.state.data` is initially `null`. 

## Solution

The solution involves checking if `this.state.data` is null or undefined before accessing its properties.  This can be done using optional chaining (?.) or a conditional statement.