Requirements
===

## Project technical stack

### Server-side

+ [python3.9](https://www.python.org/)
+ [Fast-API](https://fastapi.tiangolo.com/)
+ [SQLAlchemy](https://www.sqlalchemy.org/)
+ [Alembic](http://www.alembic.com/)
+ [Postgres](https://www.postgresql.org/)
+ [RabbitMQ](https://www.rabbitmq.com/)


### Client-side
+ [ReactJS](https://reactjs.org/)
+ [React-bootstrap](https://react-bootstrap.github.io/)

## Glossary

|Word| Meaning |
|-|-|
| room| Basically, a room is a collection of messages, that users have sent to the room|
|asynchronous|Then events come to services independent from program flow|
|web framework|An abstract library that gives opportunity to create a web application|
|CAPTCHA|test used in computing to determine whether or not the user is human|


## Stakeholders Roles

|Stakeholder’s Name|Roles|Responsibilities|
|-|-|-|
|Ivan Izmailov|Backend, DevOps|API server, CI/CD, design and architecture creator|
|Lev Lymarenko|Frontend, team management|Web client, updating docs, task distribution|
|Ivan Obraztsov|Frontend|Web client design and implementation|

## User stories

### Epic 1. Web client

#### **US-101. Rooms list**

As a anonymous user I want to go to main chat page and see full list of rooms and their short descriptions So that I can see brief history of application

#### **US-102. Messages list**

As a anonymous user when I click to avaliable room from rooms list then I see messages of this rooms from other users

#### **US-103. Room info**

As a anonymous user I want to see the username of the person who created the room and the creation date So that I can distinguish rooms with the same names

#### **US-104. Creating rooms**

As a {ref}`registered <us-201>` user I want to create new room with given name So that I can create a topic that interests me

#### **US-105. Chatting**

As a {ref}`registered <us-201>` user I want to send a text message to avaliable room So that I can chat with other people

### Epic 2. Authentication

(us-201)=
#### **US-201. Registration**

As a anonymous user I want to register my username in system So that I can become a `registered` user and be able to create rooms and chat with other people.

#### **US-202. Robots suppression**

As a registered user I don't want to see spam from robots in chats and I would like to see a way to stop robots from registering in the system So that I will be less likely to communicate with robots.

## Non-functional requirements

### Usability
User interface standards used. Provided documentation.

### Reliability
Safety and security requirements. Exception handling. Mean time between failures. 

### High-speed response
Returning a appropriate response is 99.99% of the time.
Using asynchronous fast framework.

### Implementation

System must support all popular platforms

### Interfaces
There is clear interfaces to existing systems.

