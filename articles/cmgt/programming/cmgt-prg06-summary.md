---
title: 'frontend'
slug: 'cmgt-prg06-summary'
created: '2021-11-10'
published: '2021-00-00'
modified: '2021-11-10'
author: 'Lucas van der Vegt'
class: 'Programmeren 6'
class-slug: 'PRG06'
teacher: ''
modifiedby: ['', '']
knowledgebase: 'https://luukftf.github.io/knowledgebase'
link: 'https://github.com/LuukFTF/knowledgebase/blob/master/articles/cmgt/programming/cmgt-prg06-summary.md'
lang: 'en'
tags: ['frontend', 'framework', 'react', 'javascript', 'typescript', 'backend', 'api', 'node.js']
---


# Programmeren 6: Frontend Framework & Basic Backend Api (React & Node.js)


*Knowledgebase: https://luukftf.github.io/knowledgebase*  
*(code: https://github.com/LuukFTF/knowledgebase)*  
*By: Lucas van der Vegt*

---
<br><br><br><br>
<div style="page-break-after: always; visibility: hidden"> \pagebreak </div> 

## Leerdoelen

---
<br><br><br><br>
<div style="page-break-after: always; visibility: hidden"> \pagebreak </div> 

## Index


---
<br><br><br><br>
<div style="page-break-after: always; visibility: hidden"> \pagebreak </div> 

## Topics



---
<br><br><br><br>
<div style="page-break-after: always; visibility: hidden"> \pagebreak </div> 

## A. backend - Nodejs & Express & MongoDB
https://www.youtube.com/watch?v=ENrzD9HAZK4

## Endpoint

## Middleware

## Models
Database 

Mongoose
Schema

## B. HTTP, RESTfull API & OAuth
https://www.youtube.com/watch?v=-MTSQjw5DrM

**API** *< an Application Programming Interface is an interface that defines interactions between multiple software applications or mixed hardware-software intermediaries. >*

**HTTP**

**idempotency** *< Idempotence is the property of certain operations in mathematics and computer science whereby they can be applied multiple times without changing the result beyond the initial application. >*

**Safe Method** *< Deze method veranderd niks op de server >*


### HTTP

stateless


#### Software

Postman
Insomnia

VScode extension: REST Client

#### Methods


| name    | function                 | safe  | idempotent |
| ------- | ------------------------ | :---: | :--------: |
| POST    | create                   |       |     x      |
| GET     | read                     |   x   |     x      |
| PUT     | create / update (geheel) |       |     x      |
| PATCH   | update (deel)            |       |            |
| DELETE  | destroy                  |       |     x      |
|         |                          |       |            |
| OPTIONS | get possible methods     |   x   |     x      |
| HEAD    | get without body         |   x   |     x      |
|         |                          |       |            |
| TRACE   |                          |       |            |
| CONNECT |                          |       |            |

**POST overloading** *< sending HTTP requests that doesnt exist can be done with a POST request. You send a method with the head that specifies what custom request you are using (document this correctly)>*

**Custom Methods** *< another way to use create new request methods, is to use custom http methods, just excange `post` for something else like `undelete` (document this correctly)>*

#### URIs

https://api.com/v2/comet
network location / resource

https://www.slideshare.net/landlessness/teach-a-dog-to-rest

#### Request
POST comet HTTP 1.1
VERB / resource uri / protocol 
Accept: application/json
Authorization: <token>
Connection: keep-alive

{
    "body": "body"
}


#### Response

protocol / statuscode
HTTP/1.1 200 OK
Serer: ngix
Age: 2323
Connection: keep-alive

{
    "id": "2"
    "status": "3"
}

#### Basic Networking

#### Statuscodes

2XX good
4XX client error
5XX server error

200 - OK

401 - Unauthorized

404 - Not found


### RESTfull API

**RESTful** *< Representational State Transfer, invented by Roy Fielding in 2000 >* 

JSON

### API Documentation
OpenAPI Specification
https://swagger.io/specification/

Postman



### Type RESTFULL Resources

**REST Resource** *< Het type resource wat in de body teruggestuurd word >*

Detail *< all data of specific item >*
Collection *< list of items with indexable information>*
Composition *< a combination of diffrent types of resources>*
Function *< functional resource, custom input generates custom output `/distance/rdam;adam`, GET>*
Controller *< special function, POST>*

### OAuth


## C. operations - VPS & Linux

### Virtual Private Server (VPS)

### Basic Networking / VPS commands

ssh username@ipa

### Linux
https://cheatography.com/davechild/cheat-sheets/linux-command-line/

#### Basic BASH commands

```bash
pwd # Show current directory
mkdir [dir] # Make directory
cd [dir] # Change directory to dir
cd .. # Go up a directory
ls # List files
-a # Show all (including hidden)
-t # Sort by last modified
-S # Sort by file size
cp # copy
mv # move
rm # remove

ps # process snapshot
kill [pid] # kill process
uptime # Show uptime
uname -a # Show system and kernel
whoami # Show your username
help / man # manuals and information
clear # clear screen

CTRL-C # Stop dcurrent running command
```

#### Backend MERN

```bash
sudo apt update # update apt packages
sudo apt install npm # install npm
sudo apt install nodejs # install nodejs
sudo apt install mongodb # install mondgodb

npm -v # check if npm is correctly installed
nodejs -v # check if nodojs is correctly installed
mongodb -v # check if mongodb is correctly installed

git clone / pull [repo] # clone or pull repository

cd [dir] # change directory to repo dir

npm i # install repo packages
node . # start node index.js

sudo systemctl status mongodb # check status of mongodb server

mongo --eval 'db.runCommand({ connectionStatus: 1 })' # diagnostic mongo command


sudo systemctl stop mongodb # stop mongodb server
sudo systemctl start mongodb # start mongodb server
sudo systemctl restart mongodb # restand mongodb server

sudo ufw status # check firewall status

sudo nano /etc/mongodb.conf # edit mongodb config

```

## D. frontend - React



## E. frontend - Sass
styleguides
http://styleguides.io/
https://web.archive.org/web/20170523012226/http://codepen.io/guide/#one


`end of file`  
*publish date: 0000-00-00*  
*modified date: 0000-00-00*  

<!-- LINKS -->
[google]: https://www.google.com  
[template.md]: template.md

