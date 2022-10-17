# Callback Functions

A callback is passed as an argument to another function.

mostly with Async functions, where one waits on another, e.g file having to load

```
function display(some) {
  document.getElementById("demo").innerHTML = some;
}

const calc = (x,y, myCallback) =>{
 let sum = x + y;
 myCallback(sum)
}

calc(1,5,display)
```

<!-- Remember not to use () -->
