---
id: 53f601c5-a9fa-4ad6-9b86-e810726e76ea
title: Objects
desc: ''
updated: 1611666379466
created: 1611666250726
---




## Composition over Inheritance

> [But the really big problem with inheritance is that you’re encouraged to predict the future. Inheritance encourages you to build this taxonomy of objects very early on in your project, and you are most likely going to make design mistakes doing that, because humans cannot predict the future (even though it feels like we can), and getting out of these inheritiance taxonomies is a lot harder than getting out of them.](https://medium.com/humans-create-software/composition-over-inheritance-cb6f88070205)

Ex. using `Object.assign()`:

```javascript 
const barker = (state) => ({
  bark: () => console.log('Woof, I am ' + state.name)
})
const driver = (state) => ({
  drive: () => state.position = state.position + state.speed
})
const murderRobotDog = (name)  => {
  let state = {
    name,
    speed: 100,
    position: 0
  }
  return Object.assign(
        {},
        barker(state),
        driver(state)
    )
}
const bruno =  murderRobotDog('bruno')
bruno.bark()
```