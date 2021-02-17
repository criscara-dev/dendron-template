---
id: 572e82af-7014-4202-8291-78abe99718fa
title: Modules
desc: ''
updated: 1613058712342
created: 1612989115359
---

## Modules

Import
```javascript
import {name} from "<path>";
```
or with `alias`
```javascript
import {name as n} from "<path>";

n('John','Doe')  // John Doe
```


Export
```javascript

export function name(first, second) {
  console.log(`${first} ${second}`)
}
name('John','Doe') // John Doe
```
or
```javascript

function name(first, second) {
  console.log(`${first} ${second}`)
}
name('John','Doe') // John Doe

export { name };
```
or
```javascript

export function name(first, second) {
  console.log(`${first} ${second}`)
}
name('John','Doe') // John DOe
```