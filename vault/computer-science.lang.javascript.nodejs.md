---
id: 0b782372-9d92-4227-9895-a846ed7364ed
title: Nodejs
desc: ''
updated: 1604526640664
created: 1602530634233
stub: false
---

# Node


<details><summary>
What is a server?
</summary>
A Computer that we're talking to in order to send and receive data.
In fact one App request data to a server that send back a response.
- communication
- Server is a trust environment
- JS server-side is NodeJS
</details>

<details><summary>
What is Node
</summary>

Node is a runtime environment, 
can do computerish things while JS can only do Browser things.
</details>

<details><summary>
How execute files in Node?
</summary>
ex. file name app.js
Terminal -> > Node app
</details>

<details><summary>
How to star a basic server?
</summary>

```javascript
let http = require("http");
let ourApp = http.createServer((req, res) => {
  // console.log(req.url);
  if (req.url == "/") {
    res.end("Hello, welcome to our website");
  }
  if (req.url == "/about") {
    res.end("Thanks for visiting us");
  }
  res.end("page not available, sorry.");
});
ourApp.listen(3000);

// Terminal command: Node test
```
</details>


<details><summary>
What is Express?
</summary>
Fast, unopinionated, minimalist web framework for Node.js
</details>

<details><summary>
Which tech brought success to Node?
</summary>
NPM, MongoDB, RESTful API and JSON, ExpressJS.
</details>

<details><summary>
Basics before Node
</summary>

#Interpreters -> execute directly source code (basically they read and compile); an example is #v8 Chrome JS engine.
#Compilers -> from source they create an executable file (a file a computer can execute)
#transpilers -> one source code into another source code (CoffeeScript into JS, Less in CSS)
Modern day computer understand 1010001011...( #low-level ) you normally write #high-level code / language
</details>

<details><summary>
What is Node exactly?
</summary>

web browser App take the #source-code to ->  #v8 ... -> execute.
Node is a #server-side javascript #runtime-environment.
Is built on top of #v8 Chrome JS engine.
#v8 can be called as well a JavaScript #interpreter
It's a #C++ application that now run 2 Apps:
- Script processor: in Terminal use cmd: > Node fileName
- REPL (start after you typed Node as a cmd)
It's #non-blocking-IO (tasks keeping to be added to the task list) and has a #single-threated (one task at the time) but at the same time, ==it can schedule thing for later and can keep prioritising tasks as they get added==
When you run a Node App you just specified and 'entry file'.

- you use Node specifying the file required:
```javascript
 // where I need the file
var lib = require('./lib')
 // to export the file
module.exports = whatever
```
</details>

<details><summary>
What is a REPL?
</summary>
Read Eval Print Loop (infinite repeated task)
</details>

<details><summary>
 #Node-conventions?
</summary>

- package.json:
  * it contain project basic info
  * dependencies (external code that I want to leverage on my app)
- package-lock.json: the exact version used to create the App is 'locked' so, future updates cannot break my App
- .npmrc: contain a token that let you to do things but only for you, not an anonymous user
- common testing files contain:
  * travis.yml
  * jshintrc
- #VCS normally as a:
  * .git file
  * .gitignore
- readme.md: normally in the root directory
- code comments rules (above code):
  * @Param
  * @TODO
  * @Author
  * @Date
  (or just use GIT that better comment who's doing what etc. )
- environments and configuration:
  * start App with: NODE_ENV=myEnvironmentName node index.js
  in a congif.js file
  * and used a switch as: process.env.NODE_ENV
- Start your app with every configuration variable you're going to need for that environment:
DBpassword=myDBpassword apiToken=mySecretToken
port=thePortlShouldRunOn foo=bar node index.js
- .env file ignore by source control
- style guide for Node: Airbnb and linters such as: jshint and jslint
- error handling:
  Functions should callback two parameters
  - An error (if any)
  - Data being returned (if any)
  - ErrBack (from Express convention):
  ```javascript
  exampleFunction(function(err,data){
  // Check the error
  // Do stuff with the data
  });
  ```
- avoid throwing Exceptions 'cause it kill the App since Node is single-threaded
- avoid use G lobals since create polluted namespaces
</details>

<details><summary>
From server-side to the browser, what is not available in Node that is exclusive of the browser?
</summary>

| &nbsp; | &nbsp; |
|--|--|
window.open | document
window.location | document.body
window.navigator | onchange
window.origin | onclick
window.focus | onblur
window.blur | oncopy
window.scroll | oncut
window.alert | onscroll
window.localstorage | onmouseenter
window.onload | onmouseleave
</details>

<details><summary>
From the browser to server-side, what is not available in the browser that is exclusive of the Node?
</summary>
Interact with the Filesystem, with the OS etc. and there's no way End users can see your code.
</details>

<details><summary>
cmd to generate keys for HTTPS?
</summary>

## Keygen cmd: | openssl req -newkey rsa:2048 -new -nodes -x509 -days 3650 -keyout key.pem -out cert.pem
</details>
