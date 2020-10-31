# **Introductory HTML and JavaScript**

## ~~**HTML Structure**~~
- HTML pages are text documetns
- HTML uses tags (characters that sit inside angled brackets) to give the information they surround special meaning.
- Tags are often referred to as elements.
- Tags usually come in pairs. The opening tag denotes the start of a piece of content; the closing tag denotes the end.
- Opening tags can carry attributes, which tell us more about the content of that element. 
- Attributes require a name and a value
- To learn HTML you need to know what tags are available for you to use, what they do, and where they can go.
---

## ~~**Extra Markup**~~
- **DOCTYPES** tell browsers which version of HTML you are using.
- You can add comments to your code between the ***<!! and -->*** markers, you can also use ***(ctrl+/)***
- The id and class attributes allow you to identify particular elements.
- The ***< div >*** and ***< span >*** elements allow you to group block-level and inline elements together.
- ***< iframes >*** cut windows into your web pages through which other pages can be displayed
- The ***< meta >*** tag allows you to supply all kinds of information about your web page
- Escape characters are used to include special characters in your pages such as &lt; ***(&+lt+;)***, &gt; ***(&+gt+;)***, and &copy; ***(&+copy+;)***. 
---

## ~~**HTML5 Layout**~~
- The new HTML5 elements indicate the purpose of different parts of a web page and help to describe its structure
- The new elements provide clearer code (compared with using multiple < div > elements).
- Older browsers that do not understand HTML5 elements need to be which elements are block-level elements.
- To make HTML5 elements work in older versions of Internet Explorer, extra JavaScript is needed, which is available free from Google.
---

### ***Headers & Footers*** 
*< header > and < footer >* are used for the main heder or footer that appears at the top or bottom of every page on the site ***and/or*** an individual *< article >* or *< section >* within the page.

### ***Navigation*** 
*< nav >* element is used to contain the major navigational blocks on the site such as the site navigation.
---

### ***Articles*** 
*< article >* element acts as a container for any section of a page that could stand alone and potenially be syndicated.
---

### ***Asides*** 
*< aside >* element has two purposes, depending on whether it is inside an *< article >* element or not.
- when used inside an article element, it should contain information that is related to the article but not essential to its overall meaning
- when used outside of an article element, it acts as a container for content that is related to the entire page.
---

### ***Sections*** 
The *< section >* element groups related content together, and typically each section would have its own heading
---

### ***Heading Groups***
The purpose of the *< hgroup >* element is to group together a set of one or more *< h1 > through < h6 >* elements so that they are treated as one single heading.
> some suggest that is is of little use other than as a styling hook. It has however, been popular with those developers who believe that it is useful to group together the primary heading and the subheading (as both can be integral parts of a heading)
---

### ***Figures***
***< figure >*** can be used to contain any content that is referenced from the main flow of an article. Used to reference the element not for integral  use. 
- images
- videos
- graphs
- diagrams
- code samples
- text that supports the main body of article

***< figcaption >*** used to provide a text description for the content of the  *< figure >* element 

> | Example |
> ---
> | < figure > |
> |     < img src= "imagefile.jpg" alt="image name" /> |
> |     < figcaption > ***text desciption of image*** </ figcaption > |
> | </ figure > |
---

### ***Sectioning Elements***
***< div > element will remain an important way to group together related elements, because you should not be using the new elements for purposes other than those explicitly stated.

Where there is no suitable element to group a set of elements, the *< div >* element will still be used.

### ***Linking Around Block-level Elements***
HTML5 allows web page authors to place an ***< a >*** element around a block level element that contains child elements. This allows you to turn an entire block into a link.

>| Example |
>| --- |
>| \<a href="file-name.html"> |
---

### ***Helping Older Browsers Understand***
Older browsers that do not know the new HTML5 elements wil automatically treat them as inline elements. Therefore, to help older browsers, you should include a line of CSS that states which new elements should be rendered as block-level elements.

| CSS: |
---
>header, section, footer, aside, nav, article, figure, figcaption { 
>
>   display: block;}


| HTML: |
---
>\<!--[if lt IE 9]>
>
>   \<script src="http://html5shiv.googlecode.com/svn/trunk/html5.js">\</script>
>
>\<![endif]-->

