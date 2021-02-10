---
id: 019f2058-f7d2-4248-a9df-2d2fd48e6e47
title: Promises
desc: ''
updated: 1612990505837
created: 1605287154744
---

#### [One of the best courses on ES6 Promises](https://egghead.io/courses/javascript-promises-in-depth?ck_subscriber_id=483924252)


Basic starting point
```javascript

var d = new Promise( (resolve,reject) => {
    setTimeout( () =>{
      if(true){
        resolve('ok')
    } else {
        reject('No ok')
    }
    }
      ,2000)
});

d.then( data => console.log(`Sucess: ${data}`))
.catch( (error) => console.log(`Error: ${error}`)); 
// or: d.catch( (error) => console.log(`Error: ${error}`)); 
```