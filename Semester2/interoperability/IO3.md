# Enterprise Computing

## Definition
SIE (Sistem Informasi Enterprise)
- Collection of systems those are integrated and have the capability to support organization's activity.
- Example: Enterprise Resource Planning(ERP), transactional systems, legacy systems.

Example of integrated system
![](attachments/Pasted%20image%2020220403215142.png)

## Motivation
- Customer see the services as a one service entity, can't be separated into smaller section.
- It is not a partial success. The whole process itself must be greatly planned to satisfy the customer.
- The service are associated to the whole service of the organization.

## Challenge
- Different problem domain.
- Complex SIE back-end
- Complex transaction handling and security
- Different format of communication or data transaction.

## Approach
![](attachments/Pasted%20image%2020220403215643.png)

### Homogeneous approach
Characteristics:
- Implemented on big vendors (SAP, Peoplesoft, etc).
- Integration on every aspect of the business (HR, finance, production, marketing, inventory) and standardized point of view (standardized service, standardized business).
- The integration hopefully more simple, because of the similarity of the components.

Drawbacks:
- It is not suitable for smaller organization, as the IT systems are not mature enough.
- Expensive.
- Long time to build
- Can miss tiny detail that incompatible with the standard.

### Gradual approach
Characteristics:
- Bottom-up approach and determine the existing condition
- String up the existing systems by using patterns and existing architecture.

Benefits:
- Cheap
- Based on the existing system.

Drawbacks:
- Dependent on the process
- Ad-hoc / temporary solution that is not standardized.

Example: academic integration
![](attachments/Pasted%20image%2020220403222551.png)

## Integration Strategy
- The integration should have the goal. Focus on the business process/bureaucracy, not the IT. Pay attention to the flow.
- Identify the stakeholders: role, tasks, authorization, and activity. Weave these elements into the planned flow.
- Integration model, i.e. E-R Diagram, UML, Data Flow Diagram
- The integration.