---

## ***Process & Design***
- It's important to understand who your target audience is, why they would come to your site, what information they want to find and when they are likely to return.
- Site maps allow you to plan the structure of a site.
- Wireframes allow you to organize the information that will need to go on each page.
- Design is about communication. Visual hierarchy helps visitors understand what you are trying to tell them.
- you can differentiate between pieces of information using size, color, and style.
- You can use grouping and similarity to help siplify the information you present.
---

## ***The ABC of Programming***

**A: What is a script and how do I create one?**

- A script is a series of instruction that the computer can follow in order to achieve a goal.
- Each time the script runs, it might only use a subset of all the instructions.
- Computers approach tasks in a different way than humans, so your instructions must let the computer solve the task programmatically.
- To approach writing a script, break down your goal into a series of tasks and then work out each step needed to complete that task (a flowchart can help).

**B: How do computers fit in with the world around them?**

- Computers create models of the world using data.
- The models use objects to represent physical things. Objects can have:
    + properties that tell us about the object
    + methods that perform tasks using the properties of that object
    + events which are triggered when a user interacts with the computer.
- Programmers can write code to say "When this event occurs, run that code."
- Web browsers use HTML markup to create a model of the web page. Each element creates its own node (which is a kind of object).
- To make web pages interactive, you write code that uses the browser's model of the web page.

**C: How do I write a script for a web page?**

- It is best to keep JavaScript code in its own JavaScript file. JavaScript files are text files (like HTML pages and CSS style sheets), but they have the .js extension.
- The HTML ***\<script>*** element is used in HTML pages to tell the browser to load the JavaScript file (rather like the \<link> element can be used to load a CSS file).
- If you view the source code of the page in the browser, the JavaScript will not have changed the HTML, because the script works with the model of the web page that the browser has created.

### **Learning to program with JavaScript involves:**
1. Understanding some basic programming concepts and the terms that JavaScript programmers use to describe them.
2. Learning the language itself, and, like all languages you need to konw it vocabulary and how to structure your sentences.
3. Becoming familiar with how it is applied by looking at examples of how JavaScript is commonly used in websites today.

### **How JavaScript makes web pages more interactive**

> ***JavaScript** allows you to make web pages more interactive by accessing and modifying tghe content and markup used in a web page while it is being viewed in the browser*

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

### Examples of JavaScript in the browser
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

---

## ***Computers Create Models of the World Using Data***

### ***Objects & Porperties***

**Objects (things)** - In computer programming, each physical thing in the world can be represented as an object.

>Each object can have its own:
>- Properties
>- Events
>- Methods

>Together they create a working model of that object

**Properties (characteristics)** - characteristics of an object are called properties

Each property has a name and a value, and each of these name/value pairs tells you something about each individual instance of the object.

>Properties for a car could be make, color and engine size

### ***Events***

In the real world, people interact with objects. These interactions can change the values of the properties in these objects.

**What is an event?**

There are common ways in which people interact with each type of object. For example, in a car a driver will typically use at least two pedals. The car has been designed to respond differently when the driver interacts with each of the different pedals:
- The accelerator makes the car go faster
- The brake slows it down

Similarly, programs are designed to do different things when users interact with the computer in different ways. For example, clicking on a contact link on a web page could bring up a contact form, and entering text into a search box may automatically trigger the search functionality.

An event is the computer's way of sticking up its hand to say, "Hey, this just happened!"

**What does an event do?**

Programmers choose which events they respond to. When a specific event happens, that event can be used to trigger a specific section of the code.

Scripts often use different events to trigger different types of functionality.

So a script will state which events the programmer wants to respond to, and what part of the script should be run when each of those events occur.

| Example | Object type: Hotel |
| --- | --- |
| Event | happens when: |
| book | reservation is made |
| cancel | reservation is cancelled |
| 

### ***Methods***

Methods represent things people need to do with objects. They can retrieve or update the values of an object's properties.

**What is a Method?**

Methods typically represent how people (or other things) interact with an object in the real world.

They are like questions and instructions that:
- tell you something about that object (using information stored in its properties)
- change the value of one or more of that object's properties

**What does a Method do?**

The code for a method can contain lots of instructions that together represent on task.

