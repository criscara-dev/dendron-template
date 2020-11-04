---
id: cb18c17b-5359-4c20-83f5-a9821c4b942d
title: Building-a-computer
desc: ''
updated: 1604508628153
created: 1604354116803
---

## Project based on the Coursera course:

![What I will do](/assets/images/2020-11-02-21-59-48.png)

![7 weeks program:](/assets/images/2020-11-02-22-10-29.png)


1. Builds logic gates
Concepts:
- ==Nand==, a logic gate.
- Xor, HDL (stand for Hardware Description language) program, 
![Hack, assembly code and binary code](/assets/images/2020-11-02-22-15-51.png)


<details><summary>
Abstract Boolean logic
</summary>

You can manipulate Boolean Expressions like arithmetic expressions

<details><summary>
AND
</summary>

x|y|AND
-|-|-
0|0|0
0|1|0
1|0|0
1|1|1
</details>

<details><summary>
OR
</summary>

x|y|OR
-|-|-
0|0|0
0|1|1
1|0|1
1|1|1
</details>

<details><summary>
NOT
</summary>

 x|NOT
 -|-
 0|1
 1|0
</details>

Construct Boolean function?
We want to build a computer, so we need to go from Truth table to Boolean expression.
In fact, any Boolean function can be represented using an expression containing AND, ~~OR~~ and NOT operations.
We can use the #Morgan-Law to avoid using OR:
Proof:
(x OR y) = NOT(NOT(x) AND NOT(y))

<details><summary>
With which expression we can do everything?
</summary>

NOT AND or -> NAND
x|y|NAND
-|-|-
0|0|1
0|1|1
1|0|1
1|1|0

and that lead to the Theorem:
Any Boolean function can be represented using an expression containing only ==NAND== operations.

Proof:
1) NOT(x)= (x NAND x)
2) (x AND y) = NOT(x NAND y)
</details>
</details>

<details><summary>
What do you know about logic gates?
</summary>

Logic gates:
- elementary
![](/assets/images/2020-11-04-16-33-11.png)
![](/assets/images/2020-11-04-16-34-58.png)
- composite
![](/assets/images/2020-11-04-16-37-49.png)
</details>

<details><summary>
How can you implement a circuit?
</summary>

Circuit implementation:
![](/assets/images/2020-11-04-16-42-38.png)
Both need to be true in order to light up the bulb.
Or this:
![](/assets/images/2020-11-04-16-44-57.png)
---
With OR logic we just need one port.
![](/assets/images/2020-11-04-16-43-43.png)

</details>

<details><summary>
Which of these statements are true?
</summary>

- [x] The chip interface describes what the chip is doing; the chip implementation specifies how the chip is doing it.
- [ ] There is only one possible implementation for every interface.
- [x] The user of the chip is interested in the chip interface; the builder of the chip is interested in the chip implementation.
</details>

<details><summary>
Build Logic Gates with HDL
</summary>
**Lorem ipsum dolor sit amet...**
</details>
