---
title: 'CMGT Programmeren'
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

- [Client Server Model](#client-server-model)

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

- PHP

- Javascript Frameworks

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

### V. Javascript

#### 1. Basics
##### Syntax
##### Events

#### 2. Functions
#### 3. Objects
#### 4. Classes
#### 5. DOM

Relaties

#### 6. JSON
#### 7. Ajax
#### 8. APIs
Browser API
Server API

Webservices 
Web API
Open APIs



### D. Backend

php
node.js

### E. Typescript

### F. Javascript Frameworks

React  
Angular  
Vue    

Electron

### x. Other

Socket.io  


---
`end of file`  
*publish date: 2021-03-04*  
*modified date: 2021-03-04*  
  
<!-- LINKS -->
[google]: https://www.google.com  