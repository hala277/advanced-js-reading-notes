# API Integration

## Review API Server Build

**Dynamic API Server**

An Express/Node.js based server designed to be a “model agnostic” REST API server, which can perform CRUD operations on any data model

### Support all REST/HTTP methods
+ GET: Retrieve record(s) from a data source 
+ POST: Create a new record in a data source
+ PUT: Update a single full record in a data source
+ PATCH: Update part of a single record in a data source
+ DELETE: Delete a record in a data source

## Authentication Server / Module

An Express/Node.js based server using a custom “authentication” module that is designed to handle user registration and sign in using Basic, Bearer, or OAuth along with a custom “authorization” module that will grant/deny users access to the server based on their role or permissions level.

+ Users can create an account, associated with a “role”.
+ User Roles will be pre-defined and will each have a list of allowed capabilities
  + admin can read, create, update, delete
  + editor can read, create, update
  + writer can read, create
  + user can read
+ Users can then login with a valid username and password
+ Alternatively, users can login using an OAuth provider such as Google or GitHub
+ Once logged in, Users can then access any route on the server, so long as they are permitted by the capabilities that match their role.