# Interface Concept

## Definition
Limitation between two parties (hardware, software, user) when they are communicating each other. Represented by an abstraction of an entity that is shown to other party / publicly.

![](attachments/Pasted%20image%2020220403231301.png)

## Example
## Interface Definition Language (IDL)
- Define the characteristics of procedure on server side that can be called by the clients.
	- Procedure name
	- Parameters, data types, categories (in, out, inout)
	- Specification interface to be compiled (if using different programming language)

Example of RPC:
![](attachments/Pasted%20image%2020220403231324.png)

Interface in RPC
![](attachments/Pasted%20image%2020220403231825.png)

## Interface in Programming Language
Define the behaviour that can be implemented by the arbitrary class in hierarchical structure.

Interface in Java
![](attachments/Pasted%20image%2020220403232011.png)

![](attachments/Pasted%20image%2020220403232030.png)

Client and server model in Java RMI
![](attachments/Pasted%20image%2020220403232104.png)

Interface in Corba:
- focus on what not how
- Implementation of IDL
- The syntax is similar to C, but it does not have control structure.

![](attachments/Pasted%20image%2020220403232236.png)

![](attachments/Pasted%20image%2020220403232310.png)


## Interface on other systems
- OLE/COM
- .NET
- Web Service