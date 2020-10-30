---
id: 9fcded56-7635-4a16-a5ba-3bf7a1ce57fc
title: Markdown
desc: ''
updated: 1602574007744
created: 1602574007744
stub: false
---

### [Emoji reference](https://github.com/ikatyang/emoji-cheat-sheet)
### [from html tables to md](https://jmalarcon.github.io/markdowntables/)


## [reference](https://www.dendron.so/notes/ba97866b-889f-4ac6-86e7-bb2d97f6e376.html)
# Examples:

---
```mermaid
classDiagram
      Animal <|-- Duck
      Animal <|-- Fish
      Animal <|-- Zebra
      Animal : +int age
      Animal : +String gender
      Animal: +isMammal()
      Animal: +mate()
      class Duck{
          +String beakColor
          +swim()
          +quack()
      }
      class Fish{
          -int sizeInFeet
          -canEat()
      }
      class Zebra{
          +bool is_wild
          +run()
      }
```
---
```mermaid
pie
    title Pie Chart
    "Dogs" : 386
    "Cats" : 85
    "Rats" : 150 
```
---
```mermaid
stateDiagram
    [*] --> Still
    Still --> [*]

    Still --> Moving
    Moving --> Still
    Moving --> Crash
    Crash --> [*]
```
---

```sequence {theme="hand"}
Andrew->China: Says Hello
Note right of China: China thinks\nabout it
China-->Andrew: How are you?
Andrew->>China: I am good thanks!
```
---

$f(X) = sin(x) + 12$

---
```flow
st=>start:http://www.example.com
```
---

```mermaid
graph LR
A --> B;
B --> C;
C --> A;
```
---

```ditaa {cmd=true args=["-E"]}
  +--------+   +-------+    +-------+
  |        | --+ ditaa +--> |       |
  |  Text  |   +-------+    |diagram|
  |Document|   |!magic!|    |       |
  |     {d}|   |       |    |       |
  +---+----+   +-------+    +-------+
      :                         ^
      |       Lots of work      |
      +-------------------------+
  ```

---

`
---

