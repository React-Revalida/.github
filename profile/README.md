# Welcome to Spill - our social media app! 👋

<img src="https://github.com/React-Revalida/socmed-app-frontend/blob/development/src/assets/SpillLogo.png" width="350" height="300">

## Spill - Spill your tea to the world ☕

Spill is a lightweight social media application that gives users the opportunity to share and express their thoughts freely and safely within its sphere. With Spill, you can share a tea with other users, take a sip from teas, follow desired users, maybe connect with them and have some tea time!

_New release: Now supporting Chats! Users following each other can now send messages to each other._

## Tech Stack

Spill is implemented via Spring Boot in the backend where it utilizes dependencies such as Spring Web, Spring Data JPA, Spring Security, OAuth2, Spring Cloud OpenFeign, AWS Java SDK, and WebSocket. It uses PostgreSQL driver and Digital Ocean to host photos in the cloud.  
  
In the frontend, Spill is built from React with Redux implementing the state management. It also uses a Elastic Email as its email service and has multiple dependencies such as Material UI, React Router, SockJS, STOMP, and MomentJS, to name a few.

## Backend System Requirements
* Java 17
* PostgreSQL 15

## Frontend System Requirements
* Node 18.12.1
* NPM 9.2.0

## Setup
Clone the three repositories found in this organization.

A Maven build is required to build and update the project dependencies (Spring Web, Spring Data JPA, 0Auth2, Lombok, and more). 

For the backend, a database named _socmed_ is required before running the Spring Boot application. 
Run the backend repository along with the chat service repository. The backend should be running on port 8080 and the chat service at port 8085.  

```
cd /path-to-src-resources/
psql -U postgres -W -p <port> 
create database socmed;
\c socmed;
```

Prepopulate the PostgreSQL database using the _dummydata.sql_ found in src/resources in the backend repository. 
```
\i dummydata.sql;
```
  
The frontend requires install of dependencies initially.

```
npm install --legacy-peer-deps
```

Prerequisite: An Elastic Email account is required to make the _forgot-password_ functionality work. Create an account [here](https://app.elasticemail.com/), generate an _.env_ file at the root of the directory and supply the credentials needed in the application.

```
npm start
```

The application should be running now on _http://localhost:3000_.


_In partial fulfillment of the requirements for Career Development Training Program for Seven Seven Global Services, Inc._

## Team Behind the App
CDP Batch 04-22 Group 1  
For questions, bugs, and feature requests, you may connect with the development team:
* [Brynpryl Bandiola](https://github.com/brynpryl77)
* [Lawrence Dave Paulino](https://github.com/paulinolawrence08)
* [Harvey Samson](https://github.com/samsonharveyy)
* [Ayn Gandhi Uson](https://github.com/AynUson)

## Some Helpful References
* [Get Started with Spring Boot](https://docs.spring.io/spring-boot/docs/current/reference/html/)  
* [Spring Data JPA](https://docs.spring.io/spring-data/jpa/docs/current/reference/html/)  
* [OAuth2](https://docs.spring.io/spring-security/reference/servlet/oauth2/index.html)  
* [Learn ReactJS](https://reactjs.org/docs/getting-started.html)  
* [Redux](https://react-redux.js.org/)
