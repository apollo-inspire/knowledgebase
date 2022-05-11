# Programmeren 7: Mobile Technologies & Smart Devices (React Native) [Samenvatting Lessen]
*Knowledgebase: https://luukftf.github.io/knowledgebase*  
*(code: https://github.com/LuukFTF/knowledgebase)*  
*By: Lucas van der Vegt*  
*2022-04-25*    
<!-- Editted by: NAME, NAME, NAME -->


## Leerdoelen

## Deadlines
Eindopdracht: 2022-07-01
Tentamen: Week 9

## Index

## Resources



---
<br><br><br><br>
<div style="page-break-after: always; visibility: hidden"> \pagebreak </div> 

## Les 1 - Javascript feestje

Object Destructing


Array Destructing
```js
const numbers = [123,32235,545,6,2,123];
const [firstNumber, secondNumber, ...otherNumbers] = numbers;
```
rest parameter `...otherNumbers` 


multiple return values
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
```js
const toggleSwitch = (status) => {
    ⋮
}
```

arrow function vs reg function scoping difference

arrow
```js
el.addEventlistener('click', function () { 
    console.log(this);
})
```

regular
```js
el.addEventlistener('click', () => console.log(this))
```


events
eventlistener


array iteration


```js
const pokemonCards = ['Pikachu', 'Squirtle', 'Charmander']

for (let i = 0; i < pokemonCards.length; i++) {
    console.log(pokemonCards[i]);
}

for (let item of pokemonCards) {
    console.log(item);
}
```
https://developer.mozilla.org/en-
US/docs/Web/JavaScript/Guide/Loops_and_iteration

```jsx
```

https://developer.mozilla.org/en-
US/docs/Web/JavaScript/Guide/Loops_and_iteration

functions on an array

.map

.sort

object iteration version 1

```js
const pokemonCardObject = {
    name: "pikachu",
    type: "electric",
    height: 40
}

for (let [key, value] of Object.entries(pokemonCardObject)) {
    console.log(`${key}: ${value}`);
}
```


object iteration version 2
```js
Object.entries(pokemonCardObject).map(([ key, value ])=> {
    console.log(`${key}: ${value}`);
})
```

for in loop
for of loop

object.entries()

promises

.then
.catch

```js
fetch('https://pokeapi.co/api/v2/pokemon?limit=151')
    .then((res) => res.josn())
    .then(
        (data) => loadPokemonDetail(data),
        (error) => console.log(`Onrejected: ${error}`)
    )
    .catch((error) => console.log(`Catch: ${error}`));
```

async
await

```js
async function loadPokemonData() {
    try {
        const result = await fetch('https://pokeapi.co/api/v2/pokemon?limit=151');
        const data = await result.json();
        console.log(data);
    } catch (e) {
        console.log('error', e)
    }
}

loadPokemonData()
```

## Les 2 - 