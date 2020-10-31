- [Growth Mindset](https://zenatomsk.github.io/reading-notes/)
- [Learning Markdown](https://zenatomsk.github.io/reading-notes/01-learning-markdown) 
- [The Coder's Computer](https://zenatomsk.github.io/reading-notes/02-the-coders-computer)
- [Terminal revision and the cloud....or the matrix](https://zenatomsk.github.io/reading-notes/03-revisions-and-the-cloud)
- [Html-the structure](https://zenatomsk.github.io/reading-notes/04-structure-with-html)
- [Where do you want it and what color?](https://zenatomsk.github.io/reading-notes/05-design-with-css)
- [Let's make it do stuff and things](https://zenatomsk.github.io/reading-notes/06a-dynamic-with-javascript)
- [Computer architecture and logic](https://zenatomsk.github.io/reading-notes/06b-computer-architecture-and-logic)
- [You need coffee for all this Java..Script](https://zenatomsk.github.io/reading-notes/07-programming-with-js)
- [Answer how I want you to answer, or this loop will never close](https:zenatomsk.github.io/reading-notes/08-operators-and-loops)

# **Programming with JavaScript**

### **New Vocabulary** pokemon.com
- **/** - use "/" before a character to skip next character from string
- **Script** - A script is a series of instructions that a computer can follow to achieve a goal.
- **Programmatic problem solving** - An approach to problem solving to plan the approach to your problem
- **Expression** - evaluates into (results in) a single value
    1. expressions that just assign a value to a variable *(var color = 'beige'; the value of the color is now beige)*
    2. expressions that use two or more values to return a single value *(var area = 3 * 2; the value of area is now 6)*
- **Operator** - expressions rely on things called operators; they allow programmers to create a single value from one or more values.
    - **assignment operators** - assign a value to a variable (color = 'beige'; the value of color is now beige)
    - **arithmetic operators** - perform basic math (area = 3 * 2; the value of area is now 6)
    - **string operators** - commbine two strings (greeting ='Hi ' +  'Molly'; the value of greeting is now Hi Molly.)
    - **comparison operators** - compare two values and return true or false (buy = 3 > 5; the value of buy is false)
    - **logical operators** - combine expressions and return true or false (buy = (5 > 3) && (2 < 4); the value of buy is now true.)
- **Function** -
  - **Declaration** -
  - **Call** - 
  - **Parameters** - 
  - **Arguments** - 
  - **Return value** - 
- **Refactoring** - 

## **Learning to program with JavaScript involves:**
1. Understanding some basic programming concepts and the terms that JavaScript programmers use to describe them.
2. Learning the language itself, and, like all languages you need to konw it vocabulary and how to structure your sentences.
3. Becoming familiar with how it is applied by looking at examples of how JavaScript is commonly used in websites today.

## **How JavaScript makes web pages more interactive**

>***JavaScript** allows you to make web pages more interactive by accessing and modifying tghe content and markup used in a web page while it is being viewed in the browser*

1. **Access Content** - you can use JavaScript to selec any element, attribute, or text from an HTML page.
    - select the text inside all of the < h1 > elements on a page
    - select any elements that have a class attribute with a value of note
    - Find out what was entered into a text input whose id attribut has a value of email **(confused about this one)**
2. **Modify Content** - you can use JavaScript to add elements, attributes, and text to the page, or remove them
    - add a paragraph of text after the first < h1 > element
    - change the value of class attributes to trigger new CSS rules for those elements
    - change the size or poition of an < img > element
3. **Porgram rules** - you can specify a set of steps for the browser to follow (like a recipe), which allows it to access or change the content of a page.
    - a gallery script could check which image a user clicked on and display a larger version of that image
    - a mortgage calculator could collect values from a form, perform a calculation, and display repayments.
    - an animation could check the dimensions of the browser window and move an image to the bottom of the viewable area (also known as the viewport)
            
    >***JavaScript** encompasses many of the traditional rules of porgramming. It can make the web page feel interactive by responding to what the user does.*
4. **React to Events** - you can specify that a script should run when a specific event has occurred.
    - a button is pressed
    - a link is clicked (or tapped) on
    - a cursor hovers over an element
    - information is added to a form
    - an interval of time passed
    - a web page has finished loading

## Examples of JavaScript in the browser
*Being able to change the conten of an HTML page while it is loaded in the browser is very powerful.*

>The following examples rely on the ability to:
> - **Access** the content of the page
> - **Modify** the content of the page
> - **Program** rules or instructions the browser can follow
> - **React** to events triggered by the user or browser
    
1. **Slideshows**
    - **React**: Script triggered when the page loads
    - **Access**: Get each slide from the slideshow
    - **Modify**: Only show the first slide (hide others)
    - **Program**: Set a timer: when to show next slide
    - **Modify**: Change which slide is shown
    - **React**: When user clicks button for different slide
    - **Program**: Determine which slide to show
    - **Modify**: Show the requested slide
2. **Forms**
    - **React**: User presses the submit button when they have entered their name
    - **Access**: Get value from form field
    - **Program**: Check that the name is long enough
    - **Modify**: Show a warning message if the name is not long enough
3. **Reload part of a page**
    - **React**: Script triggered when user clicks on link
    - **Access**: The link that they clicked on
    - **Porgram**: Load the new content that was requested from the link
    - **Access**: Find the element to replace in the page
    - **Modify**: Replace that content with new content
4. **Filtering data**
    - **React**: Script triggered when page loads
    - **Program**: Collect keywords from images
    - **Program**: Turn the keywords into buttons the user can click on
    - **React**: User clicks on one of the buttons
    - **Program**: Find the relevant subset of images that should be shown
    - **Modify**: Shown the subset of images that use that tag

### Script

A script is a series of instructions that a computer can follow to achieve a goal. Comparable to recipes, handbooks and manuals

To write a script, you need to first state your goal and then list the tasks that need to be completed in order to achieve it.
1. define the goal
2. design the script
3. code each step

(*As tempting as it is to start coding straight away, it pays to spend time designing your script before you start writing it.*)

Consider how you might approach a different type of script.

Sketch out the tasks in a flowchart

- A scriptis a series of instructions that the computer can follow in order to achieve a goal.
- Each time the script runs, it might only use a subset of all the instructions.
- Computers approach tasks in a different way thatn humans, so your sintructions must let the computer solve the task programmatically
- to approach writing a script, break down your goal into a series of tasks and then work out each step needed to complete that task (a flowchart can help)

### **Arithmetic operators**

JavaScript contains the following mathematical operators, which you can use with numbers.

Basic operators= addition, subtraction, division and multiplication.

Other operators
- increment ++ adds one to the current number
- decrement 