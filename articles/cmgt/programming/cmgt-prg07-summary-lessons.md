# Programmeren 7: React Native (Samenvatting Lessen)
*Knowledgebase: https://luukftf.github.io/knowledgebase*  
*(code: https://github.com/LuukFTF/knowledgebase)*  
*By: Lucas van der Vegt*  
*2022-03-02*    
<!-- Editted by: NAME, NAME, NAME -->


## Leerdoelen

## Deadlines
Eindopdracht
Tentamen

## Index

## Resources



---
<br><br><br><br>
<div style="page-break-after: always; visibility: hidden"> \pagebreak </div> 

## Les 1 - Javascript feestje

Object Destruct


Array Destructing
```js
const numbers = [123,32235,545,6,2,123];
const [firstNumber, secondNumber, ...otherNumbers] = numbers;
```
rest parameter `...otherNumbers` 


multiple return vaues
```js
function getNumbers(){
    return [123,32235,545,6,2,123]
}

const [firstNumber, secondNumber, ...otherNumbers] = getNumbers;
```

array nesting destructing
```js
const person = {
    firstName: "Zino",
    lastName: "Schubert",
    coolness: 9000
}

// todo: insert
```

arrow function 
scoping difference

events
eventlistener


array iteration

functions on an array

.map

.sort

object iteration

for in loop
for of loop

object.entries()

promises

.then
.catch

async
await
