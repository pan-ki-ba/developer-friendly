# Interview Questions

## Core Java

- **Explain OOPS Concept ?**
  - **Encapsulation**
    - Is the mechanism that binds together code and the data it manipulates,  and keeps both safe from outside interference/misuse
    - Is a protective wrapper that prevents the code and data from being arbitrarily accessed by other code defined outside the wrapper
    - Access to the code and data inside the wrapper is tightly controlled through a well-defined interface
    - The public interface of a class represents access to the external users of the class. The private methods and data can only be accessed by code that is a member of the class
  - **Inheritance**
    - Is a mechanism in which one object acquires all the properties and behaviors of a parent object.
    - Supports the concept of hierarchical classification
    - Inheritance interacts with encapsulation. If a given class encapsulates some attributes, then any subclass will have the same attributes plus any that it adds as part of its specialization
    - Code reusability
  - **Polymorphism**
    - Is the ability of an object to take many forms
    - It describes the concept that you can access objects of different types through the same interface. Each type can provide its own independent implementation of this interface.
    - Can perform a single task in different ways. In the technical world, polymorphism allows one to do multiple implementations by defining one interface.
    - Types of polymorphism
      - compile time polymorphism ( method overloading )
        - methods in the same class have the same name but different parameters
      - runtime polymorphism ( method overriding )
        - method signature (name and parameters) are the same in the superclass and the child class
  - **Abstraction**
    - Is the process of hiding certain details and showing only essential information to the user
    - Implemented in java using abstract class & interfaces
- **What is Association, aggregation, and composition in OOPs ?**
- **Expalin working/usage of HashMap ?**
- **Explain working/usage of ConcurrentHashMap ?**
- **Explain comparator & comparable interfaces, whats usage of them ?**
  - **Comparator**
    - The Comparator provides multiple sorting sequences. In other words, we can sort the collection on the basis of multiple elements such as id, name, and price etc.
    - Comparator doesn't affect the original class, i.e., the actual class is not modified.
    - Comparator provides compare() method to sort elements
    - A Comparator is present in the java.util package.
    - We can sort the list elements of Comparator type by Collections.sort(List, Comparator) method.
  - **Comparable**
    - Comparable provides a single sorting sequence. In other words, we can sort the collection on the basis of a single element such as id, name, and price
    - Comparable affects the original class, i.e., the actual class is modified
    - Comparable provides ***compareTo(T obj)** method to sort elements.
    - Comparable is present in java.lang package
    - Arrays.sort(x) and Collection.sort(x) uses compareTo() method of Comparable class
- **String Class**
- **What is the default method, and why is it required ?**
  - Method in the interface that has a predefined body is known as the default method
  - Concept of default method is introduced in java 8 to add the new methods in the existing interfaces in such a way so that they are backward compatible
- **What is lambda expression ?**
  - Lambda expressions let you express instances of single-method classes more compactly
  - A lambda expression is a short block of code which takes in parameters and returns a value

## Servlet

## Spring Framework

- **How Spring security works ?**

## Spring Boot

## JPA

## Hibernate

## Spring Data JPA

## Spring Cloud

## Microservices

- **What are the advantages of Microservices Architecture ?**
  - **Advantages**
    - **Independent developement**
      - Microservices can be assigned to specific development teams, which allows them to focus solely on one service/feature
    - **Independently deployable**
      - Microservice can be deployed independently, as needed, enabling continuous improvement and faster app updates
    - **Scalability**
      - Since all services are separate, you can more easily scale the most needed ones at the appropriate times, as opposed to the whole application. This also means scaling is faster and often more cost-efficient as well
    - **Fault Isolation**
      - If a specific microservice fails, you can isolate that failure to that single service and prevent cascading failures that would cause the app to crash. This fault isolation means that your critical application can stay up and running even when one of its modules fails
      - Microservices reduce downtime through fault isolation
    - **Mixed Technology Stack**
      - Microservices provide the flexibility to try out a new technology stack on an individual service as needed
    - **Ease to understand and maintain**
      - Smaller codebase enables teams to more easily understand the code, making it simpler to maintain
