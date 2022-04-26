# useState( ) Hook

## Making Sense of React Hooks

**What exactly are hooks?**

Hooks are a new functionality that was introduced in React 16.8. You can use state and other React capabilities without having to write a class. Hooks are React state and lifecycle features from function components that "hook into" hooks. It does not work inside classes.

**Why are hooks used?**

Hooks use the React concept (explicit data flow and composition) within a component instead of merely between them.Hooks avoid excessive nesting in your component tree, unlike patterns like render props or higher-order components. They are also immune to the downsides of mixins.

**So, what about  classes?**

Custom Hooks are the most enticing aspect of the Hooks idea, in our opinion. React, on the other hand, needs to give functions with a method to declare state and side effects in order for custom Hooks to operate. Built-in Hooks like useState and useEffect enable us to do just that.

These built-in Hooks turn out to be handy for more than just developing bespoke Hooks. They're also good for defining components in general because they provide all of the necessary aspects like state.

## the state hook

**What is a Hook?** 

A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components.


**When am I going to use a Hook?**

If you write a function component and realize you need to add some state to it, previously you had to convert it to a class. Now you can use a Hook inside the existing function component.

**What is the purpose of using useState?**

It introduces the concept of a "state variable". let say that Count is the name of our variable in useState, but it could be anything other, such as banana. This is a new way to use the same features that this.state gives in a class — useState is a new way to "preserve" some variables between function calls. Variables normally "disappear" when a function closes, but React preserves state variables.

**What does useState return?**

It returns a pair of values: the current state and a function that updates it. This is why we write `const [count, setCount] = useState()`. This is similar to `this.state.count` and `this.setState` in a class, except you get them in a pair.

## hooks api

**Effect Hook**

The Effect Hook, useEffect, adds the ability to perform side effects from a function component. It serves the same purpose as `componentDidMount`, `componentDidUpdate`, and `componentWillUnmount` in React classes, but unified into a single API. 

**Rules of Hooks**

+ Only call Hooks at the top level. Don’t call Hooks inside loops, conditions, or nested functions. 
+ Only call Hooks from React function components. 


## Reference

+ [Hooks API Reference](https://reactjs.org/docs/hooks-reference.html)