---
title: 'cmgt-prg04-summary'
created: '2020-06-24'
published: '2020-06-27'
modified: '2021-09-23'
author: 'Lucas van der Vegt'
teacher: ''
modifiedby: ['', '']
knowledgebase: 'https://luukftf.github.io/knowledgebase'
link: 'https://github.com/LuukFTF/knowledgebase/blob/master/articles/cmgt/programming/cmgt-prg04-summary.md'
lang: 'en'
tags: ['typescript', 'oop', 'gamedev']
---

# Programmeren 4: Object Oriented Game Development (TypeScript)

*Knowledgebase: https://luukftf.github.io/knowledgebase*  
*(code: https://github.com/LuukFTF/knowledgebase)*  
*By: Lucas van der Vegt*


## Leerdoelen

Ik kan de betekenis en werking van de volgende
OOP principes herkennen, uitleggen en zelf implementeren
- Classes
- Inheritance
- Composition
- Encapsulation

Ik kan een programmeervraagstuk op abstract
niveau structureren en oplossen middels een
klassendiagram (UML) waarbij gebruik
gemaakt wordt van Inheritance, Composition
en Encapsulation.

Ik kan code van anderen lezen en de werking
ervan beredeneren.



## Index

  - [1. Basic Javascript](#1-basic-javascript)
    - [1.1 Static Types](#11-static-types)
    - [1.2 Arrays](#12-arrays)
    - [1.3 Functions](#functions)
  - [2. Classes](#2-classes)
  - [3. Inheritance](#3-inheritance)
  - [4. Composition](#4-composition)
  - [5. Encapsulation](#5-encapsulation)
    - [5.1 Public & Private](#51-public--private)
    - [5.2 Get & Set](#52-get--set)
    - [5.3 Protected](#53-protected)
  - [6. Full Advanced Classes](#6-full-advanced-classes)
  - [7. Game Techniques](#7-game-techniques)
    - [7.1 Game loop](#71-game-loop)
    - [7.2 DOM Elements](#72-dom-elements)
    - [7.3 Bouding box](#73-bouding-box)
    - [7.4 Collision](#74-collision)
    - [7.5 Vector](#75-vector)
    - [7.6 Other](#76-other)
  - [8. UML](#8-uml)
    - [8.1 Example](#81-example)
    - [8.2 Inheritance](#82-inheritance)
    - [8.3 Composition](#83-composition)
    - [8.4 Encapsulation (Acces modifiers)](#84-encapsulation-acces-modifiers)


---

## 1. Basic Javascript

### 1.1 Static Types

Typescript is Javascript met `static types`

JavaScript:
```js
let a = 1
let b = true
let c = "Car" 

a = "hoi"
console.log(a)

// output = hoi
```

TypeScript:
```ts
let a = 1 : number
let b = true : boolean
let c = "Car" : string

a = "hoi"
console.log(a)

// output = ERROR
```


### 1.2 Arrays

Een array van `numbers`
```ts
let list : number = [1, 2, 3]
```

### 1.3 Functions

Bij `function argument` altijd het `type` aangeven.

```ts
function getValue(a : number) {
  return true
}
```


## 2. Classes

class example:
```ts
class Person {
  name : string

  constructor() {
    this.name = "Lucas"
  }

  sayHi(){
    console.log("${this.name} said hi!")
  }
}
```

create object example:
```ts
let p = new Person()

console.log(p.name)
p.sayHi()

// output = Lucas said hi!
```


## 3. Inheritance
Class 2 extends Class 1

Class 1 example:
```ts
class Person {
  constructor(){
    console.log("Person")
  }
}
```

Class 2 example:
```ts
class Driver extends Person {
  private vehicle : string = "bus"

  constructor(){
    super()
    console.log("Driving: " + this.vehicle)
  }
}
```

create extended object example:
```ts
let d = new Driver()

// output =
// Person
// Driving: bus
```

## 4. Composition
Class 1 has Class 2

Class 1 example:
```ts
class Driver {
  public name : string = "Lucas"

  contructor(){
  }
}
```

Class 2 example:
```ts
class Car {
  private driver : Driver

  constructor(){
    this.driver = new Driver()
    console.log("Driver is" + this.driver.name)
  }
}
```

create composistion object example:
```ts
let c = new Car()

// output = Driver is Lucas
```

## 5. Encapsulation

### 5.1 Public & Private

Class met encapsulation:
```ts
class Person {
  private age : number = 18
  public name : string = "Lucas"

  contructor(){
  }
}
```

create object:
```ts
let p = new Person()

console.log(this.Person.age)
console.log(this.Person.name)

// output =
// ERROR
// Lucas
```

### 5.2 Get & Set

```ts
class Person {
  private _age : number = 18
  public name : string = "Lucas"

  get age() { return this._age}
  set age(i:number) { this._age = i }

  contructor(){
  }
}
```

```ts
let p = new Person()

console.log(this.Person.age)
console.log(this.Person.name)

// output =
// 18
// Lucas
```

### 5.3 Protected

Protected is hetzelfde als private alleen word het geextend bij een inharitance.

```ts
```

## 6. Full Advanced Classes

```ts
```

## 7. Game Techniques

### 7.1 Game loop

Met `requestAnimationFrame()` word elke "animation frame" een keer aangeroepen, bij een normaal beeldscherm zal dit 60 keer per seconden zijn. Zo onstaat er een framerate van 60fps. De functie werkt alleen als de tab actief is.

```ts
class Game {

  constructor() {
    this.gameLoop()
  }

  private gameLoop() {
    // game loop code goes here

    requestAnimationFrame(()=> this.gameLoop())
  }
}
```

### 7.2 DOM Elements


Gebruik semantische elementen in html en css om elementen te laten bewegen.

#### 7.2.1 HTML

Semantische HTML tags, een geprefereerde manier is om semantische tags in de HTML aan te maken binnen de TypeScript class
```html
<car></car>
```

#### 7.2.2 CSS

Alle gemaakte elementen in game kunnen op deze manier gemanipuleerd worden op de gewenste manier in de typescript classes

```css
game * {
  position: absolute
  display: block
}
```

Op deze manier krijg het element een afbeelding gelinkt om zo te laten zien worden.
```css
car {
    background-image: url(../images/car.png);
    width:40px; height: 40px;
}
```
HTML element creeeren samen met de class.
#### 7.2.3 Typescript
```ts
class Car {
  div : HTMLElement
  x : number = 100
  y : number = 100

  constructor() {
    this.div = document.createElelement("car")
    document.body.appendChild(this.div)
  }

  public update() {
    this.x++

    this.div.style.transform = `translate(${this._X}px, ${this._Y}px)`
  }
}
```

### 7.3 Bouding box

Een DOM rectangle gebruik je op previes te zien waar het object staat en hoe groot het is. Hij heeft 8 properties: `left, top, right, bottom, x, y, width, height`

```ts
let rectangle : ClientRect = div.getBoundingClientRect()
```

### 7.4 Collision

Gebruik een collision function op te zien of zien twee rectangles overlappen.
```ts
function checkCollision(a : ClientRect, b : ClientRect) {
  return (a.left <= b.right &&
          b.left <= a.right &&
          a.top <= b.bottom &&
          b.top <=  a.bottom)
}
```

Function gebruiken:
```ts
this.checkCollison(this.car1.getRectangle(), this.car2.getRectangle())
```
Returns true or false


### 7.5 Vector

### 7.6 Other

Grid
```ts
let offsetX = (window.innerWidth - grid.columns * this.div.clientWidth) / 2
this.x = column * this.div.clientWidth + offsetX
this.y = row * this.div.clientHeight   + 100
```

## 8. UML

<!-- insert mermaid example -->

### 8.1 Example
- Object
    - Parameters
        - Fields
        - Properties
    - Constructor 
    - Functions


### 8.2 Inheritance
Car is a vehicle

### 8.3 Composition
Car has a driver

### 8.4 Encapsulation (Acces modifiers)
```uml
+ public
- private
# protected
```

---

`end of file`  
*publish date: 2020-06-27*  
*modified date: 2021-02-20*  
  
<!-- LINKS -->
[google]: https://www.google.com  

