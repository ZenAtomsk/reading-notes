## **Object-Oriented Programming**

### Domain Modeling

Domain modeling is the process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model

A domain model that's articulated well can verify and validate the understanding of a specific problem among various stakeholders. As a comminication tool, it defines a vocabulary that can be used within and between both technical and business teams.

### Define a constructor and initaialize properties

To defin the same properties between many objects, you'll want to use a constructor function. Below is a table that summarizes a JavaScript representation of an *EpicFailVideo

| Property | Data | Type |
| --- | --- | --- |
| epicRating | 1 to 10 | number |
| hasAnimals | true or false | Boolean |

>Implementation of the constructor function:

>var EpicFailVideo = function <br />(epicRating, hasAnimals) { <br />
  this.epicRating = epicRating; <br />
  this.hasAnimals = hasAnimals; <br />
} <br />
>
>var parkourFail = new EpicFailVideo(7, false); <br />
var corgiFail = new EpicFailVideo(4, true); <br />
>
>console.log(parkourFail); <br />
console.log(corgiFail); <br />

---

### Generate random numbers
To model the random nature of user behavior, you'll need the help of a random number generator. Fortunately, the JavaScript standard library includes a Math.random() function for just this sort of occasion.

>`var EpicFailVideo = function(epicRating, hasAnimals) { <br />
  this.epicRating = epicRating; <br />
  this.hasAnimals = hasAnimals; <br />
}
>
>EpicFailVideo.prototype.generateRandom = function(min, max) { <br />
  return Math.floor(Math.random() * (max - min + 1)) + min; <br />
}
>
>var parkourFail = new EpicFailVideo(7, false); <br />
var corgiFail = new EpicFailVideo(4, true); <br />
>
>console.log(parkourFail.generateRandom(1, 5)); <br />
console.log(corgiFail.generateRandom(1, 5));` <br />

As you can see, methods can be added to a constructor function's **prototype**. Think of the prototype as an object's stunt double. Whenever a scene is too dangerous, you can substitute in the prototype to do the work while the object takes all the glory.

This **prototype** is given a ***generateRandom*** method which is assigned a function with two parameters called **min** and **max**.

When **parkourFail** is asked to run the **generateRandom()** method, it searches through all of its own methods. When it doesn't find the **generateRandom()** method there, **parkourFail** then searches through all of the methods on its **prototype** object. When it finds the **generateRandom()** method on its prototype object, **parkourFail** calls the method, passing in **1** and **5** as the arguments. The **generateRandom(1, 5)** method runs and returns a random number between 1 and 5. The exact same process happens for **corgiFail** too.

While it certainly takes longer to locate a method on the prototype object, this technique is an established best practice in JavaScript. When a prototype is shared between two or more objects, like it is for **parkourFail** and **corgiFail**, those objects execute the same code when the **generateRandom()** method is called. And shared code means a running program consumes less memory which is important for devices like smart phones and tablets. 

>var EpicFailVideo = function(epicRating, hasAnimals) { <br />
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals; <br />
}
>
>EpicFailVideo.prototype.generateRandom = function(min, max) { <br />
  return Math.floor(Math.random() * (max - min + 1)) + min; <br />
}
>
>EpicFailVideo.prototype.dailyLikes = function() { <br />
>  var viewers, percentage; <br />
>
>  viewers = this.generateRandom(10, 30) * this.epicRating; <br />
>
>  if (this.hasAnimals) { <br />
    percentage = 0.75; <br />
  } else { <br />
    percentage = 0.40; <br />
  }
>
>  return Math.round(viewers * percentage); <br />
}
>
>var parkourFail = new EpicFailVideo(7, false); <br />
var corgiFail = new EpicFailVideo(4, true); <br />
>
>console.log(parkourFail.dailyLikes()); <br />
console.log(corgiFail.dailyLikes()); <br />

Domain modeling is the process of creating a conceptual model for a specific problem. And a domain model that's articulated well can verify and validate your understanding of that problem.

Here's some tips to follow when building your own domain models.

1. When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.
2. Model its attributes with a constructor function that defines and initializes properties.
3. Model its behaviors with small methods that focus on doing one job well.
4. Create instances using the new keyword followed by a call to a constructor function.
5. Store the newly created object in a variable so you can access its properties and methods from outside.
6. Use the this variable within methods so you can access the object's properties and methods from inside.

---

### Tables

- the \<table> element is used to add tables to a web page.
- A table is drawn out row by row. Each row is created with the \<tr> element.
- inside each row there are a number of cells represented by the \<td> element ( or \<th> if it is a header).
- you can make celss of a table span more than one row or column using the rowspan and colspan attributes
- for long tables you can split the table into a \<thead>, \<tbody>, and \<tfoot>.

### JS Objects


Update an object - pg 107

creating many objects - pg 108

Three groups of built-in objects - pg 122-134

Creating an instance of the date - pg 136

- in an object, variables are known as properties of the object; functions are known as methods of the object
- web browsers implement objects that represent both the browser window and the document loaded into the browser window.
- JavaScript also has several built-in objects. Their properties and methods offer functionality that help you write scripts.
- Arrays and objects can be used to create complex data sets (and both can contain the other). 