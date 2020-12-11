# Data Modeling

1. **Name 3 advantages to Test Driven Development** 

    [Source](https://www.codica.com/blog/test-driven-development-benefits/)

    - Better program design and higher code quality
        - When writing tests, programmers first have to define a goal they will achieve with the code piece.
    - Detailed project documentation
        - programmers immediately create a strict and detailed specification
    - TDD reduces the time required for project development

2. **In what case would you need to use beforeEach() or afterEach() in a test suite?**

    [Source](https://jestjs.io/docs/en/setup-teardown)

    - If you have some work you need to do repeatedly for many tests

3. **What is one downside of Test Driven Development**

    [Source](https://leantesting.com/test-driven-development/)

    - It necessitates a lot of time and effort up front, which can make development feel slow to begin with

4. **What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?**

    [Source](https://medium.com/javascript-scene/master-the-javascript-interview-what-s-the-difference-between-class-prototypal-inheritance-e4cd0a7562e9)

    - Inheritance.
        - Classes inherit from classes and create subclass relationships: hierarchical class taxonomies
        - A prototype is a working object instance. Objects inherit directly from other objects

5. **Why REST?**

    [Source](https://smartbear.com/blog/test-and-monitor/soap-vs-rest-whats-the-difference/)

    - REST provides a lighter-weight alternative. 

## Vocabulary Terms:

- [**functional programming**](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0#:~:text=Functional%20programming%20(often%20abbreviated%20FP,state%20flows%20through%20pure%20functions.)) - the process of building software by composing pure functions, avoiding shared state, mutable data, and side-effects. Functional programming is declarative rather than imperative, and application state flows through pure functions.

- [**object-oriented programming (OOP)**](https://en.wikipedia.org/wiki/Object-oriented_programming#:~:text=Object%2Doriented%20programming%20(OOP),(often%20known%20as%20methods).) - a programming paradigm based on the concept of "objects", which can contain data and code: data in the form of fields (often known as attributes or properties), and code, in the form of procedures (often known as methods) 

- [**class**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes) - Classes are a template for creating objects. They encapsulate data with code to work on that data. 

- [**super**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/super) - The super keyword is used to access and call functions on an object's parent. 

- [**this**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this) - A property of an execution context (global, function or eval) that, in non–strict mode, is always a reference to an object and in strict mode can be any value. 

- [**Test Driven Development (TDD)**](https://medium.com/javascript-scene/tdd-changed-my-life-5af0ce099f80) - Before you write implementation code, write some code that proves that the implementation works or fails 

- [**Jest**](https://jestjs.io/) - JavaScript Testing Framework with a focus on simplicity 

- [**Continuous Integration (CI)**](https://codeship.com/continuous-integration-essentials#:~:text=Continuous%20Integration%20(CI)%20is%20a,CI%20it%20is%20typically%20implied.) - Continuous Integration (CI) is a development practice where developers integrate code into a shared repository frequently, preferably several times a day. Each integration can then be verified by an automated build and automated tests. 

- [**REST**](https://smartbear.com/blog/test-and-monitor/soap-vs-rest-whats-the-difference/) - Instead of using XML to make a request, REST (usually) relies on a simple URL. 

- [**Data Model**](https://en.wikipedia.org/wiki/Data_model#:~:text=A%20data%20model%20(or%20datamodel,properties%20of%20real%2Dworld%20entities.)) - an abstract model that organizes elements of data and standardizes how they relate to one another and to the properties of real-world entities 
