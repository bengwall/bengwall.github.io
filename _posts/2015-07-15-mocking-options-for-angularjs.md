---
published: true
layout: post
title: Mocking Options for AngularJS
---

##Why Mocking is Important

Developing a database and REST api is expensive.  It gets more expensive when requirements change.  Mocking a backend service will enable us to validate requirements and test out UI designs and flow early on in the development process.  This will serve to greatly reduce requirements risk and UI related change requests.


##Mock Options

###Parse.com

**Description:**  A cloud based database and REST api (“backend as a service”)

**Pros/Cons:**

- Free tier
- Easy to setup and use
- Can import data
- Data can be shared between all developer workstations and on the pre-prod tiers
- Enables true REST calls
- Can simulate backend security/users/roles
- Steep learning curve to setup backend logic or validation
- Does not hook into Single Signon

**When to use:** Parse is good to use when you want to simulate REST calls and want data shared between servers/workstations

**References:**

- [www.parse.com](www.parse.com)


###JSON-Server

**Description:**  A local file based JSON database

**Pros/Cons:**

- Free and open source.  Just a JavaScript library
- Easy to setup and use
- Can initialize with mock data with the faker library
- Cannot simulate security
- Cannot run backend logic or validation


**When to use:**	JSON-Server is good to use when you want basic REST calls and do not need data saved between deploys or app restarts

**References:**

- [https://github.com/typicode/json-server](https://github.com/typicode/json-server) 
- [https://egghead.io/lessons/nodejs-creating-demo-apis-with-json-server](https://egghead.io/lessons/nodejs-creating-demo-apis-with-json-server)

###Meteor

**Description:**  Meteor is a JavaScript application platform.  It has it’s own UI framework, communication mechanism, and backend with a MongoDB database.  You write your client-side and server-side code in JavaScript and in the same project (but separate directories).  

**Pros/Cons:**

- Free and open source.
- Easy setup
- Would not truly simulate REST calls.  It would use Meteor’s communication layer.
- Requires a bit of a learning curve
- You can easily use Angular for the UI using the Angular-Meteor library.
- Deploying to development servers would require infrastructure groups

**References:**

- [https://github.com/Urigo/angular-meteor](https://github.com/Urigo/angular-meteor)

**When to use:** I would only recommend using this if you were curious about Meteor and actually might consider using Meteor and hence MongoDB.


###.Net EntityFramework, WebPI and oData

**Description:** EntityFramework, WebAPI and oData are Microsoft technologies which streamline data access and REST api development.

**Pros/Cons:**

- Requires Visual Studio 2013 or 2015
- Runs only on Windows
- Can quickly setup a SQL Server database and generate an entire REST api
- Fairly simple to get an API up and running with a database in the backend.
- Learning curve to simulate backend logic and validation for those not already familiar with EntityFramework.
- Has built in data migration for updating SQL Server schema’s as changes are made and updated code is deployed.

**When to use:**  Can be an alternative to Parse for those who want a true database backend.  The advantage here is that the data remains local and it could actually be used in a production environment is allowed.

###Angular-Mock

**Description:**  With Angular-Mock, Angular will intercept http requests and allow you to handle and respond to them in your JavaScript code. 

**Pros/Cons:**

- Very flexible but limited
- Time consuming to setup because it is all in code
- Can be deployed
- It is not connected to a database so only preset responses will be sent back
- The library restful-ng-mock makes the request handling a little simpler

**When to use:** Use when you have very basic mocking needs and do not need dynamic data from a backend database






