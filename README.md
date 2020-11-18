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
