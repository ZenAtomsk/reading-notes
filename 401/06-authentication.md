# Authentication

## Sources

- [Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)
- [Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication)
- [OWASP auth cheatsheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)
- [bcrypt docs](https://www.npmjs.com/package/bcrypt)

1. Explain what a “Singleton” is (in Computer Science terms)

    - restricts the instantiation of a class to one "single" instance.

2. Explain how the Singleton pattern can be used with Node modules, specifically with classes

    - useful when exactly one object is needed to coordinate actions across the system. Before creating, check to see if one already exists, if so use that one

3. If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?

    - export a function which accepts an options object or other parameters, which, then returns the middleware implementation based on the input parameters.


## Vocabulary

[Router Middleware](https://expressjs.com/en/guide/using-middleware.html#middleware.router) works in the same way as application-level middleware, except it is bound to an instance of express.Router().

[Dynamic Module Loading](https://medium.com/@leonardobrunolima/javascript-tips-dynamically-importing-es-modules-with-import-f0093dbba8e1) -  it enables dynamic loading of ECMAScript modules. modules are static: you must specify what you want to import and export at compile time and this static structure of imports is enforced syntactically in two ways.

[Singleton Pattern]https://en.wikipedia.org/wiki/Singleton_pattern() - restricts the instantiation of a class to one "single" instance.

[CRUD -> REST Method Matches](https://medium.com/@ritika.atal.work/crud-mapping-to-http-verbs-354a3c0009f5)  

  - GET -> READ
  - POST -> CREATE
  - PUT -> UPDATE
  - DELETE -> DELETE

[Mock Testing](https://devopedia.org/mock-testing#:~:text=Mock%20testing%20is%20an%20approach,behaviour%20of%20the%20real%20ones.) - Mock testing is an approach to unit testing that lets you make assertions about how the code under test is interacting with other system modules. In mock testing, the dependencies are replaced with objects that simulate the behaviour of the real ones.
