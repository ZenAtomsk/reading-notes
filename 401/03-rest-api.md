# Express REST API

- [Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
- [Basic routing](https://expressjs.com/en/starter/basic-routing.html)
- [Using Express Routing](https://expressjs.com/en/guide/routing.html)
- [Learn to Use the New Router in ExpressJS 4.0](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)

1. **Name 3 real world use cases where you’d want to change the request with custom middleware**

security authentication, transaction management, message queues

2. **True or false: The route handler is middleware?**  

True. a function which "handles" sending the response and a function which encapsulates behavior but does not send a response are much the same. So in that regard they are all "middleware".

3. **In what ways can a middleware function end the process and send data to the browser?**

next('when something is written in here, because there was something disagreeable');

4. **At what point in the request lifecycle can you “inject” middleware?**

any time before it reaches the server

5. **What can cause express to error with “Request headers sent twice, cannot start a second response”**

The error "Error: Can't set headers after they are sent." means that you're already in the Body or Finished state, but some function tried to set a header or statusCode. [source](https://stackoverflow.com/questions/7042340/error-cant-set-headers-after-they-are-sent-to-the-client)

Document the following Vocabulary Terms
Term

- **Middleware** - software that acts as a bridge between an operating system or database and applications, especially on a network.

- **Request Object** - main entry point for an application to issue a request to the Library. A request object is registered in the library by issuing an operation on a URL - for example PUT, POST, or DELETE

- **Response Object** - response to a request. [Lots of choices](https://developer.mozilla.org/en-US/docs/Web/API/Response)

- **Application Middleware** - This can include security authentication, transaction management, message queues, applications servers, web servers and directories

- **Routing Middleware** - An Express application is essentially a series of middleware function calls. [Routing middleware](https://expressjs.com/en/guide/using-middleware.html)

- **Test Driven Development** - is a software development process relying on software requirements being converted to test cases before software is fully developed, and tracking all software development by repeatedly testing the software against all test cases [Wiki](https://en.wikipedia.org/wiki/Test-driven_development)

- **Behavioral Testing** - human-readable descriptions of software user requirements as the basis for software tests.
