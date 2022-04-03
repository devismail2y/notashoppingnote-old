# Remote Procedure Call (RPC), Interoperability at the Early Stage

## Inter-Process Communication
Communication between two running processes. Inter-Process Communication (IPC) is carried out through sockets.
- Socket has to be defined before used. It has their own ID that can be used as reference for the sockets.
- The receiving process has to bind its socket to a specific address. The sender also has to do the same if it requires an answer from the receiver.

![](attachments/Pasted%20image%2020220403211925.png)

Problem: low-level details are a very simple, textual communication. Not talking about interoperability yet, since two parties are closely coupled (same programming language, same functionality).

## Remote Procedure Calling
When computer program causes a procedure (subroutine) to execute in a different address space (commonly on another computer on a shared network), which is coded as if it were local procedure call, without the programmer explicitly coding the details for the remote interaction.

Higher level abstraction of inter-process communication. The communication is carried out through procedure calls: one client (calling) procedure and one server (callee) procedure. This also has syntax transparency, the same syntax between local and remote calls.

![](attachments/Pasted%20image%2020220403213101.png)

RPC system does the following:
- Implementing the interface and integrating RPC mechanism with a specific programming language.
	- Marshalling and unmarshalling.
	- Selection of remote procedures triggered by a request message.
- Sending and receiving messages
- Finding a server for a specified service (binding process)

[Example](https://en.wikipedia.org/wiki/Remote_procedure_call) of RPC = 
- [NFS](https://www.ibm.com/docs/en/aix/7.1?topic=system-remote-procedure-call-protocol)
- Java RMI (Remote Method Invocation)

