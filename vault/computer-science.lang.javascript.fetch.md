---
id: aa9fe65f-9a92-4250-afea-631e46b0f14f
title: Fetch
desc: ''
updated: 1613059245026
created: 1613059189797
---

# Fetch API

```javascript
const user = 'criscara-dev'
const url = `https://api.github.com/users/${user}`

fetch(url)
  .then(response => response.json())
  .then(json => console.log(json.name))
  .catch(error => console.log(error))

  // Cristian Caratti
  ```