Roadmap
What is a Full-Stack Developer?
SEI Web Technology Stacks
Client/Server Architecture
What is HTTP?
Let's Make an HTTP Request
Anatomy of an HTTP Request Message
Anatomy of an HTTP Response Message
The Two Key Components of an HTTP Request
HTTP Methods
Ways to Send HTTP Requests From the Browser
How HTTP Requests Run Code on the Server
Essential Questions

#### What is a Full-Stack Developer?
* A full-stack developer is a developer who is comfortable working with both front-end & back-end technologies.

* Can create full-stack applications by writing code that runs in both a client, such as a browser, and a web server.

* Will often specialize in front-end or back-end technologies.


Web Technology Stack
In this unit, we'll learn 3 of the 4 technologies that comprise the MERN Stack, one of the most popular technology stacks in the industry.


#### Client/Server Architecture
The terms client and server can refer to both a physical device (computer, tablet, phone, etc.) but can also refer to a software process. For example:

* Database software such as PostgreSQL and web servers like Apache are examples of software processes behaving as servers.

* Browser software such as Chrome or Firefox are examples of software clients.

* Physical servers connected to the Internet are also referred to as hosts.

* Web developers usually think of a "web browser" when they hear "client".

Note that during development, your computer will plays the role of BOTH client and web server.

The PostgreSQL & MongoDB database servers will also be running on your computer, however, we will move to a cloud-based MongoDB server as soon as it's practical.


#### What is HTTP?
Hypertext Transfer Protocol (HTTP) is an application-level network protocol that powers the communications across the World Wide Web, more commonly referred to as just the Web.

* HTTP is fundamental to web development - regardless of which back-end or front-end web technology/framework is used.

* When a user interacts with an amazing web application we developed, it's HTTP that informs the web application what the browser wants and it's HTTP that delivers the goods from the server back to the browser.

* The process of a client sending a HTTP request, and server responding is known as the HTTP Request/Response Cycle:

When we browse to a website by typing in the address bar, this is what happens:

* When the response is received by the client, that request/response cycle has ended and there will be no further HTTP communications unless another request is sent by the client.

HTTP itself does not maintain any information regarding previous requests between client and server - this makes HTTP a stateless protocol. However, it is possible to remember "state" using cookies or by sending data in the request's body (data payload).




#### Anatomy of an HTTP Request Message
The GET request we just sent does not contain a message body nor a Content-Length header because...

The Request Body is optional and present only when the client is sending data to the server.

An example of when the body might contain data is when the contents of an HTML form are being submitted by the user.


The status code in the first line informs us on how the request/response went. It is always a three-digit number that falls within the following ranges/categories:

1xx Informational
2xx Success
3xx Redirection
4xx Client Error
5xx Server Error
Most HTTP responses will have a status code of 200, which means OK. You also might be familiar with the status code of 404- Not Found.

The Response Body is what holds the content of the requested resource.

The Content-Type header helps the browser determine what to do with the data being sent in the body of the HTTP response. For example:

* text/html: The browser will parse the body as HTML and, depending on how the HTTP request was initiated, usually replace the browser window's content with the newly received HTML.
*image/png
###### Although the HTTP protocol is text-based, the content in the body can be binary, for example, images are typically transferred in binary format.


#### The Two Key Components of an HTTP Request
We saw earlier that every HTTP request message begins with a request-line like this:

GET /sample_page.html HTTP/1.1
The two key components of any HTTP request are:

The HTTP method (GETin the example above), and
The request target, which is usually a URL (the above example is more accurately a URI)



HTTP Methods
HTTP methods, are used to indicate the desired action to be performed for a given resource (specified by the URL) on the server.

The fact that they indicate action is why they are also at times called HTTP Verbs.

We'll be using the following HTTP Methods when we start defining our application's routes:

HTTP Method (Verb)	Desired Action on Server
GET	The GET method requests a representation of the specified resource (URL). Requests using GET should only retrieve data.
POST	The POST method is used to create a resource on the server.
PUT	The PUT method replaces a resource with the request payload(data in the body).
DELETE	The DELETE method deletes the specified resource.


#### URL
URL stands for Uniform Resource Locator.

It informs the server of what resource the client wants to GET. create (POST), DELETE, etc.

