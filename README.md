# Clean-Architecture-and-CQRS
Implementation of Clean Archtecture in .NET6 | CQRS pattern using mediatR
The clean architechture can be broadly divided into four layer : 
-       Presentation
-       Application
-       Domain
-       Infrastructure     
![Capture](https://github.com/HqRhn/Architecture-Tests/assets/141786593/90a2bb38-b4a8-4b23-b3e5-4a21ed2e7f26)


**Presentation Layer**
This is the entry point of the system and contains the API endpoints, which receives the requests from clients.

**Application Layer**
Application layer orchestrates the flow of data and operations between the presentation and domain layers. 
Things like Command, Query, Behaviours sits in the application layer.

**Domain Layer**
Domain is the core of Clean acrhitecture and contains things like entities, value objects, domain events.
Domain layer must not refer projects in any other layers in the solution.
Infact, other layers should depend on Domain.


**Infrastructure Layer**
Infrastructure layer contains the implementation of external services and connections.
Implementation of connections to services like database, messaging, email, storage are present in this layer.


**CQRS Flow**

![Capture](https://github.com/HqRhn/Architecture-Tests/assets/141786593/cba9e355-305f-4ef7-9122-dcc874452dcb)


**Use of MediaR in this solution**
mediatR is used in this solution to implement CQRS pattern.
It is directing Query(read operations) and Commands(Write operations) to respective handlers(present in application layer)
And these handlers are communicating with infrastructure layer for the read/write operations.

![Capture](https://github.com/HqRhn/Architecture-Tests/assets/141786593/237c0852-291c-4138-a9e1-65f26babb8c8)

