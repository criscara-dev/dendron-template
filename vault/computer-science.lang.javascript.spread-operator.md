---
id: 3d78f773-cd18-4629-a4a3-3a4ea7491511
title: Spread Operator
desc: ''
updated: 1612988000305
created: 1612987794837
---

## Spread operator

```javascript
let first = [1,2,3]
let second = [4,5,6]

first.push(...second)

console.log(first) // [1, 2, 3, 4, 5, 6]
```