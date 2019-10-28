# Homework: Full Stack Games Hub App

### Learning Objectives

- Understand the relationship between client, server and database
- Be able to navigate a codebase that you haven't written

## Brief

Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using Vue, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.

The application includes a README.md with instructions on running the application.

![Overview of the tech stack and tooling with commands](images/tech_stack_with_commands.png)

*Overview of the tech stack and tooling with commands*

## MVP

### Task

Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

### Questions

1. What is responsible for defining the routes of the `games` resource?
Lewis: createRouter function creates the routes in create_router.js
2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?
Lewis: client dir holds the front end components and handles the user interaction and input server holds the files related to the database (clearing then creating entries via seeds and defining the restful routes for working with the database)
3. What are the the responsibilities of server.js?
Lewis: opens a connection on the server and connects the client to it, sets up middleware packages used (CORS) and a parser for the json messages.
4. What are the responsibilities of the `gamesRouter`?
Lewis: its a router which points specifically to the games api and is created from the base router template in server.js
5. What process does the the client (front-end) use to communicate with the server?
Lewis: GamesServices.js
6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs
Lewis: init, which we are using to set which REST action is being performed when modifying the database and to add body and header to the request.
7. Which of the games API routes does the front-end application consume (i.e. make requests to)?
Lewis: GET(INDEX) and POST and DELETE
8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?
Lewis: Communication between the server and the database.

## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?

Add to your diagram the dataflow for removing a game.
