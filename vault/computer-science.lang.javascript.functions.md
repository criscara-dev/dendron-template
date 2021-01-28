---
id: ecfa7ea8-9d93-4ceb-a87a-b1b55949d9e5
title: Functions
desc: ''
updated: 1611775498680
created: 1603037324435
stub: false
---
# Functions

Is like a verb.
 
- How to create the recipe, the logic?
```javascript  {.line-numbers highlight=1}
function functionName(argument){
    // code to execute
    console.log(`My name is ${argument}.` );
    // Excpectred result: My name is Cristian.
}
```

- A function in the 'purest' form return a value:
```javascript
function triple(num){
   return num * 3; 
    // Excpectred result: My name is Cristian.
}
```

in ES6
```javascript
const triple = (num) => { 
    return num * 3;
}
// or since only 1 return statement
const triple = num => num * 3
```

- To call a function, use this format:
```javascript
functionName(argument) 
```

> Summary:
In the function we can pass argument(s)
A function can 'return' a value ( or do something else, like set another value... )
I can create a variable that points to the returned value.
