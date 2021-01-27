---
id: 8cf2c2a1-a833-48f5-93d8-928fb316ee76
title: React
desc: ''
updated: 1611691752478
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
The time value in the snippet is a state component: this means that is going to change based on something (the function `new date()` ) and re-load.
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
  // set useState initial value and is returning an array with 2 items: [ how we can access the value, function to how we can update the value]
 const [theTime,setTheTime] = useState(new Date().toLocaleString()) 
 // then we set the timeout function
 setTimeout( () => setTheTime(new Date().toLocaleString()),1000)
 return <p>The current time is {theTime}.</p>
}
const Small =()=> <small>Copyright Footer Text</small>
const Pet=({name,species,age})=> <li>`{name} is a {species} and is a {age} years old.`</li>

ReactDOM.render( <OurApp/>,document.querySelector("#app"));
```
---

## Handling events

ex. Respond to a user event using `state` that re-render the part of the UI that has changed
```javascript
const LikeArea = ()=>{
  const [likeCount,setLikeCount]=useState(0) // initial value for the counter + destructuring the array of values
  const increaseLikeHandler=()=>setLikeCount( prev => prev +=1)
  const decreaseLikeHandler=()=>setLikeCount( prev => prev > 0 ? prev -=1 : 0)
  
  return(
    <>
      <button onClick={increaseLikeHandler}> Increase likes</button>
      <button onClick={decreaseLikeHandler}> Decrease likes</button>
      <h2>This page has been like {likeCount} times.</h2>
      </>
  )
}
```
  Don't mutate the State, you want React handle things from there

---

## useEffect to create persistency in data in the context of React

Can be used twice:
```javascript
// Only run once the first time this component is rendered
useEffect( ()=> {
  // for instance 
 if (localStorage.getItem('exampleData')){
   setArraydata(JSON.parse(localStorage.getItem('exampleData'))) // function that let set update the state in the component
 }
}, [])
// run every time our pet state changes ... and save it to the local Storage, for instance
useEffect(()=>{
  localStorage.setItem('exampleData',JSON.stringify(array))
}, [array])
```

Using localStorage from the browser and useEffect in React

---

## Prepare to start a project

Checklist

- [ ] Node is installed 
- [ ] run `npm init -y` 
- [ ] to run `npm install react react-dom` 
- [ ] to run React in the browser install _webpack_ from npm 
- [ ] to run `npm install webpack webpack-cli webpack-dev-server`
- [ ] create a file in the root folder _webpack.config.js_ and add this configutation code:
  ```javascript
  const path = require("path")
    module.exports = {
      entry: "./app/Main.js",
      output: {
        publicPath: "/",
        path: path.resolve(__dirname, "app"),
        filename: "bundled.js"
      },
      mode: "development",
      devtool: "source-map",
      devServer: {
        port: 3000,
        contentBase: path.join(__dirname, "app"),
        hot: true,
        historyApiFallback: { index: "index.html" }
      },
      module: {
        rules: [
          {
            test: /\.js$/,
            exclude: /(node_modules)/,
            use: {
              loader: "babel-loader",
              options: {
                presets: ["@babel/preset-react", ["@babel/preset-env", { targets: { node: "12" } }]]
              }
            }
          }
        ]
      }
    }
    ```

- [ ] to run:  `npm install @babel/core @babel/preset-env @babel/preset-react babel-loader`
- [ ] add this to package.json: 
  ```javascript
  "scripts": {
    "dev":"webpack serve",
    "test": "echo \"Error: no test specified\" && exit 1"
  }, ```
- [ ] `npm run dev`  
- [ ] under `React.render(...|)` add: `if (module.hot) {module.hot.accept()}`
 
---

## Move between pages
Client-side routing
- [ ] run in terminal: `npm install react-router-dom` or `npm i react-router-dom`
- [ ] import in the main App JS adding: `import {BrowserRouter, Switch, Route } from 'react-router-dom'`

We are not using server-side routing so we cannot use traditional html tag and its attribute `<a href="">`;
In React become `<Link to="">` tag; and where we want to use them we need to import: `import {Link} from 'react-router-dom'`

## Created Container and Page components in order to sue Composition over Inheritance and avoid to reuse the same code in different places.

- Use of `{props.children}` inside Parent component to show children content component.