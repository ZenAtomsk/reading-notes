## **Local Storage**

### **The past, present & future of local storage for web applications**

#### Diving in

Persistent local storage is one of the areas where native client applications have held an advantage over web applications. For native applications, the operating system typically provides an abstraction layer for storing and retrieving application-specific data like preferences or runtime state. These values may be store in the registry, INI files, DML files or some other place according to platform convention. If your native client application needs local storage beyond key/value pairs, you can embed your own database, invent your own file format, or any number of other solutions

Historically, web applications have had none of these luxuries. Cookies were invented early in the web’s history, and indeed they can be used for persistent local storage of small amounts of data. But they have three potentially dealbreaking downsides:
  1. Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over
  2. Cookies are included with every HTTP request, sending data unencrypted over the internet (unless your entire web applications is served over SSL)
  3. Cookies are limited to about 4KB of data - enough to slow down your application, but not enough to be terribly useful

What we really want is
  - a lot of storage space
  - on the client
  - persists beyond a page refresh
  - isn't transmitted to the server

Before HTML5, all attempts to achieve this were ultimately unsatisfactory in different ways

--- 

#### Local storage hacks before HTML5

The original in Microsoft IE was called userData, allowing 64 KB of data per domain

in 2002, adobe introduced Flash 6 allowing up to 100 KB per domain

2007 Google launched Gears. Gears can store unlimited amounts of data per domain in SQL database tables. By 2009, dojox.storage could auto-detect (and provide a unified interface on top of) Adobe Flash, Gears, Adobe AIR, and an early prototype of HTML5 storage that was only implemented in older versions of Firefox

all of them are either specific to a single browser, or reliant on a third-party plugin

this is the problem that HTML5 set out to solve: to provide a standardized API, implemented natively and consistently in multiple browsers, without having to rely on third-party plugins.

--- 

#### HTML5 Storage

“HTML5 Storage” is a specification named Web Storage, which was at one time part of the HTML5 specification proper, but was split out into its own specification for uninteresting political reasons. Certain browser vendors also refer to it as “Local Storage” or “DOM Storage.” The naming situation is made even more complicated by some related, similarly-named, emerging standards

it’s a way for web pages to store named key/value pairs locally, within the client web browser. Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you. Unlike cookies, this data is never transmitted to the remote web server (unless you go out of your way to send it manually). Unlike all previous attempts at providing persistent local storage, it is implemented natively in web browsers, so it is available even when third-party browser plugins are not.

From your JavaScript code, you’ll access HTML5 Storage through the localStorage object on the global window object.

#### Using HTML5 Storage 

HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. **The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored as a string.** If you are storing and retrieving anything other than strings, you will need to use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype.

><code>
>interface Storage { <br />
>&nbsp;  getter any getItem(in DOMString key);<br />
>&nbsp;  setter creator void setItem(in DOMString key, in any data); <br />
>};
></code>

Calling **setItem()** with a named key that already exists will silently overwrite the previous value. Calling **getItem()** with a non-existent key will return null rather than throw an exception.

Like other JavaScript objects, you can treat the localStorage object as an associative array. Instead of using the **getItem()** and **setItem()** methods, you can simply use square brackets.

    For example:

    >var foo = localStorage.getItem("bar");
    // ...
    localStorage.setItem("bar", foo);

    …could be rewritten to use square bracket syntax instead:

    var foo = localStorage["bar"];
    // ...
    localStorage["bar"] = foo;

There are also methods for removing the value for a given named key, and clearing the entire storage area (that is, deleting all the keys and values at once).

    interface Storage {
      deleter void removeItem(in DOMString key);
      void clear();
    };

Calling **removeItem()** with a non-existent key will do nothing.

Finally, there is a property to get the total number of values in the storage area, and to iterate through all of the keys by index (to get the name of each key).

    interface Storage {
      readonly attribute unsigned long length;
      getter DOMString key(in unsigned long index);
    };

If you call key() with an index that is not between 0–(length-1), the function will return null.

---

#### Tracking changes to the HTML5 Storage area

If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event is fired on the window object whenever **setItem()**, **removeItem()**, or **clear()** is called and actually changes something. For example, if you set an item to its existing value or call **clear()** when there are no named keys, the storage event will not fire, because nothing actually changed in the storage area.

#### Limitations in current browsers

“5 megabytes” is how much storage space each origin gets by default. This is surprisingly consistent across browsers, although it is phrased as no more than a suggestion in the HTML5 Storage specification.

“QUOTA_EXCEEDED_ERR” is the exception that will get thrown if you exceed your storage quota of 5 megabytes
