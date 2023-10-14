# Clean-Architecture-and-CQRS
Implementation of Clean Archtecture in .NET6 | CQRS pattern using mediatR
The clean architechture can be broadly divided into four layer : 
-       Presentation
-       Domain
-       Application
-       Infrastructure     
![Capture](https://github.com/HqRhn/Clean-Architecture-and-CQRS/assets/141786593/c08aace5-fc99-4ad0-ab37-588a91a0dc0c)


**Presentation Layer**
This is the entry point of the system and contains the API endpoints, which receives the requests from clients.

**Domain Layer**
Domain is the core of Clean acrhitecture and contains things like entities, value objects, domain events.
Domain layer must not refer projects in any other layers in the solution.
Infact, other layers should depend on Domain.

**Application Layer**
Application layer orchestrates the flow of data and operations between the presentation and domain layers. 
Things like Command, Query, Behaviours sits in the application layer.

**Infrastructure Layer**
Infrastructure layer contains the implementation of external services and connections.
Implementation of connections to services like database, messaging, email, storage are present in this layer.

**Use of MediaR in this solution**
mediatR is used in this solution to implement CQRS pattern.
It is directing Query(read operations) and Commands(Write operations) to respective handlers(present in application layer)
And these handlers are communicating with infrasture layer for the read/write operations.
![Capture](https://github.com/HqRhn/Clean-Architecture-and-CQRS/assets/141786593/4aab83a5-a8cc-42ed-a280-55017b39c375)
