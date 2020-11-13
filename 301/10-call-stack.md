# **The Call Stack and Debugging**

- [Call stack - MDN](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack)
- [Call stack wiki](https://en.wikipedia.org/wiki/Call_stack)
- [The JavaScript Call Stack - What It Is and Why It's Necessary](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)
- [JavaScript error messages && debugging](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

## Call stack

A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.

- When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.
- Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
- When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
- If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

we start with an empty Call Stack. Whenever we invoke a function, it is automatically added to the Call Stack. Once the function has executed all of its code, it is automatically removed from the Call Stack. Ultimately, the Stack is empty again.

### **What causes a stack overflow?**

A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accommodate before throwing a stack error.

## **JavaScript error messages && debugging**

Most of your time as a developer is spent reading code followed by debugging that same code, most likely to be able to read it or solve a bug

### **Types of error messages**

The first thing that indicates you that something is wrong with your code is an error message usually appears on your console

#### **Reference errors**

This is as simple as when you try to use a variable that is not yet declared you get this type os errors.

    console.log(foo) // Uncaught ReferenceError: foo is not defined

#### **Syntax errors**

this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.

    JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1

This can be solved by just fixing the syntax, in this case the object should be a JSON.

    JSON.parse('{"foo":"bar"}')

#### **Range errors**

Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

    var foo= []
    foo.length = foo.length -1 // Uncaught RangeError: Invalid array length

#### **Type errors**

Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

    var foo = {}
    foo.bar // undefined
    foo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined

### **Debugging**

To debug your JS code, the easiest and maybe the most common way its to simply **console.log()** the variables you want to check

The breakpoint can also be achieved by putting a **debugger** statement in your code in the line you want to break.

You can also add conditional breakpoints by right-clicking a previous set breakpoint, which will make your program stop at that point only if a condition is met, this is awesome for when you want to debug huge cycles for specific values.

### **Handling errors**

An alternative it’s to encapsulate our problematic function code with a try…catch which would make an error be thrown but this time, not “uncaught” so we can send it to a error logging to be checked later and send a fallback to the function so that our code continues without problems.

This will make your error message show up slightly different and instead of a console.error you could have some kind of logging system as pointed before so you can check your client errors and fix them without waiting for a report.

The worthiest outcome of using try…catch tough is the fact that your application will keep on running, maybe with some side effects

### **Conclusion**

practice makes better..not perfect.