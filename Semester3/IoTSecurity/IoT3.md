# Security Engineering for IoT Development


## Task
- What could various levels of RSE (Road Side Equipment) compromise result in from a safety perspective? 
- What type of service could a compromised RSE invoke locally at the roadside? 
- Could it actually cause a safety-of-life event, for example, read out an improper speed warning so that drivers are ill prepared for an upcoming traffic condition? 
- Or, could it invoke a non-safety-related service in the traffic signal controller that merely interrupts and degrades traffic flow around the signalized intersection?

## Security Engineering
Security engineering focus on security aspects in the design of systems that need to be able to deal robustly with possible sources of disruption, ranging from natural disasters to malicious acts.  
  
Gartner estimates 2017, 50% of all IoT solutions will originate from startup less than 3 years old. This imposes security challenge.  

Engineering team should consider the security from the beginning of the project. However, in this fast-paced agile development programs, it is quite rare.  

Generally it is cheaper to invest rather than you need to patch or recall your products. To understand the security practice by peer organization: https://www.bsimm.com/

## Security in Agile Developments
Microsoft Security Development Lifecycle (https://www.microsoft.com/en-us/sdl/) define security during the development.
- Training
- Requirements
- Design
- Implementation
- Verification
- Release and Response

Agile principle manifesto defines principles, some of which present difficulties to the integration of security engineering approaches:
- Deliver working software frequently.
- Working software is the primary measure of progress.

**Directly to page 75**
To tackle this problem, multiple requirements can be added to the product backlog and prioritized as needed by the product owner.
- As a user, i want to ensure that all access passwords on IoT service are strong enough.
- As a user, I want to be able to track IoT device authorized usage.
- As a user, I want to ensure that any data stored on my IoT device is encrypted.
- As a user, I want to ensure that  any key material stored on my IoT device is safeguarded from disclosure or other unauthorized access.
- As a user, I want to ensure that any unnecessary software and services are disabled and removed.
- As a user, I want to ensure that my IoT device only collects data that is meant to be collected.

Hardware-centric security user stories (http://safecode.org/publication/SAFECode_Agile_Dev_Security0712.pdf):
- As a security and QA engineer, I want to ensure that the UART interface is password protected.
- As a security and QA engineer, I want to disable JTAG interfaces prior to product launch.
- As a security and QA engineer, I want to implement tamper response into my IoT device casing.

## IoT Device Operation
IoT product-as-a-service offering: customers pay for a certain set of entitlements on a regular basis. This mode is characterized by the leasing of IoT hardware to customers followed by tracking its use for billing purposes.  

Master Service Agreement (MSA) enables outsourcing by creating agreement between OEM (incorporates operational expenses) and ODM (manages infrastructure).


**Directly to page 78**

## Secure Design
IoT security lifecycle:  

![](attachments/Pasted%20image%2020220912143558.png)  

## Safety and Security Design
Threat modelling within IoT device and system developments.

### Threat modelling
apa?
### Privacy impact assessment
### Safety impact assessment
### Compliance

