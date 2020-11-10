# **REST**

**REST** provides a definition of a “resource”, which is what HTTP points to.

A web page is a “*representation*” of a resource. Resources are just concepts. URLs tell the browser that there's a concept somewhere. A browser can then go ask for a specific representation of the concept. Specifically, the browser asks for the web page representation of the concept.

**Web Services**” or "**APIs**". It means a lot of different things to a lot of different people but the basic concept is that machines could use the web just like people do.

computers can use those same protocols to send messages back and forth to each other.

**Redirect** is a way of having one machine tell another machine about a resource that might be on yet another machine.

There's a powerful concept in programming and CS theory called “**polymorphism**”. That's a geeky way of saying that ***different nouns can have the same verb applied to them***.

You can apply those same exact verbs to any of the objects sitting there. some verbs are almost universal like GET, PUT, and DELETE.

when you go to a web page, the browser does an HTTP GET on the URL you type in and back comes a web page. The web page just specifies the URLs to the images and the browser goes and does more GETs using the HTTP protocol on them until all the resources are obtained and the web page is displayed. But the important thing here is that very different kinds of nouns can be treated the same.

web pages are designed to be understood by people. A machine doesn't care about layout and styling. Machines basically just need the data. Ideally, every URL would have a human readable and a machine readable representation. When a machine GETs the resource, it will ask for the machine readable one. When a browser GETs a resource for a human, it will ask for the human readable one.

Each of the systems would retrieve information from each other using a simple HTTP GET. If one system needs to add something to another system, it would use an **HTTP POST**. If a system wants to replace something in another system, it uses an **HTTP PUT**, or, to do a partial update, it'll hopefully use **PATCH**. The only thing left to figure out is what the data models should look like.

