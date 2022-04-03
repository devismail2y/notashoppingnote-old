# Common Object Request Broker Architecture (CORBA)

## Why
Heterogeneity in distributed application
- Computer hardware
- Operating systems
- Network infrastructure
- Application programs
	- Programming language
	- Programming style
	- Interfaces
	- Databases

## Definition
Dealing with high-level interoperability issues with the concept of intermediary layer of the application level.

Object Management Group's (OMG) open, vendor independent architecture and infrastructure for application interoperability.
- Specification, not a software product.
- Based on standard protocol, called Internet Interoperability Protocol.
- Allows CORBA-based programs to communicate regardless of difference in their platform.

## Object Management Architecture
Standard to deliver the common architectural framework based on which applications are built.

![](attachments/Pasted%20image%2020220403233359.png)

- Application objects: objects developed for specific applications. Not standardized by Object Management Group (user-defined).
- Corba services: system-level, domain-independent objects used by application objects, i.e. naming service, object synchronization, etc.
- Vertical CORBA facilities: domain specific objects that provide common services in specific application areas, i.e. manufacturing, health, finance, etc
- Horizontal CORBA facilities: objects that provide common services for end-user applications, i.e. document manipulation, file services, etc.
- ORB: the communication platform for all objects.

Communication through Object Request Broker (ORB)
![](attachments/Pasted%20image%2020220403234117.png)

Object Remote Invocation
![](attachments/Pasted%20image%2020220403234147.png)

CORBA Architecture
![](attachments/Pasted%20image%2020220403234207.png)

