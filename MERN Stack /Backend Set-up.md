#### Serverside Backend Setup with JWT authorization
1. Setup backend using npm and install ncessary packages
2. Set up MongoDB database unsing MongoDB atlas cloud
3. Create a Database schema to define user for registration and login
4. Set up two API routes (register and login) using jsonwebtoken for authentication and build input validation without any dependenciess.
5. Test our API routes using Postman.

## Set up Backend
##### Create a project folder in your workspace to build REST API (backend) and run the following command.
* npm init 
###### After running the command, package.json will be created and set up index.js as the default entry point.

## Install NPM Packages
###### Next, Install the NPM dependences by running the below command
* npm i express jsonwebtoken bcrypt body-parser 
cors mongoose dotenv

###### Brief information about each package and why we are using this to build rest APIs.
* Express: Express is a nodejs web application framework that helps in creating rest APIs.
* Brcypt: A library to hash passwords.
* Body-parser: It is used to parse incoming request bodies in a middleware.
* Jsonwebtoken: This package creates a token used for authorization for secure communication between client and server.
* Mongoose: Mongoose is an Object Data Modeling (ODM) library for MongoDB and Node. js that allows you to interact with MongoDB database.
* Cors: CORS is a node.js package for providing a Connect Express middleware that can be used to enable CORS with various options.
* Dotenv: Dotenv is a zero-dependency module that loads environment variables from a .env file.

##### Let's install nodemon which helps in monitoring and starting the node server when any changes occurs in the server files. 
* npm i -D nodemon


## Set up  our express.js server

const express = require('express');
const app = express();

const port = 8000;

app.listen(port, () => {
   console.log(`Hello World`)
})

## Setting up the env file and connecting our server with MongoDB
* Create .env file on the root folder by running the commandtouch .env
* Add MongoDB URL (databaseURL) and Port

PORT=8000
DATABASE=mongodb+srv://<username>:<password>@cluster0.suxf5.mongodb.net/<dbname>?retryWrites=true&w=majority

* Add code to index.js to test 

require('dotenv').config();

const express = require('express');
const cors = require('cors')
const bodyParser = require('body-parser');
const connectDB = require("./config/db")
const app = express();

const { PORT = 8000} = process.env || 8000;

//database connection
connectDB()

//middlewares
app.use(cors());
app.use(bodyParser.json());


// Express Listener
app.listen( PORT, () => console.log(`Express is listening on:, port ${PORT}`));

* in config folder touch db.js and add 
//connect mongoose db
const mongoose = require('mongoose');

const connectDB = async () => { 
  try {
    const conn = await mongoose.connect(process.env.DATABASE);
    console.log(`MongoDB Connected: ${conn.connection.host}`);
  } catch (error) {
    console.log(error);
    process.exit(1); // Exit the process with failure
  }
};

module.exports = connectDB

##### Define User Schema
* define user schema using mongoose ODM. It allows us to retrieve the data from the database.

mkdir models
cd models
touch User.js






Source: https://medium.com/swlh/user-authentication-using-mern-stack-part-1-backend-cd4d193f15b1