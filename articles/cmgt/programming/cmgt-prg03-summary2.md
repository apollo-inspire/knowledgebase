# Programmeren 3: Javascript & Webservices
*Knowledgebase: https://luukftf.github.io/knowledgebase*  
*(code: https://github.com/LuukFTF/knowledgebase)*  
*By: Lucas van der Vegt*
*2022-02-15*
<!-- Editted by: NAME, NAME, NAME -->

## Leerdoelen

## Deadlines

## Index

## Resources

## A. Client Server Model
Client Server Model flowchart:
1. Pagina wordt geladen. Dit kan zowel een `.html` als een `.php` bestand zijn. Resultaat is hetzelfde namelijk HTML, CSS en Javascript.
2. Na wachten op het `load` event van het `window`, wordt de Javascript van de applicatie uitgevoerd en is de applicatie klaar met `renderen`
3. Als we dynamisch data willen inladen op onze webpagina kunnen we `AJAX` calls doen dmv de `fetch` functie in Javascript. Deze functie doet een `request` naar een specifiek PHP bestand op de server.
4. De `response` vanuit de server zal `JSON` data bevatten die weer verwerkt kan worden in Javascript.
5. De Javascript van de pagina verwerkt de `response` ern in `callback functie` waarna alle bekende Javascript functies (HTML elementen aanroepen, aanmaken, etc) weer aangeroepen kunnen worden.

**Client** *< de gebruikerskant van de website >*  
HTML CSS JS

**Server** *< de client kan geen code zien>*
Backend
Web server  
ngix/ apache  
PHP  
Database  

**API**
AJAX call
JSON response  

Fetch API


## B. Basic Frontend: HTML & CSS

Frontend
HTML 
CSS  

### HTML Boilerplate


## C. Javascript

### 1. Syntax

### 2. Events

### 3. Functions

### 4. Objects

### 5. Classes

### 6. DOM

Relaties

### 7. JSON

### 8. APIs 
Browser API
Server API

Webservices 
Web API
Open APIs


### 9. RESTful

### 10. AJAX

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


## D. Basic Backend: PHP

php

node.js

## X. Extra Info

Websocket > Socket.io  

### Typescript

PRG04 > uitbreiding op javascript

### Javascript Frameworks

React  
Angular  
Vue    

Progressive Web App:
Angular PWA
React Native

Flutter
Electron  

---
`end of file`  
*publish date: 2022-02-15*  
*modified date: 2022-02-15*  
  
<!-- LINKS -->
[google]: https://www.google.com  