---
title: 'CMGT-PRG03-summary'
subject: 'Programmeren3'
created: '2021'
modified: '2021'
published: ''
---

# CMGT Programmeren 3: Javascript & Webservices

_**door: Lucas van der Vegt**_

## Leerdoelen

## Topics


## Main

Client Server Model


Client
HTML CSS
Javascript
Fetch API

Web server
ngix/ apache
PHP
Database

AJAX call
JSON response


Webservices
APIs
OpenAPIs

1. Pagina wordt geladen. Dit kan zowel een `.html` als een `.php` bestand zijn. Resultaat is hetzelfde namelijk HTML, CSS en Javascript.
2. Na wachten op het `load` event van het `window`, wordt de Javascript van de applicatie uitgevoerd en is de applicatie klaar met `renderen`
3. Als we dynamisch data willen inladen op onze webpagina kunnen we `AJAX` calls doen dmv de `fetch` functie in Javascript. Deze functie doet een `request` naar een specifiek PHP bestand op de server.
4. De `response` vanuit de server zal `JSON` data bevatten die weer verwerkt kan worden in Javascript.
5. De Javascript van de pagina verwerkt de `response` ern in `callback functie` waarna alle bekende Javascript functies (HTML elementen aanroepen, aanmaken, etc) weer aangeroepen kunnen worden.

React
Angular
Vue

Node.js

Socket.io