---
title: API
---

All the functionality of the GLAMpipe is available via REST API. One can create projects, import data, create nodes and run them, and get data on any collection.

#### Login
If you installed GLAMpipe to locally, then you can forget authentication. But if you are using hosted version of GLAMpipe, then you need to authenticate for PUT, POST and DELETE requests. All GET requests are "free". 

Authentication is token based. It means that you send your username and password once to the server and then the server sends a token back to you. You need to send that token with every PUT, POST and DELETE request.

        
        
| path          | method | parameters     | info            |
|---------------|--------|----------------|-----------------|
| api/v1/login  | POST   | email password | Get a token     |
| api/v1/signup | POST   | email password | Create new user |

##### example

Get token:

		curl -H "Content-Type: application/json" -d '{"email":"myuser","password":"mypass"}' http://localhost:3000/api/v1/login

### Projects

Creating projects is simply, just send the name of the project:

| path                   | method | parameters    | info               |
|------------------------|--------|---------------|--------------------|
| api/v1/projects        | POST   | title (token) | Create project     |
| api/v1/projects        | GET    |               | Get all projects   |
| api/v1/projects/titles | GET    |               | Get project titles |