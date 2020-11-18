# **Sending form data**

- [MDN Sending form data](https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data)

- [Forms in HTML5](https://htmlreference.io/forms/)

## **Client/server architecture**

a client (usually a web browser) sends a request to a server (most of the time a web server, using the HTTP protocol. The server answers the request using the same protocol.

An HTML form on a web page is nothing more than a convenient user-friendly way to configure an HTTP request to send data to a server. This enables the user to provide information to be delivered in the HTTP request.

## **On the client side: defining how to send the data**

The \<form> element defines how the data will be sent. All of its attributes are designed to let you configure the request to be sent when a user hits a submit button. The two most important attributes are action and method

The action attribute defines where the data gets sent. Its value must be a valid relative or absolute URL. If this attribute isn't provided, the data will be sent to the URL of the page containing the form — the current page.

    sent to an absolute URL:
    <form action="https://example.com">

    sent to relative URL on same origin:
    <form action="/somewhere_else">

    When specified with no attributes, data is sent to the same page that the form is on:
    <form>

The names and values of the non-file form controls are sent to the server as name=value pairs joined with ampersands. The action value should be a file on the server that can handle the incoming data, including ensuring server-side validation. The server then responds, generally handling the data and loading the URL defined by the action attribute, causing a new page load (or a refresh of the existing page, if the action points to the same page)

## **The method attribute**

The method attribute defines how data is sent. The HTTP protocol provides several ways to perform a request; HTML form data can be transmitted via a number of different methods, the most common being the GET method and the POST method

An HTTP request consists of two parts: a header that contains a set of global metadata about the browser's capabilities, and a body that can contain information necessary for the server to process the specific request.

### **The GET method**

used by the browser to ask the server to send back a given resource

if a form is sent using this method the data sent to the server is appended to the URL.

### **The POST method**

the method the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request

If a form is sent using this method, the data is appended to the body of the HTTP request.

When the form is submitted using the POST method, you get no data appended to the URL

The Content-Length header indicates the size of the body, and the Content-Type header indicates the type of resource sent to the server

sending form data is easy, but securing an application can be tricky. Just remember that a front-end developer is not the one who should define the security model of the data.It's possible to perform client-side form validation, but the server can't trust this validation because it has no way to truly know what has really happened on the client-side