## Forms and Events

---

### **Forms**

- Whenever you want to collect information from visistors you will need a form, which lives inside a \<form> element

- Information from a form is sent in name/value pairs

- Each form control is given a name, and the text the user types in or the values of the options they select are sent to the server.

- HTML5 introduces new form elements which make it easier for visitors to fill in forms.

---

### How forms work

1. A user fills in a form and then presses a button to submit the information to the server

2. The name of each form control is sent to the server along with the value the user enters or selects

3. The server processes the information using a programming language such as PHP, C#, VB.net, or Java. It may also store the information in a database.

4. The server creates a new page to send back to the browser based on the information received.

A form may have several form controls, each gathering different information. The server needs to know which piece of inputted data corresponds with which form element

To differentiate between various pieces of inputted data, information is sent from the browser to the server using name/value pairs. In this example, the form asks for the visitor's username and also for their favorite jazz musician. The name/value pairs sent to the server are:

- ***username=Ivy*** If the form control allows the user to enter text, then the value of the form control is whatever the user has typed in.

- ***vote=Herbie*** If the form control allows you to choose from a fixed set of answers (e.g. radio buttons, checkboxes or a drop down list), the web page author will add code that gives each option an automatic value.

---

### Form Structure

\<form> <br />
Form controls live inside a \<form> element. This element should always carry the action attribute and will usually have a method and id attribute too.

action <br />
Every \<form> element requires an action attribute. Its value is the URL for the page on the server that will receive the information in the form when it is submitted

method <br />
Forms can be sent using one of two methods: get or post. With the get method, the values from the form are added to the end of the URL specified in the action attribute. The get method is ideal for:

- short forms (such as search boxes)

- when you are just retrieving data from the web server
(not sending information that should be added to or deleted from a database)

With the post method the values are sent in what are known as HTTP  headers. As a rule of thumb you should use the post method if your form:

- allows users to upload a file

- is very long

- contains sensitive data (e.g. passwords)

- adds information to, or deletes information from, a database

If the method attribute is not used, the form data will be sent using the get method.

id <br />
We look at the id attribute on page 183, but the value is used to identify the form distinctly from other elements on the page (and is often used by scripts — such as those that check you have entered information into fields that require values).

Different kinds of forms from pg 152-168

---

### Lists, Tables and Forms

- In addiction to CSS properties covered in other chapters which work with the contents of all elements, there are several others that are specifically used to control the appearance of lists, tables, and forms.

- List markers can be given different appearances using the ***list-style-type and list-style image*** properties

- Table cells can have different borders and spacing in different browsers, but there are properties you can use to control them and make them more consistent.

- Forms are easier to use if the form controls are vertically aligned using CSS.

- Forms are easier to use if the form controls are vertically aligned using CSS

- Forms benefit from styles that make them feel more interactive.

---

### Events

Different Event Types pg 246

#### How events trigger javascript code

1. select the element node(s) you want the script to respond to.

2. indicate which event on the selected node(s) will trigger the response

3. State the code you want to run when the event occurs

Three ways to bind an even to an element

1. HTML event handlers (do not use)

2. Traditional DOM even handlers

3. Dom level 2 event listeners

Events:

- events are the browser's way of indicating when something has happened (such as when a page has finished loading or a button has been clicke).

- Binding is the process of stating which event you are waiting to happen, and which element you are waiting for that event to happen upon.

- When an event occurs on an element, it can trigger JavaScript function. When this function then changes the web page in some way, it feels interactive because it has responded to the user.

- You can use event delegation to monitor for events that happen on all of the children of an element.

- The most commonly used events are W3C DOM events, although there are others in the HTML5 specification as well as browser-specific events.