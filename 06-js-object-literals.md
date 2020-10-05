## JS Object Literals; The DOM

### Why Problem Domains are Hard

The reason problem domains are hard, is because you can't really see what you are trying to build very clearly. There is no picture to look at seperately.

1. make the problem domain eaier
    - you can often make the problem domain easier by cutting out cases and narrowing your focus to a particular part of the problem.

2. Get better at understanding the problem domain
    - Best to resist the temptation to “not waste anymore time talking” and make sure you understand a problem inside and out before you try and solve it with code.  It is much more expensive and time consuming to do things over than it is to do them right the first time. 

--- 

### What is an ***Object***?

***Objects*** troup together a set of variables and functions to create a model of something you would recognize from the real world. In an object, variables and functions take on new names.

#### **In an object: variables become known as properties**

If a variable is part of an object, it is called a **property**. Properties tell us about the object, such as the name of a hotel or the number of rooms it has. Each individual hotel might have a different name and a different number of rooms.

#### **In an object: functions become known as methods**

 If a function is part of an object, it is called a **method**. Methods represent tasks that are associated with the object. For example, you can check how many rooms are available by subtracting the number of booked rooms from the total number of rooms.

 Like variables and named functions, properties and methods have a name and a value. In an object, that name is called a **key**.

 An object cannot have two keys with the same name. This is because keys are used to access their corresponding values.

 The value of a property can be a string, number, Boolean, array, or even another object. The value of a method is always a function.
 
 Programmers use a lot of name/value paris:
 - HTML uses attribute names and values
 - CSS uses property names and values.

In JavaScript:
- variables have a name and you can assign them a value of a string, number, or Boolean.
- Arrays have a name and a group of values. (Each item in an array is a name/value pair because it has an index number and a value.)
- Named function have a name and value that is a set of statemnts to run if the function is called.
- Objects consist of a set of name/value pairs (but the names are referred to as keys).

---

### Creating an Object: Literal Notation

Literal notation is the easiest and most popular way to create objects. (there are several ways to create objects.)

The object is the curly braces and their contents. <br />
The object is stored in a variable called **hotel**, <br />
so you would refer to it as the ***hotel object***.

---

## **Document Object Model**

The **Document Object Model (DOM)** specifies how browsers should creat a model of an HTML page and ow JavaScript can access and update the contents of a web page while it is in the browser window.

- The browser represents the page using a Dom tree.

- Dom trees have four types of nodes: 

    1. document nodes - represents the entire page

    2. element nodes - describe the structure of an HTML page

    3. attribute nodes - the opening tags of HTML elements can carry attributes and these are represented by attribute nodes in the DOM tree

    4. text nodes - once an element node is accessed, you can then reach the text within, stored in its own text node

- You can select element nodes by their id or class attributes, by tag name, or using CSS selector syntax.

- Whenever a **DOM** query can return more than one node, it wil always return a NodeList.

- From an element node, you can access and update its content using properties such as **textContent** and **innerHTML** or using DOM manipulation techniques.

- An element node can contain multiple text nodes and child elements that are siblings of each other.
- In older browsers, implementation of the DOM is inconsistent (and is a popular)

- Browswer offer tools for viewing the DOM tree.


> ***The DOM tree is a model of a web page***

### Catching DOM Queries

Methods that find elements in the DOM tree are called DOM queries. When you need to work with and element more than once, you should use a variable to store the result of this query.

When a script selects an element to access or update, the interpreter must find the element(s) in the DOM tree.

> For an element whose **id** attribute has a value of **one**: <br />
>
> ---  
>
> **getElementById('one');**

When people talk about storing elements in variables, they are really storing the location of the element(s) within the DOM tree in a variable. The properties and methods of that element node work on the variable.

If your script needs to use the same element(s) more than once, you can store the location of the element(s) in a variable

This saves the browser looking through the DOM tree to find the same element(s) again. It is known as ***caching*** the selection.

The ***var stores a reference*** to the object in the DOM tree. **(it is storing the location of the node)**

> var itemOne = getElementById('one'); <br />
>**itemOne** does not store the **\<li>** element, it stores a reference to where that node is in the DOM tree. <br />
> To access the text content of this element, you might use the variable name: **itemOne.textContent**

--- 

### **Accessing Elements**

1. getElementById('id')
    >document.getElementById('one)

2. querySelector('css selector')

3. getElementsByClassName('class')

4. getElementsByTagName('tagName')

5. querySelectorAll('css selector')

#### **Selecting an Element from a Nodelist**

There are two ways to select an element from a NodeList: 

1. **the *item()* method**

    - will return an individual node from the NodeList. you specify the index number of the element you want as a parameter of the method (inside the parentheses).

    - check that there is a least one item in the NodeList before running any code. To do this, use the length property of the NodeList - it tells you how many items the NodeList contains.

    - Here you can see that an **if** statment is used. The condition for the **if** statement is whether the **length** property of the NodeList is greater than zero. If it is, then the statement inside the **if** statement are executed.. If not, the code continues to run after the second curly brace.

    > 1. var elements = document.getElementsByClassName('hot') <br />
    > 2. if (elements.length >= 1) { <br />
    > 3. var firstItem = elements.item(0); <br />
    > }
    > 
    
    > 1. select elements that have a class attribute whose value is **hot** and store the NodeList in a variable called elements.
    >2. use the length property to check how many elements were found. If 1 or more are found, run the code in the **if** statement.
    >3. Store the first element from the NodeList in a variable called **firstItem**.

2. **Array Syntax**

Array syntax is preferred over the **item()* method because it is faster. Before selecting a node from a NodeList, check that it contains nodes. If you repeatedly use the NodeList, store it in a variable.

- you can access individual nodes using a square bracket syntax similar to that used to access individual items from an array.

- you specify the index number of the element you want inside square brackets that follow the NodeList.

- As with all DOM queries, if you need to access the same NodeList several times, store the result of the DOM query in a variable.

    > 1. var elements = document.getElementsByClassName('hot') <br />
    > 2. if (elements.length >= 1) { <br />
    > 3. var firstItem = elements[0]; <br />
    > }
    > 

    > 1. select elements that have a class attribute whose value is **hot** and store the NodeList in a variable called elements.
    >2. use the length property to check how many elements were found. If 1 or more are found, run the code in the **if** statement.
    >3. Get the first element from the NodeList

### Repeating actions for an entire NodeList

When you have a NodeList, you can loop through each node in the collection and apply the same statements to each.

- Once a NodeList has been created, a **for** loop is used to go through each element in the NodeList.

- All of the statements inside the **for** loop's curly braces are applied to each element in the NodeList one-by-one.

- To indicate which item of the NodeList is currently being worked with, the counter **i** is used in the array-style syntax.

>1. var hotItems = document.querySelectorAll('li.hot');
>2. for (var i = 0; i < hotItems.length; i++) {
>3. hotItems[i].className = 'cool';
>4. }

>1. the variable **hotItems** contains a NodeList. It contains all list items whos **class** attribute has a value of **hot**. They are collected using the **querySelectorAll()** method.
>2. the **length** property of the NodeList indicates how many elements are in the NodeList. The number of elements dictates how many times the loop should run.
>3. Array syntax is used to indicate which item in the NodeList is currently being worked with: **hotItems[i]** <br />
It uses the counter variable inside the square brackets.
