Lesson Objectives
Read URL parameters
Common error: two responses
Common error: Place routes in correct order
Multiple Params
Request Object
URL Queries
Environment Variables


### Express - A Review and Re-Cap
##### Express is a code library hosted on npmthat is written in JavaScript. Express is a library/un-opinionated framework for building a web server
* we initialize our folder as an npm project by typing npm init
* we add npm packages by typing npm install <package-name>e.g. npm install express
* we use the require()function to bring in the code
* we add app.listen(port)to turn on our server, by default, it will listen to http://localhost, we have to pick a port, usually ports for servers that we'll be building are in the numeric range of 3000 - 9000. When we host our projects on the web, the port will be automatically configured for us

Express Routes
Once our server is configured, we have to add routes.

Routes are kind of like event listeners. They get set up and they just wait. But rather that waiting for a user to click on a button, the routes wait for someone to go to their URL in the browser. When you type in the browser, the only type of request you can make is a getrequest. We'll learn later how to make other types of request. But for today, all routes will start with app.get('/')

Once someone goes to that URL, it'll trigger a callback. The callback always needs two parameters requestthen responseand always in that order.

requestand response(or can be named reqand resfor short) are objects that have a lot of properties and functions built-in. You can console.logeach of these params.

One function on the response object is send(), which let's us send a string back to the browser.

``` 
app.get("/free_samples", (request, response) => {
  response.send("here are some free samples")
})
``` 

Read URL parameters
Most of the time, we'll use segments in the path section of the URL to modify how our application works.

To do this, we'll use request parameters. To the user, it'll just look like an extension of the url path.

Let's think of Amazon again. With 300 million products and counting, hard coding a route for each product and keeping track of it all would be nightmarish.

We'll work with a simplified example. Imagine a store: The Botany Expressthat sells a few plants. Rather than having a dedicated route for each plant, the plants are stored as data (in our case an array of strings). We can access the data by passing in the index as a part of the request URL.

To set URL parameters in your server.js, just add a colon after the forward slash and then a variable name.

'Regular' URL: /plants

URL parameter: /:indexOfPlantsArray

The entire route:

app.get("/:indexOfPlantsAraay", (req, res) => {
  res.send(plants[req.params.indexOfPlantsArray])
})

We can access the value of :indexOfPlantsArraywith req.params.indexOfPlantsArray

Let's code together to see this in action.
mkdir express-plants
cd express-plants
touch server.js
npm init
npm i express
Here is an array of plants, we can copy paste this bit of 'data':

const plants = [
  "Monstera Deliciosa",
  "Corpse Flower",
  "Elephant-Foot Yam",
  "Witches' Butter",
]



Let's add this data array to an express "boilerplate"; here's what we should aim for:

const express = require("express")
const app = express()
const port = 3000

const plants = [
  "Monstera Deliciosa",
  "Corpse Flower",
  "Elephant-Foot Yam",
  "Witches' Butter",
]

app.get("/:indexOfPlantsArray", (req, res) => {
  //
  res.send(plants[req.params.indexOfPlantsArray])
})

app.listen(port, () => {
  console.log("listening on port", port)
})



Start up your server in terminal

Now visit http://localhost:3000/0in your browser

Monstera Deliciosa

Now visit http://localhost:3000/3in your browser

Witch's Butter

Note: http://localhost:3000

