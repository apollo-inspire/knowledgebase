# Programmeren 3: Javascript & Webservices
*Knowledgebase: https://luukftf.github.io/knowledgebase*  
*(code: https://github.com/LuukFTF/knowledgebase)*  
*By: Lucas van der Vegt*
*2022-03-01*
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

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <script src="index.js"></script>
    <title>HTML 5 Boilerplate</title>
  </head>
  <body>
      insert here
  </body>
</html>
```

Advanced:
https://www.matuzo.at/blog/html-boilerplate/

## C. Javascript

### 1. Syntax

### 2. Events

### 3. Functions

### 4. Objects

```js
const person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
}

let cat = {
    hair: "long"
    age: 5,
    color: "white",
    mew: function() {
        console.log("new!");
    }
    eat: function() {
        console.log("nomnom")
    }
    play: function() {
        this.mew();("Where is my catnip")
        console.log
    }
}

can.mew();
can.eat();
cat.play();
```

### 5. Classes

### 6. DOM

Document Object Model


```js
let placeholder = document.getElementById('myVariablePlaceholder');
placeholder.innerHTML = "hier komt een php variable"
```

html
```html
:
<body>
    <main>
        <h1i id="title">Title</h1>
        <h2 id="total">Total:</h2>
        <ul class="cart">
            <li>A</li>
            <li>B</li>
            <li>V</li>
            <li>D</li>
        </ul>
    </main>
</body>
:
```

ID
```js
let elementTotal = document.getElementById("total");
elementTotal.innerHTML = "100";
```

Class
```js
let elementsCart = document.getElementByClassName("cart");
```

CSS Query One
```js
let elementTotal = document.querySelector("#total");
```

CSS Query All
```js
let elementsCartItems = document.SelectorAll(".cart li");
```

DOM Relaties

- Parent
- Child
- Sibling
- LastChild


### 7. JSON

**JavaScript Object Notation**, is a **text-based** open standard designed for human-readable **data interchange**.

It is derived from the **JavaScript** scripting language for representing simple **data structures** and associative arrays, called objects.

Despite its relationship to JavaScript, it is **language-independent**, with parsers available for many languages.

json example
```json
{ // json object
    "company": "mycompany", // string value
    "companycontacts": { // object inside object
        "phone": "123-123-1234",
        "email": "example@example.com"
    },
    "employees": [ // json array
        {
            "id": 101, // number value
            "name": "John",
            "contacts": [ // array inside array
                "johnwork@example.com",
                "johnpersonal@example.com"
            ]
        },
        {
            "id": 102 
            "name": "William",
            "contacts": null // null value
        }
    ] 
}
```

```js
header("Content-Type: application/json")
echo json_encode("test")
```

### 8. APIs 
Browser API
Server API

Webservices 
- REST
- GraphQL
- SOAP
Open APIs
Authenticated APIs 

WebAPI (camera, locatie)





### 9. RESTful

#### HTTP Statuscode

1XX: Informational
2XX: Succes
3XX: Redirection
4XX: Client Error (404: not found)
5XX: Server Error

### 10. AJAX
https://www.w3schools.com/js/js_ajax_intro.asp


Asynchronous JavaScript And XML.

AJAX is not a programming language.

AJAX just uses a combination of:
- A browser built-in XMLHttpRequest object (to request data from a web server)
- JavaScript and HTML DOM (to display or use the data)

Synchronous: Kan pas de volgende functie aanroepen als de vorige klaar is.

Asynchronous: Roept de volgende functie aan direct nadat de vorige is begonnen.


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
    (Pennywise)

### Javascript Libraries

Websocket > Socket.io  
D3.js (Data-Driven Documents)
Codepen (JS Animations)
Microcontroller
Makecodearcade


---
`end of file`  
*publish date: 2022-02-15*  
*modified date: 2022-03-01*  
  
<!-- LINKS -->
[google]: https://www.google.com  