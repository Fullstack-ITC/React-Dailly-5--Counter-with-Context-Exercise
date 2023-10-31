# React Counter with Context Exercise

## Recap

In the previous exercise, you built a simple counter application using React components. You split the application into three components: `App`, `CounterButton`, and `CounterDisplay`. If you haven't completed the previous exercise, I suggest you start there before moving on to this one.

## Objective

Refactor the counter application to use React Context for state management, allowing you to easily manage and share the counter's state between components without prop-drilling.

## Instructions

### Setting up the Context

1. Create a new file called `CounterContext.js`.
2. Inside, initialize a new context using `createContext()`. This will give you a `Provider` and a `Consumer`.
3. Export both the context itself and a custom `Provider` component. The custom `Provider` component should manage the state of the counter (both the count value and the functions to increment/decrement it).

### Integrating the Context into the App

- In your main `App` component, wrap the entire component tree inside your custom `Provider` from `CounterContext.js`.
- You won't need to pass down state and functions as props anymore. Instead, the child components will consume the values directly from the context.

### Using the Context in the Child Components

#### CounterButton Component

- Instead of receiving props, use the `useContext` hook to consume the context and get access to the counter's functions.

#### CounterDisplay Component

- Similarly, use the `useContext` hook to get access to the count value and display it.

## Bonus

- Add functionality to reset the counter to its initial state.
- Implement a `CounterControls` component where users can input a number and set the counter to that specific value using context.
