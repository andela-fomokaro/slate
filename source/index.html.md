---
title: DocStar API Reference

language_tabs:
  - javascript


toc_footers:
  - <span>&copy; Andela, developed by Omokaro Faith</span>

includes:
  - users
  - documents
  - roles

search: true
---


# Introduction

The Document management system provides REST API enpoints for a document management system. It allows users create, retrieve, update and delete their documents.
It also ensures that users are authorized for the basic actions to be carried out.



## Usage
- Use Postman collection
  [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/8d7dc3154fb4a75853f2)

## Development

Document Management System API is built with the following technologies;
- JavaScript (ES6)
- [NodeJs](https://nodejs.org)
- [Express](http://expressjs.com/)
- [Postgresql](https://www.postgresql.org/)
- [Sequelize ORM](http://docs.sequelizejs.com/en/v3/)

## Installation
  - Install [NodeJs](https://nodejs.org/en/) and [Postgres](https://www.postgresql.org/) on your machine
  - Clone the repository `$ git clone https://github.com/andela-fomokaro/Document=Management-System.git`
  - Change into the directory `$ cd /dms`
  - Install all required dependencies with `$ npm install`
  - Start the app with `npm start`
  - Run Test `npm test`

## Contributing
- Fork this repository to your GitHub account
- Clone the forked repository
- Create your feature branch
- Commit your changes
- Push to the remote branch
- Open a Pull Request

## API Summary
### Users
EndPoint                      |   Functionality
------------------------------|------------------------
POST /users/login         |   Logs in a user.
POST /users/logout        |   Logs out a user.
POST /users/              |   Creates a new user.
GET /users/               |   Gets all users (available only to the Admin).
GET /users/:id           |   Finds user by id.
PUT /users/:id           |   Updates a user's attributes based on the id specified (available to the profile owner or admin)
DELETE /users/:id        |   Deletes user (available only to the profile owner)
GET /users/:id/documents   | Gets all documents for a particular user
### Documents
EndPoint                      |   Functionality
------------------------------|------------------------
POST /documents/          |   Creates a new document instance.
GET /documents/           |   Gets all documents.
GET /documents/:id       |   Find document by id.
PUT /documents/:id       |   Updates a document attributes. (available only to the author)
DELETE /documents/:id    |   Delete document. (available only to the author)
GET search/documents/?q=${query} | Get all documents with title containing the search query
### Roles (available only to the Admin)
EndPoint                      |   Functionality
------------------------------|------------------------
GET /roles/               |   Get all Roles.
POST /roles/               |   Create a Role.
PUT /roles/:id               |   Edit a Role.
DELETE /roles/:id               |   Delete a Role.
