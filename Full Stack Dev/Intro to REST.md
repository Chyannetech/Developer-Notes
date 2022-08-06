Lesson Objectives
Describe REST and list the various routes
Create an Index route
Install JSONView to make viewing JSON easier
Create a Show route
Enhance the data in your data array



# Describe REST and list the various routes
### REST stands for Representational state transfer
It's just a set of principles that describe how networked resources are accessed and manipulated
We have 7 RESTful routes that allow us basic operations for reading and manipulating a collection of data:
URL	HTTP Verb	Action
/photos/	GET	index
/photos/:id	GET	show
/photos/new	GET	new
/photos	POST	create
/photos/:id/edit	GET	edit
/photos/:id	PATCH/PUT	update
/photos/:id	DELETE	destroy


Create an Index route



Setup our app
Create a directory called fruits
npm init
Create a server.jsfile.
install express
require express and set up a basic server that logs listening when you start the app
start the app with nodemon and make sure it is working
Let's have a set of resources which is just a javascript array. To create an index route, we'd do the following:

const express = require("express")
const app = express()

const fruits = ["apple", "banana", "pear"]

app.get("/fruits/", (req, res) => {
  res.send(fruits)
})

app.listen(3000, () => {
  console.log("listening")
})
Now go to http://localhost:3000/fruits/




Install JSON Formatter to make viewing JSON easier
JSON stands for Javascript Object Notation
It's just a way to represent data that looks like a Javascript object or array
JSON Formatter extension just makes it easier to view JSON data.
If you don't have it already, let's make sure we install it:

Click here:  https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa
Click on "Add To Chrome"



Create a Show route
To create a show route, we'd do this:

const express = require("express")
const app = express()

const fruits = ["apple", "banana", "pear"]

app.get("/fruits/", (req, res) => {
  res.send(fruits)
})

//add show route
app.get("/fruits/:indexOfFruitsArray", (req, res) => {
  res.send(fruits[req.params.indexOfFruitsArray])
})

app.listen(3000, () => {
  console.log("listening")
})
Now go to http://localhost:3000/fruits/1




Enhance the data in your data array
Right now are data array fruitsis just an array of strings
We can store anything in the array, though.
Let's enhance our data a bit:
const express = require("express")
const app = express()

const fruits = [
  {
    name: "apple",
    color: "red",
    readyToEat: true,
  },
  {
    name: "pear",
    color: "green",
    readyToEat: false,
  },
  {
    name: "banana",
    color: "yellow",
    readyToEat: true,
  },
]

app.get("/fruits/", (req, res) => {
  res.send(fruits)
})

app.get("/fruits/:indexOfFruitsArray", (req, res) => {
  res.send(fruits[req.params.indexOfFruitsArray])
})

app.listen(3000, () => {
  console.log("listening")
})


https://en.wikipedia.org/wiki/Representational_state_transfer
https://expressjs.com/en/4x/api.html#app