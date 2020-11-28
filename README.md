# Notes

## Tutorial - 1 - Introduction

### What are Hooks?

Hooks are a new feature addition in React version 16.8 which allow us to use React features without having to write a class.

Eg: State of a component

Hooks don't work inside classes.

### Why Hooks?

Reason Set 1

Understanding how _this_ keyword works in JS

Remember to bind event handlers in class components

Classes don't minify very well and make hot reloading very unreliable.

Reason Set 2

There is no particular way to reuse stateful component logic

HOC and render props patters do address this problem

Makes the code harder to follow

There is a need to share stateful logic in a better way.

Reason Set 3

Create component for complex scenarios such as data fetching and subscribe to events

Related code is not organized in one place

Eg: Data fetching - in componentDidMount and ComponentDidUpdate

Eg: Event listeners - in componentDidMount and componentWillUnmount

Due to stateful logic - Cannot break components into smaller ones

### Noteworthy Point

React version 16.8 or higher

Completely opt in

Hooks don't contain any breaking changes and the release is 100% backwards compatible

Classes won't be removed from React

Can't use Hooks inside of a class component

Hooks don't replace the existing knowledge of React concepts

Instead Hooks provide a more direct API to the React concepts you already know.

## Tutorial - 2 - useState Hook

### Rules of Hooks

**Only Call Hooks at the top level**

Don't call Hooks inside loops, conditions, or nested functions

**Only Call Hooks from React Functions**

Call them from within React functional components and not just any regular JS function.

## Tutorial - 4 - useState with object

useState does not automatically merge and update the object. This is a key difference to setState which we come across in class variables. We have to do this manually using the spread operator.

## Tutorial - 5 - useState with array

The useState hook lets us add state to functional components

In classes, the state is always an object

With the useState hook, the stae doesn't have to be an object

the UseState hook returns an array with 2 elements

The first element is the current value of the state and the second element is state setter function

New state value depends on the previous state value> You can pass a function to the setter function

When dealing with objects or arrays, always make sure to spread your state variables and then call the setter function

## Tutorial - 6 - useEffect Hook

The Effect Hook lets you perform side effects in functional components

It is a close replacement for componentDidMount, componentDidUpdate and componentWillUnmount.

## Tutorial - 7 - useEffect after render

useEffect runs after every render.

useEffect is placed inside the component

## Tutorial - 8 - Conditionally run effects

When the useEffect runs after every render can be a reason for performance issues. Here we look for ways to mediate that issue.

## Tutorial - 18 - useReducer Hook

useReducer is a hook that is used for state management

It is an alternative to useState

What's the difference?

useState is built using useReducer

When to use useReducer vs useState?

### Hooks so far

useState - state

useEffect - side effects

useContext - context API

useReducer - reducers

| reduce in JS                                       | useReducer in React                                          |
| -------------------------------------------------- | ------------------------------------------------------------ |
| array.**reduce(reducer,** initialValue)            | **useReducer(reducer,** initialState)                        |
| singleValue = **reducer** (accumulator, itemValue) | newState = **reducer** (currentState, action)                |
| **reduce** method returns a single value           | **useReducer** returns a pair of value, [newState, dispatch] |

## useState vs useReducer

| Scenerio                    | useState                | useReducer             |
| --------------------------- | ----------------------- | ---------------------- |
| Type of state               | Number, String, Boolean | Object or Array        |
| Number of state transitions | One or Two              | Too many               |
| Related state transitions ? | No                      | Yes                    |
| Business logic              | No business logic       | Complex business logic |
| Local vs global             | Local                   | Global                 |
