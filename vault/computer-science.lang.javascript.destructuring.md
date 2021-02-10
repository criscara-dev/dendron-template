---
id: 65de3065-14d6-4168-a4f0-f95ca8fc9d3a
title: Destructuring
desc: ''
updated: 1612989064795
created: 1612988237858
---

## Destructuring

```javascript
var {color} = {
  color:'red'
}

console.log(color) // 'red'
```

```javascript
function generateObj(){
return {
color: "blue",
name: "John"
state: "New York",
position: "Forard"
    }
}

var {name: firstName, state: Location} = generateObj();
console.log(firstName); // John
console.log (Location); // New York

---

var [first,,,,fifth] = ["red", "yellow", "green" ,"blue" ,"Orange" ] ;
console.log( first) // red
console.log( fifth)  // orange

```