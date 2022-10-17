# JavaScript Skills You Need For React (+ Practical Examples)

[According to Reed Barger](https://www.freecodecamp.org/news/javascript-skills-you-need-for-react-practical-examples/)

### 1. Function Declarations and Arrow Functions

There a 2 ways of writting funtions in React:

- using the function keyword
- arrow functions

```
function JavascriptFunction(){
    return 'Hello';
}

const MyComponent = () =>{
    return 'hello';
}

```

Key things to remember with arrow functions:

- if no arguments, we use empty () in decleration

```
const MyComponent = () =>{
    return 'hello';
}
```

- when there's one argument we may omit the ()

```
const MyComponent = name =>{
    return name;
}
```

- shortcut to use when returning a value(shorthand)

```
const MyComponent = name => name
<!-- equals to above  -->
```

### 2. Template Literals
