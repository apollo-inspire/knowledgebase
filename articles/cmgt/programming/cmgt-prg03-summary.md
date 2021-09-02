---
title: 'CMGT Programmeren 3'
code: 'cmgt-prg03-summary'
created: '2021-02-18'
published: '2021-03-04'
modified: '2021-03-04'
author: 'Lucas van der Vegt'
teacher: ['Antwan', 'Erik']
modifiedby: ['', '']
knowledgebase: 'https://github.com/LuukFTF/knowledgebase/blob/master/articles/cmgt/programming/cmgt-prg03-summary.md'
link: 'https://luukftf.github.io/knowledgebase/articles/cmgt/programming/cmgt-prg03-summary.html'
lang: 'nl'
tags: ['Programmeren3', '', '']
---

# Programmeren 3: Javascript & Webservices
*Knowledgebase: https://luukftf.github.io/knowledgebase*  
*(code: https://github.com/LuukFTF/knowledgebase)*  
*By: Lucas van der Vegt*
<!-- Editted by: NAME, NAME, NAME -->


## Leerdoelen

Ik ken:  
- de rol van HTML, CSS, JS en PHP binnen het client-server-model.
- het verschil tussen simpele en complexe webservices in de back-end.
- het concept van JSON en wanneer je dit kunt gebruiken.
- het verschil tussen native Javascript en verwante libraries/frameworks.
- de structuur van een DOM en hoe deze is opgebouwd.
- de rol van AJAX en hoe asynchrone communicatie werkt.
- het principe van events, welke er zijn en waarom ik ze zou gebruiken.
- de rol van Web API’s en hoe die zich verhouden tot de browser.  

Ik kan:  
- gebruik maken van een simpele webservice met PHP, zodat ik data uit eenexterne bron kan inladen.
- JSON schrijven en aanbieden als een webservice in PHP.
- native Javascript (hierna: “Javascript”) toepassen binnen de front-end van eenapplicatie, inclusief het manipuleren van de DOM.
- via Javascript events lezen en schrijven waarmee ik een applicatieinteractiever maak.
- via AJAX dynamische data ophalen van zowel externe als eigen geschrevenwebservices, en dit verwerken in mijn applicatie.
- via Javascript, Web API’s (must: localstorage) van mijn browser aanspreken enverwerken in mijn applicatie

## Topics

- [Client Server Model](#a-client-server-model)

- Basic Frontend: HTML & CSS
    - HTML Basics
    - CSS Basics

- Javascript
    - Basics
        - Events
    - Functions
    - Objects
    - Classes
    - DOM
    - JSON
    - Ajax
    - APIs
        - Browser API
        - Server API
        - Web API

- Backend
    - PHP
    - node.js

- Typescript

- Javascript Frameworks

---

## Main

### A. Client Server Model

Client Server Model flowchart:
1. Pagina wordt geladen. Dit kan zowel een `.html` als een `.php` bestand zijn. Resultaat is hetzelfde namelijk HTML, CSS en Javascript.
2. Na wachten op het `load` event van het `window`, wordt de Javascript van de applicatie uitgevoerd en is de applicatie klaar met `renderen`
3. Als we dynamisch data willen inladen op onze webpagina kunnen we `AJAX` calls doen dmv de `fetch` functie in Javascript. Deze functie doet een `request` naar een specifiek PHP bestand op de server.
4. De `response` vanuit de server zal `JSON` data bevatten die weer verwerkt kan worden in Javascript.
5. De Javascript van de pagina verwerkt de `response` ern in `callback functie` waarna alle bekende Javascript functies (HTML elementen aanroepen, aanmaken, etc) weer aangeroepen kunnen worden.

**Client** *< de gebruikerskant van de website >*  
Server

Backend
Web server  
ngix/ apache  
PHP  
Database  

AJAX call
JSON response  

Fetch API

### B. Basic Frontend: HTML & CSS

Frontend
HTML 
CSS  

### C. Javascript

#### 1. Basics

##### Syntax

##### Events

#### 2. Functions
#### 3. Objects
#### 4. Classes
#### 5. DOM

Relaties

#### 6. JSON

#### 7. APIs 
Browser API
Server API

Webservices 
Web API
Open APIs


#### 8. RESTful

#### 9. AJAX

Fetch GET
```js
fetch('https://swapi.dev/api/films/', { method: 'GET' })
    .then(response => response.json())
    .then(data => return data)
```

Fetch POST
```js
fetch('https://swapi.dev/api/films/', { 
    method: 'POST',
    headers: { 'content-type': 'application/json'},
    body: JSON.stringify({
        name: 'User 1'
    })
})
    .then(response => response.json())
    .then(data => return data)
```


Fetch GET with error handling
```js
fetch('https://swapi.dev/api/films/', { method: 'GET' })
    .then((response) => {
        if (!response.ok) {
            throw new Error(response.statusText);
        }
        return response.json();
    })
    .then(getSuccessHandler)
    .catch(getErrorHandler);
```

Fetch POST with error handling
```js
fetch('https://swapi.dev/api/films/', { 
    method: 'POST',
    headers: { 'content-type': 'application/json'},
    body: JSON.stringify({
        name: 'User 1'
    })
})
    .then((response) => {
        if (!response.ok) {
            throw new Error(response.statusText);
        }
        return response.json();
    })
    .then(getSuccessHandler)
    .catch(getErrorHandler);
```

### D. Backend

php

node.js

### E. Typescript

PRG04 > uitbreiding op javascript

### F. Javascript Frameworks

React  
Angular  
Vue    

Progressive Web App:
Angular PWA
React Native

Flutter
Electron  

### X. Other

Socket.io  

---

course end code
```js
window.addEventListener('load', init);

//Global vars
let apiUrl = 'https://pokeapi.co/api/v2/pokemon?limit=151';
let loadPokemon = false;
let $button;
let $types;

function init() {
    $button = document.getElementById('load-pokemon');
    $button.addEventListener('click', () => ajaxRequest(apiUrl, getPokemonsSuccessHandler));
    $types = document.getElementById('types');
}

/**
 * Do the actual AJAX call to the provided URL
 */
function ajaxRequest(url, successCallback) {
    fetch(url)
        .then((response) => {
            if (!response.ok) {
                throw new Error(response.statusText);
            }
            return response.json();
        })
        .then(successCallback)
        .catch(ajaxRequestErrorHandler);
}

/**
 * Do something nice with the data you got from the external API
 *
 * @param data
 */
function getPokemonsSuccessHandler(data) {
    //Prevent this function from being executed more than once
    if (loadPokemon === true) {
        return;
    }

    //Create a new ul element & add event listener on this parent
    let $ul = document.createElement('ul');
    $ul.addEventListener('click', pokemonClickHandler);
    $ul.id = 'pokemons';

    //Loop through data and create a li element per pokemon
    for (let pokemon of data.results) {
        let $li = document.createElement('li');
        $li.innerHTML = pokemon.name;
        $li.dataset.url = pokemon.url; //Store URL in element
        $ul.appendChild($li);
    }

    //Append new list to the DOM
    document.querySelector('body').appendChild($ul);

    //Prevent to load double data by switching the state
    loadPokemon = true;
}

/**
 * After clicking on a Pokémon it's time to load the extra API information
 *
 * @param e
 */
function pokemonClickHandler(e) {
    //First make sure we actually clicked on a li element
    let $target = e.target;
    if ($target.nodeName !== "LI") {
        return;
    }

    //Get the URL
    let url = $target.dataset.url;

    //Load the new data
    ajaxRequest(url, getPokemonDetailSuccessHandler)
}

/**
 * Write the types of the Pokémon in the existing HTML element
 *
 * @param data
 */
function getPokemonDetailSuccessHandler(data) {
    let types = [];
    for (let typeData of data.types) {
        types.push(typeData.type.name);
    }
    $types.innerHTML = types.join(', ');
}

/**
 * Do something useful with the error you got back from the external API
 * We will use this error function for both API calls for now
 *
 * @param data
 */
function ajaxRequestErrorHandler(data) {
    console.error(data);
}


```


---
`end of file`  
*publish date: 2021-03-04*  
*modified date: 2021-03-04*  
  
<!-- LINKS -->
[google]: https://www.google.com  