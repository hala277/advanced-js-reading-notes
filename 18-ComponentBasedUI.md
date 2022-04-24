# Component Based UI

## react hello world

```ReactDOM
  .createRoot(document.getElementById('root'))
  .render(<h1>Hello, world!</h1>);
  ```

## Introducing JSX

```js
const element = <h1>Hello, world!</h1>;
```

This tag syntax isn't a string or an HTML document.It's called JSX, and it's a JavaScript syntax extension. It's best to use it alongside React to describe how the UI should look. JSX looks like a template language, but it has all of JavaScript's capabilities.

### Why JSX?

React recognizes that rendering logic is inextricably linked to other UI logic, such as how events are handled, state changes over time, and data preparation for display.React separates issues through loosely connected units called "components" that incorporate both, rather than artificially dividing technologies by putting markup and functionality in separate files. We'll return to components in a later section, but if you're still hesitant to use JS for markup, this talk might persuade you otherwise.Although using JSX isn't required by React, most people find it useful as a visual aid when dealing with UI in JavaScript code. React can now provide more informative error and warning messages.

## Rendering Elements

**Elements are the smallest building blocks of React apps.**

An element describes what you want to see on the screen:

```js
const element = <h1>Hello, world</h1>;
```

React elements, unlike browser DOM elements, are simple objects that are easy to generate. The DOM is updated to match the React elements by React DOM.

**DOM:** 
The Document Object Model (DOM) is a data representation of the objects that make up a web document's structure and content. This guide will cover how to leverage APIs to generate online content and applications, as well as how to use the DOM to represent an HTML document in memory.

A single root DOM node is typically used in React applications. You can have as many segregated root DOM nodes as you like when integrating React into an existing project.To render a React element, first pass the DOM element to `ReactDOM.createRoot()`, then pass the React element to `root.render()`.
