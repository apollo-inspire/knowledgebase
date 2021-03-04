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

## Topics

- Client Server Model

- API

- Javascript

- DOM

- Web Api's

- Ajax



## Main

### Client Server Model

Client Server Model flowchart:
1. Pagina wordt geladen. Dit kan zowel een `.html` als een `.php` bestand zijn. Resultaat is hetzelfde namelijk HTML, CSS en Javascript.
2. Na wachten op het `load` event van het `window`, wordt de Javascript van de applicatie uitgevoerd en is de applicatie klaar met `renderen`
3. Als we dynamisch data willen inladen op onze webpagina kunnen we `AJAX` calls doen dmv de `fetch` functie in Javascript. Deze functie doet een `request` naar een specifiek PHP bestand op de server.
4. De `response` vanuit de server zal `JSON` data bevatten die weer verwerkt kan worden in Javascript.
5. De Javascript van de pagina verwerkt de `response` ern in `callback functie` waarna alle bekende Javascript functies (HTML elementen aanroepen, aanmaken, etc) weer aangeroepen kunnen worden.

**Client**  *< de gebruikerskant van de website >*  
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

  

React  
Angular  
Vue      

Node.js 

Socket.io  

---
`end of file`  
*publish date: 2021-03-04*  
*modified date: 2021-03-04*  
  
<!-- LINKS -->
[google]: https://www.google.com  