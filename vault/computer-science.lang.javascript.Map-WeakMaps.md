---
id: f8b2e73f-6d8e-489a-b0ab-5c3900d05117
title: Maps and WeakMaps
desc: ''
updated: 1613055335417
created: 1613054307865
---

# Maps and WeakMaps

Maps offers thing that we don't get from Objects
In Objects keys are strings while in Maps they can be functions, an Object, a Primitive
Maps have methods can then quickly get the size


```javascript
//Maps and WeakMaps with ES6

var myMap = new Map();

//API
/*
set()
get()
size
clear()
has()
*/

var myObj = {};
var myFunc = function(){};

myMap.set(myObj, 'bar');
myMap.set(myFunc, 'world');
myMap.set('string', 2);

console.log('get on myMap = ' + myMap.get(myObj)) || displayInPreview('get on myMap = ' + myMap.get(myObj));

//myMap.clear();

console.log('has on non-existing key = ' + myMap.has('qwerty')) || displayInPreview('has on non-existing key = ' + myMap.has('qwerty'));

//Iterators
//keys()
//entries()
//values

for(var [key, value] of myMap.entries()){
  console.log(key + ' = ' + value) || displayInPreview(key + ' = ' + value);
}

//WeakMap Restrictions
/*
Because no references to keys are stored we do not have access to methods that require the ability to iterate the map such as:
keys()
values()
entries()
AND
clear()
*/
var myWeakMap = new WeakMap();

var myObj2 = {};
var myFunc2 = function(){};

myMap.set(myObj2, 'bar');
myMap.set(myFunc2, 'world');

console.log(myMap.get(myObj)) || displayInPreview(myMap.get(myObj));



// display in plunker preview
function displayInPreview(string) {
  var newDiv = document.createElement("div"); 
  var newContent = document.createTextNode(string); 
  newDiv.appendChild(newContent);
  document.body.appendChild(newDiv)
}
```