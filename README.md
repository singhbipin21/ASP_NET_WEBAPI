# ASP_NET_WEBAPI
 ASP.NET Web API

### 1. What is ASP.NET Web API?

Ans.:- It is a framework for building Web API. I.e. HTTP based services on top of .net Framework. It is majorly used for creating Restful Services, but can also be used for creating non-Restful Services.

### 2. Who can consume ASP.NET services?

Ans.:-  a. Browsers
        b. Mobile Application
        c. Desktop Application
        d. IOTs

### 3. What are the Restful services?

Ans.:- Rest Stands for Representational State Transfer. 
It is an architectural pattern for creating an API that uses HTTP as its underlying communication method. 
It has some constraints.

### 4. What are the REST Constraints?

Ans.:- Client-Server:- Client sends a request and the server sends the response. 
      This separation of concerns provides the flexibility for client-side and server-side logic separation.

Stateless:- Communication between client and server should be stateless between request. 
      In this server should not store any information about the client, but the client can store server information for processing a request.

Cacheable:- Server sends the information to the client about how long the information is correct, 
      so that the client should not come again and again for the same information which will increase the performance of the application.

Uniform Interface:- It defines the uniformity between client and server. it is managed by resouce and HTTP verbs like GET, PUT, POST & DELETE etc.

E.g.:-
Employee    ===>  GET   ===>    Get List of Employee

Employee/1  ===>  GET   ===>    Get Employee with Id = 1

Employee    ===>  POST  ===>    Create new employee

Employee/1  ===>  PUT   ===>    Update the employee with Id = 1

Employee/1  ===>  DELETE===>    Delete the employee with Id = 1

Another concept related to Uniform Interface is HATEOAS. HATEOAS stands for Hypermedia as the Engine of Application State. 
All this means is that in each request there will be set of hyperlinks that let's you know what other actions can be performed on the resource. 

Layered System :-
Code on Demand (optional) :- 


### 5. Difference between WCF and Web API. When to choose one over the other?

Ans.:- WCF (Windows Communication Foundation) - One of the choices available in .NET for creating RESTful services is WCF. The problem with WCF is that, a lot of configuration is required to turn a WCF service into a RESTful service. The more natural choice for creating RESTful services is ASP.NET Web API, which is specifically created for this purpose.

WCF is more suited for building services that are transport/protocol independent. For example, we want to build a single service, that can be consumed by 2 different clients - Let's say, a Java client and .NET client. Java client expects transport protocol to be HTTP and message format to be XML for interoperability, where as the .NET client expects the protocol to be TCP and the message format to be binary for performance. For this scenario WCF is the right choice. What we do here is create a single WCF service, and then configure 2 end points one for each client (i.e one for the Java client and the other for the .NET client). 

There is nothing wrong to use WCF to create RESTful services. It's just that it's a bit more complex and configuration can be a headache. If we are stuck with .NET 3.5 or we have an existing SOAP service to support but want to add REST to reach more clients, then use WCF. 

If we don't have the limitation of .NET 3.5 and we want to create brand new restful service then use ASP.NET Web API.


### 6. HTTP Request and response system.

Ans.:- Request Verbs : These HTTP verbs (GET, POST, PUT & DELETE) describe what should be done with the resource. For example do you want to create, read, update or delete an entity. 

Request Header : When a client sends request to the server, the request contains a header and a body. The request header contains additional information such as what type of response is required. For example, do you want the response to be in XML or JSON.

Request Body : Request Body contains the data to send to the server. For example, a POST request contains the data for the new item that you want to create. The data format may be in XML or JSON.

Response Body : The Response Body contains the data sent as response from the server. For example, if the request is for a specific product, the response body includes product details either in XML or JSON format.

Response Status codes : Provides the client, the status of the request. Some of the common status codes are 200/OK, 404/Not Found, 204/No Content.


