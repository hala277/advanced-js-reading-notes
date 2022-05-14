# Context API

## Context
Context allows you to transfer data down the component tree without having to explicitly pass props at each level.

### When to Use Context?
Context is used to exchange information that is deemed "global" for a React component tree, such as the current authorized user, theme, or chosen language.When numerous components at various nesting levels need access to the same data, context is employed. It should be used with caution because it makes component reuse more difficult.

### API

+ **React.createContext**

`const MyContext = React.createContext(defaultValue);`

This method creates a Context object. React will read the current context value from the closest matching Provider above it in the tree when rendering a component that subscribes to this Context object.

When a component doesn't have a matching Provider above it in the tree, the defaultValue parameter is utilized. This default value is useful for testing components without enclosing them in a container. Note that supplying undefined as a Provider value does not force defaultValue to be used by consuming components.

+ **Context.Provider**

`<MyContext.Provider value={/* some value */}>`

A Provider React component is included with every Context object, allowing consuming components to subscribe to context changes.

A value prop is supplied to consuming components that are descendants of this Provider by the Provider component. Many consumers can be connected to a single provider. To override values farther down the tree, providers can be nested.

+ **Class.contextType**

A Context object created by React can be applied to a class's contextType attribute. createContext(). This property allows you to use this.context to get the closest current value of that Context type. Any of the lifecycle methods, including the render function, can reference this.

+ **Context.Consumer**

```js
<MyContext.Consumer>
  {value => /* render something based on the context value */}
</MyContext.Consumer>
```

A React component that listens for changes in the context. You can subscribe to a context within a function component by using this component.

A child function is required. The current context value is passed to the function, which returns a React node. The value prop of the closest Provider for this context above in the tree will be provided as the value argument to the function. If no Provider is specified for this context, the value parameter will be the defaultValue supplied to createContext ().

+ **Context.displayName**

Context object accepts a displayName string property. React DevTools uses this string to determine what to display for the context.






