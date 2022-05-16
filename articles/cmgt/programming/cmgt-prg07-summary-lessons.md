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

## Les 3 - React Native basics

Native app development
(oldschool)
Android (Andriod Studio):
- java
- kotlin

IOS (Xcode):
- Objective-C
- Swift

### React Native
Javascript (maar native gerenderd)
Based off react (https://reactjs.org/)
Cross platform
Specifieke libraries per platform mogelijk
Xcode en/of Android studio nodig
Released door facebook/meta in 2015, heeft een grote community
Native components voor mobile development
https://reactnative.dev/

### Expo (library)
Toolchain voor React Native
Android, IOS en web in universal build
Fast development via `Expo Go` app op mobile
Geen Xcode of Android studio nodig, maar ook geen platform specifieke libraries
https://expo.dev/


### Expo Install
https://docs.expo.dev/get-started/installation/

node / npm
git

Watchman (alleen voor macos): https://facebook.github.io/watchman/docs/install

VScode expo plugin: https://marketplace.visualstudio.com/items?itemName=byCedric.vscode-expo

Expo CLI
Expo Go app mobile

### Expo Initialisation
https://docs.expo.dev/get-started/create-a-new-app/

```bash
expo init 
```

```bash
expo start
```
### Debugging

Errors in Expo Go en console
`Console.log()`


### Components

geen html, maar native components
JSX
Components maken gebruik van de native API van het platform
Uitgebreide API documentatie bij react
https://reactnative.dev/docs/components-and-apis

### UI
View: https://reactnative.dev/docs/view
Tekst: https://reactnative.dev/docs/text

https://docs.expo.dev/tutorial/text/

### Styles

Zo close mogelijk bij normale css
camelCase ipv kebab-case
Inline vs StyleSheet

https://reactnative.dev/docs/style

### Button
https://reactnative.dev/docs/button
TouchableOpacity + Text

https://docs.expo.dev/tutorial/button/

### Aanvullende documentatie

Tutorials bij Expo: https://docs.expo.dev/tutorial/planning/
API docs React: https://reactnative.dev/docs/accessibilityinfo
Bijvoorbeeld alert: https://reactnative.dev/docs/alert


### State
React Native == React
useState

### Netwerk
React Native == Javascript
fetch

### Werkcollege




Onclick
