# COMMON REACT Interview Questions

[Link](https://www.youtube.com/watch?v=v6Myf4WoL00)

Notes:

### What is React?

React is an open-source JavaScript frontend library for creating user interfaces. It uses component-based approach to create complicated, interactive web and mobile user interfaces.

Developing a single-page application with React is effortless especially using the integrated toolchain called Create React App.

### What are the advantages of React?

First is the increased performance with Virtual DOM. React is insanely blazing fast.
Second, React uses JSX that makes code painless to read and write.
Third, React works on both the client and server-side.
Fourth, it is simple to integrate this library with other frameworks since it is only a view library.
Last, it is easy to write unit tests.

### What is JSX?

JSX is a syntax extension to JavaScript that describes what the UI should look with the full power of JavaScript. JSX provides syntactic sugar for the React.createElement() function.

### What is the difference between Element and Component?

React elements are the building blocks of React applications.
It describes what you want to see on the screen. React elements are immutable.

React components are small, reusable pieces of code that return a React element to be rendered to the page.

You can say that a component is a factory for creating multiple elements.

### What is react fragments?

Fragments let you group a list of children without adding extra nodes to the DOM because fragments are not rendered to the DOM.

This is also very useful for CSS Flexbox and Grid as they have a special parent-to-child relationship as adding an extra tag in between will break the layout.

### What is prop in React?

Props or properties are arguments passed into React components. It contains data coming down from a parent component to a child component.

### What is "key" prop?

Keys help react identify which elements were added, changed or updated, and removed. It should be given to array elements to provide a unique identity for each element.

React would be able to reorder elements without needing to re-evaluate as much.

### What is state in React?

State holds some information that may change over the lifetime of the component. It is private and fully controlled by the component until the owner component decides to pass it.

State Management?
Prop Trailing?

### Why should we not update the state directly?

Updating the state directly, like below will not cause the component to re-render.

Instead, use setState() method. This method will schedule an update to a component's state object. When state changes, the component responds by re-rendering.

### What are lifecycle methods?

Lifecycle methods are custom functionality that gets executed during the different phases of a component.

These are methods are available when the component gets created or inserted into the DOM.

### What are Controlled and Uncontrolled Component?

A Controlled Component is one that takes a value through props and notify changes through callbacks like onChange or onClick.

Form data is handled by React component.

Uncontrolled Component is one that stores its own state internally, and queries the DOM using a ref or reference to find the current value when it is needed.

Form data is handled by the DOM.

In most cases, Controlled components are recommended to be used when implement forms.

### What is the use of refs?

The ref is used to return a reference to the element. They can be useful when you need direct access to the DOM element or an instance of a component.

### Why should component names start with capital letters?

The type of a component is determined by the way the tags are named. Both capitalized and dot notations are treated as React component while lowercase are treated as DOM elements.

### What is Virtual DOM?

Virtual DOM or VDOM is lightweight JavaScript representation of the DOM. The representation of User Interface is kept in memory and synced with the "real" DOM. Update on virtual DOM is cheaper and faster than updating the actual DOM.

When React finds the differences between the previous virtual DOM and the current virtual DOM, it only makes the necessary changes to the actual DOM.

# ADVANCE REACT Interview Questions

[link](https://www.youtube.com/watch?v=mYnsLOAIOCc)

### What are React Hooks?

They let you use state and other React features without converting functional components to a class. Hooks does the same job with less code and with less code means less chances of producing bugs.

- Basic Hooks

  - useState
  - useEffect
  - useContext

- Additional Hooks

  - useReducer
  - useCallback
  - useMemo
  - useRef
  - useImperativeHandle
  - useLayoutEffect
  - useDebugValue

- Rules to follow?
  - only call hooks on the highest level in our components, meaning we should never call hooks inside functions, loops, etc
  - only called in functional components

### What is context?

Context provides a way to pass data through component tree without having to pass props down manually at every level. It is designed to share data that can be considered “global” for a tree of React components.

### How to pass data between components?

1. To pass data from parent to child, use props
2. To pass data from child to parent, use callbacks
3. To pass data among siblings AND anywhere else
   - use React’s Context API also use state management libraries

### What are some limitations of React?

First, JSX can make the coding complex. It will have a steep learning curve for the beginners
Second, React documentation is not user friendly and thorough as it should be.
Third, every React project are unique to engineers as they will rely on numerous r technologies to incorporate in their projects.

### What is prop drilling and how can you avoid it?

Prop Drilling is the process by which data is passed from one component to deeply nested components.

A common approach to avoid prop drilling is to use React context and state management libraries.

### What is the use of dangerouslySetInnerHTML?

This property is React’s replacement for using innerHTML in the browser.
This property can be used to render raw HTML in a component.

### Name a few techniques to optimize React app performance.

First, Use React.Suspense and React.Lazy for Lazy Loading Components
This will only load component when it is needed.
Second, Use React.memo for Component Memoization
React.memo is a higher order component that will render the component and memoizes the result. Before the next render, if the new props are the same, React reuses the memoized result skipping the next rendering

Third, Use React.Fragment to Avoid Adding Extra Nodes to the DOM
React Fragments do not produce any extra elements in the DOM
Fragment’s child components will be rendered without any wrapping DOM node.

This is a cleaner alternative rather than adding divs in the code.

Fourth, Use Reselect / Re-reselect in Redux to Avoid Frequent Re-render
Reselect is a library for building memoized selectors that is commonly used for redux.

Re-reselect is a lightweight wrapper around Reselect to enhance selectors with deeper memoization and cache management.

Last, Use Production Build
Ensure that application is bundled for production before deploying.

### What is reconciliation?

When a component's props or state change, React decides whether an actual DOM update is necessary by comparing the newly returned element with the previously rendered one. When they are not equal, React will update the DOM.

### What are Higher-Order Components?

A higher-order component (HOC) is an advanced technique in React for reusing component logic. It is a function that takes a component and returns a new component.

### What is children prop?

It is a prop that allow us to pass components as data to other components, just like any other prop. Component tree between the component's opening tag and closing tag will be passed to that component as children prop.

### How to pass a parameter to an event handler or callback?

You can use an arrow function to wrap around an event handler and pass parameters:

You can also pass arguments to a function which is defined as arrow function

### Why do we need to pass a function to setState()?

setState() is an asynchronous operation.
React batches state changes for performance reasons. This means state may not change immediately after setState() is called.

We should not rely on the current state when calling setState() since we can't be sure what that state will be.

The solution is to pass a function to setState(), with the previous state as an argument.

### Design Patterns?

- MVC
  divinding over code into sections
