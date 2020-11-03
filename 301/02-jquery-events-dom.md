# **jQuery, Events, and The DOM**

##

JavaScript and jQuery book by Jon Duckett pages 293-301, 306-331 and 354-357

JavaScript and jQuery book by Jon Duckett pages 332-335

JavaScript and jQuery book by Jon Duckett pages 302-305

[6 Reasons for Pair Programming](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)

## jQuery Notes

    Script plugin for <head>
    <script src="https://code.jquery.com/jquery-3.1.1.js"></script>

    Ready event of the document object:

    $(document).ready(function() {
      // jQuery code goes here
    });

  Shortcut:

    $(function() {
      // jQuery code goes here
    });


    <!DOCTYPE html>
    <html>
    <head>
      <title>Page Title</title>
      <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
      <div id="start">Start</div>
    </body>
    </html>

    $ accesses jQuery
    $("p").hide()  // hides all <p> elements
    $(".demo").hide()  // hides all elements with class="demo"
    $("#demo").hide()  // hides the element with id="demo"
    $("#start").html("Go!");


Adding attributes

The attr() method is used for getting the value of an attribute. For Example:

    HTML:

    <a href="www.sololearn.com">
      Click here
    </a>

    JavaScript:
    $(function() {
    var val = $("a").attr("href");
    alert(val);
    });
    // alerts "www.sololearn.com"

    Removing attributes:
    $("table").removeAttr("border");
    $("table").removeAttr("class"); 


Set Content

The same html() and text() methods can be used to change the content of HTML elements.
The content to be set is provided as a parameter to the method, for example:

    HTML:
    <div id="test">
      <p>some text</p>
    </div>

    JS:
    $(function() {
    $("#test").text("hello!");
    });

    $(function() {
    $("#test").html("<p>hello!</p>");
    });

The following jQuery methods are available to get and set content and attributes of selected HTML elements:
text() sets or returns the text content of selected elements.
html() sets or returns the content of selected elements (including HTML markup).
val() sets or returns the value of form fields.
attr() sets or returns the value of attributes.
removeAttr() removes the specified attribute.





Adding Content

As we have seen in the previous lessons, the html() and text() methods can be used to get and set the content of a selected element. However, when these methods are used to set content, the existing content is lost.
jQuery has methods that are used to add new content to a selected element without deleting the existing content:
append() inserts content at the end of the selected elements.
prepend() inserts content at the beginning of the selected elements.
after() inserts content after the selected elements.
before() inserts content before the selected elements.

Multiple Properties

To set multiple CSS properties, the css() method uses JSON syntax, which is:
css({"property":"value","property":"value",...});

As you can see, the syntax consists of "property":"value" pairs, which are comma separated and enclosed in curly brackets { }.
For Example:
$("p").css({"color": "red", "font-size": "200%"});

This will set the color and font-size properties of the paragraph.
You can specify any number of properties using this JSON syntax.

Summary DOM Traversal
An ancestor is a parent, grandparent, great-grandparent, and so on.
A descendant is a child, grandchild, great-grandchild, and so on.
Siblings share the same parent.


The jQuery remove() method removes the selected element(s), as well as its child elements.

empty() removes the child elements of the selected element(s).

Common Events

The following are the most commonly used events:
Mouse Events:
click occurs when an element is clicked.
dblclick occurs when an element is double-clicked.
mouseenter occurs when the mouse pointer is over (enters) the selected element.
mouseleave occurs when the mouse pointer leaves the selected element.
mouseover occurs when the mouse pointer is over the selected element.

Keyboard Events:
keydown occurs when a keyboard key is pressed down.
keyup occurs when a keyboard key is released.

Form Events:
submit occurs when a form is submitted.
change occurs when the value of an element has been changed.
focus occurs when an element gets focus.
blur occurs when an element loses focus.

Document Events:
ready occurs when the DOM has been loaded.
resize occurs when the browser window changes size.
scroll occurs when the user scrolls in the specified element.

The Event Object

Every event handling function can receive an event object, which contains properties and methods related to the event:
pageX, pageY the mouse position (X & Y coordinates) at the time the event occurred, relative to the top left of the page.
type the type of the event (e.g. "click").
which the button or key that was pressed.
data any data that was passed in when the event was bound.
target the DOM element that initiated the event.
preventDefault() prevent the default action of the event (e.g., following a link).
stopPropagation() Stop the event from bubbling up to other elements.

Hide/Show

jQuery has some easy-to-implement effects to create animations.
The hide() and show() methods are used to hide and show the selected elements.
The toggle() method is used to toggle between hiding and showing elements.

    For example:

    $(function() {
    $("p").click(function() {
      $("div").toggle();
    });
    });

The hide/show/toggle methods can take an optional argument, speed, which specifies the animation speed in milliseconds.

    For example, let's pass 1000 millisecond as the speed argument to the toggle() method:

    $(function() {
    $("p").click(function() {
      $("div").toggle(1000);
    });
    });

The hide/show/toggle methods can also take a second optional parameter callback, which is a function to be executed after the animation completes..

Fade In/Out

Similar to the hide/show methods, jQuery provides the fadeIn/fadeOut methods, which fade an element in and out of visibility.
Just like the toggle() method switches between hiding and showing, the fadeToggle() method fades in and out.

    Let's see fadeToggle() in action:

    $(function() {
    $("p").click(function() {
      $("div").fadeToggle(1000);
    });
    });

Just like toggle(), fadeToggle() takes two optional parameters: speed and callback.
Another method used for fading is fadeTo(), which allows fading to a given opacity (value between 0 and 1). For example: $("div").fadeTo(1500, 0.7);

Slide Up/Down

