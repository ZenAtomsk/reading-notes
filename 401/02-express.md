# Express

1. What’s the difference between PUT and PATCH?

    - 'The main difference between the PUT and PATCH method is that the PUT method uses the request URI to supply a modified version of the requested resource which replaces the original version of the resource, whereas the PATCH method supplies a set of instructions to modify the resource' [wiki](https://en.wikipedia.org/wiki/Patch_verb#:~:text=The%20main%20difference%20between%20the,instructions%20to%20modify%20the%20resource.)

2. Provide links to 3 services or tools that allow you to “mock” an API for development like json-server

    - [Mocky](https://designer.mocky.io/)
    - [MockServer](https://www.mock-server.com/)
    - [list of 10](https://nordicapis.com/10-tools-to-mock-http-requests/)

3. Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?

[swagger:](https://swagger.io/docs/specification/describing-responses/) 

    responses:
      '401':
        description: Authorization information is missing or invalid.
      '404':
        description: A user with the specified ID was not found.

[APIDoc:](https://apidocjs.com/#getting-started)

    response:
      HTTP/1.1 404 Not Found

4. Compare and contrast [SOAP and ReST](https://smartbear.com/blog/test-and-monitor/soap-vs-rest-whats-the-difference/)

- SOAP is a more rigid set of messaging patterns
- The rules in SOAP are important
- SOAP relies exclusively on XML to provide messaging services
- working with SOAP in JavaScript means writing a ton of code to perform simple tasks because you must create the required XML structure every time.

- REST as an architecture style does not require processing and is naturally more flexible
- REST provides a lighter-weight alternative

## **Vocabulary**

- [Web Server](https://whatis.techtarget.com/definition/Web-server#:~:text=A%20web%20server%20is%20software,and%20delivering%20webpages%20to%20users.) - A web server is software and hardware that uses HTTP (Hypertext Transfer Protocol) and other protocols to respond to client requests made over the World Wide Web. The main job of a web server is to display website content through storing, processing and delivering webpages to users.
- [Express](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction) - Express is the most popular Node web framework, and is the underlying library for a number of other popular Node web frameworks.
- [Routing](https://medium.com/@fro_g/routing-in-javascript-d552ff4d2921) - It is the piece of software in charge to organize the states of the application, switching between different views.
- [WRRC](https://medium.com/@jen_strong/the-request-response-cycle-of-the-web-1b7e206e9047) - Web Request Response Cycle - The web is a cycle of requests and responses that flow between clients and servers.

