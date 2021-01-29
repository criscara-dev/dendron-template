---
id: 2c9b8d93-23e8-496a-a14a-3b983e9a9852
title: Hof
desc: ''
updated: 1611953100012
created: 1611951943423
---

## HOF

A higher-order function is a function that either: 
(A) Accepts a function as an argument 
(B) and/or Returns a function

Lesson Overview 
1. Example of function that a function as an argument 

```javascript
document.addEventListener('click',callbackFunction)
```

2. Create an example function that returns a function 
```javascript
function createMultiplier(multiplier) { 
    return function(x) { 
        return x * multiplier
     }
 }
 let doubleMe = createMu1tip1ier(2) 
 let tripleMe = createMu1tip1ier(3) 
 let quadrupleMe = createMu1tip1ier(4)

quadrupleMe(4) // Expected: 16

```
3. Useful higher-order functions that are part of the language itself (and not just web browser jargon).
```javascript
// Those HOF have to deal with array
// forEach
let myColors = ['red', ' orange', 'yellow']
myColors.forEach(saySomething)
const saySomething = (color) => console.log(`I love the ${color} color!`)
// Map
myColors.map( color => console.log(`I love the ${color} color!`))
//Filter
myColors.filter( color => color == 'red').map( color => console.log(`I love the ${color} color!`))
```