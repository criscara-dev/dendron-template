---
id: 7f9c3b62-bc89-427c-a78d-1c38de7b9c8d
title: Object
desc: ''
updated: 1602348869815
created: 1602348869815
stub: false
---
# Object

ex.

Object is a data structure that contain properties and methods (functions)

Generic template
```javascript
let cat = {
    property1:'string',
    property2:boolean,
    property3:number,
    method(){ 
        console.log('some text...')
        or
        return value;
        }
    }
```
example:
```javascript
let cat = {
    name:'Purr',
    eyeColor:'grey',
    age:7,
    nice:true,
    meow(){ console.log('Mewwww!!!!')
        }
    }
```

how to use the object?
```javascript
cat.name
// result: Misha
cat.meow()
// result: Meow!!!!
```

Browser objects have their own props and methods:
```javascript
document.addEventListener('event we are listening', callback_function)
```



Summary:
You can nest object(s) into object
some objects (like the browser _window_ or _document_ object) have already their own methods and properties. 