- **What are the disadvatages/challenges of Microservices Architecture ?**
  - **Disadvantages**
    - **Communication between services is complex**
      - Communication between services can be complex. An application can include dozens or even hundreds of different services, and they all need to communicate securely
    - **Debugging problems can be harder**
      - Debugging becomes more challenging with microservices. With an application consisting of multiple microservices and with each microservice having its own set of logs, tracing the source of the problem can be difficult
    - **Global testing is difficult**
      - Unit testing may be easier with microservices, integration testing is not. The components are distributed, and developers can’t test an entire system from their individual machines/workspaces
    - **Interface control is even more critical**
      - Each microservice has its own API, which apps rely on to be consistent. While you can easily make changes to a microservice without impacting the external systems interacting with it, if you change the API (the interface), any application using that microservice will be affected if the change is not backwards compatible
    - **Up-front costs may be higher with microservices**
    - **Distributed transactions handling could be complex/difficult to handle**
- **Explain RESTful API is stateless services ?**
  - **Statelessness of REST Api** 
    - Statelessness means that every HTTP request happens in complete isolation
    - Each request must contain all of the information necessary to be understood by the server, rather than be dependent on the server remembering prior requests.
    - Storing session state on the server violates the stateless constraint of the REST architecture
    - If any such information is important then the client will send that as part of the current request
  - **The stateless constraint**
    - Each request from client to server must contain all of the information necessary to understand the request, and cannot take advantage of any stored context on the server
    - Session state kept entirely on the client
  - **Authentication and authorization**
    - If the client requests protected resources that require authentication, every request must contain all necessary data to be properly authenticated/authorized.
    - HTTP authentication is presumed to be stateless: all of the information necessary to authenticate a request MUST be provided in the request, rather than be dependent on the server remembering prior requests and **authentication data should belong to the standard HTTP Authorization header**
    - **how authentication/authorization works**
      - For authentication, you could use the Basic HTTP Authentication scheme, which transmits credentials as username and password pairs, encoded using Base64: ***Authorization: Basic \<credentials>***
      - If you don't want to send the username and password in each request, the username and password could be exchanged for a token (such as JWT) that is sent in each request. JWT can contain the username, an expiration date and any other metadata that may be relevant for your application: ***Authorization: Bearer \<token>***
- **Scalable microservicess ?**
- **What are the best practices to design microservices ?**

## Architecture

- **Explain SOLID principle ?**
  - SOLID is a set of 5 design principles which encourage us to create more maintainable, understandable, and flexible object oriented software
  - **S**ingle Responsibility
    - **A class should have only one reason to change,** means that each class only does one thing and every class or module only has responsibility for one part of the software’s functionality
  - **O**pen for extensions, close for modifications
    - **Open for extension,** meaning that the class’s behavior can be extended and **Closed for modification,** meaning that the source code is set and cannot be changed.
  - **L**iskov Substitution principle
    - Every derived class should be substitutable for its parent class
    - In a lot of ways it’s simply an extension of open-closed principle, as it’s a way of ensuring that derived classes extend the base class without changing behavior
    - Respecting this principle brings more stability over time to your complex systems with a hard focus on retro-compatibility
    - Objects of a superclass shall be replaceable with objects of its subclasses without breaking the application. That requires the objects of your subclasses to behave in the same way as the objects of your superclass. Its done by ***design by contract concept***
  - **I**nterface Segregation
    - Clients should not be forced to depend upon interfaces that they don't use
    - Fine grained interfaces shoulde be designed that are client-specific and they should not be forced to implement interfaces they do not use.
    - Should have client specific interfaces and avoid general purpose fat interface
  - **D**ependency Inversion
    - High-level modules should not depend on low-level modules. Both should depend on abstractions. Depend on abstractions, not on concretions
    - ***High Level Classes --> Abstraction Layer --> Low Level Classes***
- **How sessions are handled in web applications ?**
  - HTTP protocol and Web Servers are stateles
  - Session is a conversional state between client and server and it can consists of multiple request and response between client and server. Since HTTP and Web Server both are stateless, the only way to maintain a session is when some unique information about the session (session id) is passed between server and client in every request & esponse
  - several ways to handle session information
    - URL rewriting
    - Cookies
    - Hidden Form fields
    - HttpSession Api
  