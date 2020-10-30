---
id: 610f14a0-d106-42be-ab42-1b21603ec3a6
title: Decision
desc: ''
updated: 1603222895573
created: 1603222895573
stub: false
---

# Decisions

 #if statement:
 ```javascript {.line-numbers }
 let strawberryCount = 20;
  // if the condition is not true (false) using: !
// if (!strawberryCount > 9) {
    // or asking if variable exist
    // if (strawberryCount) {
 // if the condition is true
if (strawberryCount > 9) {
    console.log("Congrats!") } else {
        console.log("Sorry!")
    }
    // Congrats!
 ```

 #ternary operator:
 ```javascript {.line-numbers }
 let strawberryCount = 20;
strawberryCount > 9 ? console.log("Congrats!") : console.log("Sorry!")
// Congrats!
 ```

 #while 
 ```javascript {.line-numbers }
let strawberryCount = 2;
while (strawberryCount < 200) {
    console.log(`There are ${strawberryCount} strawberry`)
    strawberryCount+=1;
    // strawberryCount++;
    }
```

 Summary
 > Decision use a #Boolean to evaluate the condition.
 this Boolean can be as well 'truty' or 'falsy'
 while is running until the condition evaluate to false. DONT forget to increase/decrease the counter to avoid the ♾️ loop.
