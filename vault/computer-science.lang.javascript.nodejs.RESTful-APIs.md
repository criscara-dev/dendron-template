---
id: 10614a85-04d7-4ad0-a3e9-459543628f21
title: Restful-apis
desc: ''
updated: 1605356705799
created: 1605090506626
---

## Build a RESTful API with Stripe and Mailgun services

- [ ] copy the Pirple Repo and get rid of aa not useful
    - config, handlers, server
- [ ] workers services?  need to contain the method for the APIs
- [ ] helpers: Stripe API 
- [ ] helpers: MailGun API 
- [ ]  users req: name, email address, and street address.
- [ ] users Token same as Pirple API
- [ ] create a JSON menu (hardcoded) name,desc, amount/price, currency like api2
- [ ] method available GET (menu items) 
- [ ] flow lead of API3


 
## References: 
- [Node docs](https://nodejs.org/dist/latest-v14.x/docs/api/stream.html)
- [Pirple reference](https://www.pirple.com/courses/take/the-nodejs-master-class/assignments/9455916-homework-assignment-2)
- [Stripe API](https://stripe.com/docs/payments/accept-a-payment?integration=elements)
- [Mailgun API](https://documentation.mailgun.com/en/latest/faqs.html#how-do-i-pick-a-domain-name-for-my-mailgun-account)


Dir Schema:

- https: contain the environment set up
- server: 
    - contain dependencies
    - start server
    - routing map 

    ```javascript
    server.router = {
    'ping' : handlers.ping,
    'users' : handlers.users,
    'tokens' : handlers.tokens,
    'products' : handlers.products,
    'cart' : handlers.cart,
    'checkout' : handlers.checkout
    };
    ```
- data contain:
    - the db pizza json items
    - function to read the db items (CRUD)

- handlers are functions that let you handle the HTTP requests:
    - /ping /notFound -> to test (inherited from previous rest API)
    - /users (post,edit(put),get,delete)
    - /tokens (post, edit(put), delete
    - /products (get)
    - /cart (post,edit(put),get)
    - /checkout (post)
    - validateToken (inherited from previous rest API)


- helpers: extra functions to help the 'handlers'
     - to create an email receipt
     - check email address if valid
     - to send mailgun emails
     - inherited from RESTFUL API Ccourse: hash, parsetoobject, createrendomstring, 
     - create Stripe receipt cost

- logs

- workers are functions that helps the app run and do:
    - rotating log to dir

- index: initialize the App