# Context API 2

## Context
Context allows you to transfer data down the component tree without having to explicitly pass props at each level.

### When to Use Context?
Context is used to exchange information that is deemed "global" for a React component tree, such as the current authorized user, theme, or chosen language.When numerous components at various nesting levels need access to the same data, context is employed. It should be used with caution because it makes component reuse more difficult.

### Context Update from a Nested Component
It's common to need to change the context from a component that's deep down in the component tree. You can pass a function down the context in this scenario to allow consumers to update the context.

### Consuming Multiple Contexts: 
React needs to create each context consumer a different node in the tree to maintain context re-rendering fast.

### Caveats:
When a provider's parent re-renderings, context uses reference identity to determine when to re-render, there are several gotchas that could cause inadvertent renders in consumers.

