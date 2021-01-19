---
id: 8cf2c2a1-a833-48f5-93d8-928fb316ee76
title: React
desc: ''
updated: 1611087731628
created: 1611082314842
---

# React

## Preparation

Two Questions
 1. What is React? 
 2. What problem does React solve? 

 - Look at Approach #1 (DOM Focused) 
 - Look at Approach #2 (Data / Declarative view)

react ==reacts== to changes in your JS and reload just what has changed making the App faster, reactive and performant

---

## Basic React
A React component is a function, written a normal or ES6 function:

```javascript
const App=()=> return(
    <>
    <OurHeader />
       <TimeArea />
       <Small />
    </>
)

const OurHeader=()=> <h1 className="special">Our amazing app header</h1>
const TimeArea =()=><p>The current time is {new Date().toLocaleString()}.</p>
const Small = () => <small>Copyright Footer Text</small>

// React.render(what, where)
setInterval(()=>ReactDOM.render( <OurApp/>,document.querySelector("#app")),1000);
```

 ## Props
 In React we cannot only use attributes such as: href, src,id,class etc. but as well properties or "props"

   ```javascript {.line-numbers}
    const OurApp = () =>{
    return (
        <>
        <OurHeader />
        <TimeArea />
        <ul>
            <Pet name="Meowalot" species="cat" age="5" />
            <Pet name="Barksalot" species="dog" age="2" />
            <Pet name="Fluffy" species="rubbit" age="3" />
        </ul>
        <Small />
        </>
    )
    }

    const OurHeader=()=> <h1 className="special">Our amazing app header</h1>
    const TimeArea =()=><p>The current time is {new Date().toLocaleString()}.</p>
    const Small =()=> <small>Copyright Footer Text</small>
    const Pet=(props)=> <li>`{props.name} is a {props.species} and is a {props.age} years old.`</li>

    setInterval(()=>ReactDOM.render( <OurApp/>,document.querySelector("#app")),1000);
   ```

and with some [destructuring assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment), an ES6 feature:
```javascript {.line-numbers highlight=19}
const OurApp = () =>{
   return (
     <>
       <OurHeader />
       <TimeArea />
       <ul>
         <Pet name="Meowalot" species="cat" age="5" />
         <Pet name="Barksalot" species="dog" age="2" />
         <Pet name="Fluffy" species="rubbit" age="3" />
       </ul>
       <Small />
     </>
   )
}

const OurHeader=()=> <h1 className="special">Our amazing app header</h1>
const TimeArea =()=><p>The current time is {new Date().toLocaleString()}.</p>
const Small =()=> <small>Copyright Footer Text</small>
const Pet=({name,species,age})=> <li>`{name} is a {species} and is a {age} years old.`</li>
// Above here the destructuring assignment

setInterval(()=>ReactDOM.render( <OurApp/>,document.querySelector("#app")),1000);
```
    
  ![](/assets/images/2021-01-19-19-11-42.png)

## Loop through collection in JSX

```javascript {.line-numbers highlight=15}
const pets = [
  { name: "Meowsalot", species: "cat", age: "5", id: 123456789 },
  { name: "Barksalot", species: "dog", age: "3", id: 987654321 },
  { name: "Fluffy", species: "rabbit", age: "2", id: 123123123 },
  { name: "Purrsloud", species: "cat", age: "1", id: 456456456 },
  { name: "Paws", species: "dog", age: "6", id: 789789789 }
]

const OurApp = () =>{
   return (
     <>
       <OurHeader />
       <TimeArea />
       <ul>
         {pets.map( pet=><Pet name={pet.name} species={pet.species} age={pet.age} key={pet.id} /> )}
       </ul>
       <Small />
     </>
   )
}

const OurHeader=()=> <h1 className="special">Our amazing app header</h1>
const TimeArea =()=><p>The current time is {new Date().toLocaleString()}.</p>
const Small =()=> <small>Copyright Footer Text</small>
const Pet=({name,species,age})=> <li>`{name} is a {species} and is a {age} years old.`</li>

setInterval(()=>ReactDOM.render( <OurApp/>,document.querySelector("#app")),1000);
```

## State
What is state?
The time value in the snippet is a state component.
How do we start working with state data?

Check the comments in the code snippets

```javascript {.line-numbers highlight=15}
// Below we declare the pointer to the React object that has a propertiy called useState to manage state.
const useState = React.useState;

const pets = [
  { name: "Meowsalot", species: "cat", age: "5", id: 123456789 },
  { name: "Barksalot", species: "dog", age: "3", id: 987654321 },
  { name: "Fluffy", species: "rabbit", age: "2", id: 123123123 },
  { name: "Purrsloud", species: "cat", age: "1", id: 456456456 },
  { name: "Paws", species: "dog", age: "6", id: 789789789 }
]

const OurApp = () =>{
   return (
     <>
       <OurHeader />
       <TimeArea />
       <ul>
         {pets.map( pet=><Pet name={pet.name} species={pet.species} age={pet.age} key={pet.id} /> )}
       </ul>
       <Small />
     </>
   )
}

const OurHeader=()=> <h1 className="special">Our amazing app header</h1>
const TimeArea =()=>{
  // useState is returning an array with 2 items: [ how we can access the value, function to how we can update the value]
 const [theTime,setTheTime] = useState(new Date().toLocaleString()) 
 // then we set the timeout function
 setTimeout( ()=> setTheTime(new Date().toLocaleString()),1000)
 return <p>The current time is {theTime}.</p>
}
const Small =()=> <small>Copyright Footer Text</small>
const Pet=({name,species,age})=> <li>`{name} is a {species} and is a {age} years old.`</li>

ReactDOM.render( <OurApp/>,document.querySelector("#app"));
```
---

## Handling events