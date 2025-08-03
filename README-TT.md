# React
## React lifecycle
In React, lifecycle has three main stages:
1. Mounting stage – when the component is created and added to the DOM.
- In class components: constructor, componentDidMount.
- In function components: use hooks useEffect to run after the initial render
2. Updating stage – when props or state change.
- In class components: componentDidUpdate.
- In function components: useEffect runs again if the specified dependencies change.
3. Unmounting stage – when the component is removed from the DOM.
- In class components: componentWillUnmount.
- In function components: handle cleanup by returning a function inside useEffect.

## useRef
useRef is a React hook that returns a mutable ref object.
It can be used to access DOM elements or store mutable values that persist across renders without causing re-renders.
For example, you can use useRef to store a reference to an input element and access its value directly.
It can also be used to store any mutable value that you want to keep across renders, like a timer ID or a previous value.
useRef does not trigger re-renders when the value changes, making it suitable for performance optimization.

## virtual DOM
Virtual DOM is a JavaScript object that stand for the real DOM in memory.
Direct DOM operations are slow and had a bad performance,
so React uses virtual DOM when state changes, Virtual DOM will compare the new state with the previous state, this process is called diffing.
Then React will update the real DOM only when necessary, this process is called patching.
it can reduce the direct DOM operations and update the real DOM efficiently.

# Redux
## how does Redux work?
Redux is a state management library that follows the Flux architecture.
It has three main principles:
1. Single source of truth: The entire application state is stored in a single store.
2. State is read-only: The state can only be changed by dispatch actions.
3. Changes are made with pure functions: Reducers are pure functions that take the current state and an action, and return a new state.
Redux uses a unidirectional data flow, meaning that data flows in one direction:
- The view dispatches an action.
- The action is sent to the reducer.
- The reducer returns a new state.
- The store updates the state and notifies the view to re-render.

# React-Router

# Next.js

# CSS

# JS

# TypeScript

# Testing

# Webpack & Vite

# Babel

# ESLint & Prettier

# Git

# Node.js