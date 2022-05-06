# Advanced State with Reducers

The useReducer() hook in React allows you to decouple the component's state management from its rendering logic.

`const [state, dispatch] = useReducer(reducer, initialState)`

 **Accepts 2 argument:** 
 + The reducer function 
 + The initial state. 

## When to use useReducer?

When you have complex state logic involving multiple sub-values or when the next state is dependent on the previous one, useReducer is usually preferred over useState. Because you may pass dispatch down instead of callbacks, useReducer can help you improve performance for components that trigger deep modifications.

## How does it work? How does the Reducer Hook work?

The application Reducer Hook, like useState Hook, is used to store and update states. The first parameter is a reducer function, while the second is the initial state.

useReducer delivers an array containing the current state value as well as a dispatch function to which you may send an action to be executed later. While this design is similar to Redux's, there are a few distinctions.

## There are three main building blocks in Redux:
1. A store is an immutable object that holds the state data of an application.
2. A reducer is a function that is activated by an action type and returns some state data.
3. An action is a type of object that instructs the reducer on how to update the state. It must have a type property and can have a payload property as well.

## CODE EXAMPLE:

```js
import React, { useReducer } from "react";

const initialState = { count: 0 };
// The reducer function
function reducer(state, action) {
  switch (action.type) {
    case "increment":
      return { count: state.count + 1 };
    case "decrement":
      return { count: state.count - 1 };
    case "reset":
      return { count: (state.count = 0) };
    default:
      return { count: state.count };
  }
}

export default function Counter() {
  const [state, dispatch] = useReducer(reducer, initialState);
  return (
    <>
      Count: {state.count}
      <button onClick={() => dispatch({ type: "reset" })}>Reset</button>
      <button onClick={() => dispatch({ type: "decrement" })}>-</button>
      <button onClick={() => dispatch({ type: "increment" })}>+</button>
    </>
  );
}
```

We begin by setting the state to 0 and then writing a reducer function that takes the current state of our count as an argument and performs an action. The reducer updates the state according to the action type. The action types increment, decrement, and reset all update the state of our app when they are sent.We just set count to state to increase the state count const initialState = count: 0.When the increment action type is dispatched, count + 1.

