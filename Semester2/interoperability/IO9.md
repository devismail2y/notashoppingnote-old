# Inter-Process Communication
## Inter-Process Communication (IPC)
![](attachments/Pasted%20image%2020220425103915.png)
Communication using socket, 

socket null() to receive any connection in the port (LISTENING mode).

Port is hardware terminology.

## Remote Procedure Calling
Higher level abstraction (in program level) of inter-process communication, in comparison of processing directly  through socket. Communication is carried out through procedure calls. Process who called and calling are on the different computers.

In RPC, pointers are meaningless because remote process can not refer the memory point in other systems. There have to be another method.  The answer is Interface Definition Language (IDL)

IDL is the way to define interface, procedure that will be called, how, and parameter type in RPC.

![](attachments/Pasted%20image%2020220425112618.png)

Marshalling, is the form of serialization. In order to send data, each process need to speak a common language. Native process could represents data in various format, so this is important to be communicate each other. The other process is the unmarshall is the process of deserialization / converting into native process format.

Issues:
- Interference when communicate
- Abnormality on the communication

 
## Network File System


## Java RMI (Remote Method Invocation)
![](attachments/Pasted%20image%2020220425115144.png)
Just like RPC in C, however RMI only integrated with Java itself. The interface (IDL) is also created in Java. It is not fully interoperable with other programming language.


RPC, IPC is not very usable today.