When you use a method, you do not always need to know how it achieves its task; you just need to know how to ask the question and how to interpret any answers it gives you.

| Example | Object type: Hotel |
| --- | --- |
| METHOD | what it does: |
| makeBooking() | increses value of bookings property |
| cancelBooking() | decreases value of bookings property |
| checkAvailability() | subracts value of bookings property from value of rooms property and returns number to rooms available |
|

### ***Putting it all together***

Computers use data to create models of things in the real world. The events, methods, and properties of an object all relate to each other: Events can trigger methods, and methods can retrieve or update an object's properties

OBject type: Hotel

 
1. | Event | happens when: | method called: |
    | --- | --- | --- |
    | book | reservation is made | makeBooking() |
    | cancel | reservation is cancelled | cancelBooking() |
    |
2. | Method | What it does: |
    | --- | --- |
    | makeBooking() | increases value of bookings property |
    | cancelBooking() | decreases value of bookings property |
    | checkAvailability() | subtracts value of bookings property from value of rooms property and returns number of rooms available
    |
3. | Properties | Characteristics |
    | --- | --- |
    | name | Quay |
    | rating | 4 |
    | rooms | 42 |
    | bookings | 22 |
    | gym | false |
    | pool | true |
    |

### ***Web browsers are programs built using objects***

Web browsers create similar models of the web page they are showing and of the browser window that the page is being shown in.

## ***How a browser sees a web page***

In order to understand how you can change the content of an HTML page using JavaScript, you need to know how a browser interprets the HTML code and applies styling to it.

1. Receive a page as HTML code
    - Each page on a website can be seen as a separate document. So the web consists of many sites, each made up of one or more documents.
2. Create a model of the page and store it in memory
3. Use a rendering engine to show the page on screen
    - if there is no CSS, the rendering engine will apply default styles to HTML elements. If there is a link to a CSS style sheet, the browser requests that file and displayes the page accordingly
    - When the browser receives CSS rules, the rendering engine processes them and applies each rule to its corresponding elements. This is how the browser positions the elements in the correct place, with the right colors, fonts, and so on.

## **How HTML, CSS and Javascript fit together**

Web developers usually talk about three languages that are used to create web pages: HTML, CSS, and JavaScript.
*each language forms a separate layer with different purpose. Each layer, builds on the previous one.

1. **Content Layer** *.html files*
    - this is where the content of the page lives. The HTML gives the page structure and adds semantics.

2. **Presentation Layer** *.css files*
    - The CSS enhances the HTML page with the rules that state how the HTML content is presented (backgrounds, borders, box dimensions, colors, fonts, etc.).

3. **Behavior layer** *.js files*
    - This is where we can change how the page behaves, adding interactivity. We will aim to keep as much of our JS as possible in separate files.

### Progressive enhancement

These three layers form the basis of a popular approach to building web pages called progressive enhancement.

### Creating a basic JAVASCRIPT

JavaScript is written in plain text, just like HTML and CSS, so you do not need any new tools to write a script.

### Linking to a JavaScript file from an HTML page

When you want to use JavaScript with a web page, you use the HTML \<script> element to tell the browser it is coming across a script.
Its ***src*** attribute tells people where the JavaScript file is stored

### Placing the script in the page

You may see JavaScript in the HTML between opening ***\<script>*** and closing ***\</script>*** tags (but it is better to put scripts in their own files)
- document.write() writes content into the document. It is a simple way to add content to a page, but not always the best.

## How to use Objects and Methods

Breakdown:

***document.write('Good afternoon!');***

1. Document = Object - The document ovject represents the entire web page. All web browsers implement this object, and you can use it just by giving its name.
2. Period after document = Member Operator - The document object has several methods and properties they are known as members of that object. You can access the members of an object using a dot between the object name and the member you want to access. it is called a member operator.
3. Write() = Method - the write() method of the document object allows new content to be written into the page where the \<script> element sits.
4. Parameters - whenever a method requires some information in order to work, the data is given inside the parentheses. Each piece of informations is called a parameter of the method. In this case, the write() method needs to know what to write into the page.

## JavaScript runs where it is found in the HTML

When the browser comes across a \<script> element, it stops to load the script and then checks to see if it needs to do anything.