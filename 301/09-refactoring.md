# **Refactoring**

- [Concepts of functional programming in js](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

- [Refactoring JavaScript for Performance and Readability](https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec)

## **Functional Programming**

Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data

### **Pure functions**

- It returns the same result if given the same arguments (it is also referred as deterministic)
- It does not cause any observable side effects

The first fundamental concept we learn when we want to understand functional programming is **pure functions**.

Imagine we want to implement a function that calculates the area of a circle. An impure function would receive radius as the parameter, and then calculate radius * radius * PI:

    let PI = 3.14;

    const calculateArea = (radius) => radius * radius * PI;

    calculateArea(10);

It is impure because it uses a global object that was not passed as a parameter to the function.

Now imagine some mathematicians argue that the PI value is actually 42and change the value of the global object.
Our impure function will now result in 10 * 10 * 42 = 4200. For the same parameter (radius = 10), we have a different result.

    let PI = 3.14;

    const calculateArea = (radius, pi) => radius * radius * pi;

    calculateArea(10, PI);

Now we’ll always pass the PI value as a parameter to the function. So now we are just accessing parameters passed to the function. No external object.

- For the parameters radius = 10 & PI = 3.14, we will always have the same result: 314.0
- For the parameters radius = 10 & PI = 42, we will always have the same result: 4200

### **Reading Files**

If our function reads external files, it’s not a pure function — the file’s contents can change.

    const charactersCounter = (text) => `Character count: ${text.length}`;

    function analyzeFile(filename) {
      let fileContent = open(filename);
      return charactersCounter(fileContent);
    }

### **Random number generation**

Any function that relies on a random number generator cannot be pure.

### **It does not cause any observable side effects**

Examples of observable side effects include modifying a global object or a parameter passed by reference.

    let counter = 1;

    function increaseCounter(value) {
      counter = value + 1;
    }

    increaseCounter(counter);
    console.log(counter);

We have the counter value. Our impure function receives that value and re-assigns the counter with the value increased by 1.
Observation: mutability is discouraged in functional programming.
We are modifying the global object. But how would we make it pure? Just return the value increased by 1.

    let counter = 1;

    const increaseCounter = (value) => value + 1;

    increaseCounter(counter); //2
    console.log(counter); //1

See that our pure function increaseCounter returns 2, but the counter value is still the same. The function returns the incremented value without altering the value of the variable.

If we follow these two simple rules, it gets easier to understand our programs. Now every function is isolated and unable to impact other parts of our system.

Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result.

### **Immutability**

Unchanging over time or unable to be changed.

When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.

### **Referential transparency**

if a function consistently yields the same result for the same input, it is referentially transparent.
pure functions + immutable data = referential transparency
With this concept, a cool thing we can do is to memoize the function.

### **Functions as first-class entities**

The idea of functions as first-class entities is that functions are also treated as values and used as data.

Functions as first-class entities can:

- refer to it from constants and variables
- pass it as a parameter to other functions
- return it as result from other functions

The idea is to treat functions as values and pass functions like data. This way we can combine different functions to create new functions with new behavior.

### **Higher-order functions**

When we talk about higher-order functions, we mean a function that either:
- takes one or more functions as arguments, or
- returns a function as its result

### **Filter**

Given a collection, we want to filter by an attribute. The filter function expects a true or false value to determine if the element should or should not be included in the result collection. Basically, if the callback expression is true, the filter function will include the element in the result collection. Otherwise, it will not.

### **Map**

The idea of map is to transform a collection.

The map method transforms a collection by applying a function to all of its elements and building a new collection from the returned values.

### **Reduce**

The idea of reduce is to receive a function and a collection, and return a value created by combining the items.

A common example people talk about is to get the total amount of an order. Imagine you were at a shopping website. You’ve added Product 1, Product 2, Product 3, and Product 4 to your shopping cart (order). Now we want to calculate the total amount of the shopping cart.

In imperative way, we would iterate the order list and sum each product amount to the total amount.

    var orders = [
      { productTitle: "Product 1", amount: 10 },
      { productTitle: "Product 2", amount: 30 },
      { productTitle: "Product 3", amount: 20 },
      { productTitle: "Product 4", amount: 60 }
    ];

    var totalAmount = 0;

    for (var i = 0; i < orders.length; i++) {
      totalAmount += orders[i].amount;
    }

    console.log(totalAmount); // 120

Using reduce, we can build a function to handle the amount sum and pass it as an argument to the reduce function.

    let shoppingCart = [
      { productTitle: "Product 1", amount: 10 },
      { productTitle: "Product 2", amount: 30 },
      { productTitle: "Product 3", amount: 20 },
      { productTitle: "Product 4", amount: 60 }
    ];

    const sumAmount = (currentTotalAmount, order) => currentTotalAmount + order.amount;

    const getTotalAmount = (shoppingCart) => shoppingCart.reduce(sumAmount, 0);

    getTotalAmount(shoppingCart); // 120
Here we have shoppingCart, the function sumAmount that receives the current currentTotalAmount , and the order object to sum them.

The getTotalAmount function is used to reduce the shoppingCart by using the sumAmount and starting from 0.


