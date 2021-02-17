---
id: c09bdffd-c5ee-4aab-a266-6ca551d995c3
title: Rest Parameters
desc: ''
updated: 1613055265649
created: 1613054902886
---

## Rest parameters

```javascript
//rest parameters vs arguments keyword

function Store() {
  var aisle = {
    fruit: [],
    vegetalbe: []
  }
  return {
    //Store().add('category', 'item1', 'item2');
    add: function(category, ...items) {
      //var items = [].splice.call(arguments, 1);
      console.log(items) || displayInPreview(items);
      items.forEach(function(value, index, array) {
        aisle[category].push(value);
      });
    },
    aisle: aisle
  }
}

var myGroceryStore = new Store();

myGroceryStore.add('fruit', 'apples', 'oranges');
console.log(myGroceryStore.aisle) || displayInPreview(myGroceryStore.aisle.fruit);

```