error cannot GET (we didn't write a route for this)

Let's breakdown the contents of our localhost URL:

    http://localhost:3000/2
    \___/  \_______/ \__/ \_/
  protocol    host   port   path*
Path can be a URL or a URL parameter: it will look the same in the browser. The difference will be in the server.

The URL parameter, will be added as a key:valuepair inside the request.paramsobject.

The key is what we named it in our server, the value will be whatever the user has typed in the browser.




A Common Error
You can only have one response for every request. If you try to send multiple responses you'll get an error. Let's try it!

app.get("/oops/:indexOfPlantsArray", (req, res) => {
  res.send(plants[req.params.indexOfPlantsArray])
  // error cannot send more than one response!
  res.send("this is the index: " + req.params.indexOfPlantsArray)
})
We can, however, have multiple statements if we use our ifstatements or other program logic correctly:

app.get("/fixed/:indexOfPlantsArray", (req, res) => {
  if (plants[req.params.indexOfPlantsArray]) {
    res.send(plants[req.params.indexOfPlantsArray])
  } else {
    res.send(
      "cannot find anything at this index: " + req.params.indexOfPlantsArray
    )
  }
})



Place routes in correct order
Express starts at the top of your server.jsfile and attempts to match the url being used by the browser with routes in the order in which they're defined
URL params (e.g. :foo, :example, :indexOfPlantsArray) can be anything, a number, or even a string
Therefore if you have these routes in this order in your server.js:
/:color
/plants
And you want to get to /plants- you'll always hit the /:colorroute because the URL parameter will accept any string, it doesn't know that plantsis something specific/special
To fix this, we put the more specific routes first
/plants
/:colorNow, from top to bottom, the more specific route /plantswill be triggered when the URL has plantsand if it doesn't match plants, it will go to the next route.
Let's code an example of this together:

const express = require("express")
const app = express()
const port = 3000

const plants = [
  "Monstera Deliciosa",
  "Corpse Flower",
  "Elephant-Foot Yam",
  "Witches' Butter",
]

app.get("/:indexOfPlantsArray", (req, res) => {
  //:indexOfPlantsArray can be anything, even awesome
  res.send(plants[req.params.indexOfPlantsArray])
})

app.get("/awesome", (req, res) => {
  //this will never be reached
  res.send(`
    <h1>Plants are awesome!</h1>
    <img src="https://static.boredpanda.com/blog/wp-content/uuuploads/plant-sculptures-mosaicultures-internationales-de-montreal/plant-sculptures-mosaicultures-internationales-de-montreal-14.jpg" >
  `)
})

app.listen(port, () => {
  console.log("listening on port", port)
})


If this happens, reorder them so that more specific routes come before less specific routes (those with params in them)

const express = require("express")
const app = express()
const port = 3000

const plants = [
  "Monstera Deliciosa",
  "Corpse Flower",
  "Elephant-Foot Yam",
  "Witches' Butter",
]

app.get("/awesome", (req, res) => {
  res.send(`
    <h1>Plants are awesome!</h1>
    <img src="https://static.boredpanda.com/blog/wp-content/uuuploads/plant-sculptures-mosaicultures-internationales-de-montreal/plant-sculptures-mosaicultures-internationales-de-montreal-14.jpg" >
  `)
})

app.get("/:indexOfPlantsArray", (req, res) => {
  res.send(plants[req.params.indexofPlantsArray])
})

app.listen(port, () => {
  console.log("listening on port", port)
})



Multiple Params
We can store multiple params in the req.paramsobject:

??? Write in (5 min)

app.get("/hello/:firstname/:lastname", (req, res) => {
  console.log(req.params)
  res.send("hello " + req.params.firstname + " " + req.params.lastname)
})
In your browser, go to localhost:3000/hello/bob/bobbybob
??? Check the req.params console.log in Terminal



Try entering different firstnames and lastnames in your URL and check the results



The Request object
This is just interesting, as well as informative, but not necessary to get anything to work.

What happens if we console.log the entire Request Object?

console.log(req)?

In the hello/:firstname/:lastnameroute, before res.send, write in:

console.log("=========================================")
console.log(
  "This is the entire Request Object sent from the browser to the server: "
)
console.log(req)
console.log("========================================")
This will allow you to see the entire request object. This object contains all of the information that the browser sends to the server. There's a ton of information in there!

app.get("/hello/:firstname/:lastname", (req, res) => {
  // console.log(req.params);
  console.log("=========================================")
  console.log(
    "This is the entire Request Object sent from the browser to the server: "
  )
  console.log(req)
  console.log("========================================")
  res.send("hello " + req.params.firstname + " " + req.params.lastname)
})



??? Activity (5 min)

In the browser, go to the /hello/firstname/lastname route
Have a look through the entire request object in Terminal
Find the req.paramsobject within it.
The reqobject is where the req.paramsobject is stored when the browser makes a request to the server.
req.paramsis an object nested within the reqobject.

req.paramsis the only one we will need for today.




req.query
A query is a key-value pair separated with an =, and added to the URL with a ?. It is put at the end or the URL. These vallues are stored in a separate object from req.params: they are stored in the object req.query

?someKey=someValue

localhost:3000/howdy/Edinburgh?title=duke
app.get("/howdy/:firstName", function (req, res) {
  console.log(req.params)
  console.log(req.query)
  res.send("howdy " + req.query.title + " " + req.params.firstName)
})


You can add multiple queries

localhost:3000/hello?title=duke&year=2001
Spaces are represented with a %20.




Environment Variables
Currently you are using your computer's nodejsas your environment. This is different than the environment in the browser. If you were to try run the alert()function in your server.jsit would give an error - because the browser and node are two different environments that both run JavaScript.

If you wanted to collaborate on this project, you'd likely have your collaborator get a copy of your code from github.

They would be running the app on their environment(computer).

If you were to host your app on the internet on a virtual server, you'd likely need to set different environment variables than the ones you have on your computer.

This is a contrived example, but simple enough to demonstrate the problem and a solution:

Let's say you want to run this app on port 3000. Your collaborator wants to run it on port 3001and your hosted version on the internet wants to run it on port 8888.

You could, constantly update it in your server.js... but that seems problematic.

A better option would be to add another npm package like dotenv

Go ahead and run:

npm i dotenv

At the top of server.jsadd, as per the docs

require("dotenv").config()
touch .envon the same level of server.js

touch .gitignore(if you haven't already), be sure to add node_modulesand .env

As per the docs, no spaces, no commas, no semi-colons. If you have a second variable, you would put it on the next line.

In .env

PORT = 3000
In server.js

const port = process.env.PORT
Your environmental variables are yours, and should be private. If you put them on github everyone can see! So you should have git ignore them.

Remember that we've already installed a global .gitignoreso we won't need to take any action.
Port numbers aren't sensitive, but you could use this file to store passwords, api keys and encryption codes and more. So you want to be mindful of this file and keep it safe.

let's see if we can access this variable

server.js

require("dotenv").config()
const express = require("express")
const app = express()
console.log(process.env.PORT)
We should see the port number we put inside our .envfile

We can now update our port. We can use ||to also set a default.

const port = process.env.PORT || 3003
and update our app.listen

app.listen(port, () => {
  console.log("I am listening on port", port)
})