The slideUp() and slideDown() methods are used to create a sliding effect on elements.
Again, similar to the previous toggle methods, the slideToggle() method switches between the sliding effects and can take two optional parameters: speed and callback.

    For example:
    $(function() {
    $("p").click(function() {
      $("div").slideToggle(500);
    });
    });

    Animate()

The animate() method lets you animate to a set value, or to a value relative to the current value.
You need to define the CSS properties to be animated as its parameter in JSON format ("key":"value" pairs).

The second parameter defines the speed of the animation.
For example, the following code animates the width property of the div in 1 second to the value 250px:

    $("div").click(function() {
    $("div").animate({width: '250px'}, 1000);
    });

Note the JSON format for providing the CSS parameters. The JSON syntax was also used in the previous modules when manipulating CSS properties.
You can animate any CSS property using the above mentioned syntax, but there is one important thing to remember: all property names must be camel-cased when used with the animate() method (camelCase is the practice of writing compound words or phrases such that each word or abbreviation begins with a capital letter with the first word in lowercase).

You will need to write paddingLeft instead of padding-left, marginRight instead of margin-right, and so on.
animate()

Multiple properties can be animated at the same time by separating them with commas.

    For example:

    $("div").animate({
    width: '250px',
    height: '250px'
    }, 1000);

It is also possible to define relative values (the value is then relative to the element's current value). This is done by putting += or -= in front of the value:

    $("div").animate({
    width: '+=250px',
    height: '+=250px'
    }, 1000);

To stop an animation before it is finished, jQuery provides the stop() method.
Animation Queue

By default, jQuery comes with queue functionality for animations.
This means that if you write multiple animate() calls one after another, jQuery creates an "internal" queue for these method calls. Then it runs the animate calls one-by-one.

    For example:

    var div = $("div");
    div.animate({opacity: 1});
    div.animate({height: '+=100px', width: '+=100px', top: '+=100px'}, 500);
    div.animate({height: '-=100px', width: '-=100px', left: '+=100px'}, 500);
    div.animate({height: '+=100px', width: '+=100px', top: '-=100px'}, 500);
    div.animate({height: '-=100px', width: '-=100px', left: '-=100px'}, 500);
    div.animate({opacity: 0.5});
 
Each animate() method call will run one after another.
Remember, to manipulate the position of elements, you need to set the CSS position property of the element to relative, fixed, or absolute.
The animate() method, just like the hide/show/fade/slide methods, can take an optional callback function as its parameter, which is executed after the current effect is finished.
 
Drop-Down Menu

Let's create a simple drop-down menu that will open upon clicking on the menu item.

    HTML:

    <div class="menu">
    <div id="item">Drop-Down</div>
    <div id="submenu">
      <a href="#">Link 1</a>
      <a href="#">Link 2</a>
      <a href="#">Link 3</a>
    </div>
    </div>

    JS:
    $("#item").click(function() {
    $("#submenu").slideToggle(500);
    });

The code above handles the click event of the id="item" element and opens/closes the submenu in 500 milliseconds.
Run the code to see it in action. You can also check out the CSS used for styling the items.

### **Summary**

- jQuery is a JavaScript file you include in your pages
- Once included, it makes it faster and easier to write cross-browser JavaScript, based on two steps:
  1. Using CSS-style selectors to collect one or more nodes from the DOM tree.
  2. Using jQuery's built-in methods to work with the elements in that selection
- jQuery's CSS-style selector syntax makes it easier to select elements to work with. It also has methods that make it easier to traverse the DOM.
- jQuery makes it easier to handle events because the event methods work across all browsers.
- jQuery offers methods that make it quick and simple to achieve a range of tasks that JavaScript programmers commonly need to perform.

## **6 Reasons for Pair Programming**

1. Greater efficiency - It is a common misconception that pair programming takes a lot longer and is less efficient. In reality, when two people focus on the same code base, it is easier to catch mistakes in the making. Research indicates that pair programing takes slightly longer, but produces higher-quality code that doesn’t require later effort in troubleshooting and debugging (let alone exposing users to a broken product). So, in the long-run, it’s often actually more efficient than two people working on separate features. When coming up with ideas and discussing solutions out loud, two programmers may come to a solution faster than one programmer on their own. Also, when the pair is stuck, both programmers can research the problem and reach a solution faster. Researches also identified pairing enhances technical skills, team communication, and even enjoyability of coding in the workplace.

2. Engaged collaboration - When two programmers focus on the same code, the experience is more engaging and both programmers are more focused than if they were working alone. It is harder to procrastinate or get off track when someone else is relying on you to complete the work.

3. Learning from fellow students - Everyone has a different approach to problem solving; working with a teammate can expose developers to techniques they otherwise would not have thought of. If one developer has a unique approach to a specific problem, pair programming exposes the other developer to a new solution.

4. Social skills - Pair programming is great for improving social skills. When working with someone who has a different coding style, communication is key. This can become more difficult when two programmers have different personalities. Pair programming not only improves programming skills, but can also help programmers develop their interpersonal skills. When just grabbing the keyboard and taking over isn’t an option, getting good at finding the right words is a skill unto itself.

5. Job interview readiness - A common step in many interview processes involves pair programming between a current employee and an applicant, either in person or through a shared screen. They will carry out exercises together, such as code challenges, building a project or feature, or debugging an existing code base. By doing so, companies can get a better feel for how an applicant will fit into the team and their collaboration style.

6. Work environment readiness - Many companies that utilize pair programing expect to train fresh hires from CS-degree programs on how they operate to actually deliver a product. Code Fellows graduates who are already familiar with how pairing works can hit the ground running at a new job, with one less hurdle to overcome.