---
title: cmgt-prg04-summary
created: '2020-06-24'
modified: '2020-06-27'
published: '2020-06-27'
---

# CMGT Programmeren 4: Object Oriented Game Development
_**Object Oriented Game Development - TypeScript**_
_**door: Lucas van der Vegt**_

---
title: CMGT-PRG01-summary
created: '2020-09-06'
modified: '2020-09-06'
---

# CMGT Programmeren 1: JavaScript Basics & Adafruit development

_**door: Lucas van der Vegt**_

## Leerdoelen

## Topics

## Main Meterial


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


## Topics

- Basic Javascript
  - Static Types
  - Arrays
  - Functions

- Classes

- Inheritance
  - Class 2 extends Class 1

- Composition
  - Class 1 has Class 2

- Encapsulation
  - Private
  - Public
  - Protected
  - Get & Set

- Full Advanced Classes

- Game Techniques
  - Game loop
  - DOM Elements
    - HTML
    - CSS
    - TS
  - Bouding box
  - Collision
  - Vector

- UML
  - Class
  - Inheritance
  - Composition
  - Encapsulation


## Main Meterial

### Basic Javascript

#### Static Types

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


#### Arrays

Een array van `numbers`
```ts
let list : number = [1, 2, 3]
```

#### Functions

Bij `function argument` altijd het `type` aangeven.

```ts
function getValue(a : number) {
  return true
}
```


### Classes

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


### Inheritance
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

### Composition
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

### Encapsulation

#### Public & Private

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

#### Get & Set

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

#### Protected

Protected is hetzelfde als private alleen word het geextend bij een inharitance.

```ts
```

### Full Advanced Classes

```ts
```

### Game Techniques

#### Game loop

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

#### DOM Elements


Gebruik semantische elementen in html en css om elementen te laten bewegen.

##### HTML

Semantische HTML tags, een geprefereerde manier is om semantische tags in de HTML aan te maken binnen de TypeScript class
```html
<car></car>
```

##### CSS

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
##### TS
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

#### Bouding box

Een DOM rectangle gebruik je op previes te zien waar het object staat en hoe groot het is. Hij heeft 8 properties: `left, top, right, bottom, x, y, width, height`

```ts
let rectangle : ClientRect = div.getBoundingClientRect()
```

#### Collision

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


#### Vector

#### Other

Grid
```ts
let offsetX = (window.innerWidth - grid.columns * this.div.clientWidth) / 2
this.x = column * this.div.clientWidth + offsetX
this.y = row * this.div.clientHeight   + 100
```

### UML

#### Example
- Object
    - Parameters
        - Fields
        - Properties
    - Constructor 
    - Functions


#### Inheritance
Car is a vehicle

#### Composition
Car has a driver

#### Encapsulation (Acces modifiers )
```uml
+ public
- private
# protected
```



