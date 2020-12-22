---
id: 564980e9-41b1-414c-80fc-b7f42dad18a3
title: Data
desc: ''
updated: 1608582331177
created: 1602345873229
stub: false
---

## The Data model/Schema

- Dan Abramov Just JavaScript course:
    - Lesson 2 
    ![JS Universe](assets/images/universe.png)

    Let’s recap what we know so far:
    _**There are values, and then there’s everything else.**_ We can think of values as different things “floating” in our JavaScript universe. They don’t exist inside our code, but we can refer to them from our code.
    _**There are two categories of values: there are Primitive Values, and then there are Objects and Functions.**_ In total, there are nine separate types. Each type serves a specific purpose, but some are rarely used.
    Some values are lonely. For example, null is the only value of the Null type, and undefined is the only value of the Undefined type. As we will learn later, these two lonely values are quite the troublemakers!
    _**We can ask questions with expressions.**_ JavaScript will answer to us with values. For example, the 2 + 2 expression is answered with 4.
    _**We can inspect the type of something by wrapping it in a typeof expression.**_ For example, typeof(4) is the string value "number".
    
    - Lesson 3:
    Primitive values are immutable:
    ![](/assets/images/2020-12-20-19-58-19.png)
    Variables are wires.
    Variables are not values.
    Variables point to values.
    We can’t point variables to each other! Variables always point at values.
    ```javascript
    let x = 10;
    let y = x;
    x = 0;
    ```
   Recap
    _**Primitive values are immutable.**_ There’s nothing we can do in our code to affect them or change them in any way. They stay what they are. For example, we can’t set a property on a string value because it is a primitive value. Arrays are not primitive, so we can set their properties.
    _**Variables are not values.**_ Each variable points to a particular value. We can change which value it points to by using the = assignment operator.
   _**Variables are like wires.**_ A “wire” is not a JavaScript concept — but it helps us imagine how variables point to values. There’s also a different kind of “wire” that’s not a variable, but we haven’t discussed it yet.
    _**Look out for contradictions.**_ If two things that you learned seem to contradict each other, don’t get discouraged. Usually it’s a sign that there’s a deeper truth lurking underneath.
    _**Nouns and verbs matter.**_ We’re building a mental model so that we can be confident in what can or cannot happen in our universe. It’s fine to be sloppy in casual speech, but our thinking needs to be precise.

    - Lesson 4
        * The “celestial spheres” of JavaScript to meet different values: Booleans, Numbers, Strings, and so on.
        * Undefined: Only one value, undefined.
        * Null: Only one value, null.
        * Booleans: Two values: true and false.
        * Numbers: One value for each floating point math number.
        * BigInts: One value for every conceivable integer.
        * Strings: One value for every conceivable string.
        * Objects: One value for every object that we create.
        * Function: One value for every function definition we step through.
    ![](/assets/images/2020-12-21-19-45-34.png)

    Let’s recap JavaScript numbers:
   _**JavaScript implements a standard called “floating point math”. _** Its numbers are more precise closer to 0, and less precise further away from it.
    _**Numbers resulting from invalid math operations like 1 / 0 or 0 / 0 are special.**_ NaN is one of such special numbers.
    _**typeof(NaN) is a number because it is a numeric value.**_ It’s called “Not a Number” because it represents the idea of an "invalid" number.
    > In our mental model, all of the primitive values we’ve discussed — null, undefined, booleans, numbers, and strings — have “always existed”. We can’t “make” a new string or a new number, we can only “summon” that value
    
    _**Every time we execute a line of code that contains a function declaration, a brand new function value appears in our universe.**_
    ![function](/assets/images/functioncreation-optim.gif)

    Summary:
    - For example, writing 2 or "hello" always “summons” the same number or a string value. But writing {} or declaring a function always creates a brand new, different value.