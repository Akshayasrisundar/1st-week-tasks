# 1st-week-tasks

1) Difference between http1.1 and http2
   
   Key Features of HTTP/1.1:
It was no longer required for each connection to be terminated immediately after every request was served with a response; instead, with the keep-alive header, it was possible to have persistent connections. It allowed multiple requests/responses per TCP connection.
The Upgrade header was used to indicate a preference from the client that made it possible to switch to a more preferred protocol if found appropriate by the server.
HTTP/1.1 provided support for chunk transfers that allowed streaming of content dynamically as chunks and for additional headers to be sent after the message body. This enhancement was particularly useful in cases where values of a field remained unknown until the content had been produced. For example, when the content had to be digitally signed, it was not possible to do so before the entire content gets generated.
Other features that reinforced its stability were introduced such as:
pipelining (the second request is sent before the response to the first is adequately served)
content negotiation (an exchange between client and server to determine the media type, it also provides the provision to serve different versions of a resource at the same URI)
cache control (used to specify caching policies in both requests and responses).
   key Features of HTTP/2.0:
It introduces the concept of a server push where the server anticipates the resources that will be required by the client and pushes them prior to the client making requests. The client retains the authority to deny the server push; however, in most cases, this feature adds a lot of efficiency to the process.
Introduces the concept of multiplexing that interleaves the requests and responses without head-of-line blocking and does so over a single TCP connection.
It is a binary protocol i.e. only binary commands in the form of 0s and 1s are transmitted over the wire. The binary framing layer divides the message into frames that are segregated based on their type – Data or Header. This feature greatly increases efficiency in terms of security, compression and multiplexing.
HTTP/2 uses HPACK header compression algorithm that is resilient to attacks like CRIME and utilizes static Huffman encoding.

2)5 Differences between browser js and node js:
    
1.	Javascript is a programming language that is used for writing scripts on the website.	NodeJS is a Javascript runtime environment.
2.	Javascript can only be run in the browsers.	NodeJS code can be run outside the browser.
3.	It is basically used on the client-side.	It is mostly used on the server-side.
4.	Javascript is capable enough to add HTML and play with the DOM.	Nodejs does not have capability to add HTML tags.
5.	Javascript can run in any browser engine as like JS core in safari and Spidermonkey in Firefox.	Nodejs can only run in V8 engine of google chrome.
6.	Javascript is used in frontend development.	Nodejs is used in server-side development.
7.	Some of the javascript frameworks are RamdaJS, TypedJS, etc.	Some of the Nodejs modules are Lodash, express etc. These modules are to be imported from npm.
8.	It is the upgraded version of ECMA script that uses Chrome’s V8 engine written in C++.	Nodejs is written in C, C++ and Javascript.

3)What happens when u type a url in address bar?
 
You enter a URL into a web browser
The browser looks up the IP address for the domain name via DNS
The browser sends a HTTP request to the server
The server sends back a HTTP response
The browser begins rendering the HTML
The browser sends requests for additional objects embedded in HTML (images, css, JavaScript) and repeats steps 3-5.
Once the page is loaded, the browser sends further async requests as needed.

4)Difference between copy by value and copy by reference

simple and exact difference between copy by value and reference is

when we declare 2 variable the memory will be allocated to one and the another one will be pointing the first and will not be allocated memory.
The changes made in one variable will affect the another.This is called as copy by reference.

When we declare 2 variable the memory will allocate difference locations and the change made in one will not affect the another.This is caleed as
copy by value.

5)How to copy by value a composite data type?

There are 3 ways to copy by value for composite data types.

Using the spread (...) operator
Using the Object.assign() method
Using the JSON.stringify() and JSON.parse() methods

1. Using Spread
Spread operator allows an iterable to expand in places where 0+ arguments are expected. 
It is mostly used in the variable array where there is more than 1 values are expected.
It allows us the privilege to obtain a list of parameters from an array.
Using spread will clone your object. Note this will be a shallow copy.

2. Using Object.assign()
The Object.assign() method copies all enumerable own properties from one or more source objects to a target object. 
It returns the target object. Note this will be a shallow copy.

3. Using JSON.parse() and JSON.stringify()
The JSON object, available in all modern browsers, has two useful methods to deal with JSON-formatted content: parse and stringify. 
JSON.parse() takes a JSON string and transforms it into a JavaScript object. 
JSON.stringify() takes a JavaScript object and transforms it into a JSON string.
Using JSON.parse() and JSON.stringify() for copy performs deep copy.
