# Using the Effect Hook

The Effect Hook allows you to perform side effects in function components.

**There are two common kinds of side effects in React components:**
+ those that don’t require cleanup
+ and those that do.

## Effects Without Cleanup
The render method in React class components should not have any side effects. We usually want to perform our effects after React has refreshed the DOM, therefore this would be too early.This is why side effects are added to componentDidMount and componentDidUpdate in React classes.

In class, we must duplicate the code between these two lifecycle methods.This is due to the fact that in many circumstances, we want to conduct the same side effect regardless of whether the component was just mounted or changed. We'd like it to happen after every render, but React class components don't provide a method for it. We could extract a separate method, but then we'd have to call it twice.

## What does useEffect do?
By using this Hook, you tell React that your component needs to do something after render. React will remember the function you passed (we’ll refer to it as our “effect”), and call it later after performing the DOM updates. In this effect, we set the document title, but we could also perform data fetching or call some other imperative API.

## Why is useEffect called inside a component?
By including useEffect within the component, we can access the count state variable (or any props) directly from the effect. It's already in the function scope, so we don't need a new API to read it. Hooks support JavaScript closures and avoid providing React-specific APIs where JavaScript already has a solution.

## Does useEffect run after every render?
Yes! It is set to run after the first render and after each update by default. Instead of "mounting" and "updating," you might find it easier to conceive of effects as occurring "after render." React ensures that the DOM has been updated by the time the effects are executed.

## Effects with Cleanup
We investigated how to express side effects that do not necessitate any cleanup. Some consequences, however, do. For example, we may set up a subscription to an external data source. In that situation, we must clean up so that we do not introduce a memory leak.

You could imagine that performing the cleanup would necessitate the use of a separate effect. However, the code for adding and canceling subscriptions is so inextricably linked that useEffect is meant to keep it together. If your effect returns a function, React will execute it when it is time to clean up.

## Why did we return a function from our effect? 
This is an optional effect cleanup technique. Every effect has the option of returning a function that cleans up after itself. This allows us to maintain the logic for adding and removing subscriptions together. They're both contributing to the same outcome!

## When exactly does React clean up an effect?
When the component is unmounted, React cleans up. However, as we previously know, effects are applied to each render, not just the first. This is why React cleans up effects from earlier renders before running them again.