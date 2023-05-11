# Api Design Best Practices

## What is REST?

- In 2000, Roy Fielding proposed Representational State Transfer (REST) as an architectural approach to designing web services. REST is an architectural style for building distributed systems based on hypermedia. REST is independent of any underlying protocol and is not necessarily tied to HTTP. However, most common REST API implementations use HTTP as the application protocol, and this guide focuses on designing REST APIs for HTTP.

A primary advantage of REST over HTTP is that it uses open standards, and does not bind the implementation of the API or the client applications to any specific implementation. For example, a REST web service could be written in ASP.NET, and client applications can use any language or toolset that can generate HTTP requests and parse HTTP responses.

Here are some of the main design principles of RESTful APIs using HTTP:

- REST APIs are designed around resources, which are any kind of object, data, or service that can be accessed by the client.

- A resource has an identifier, which is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be:


Clients interact with a service by exchanging representations of resources. Many web APIs use JSON as the exchange format.


- Q. What does REST stand for?


- A. Rest stands for Representational State Transfer


- Q. REST APIs are designed around a ____.


- A. Resources


- Q. What is an identifier of a resource? Give an example.


- A. A URI that uniquely identifies that resource.


- Q. What are the most common HTTP verbs?


- A. The most common HTTP verbs are GET, POST, PUT, PATCH, and DELETE


- Q. What should the URIs be based on?


- A. URIs should be based on nouns (the resource) and not verbs (the operations on the resource). 


- Q. Give an example of a good URI.


- A. "https://adventure-works.com/orders/1"


- Q. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?


- A.


- Q. What status code does a successful GET request return?


- A.


- Q. What status code does an unsuccessful GET request return?


- A.


- Q. What status code does a successful POST request return?


- A.


- Q. What status code does a successful DELETE request return?


- A. 
