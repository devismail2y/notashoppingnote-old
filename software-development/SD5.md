# The Essence of Software Development
Kuliah by Ridi Ferdiana

## Software Project
**Software Project** temporary activity to produce a software or a process.
Project Management Institute; guide, training and certification in project management.

Example:
- Application builder
	- One-offs/bespoke systems
	- Off-the-self application
	- Customized off-the-shelf-application
- Workflow
- API
- Integration service
	- Vertical
	- Horizontal
- Consulting services
- Installation and training services

Output:
- Software product
- Software artifact (anything related to the software except the software itself)
	- Architecture
	- Documentation
	- Design/mock up

## Managing Software Project
A shared vision between a project manager and project stake holder. Communication is an only way to have shared vision.

Activities Diagram

![](attachments/Pasted%20image%2020210922091852.png)

1. Assess feasibility: Is it feasible. 
- Human resources: Do you have the developer for certain programming language?
- Risk management: Can you take the risk for creating this project with the time limit?
- Quality management: Can you make the bug free solution, resilience, scalable, high availability?
- Change control and configuration management: Can you accept if there is changing environment or requirement?
2. Formalize goals: Define a goal, part of plan section
- Define business value for customer: financial (gaining profit) or non financial (increase productivity, easier communication, gain popularity, trust)
- Define schedule, based on activity that you need to do. WBS: Work Breakdown Structure.
- Define cost
3. Execute and monitor
- Kick off activities, start the software project
- Develop: i.e. using agile
- Collect outputs
4. Close
- Close
- Release

## Managing Software Development Lifecycle Process
![](attachments/Pasted%20image%2020210922100129.png)

**1. Requirement Engineering**
Understand the complex problem:
- needs
- constrains/limitation: budget, time, IDE, user requirements

![](attachments/Pasted%20image%2020210922100432.png)

**2. Business Modelling**
Understand how an organization is structured and works

![](attachments/Pasted%20image%2020210922101011.png)

- Understanding the current business process
- Improving the current business process
	- Re-engineering: finding the gap in the current business process + modification.
	- Transforming: different business model, different way to do business. Transformation or re-engineer decision is based on how the constrains affects your project.

**3. UX Design**
Start from UX design? because the customer can see the final product.

![](attachments/Pasted%20image%2020210922104219.png)

- User profile / persona
- Story board / usage scenario
- Design prototype
	- Mock up / low fidelity prototype (photoshop, canva, powerpoint, writings)
	- Minimum Viable Product (MVP) / Proof of Concept (PoC) / high fidelity prototype (build by real software development tools / IDE)	

**4. System Design**
- Software architecture (where to put software, databases, services).
	- Layered architecture
	- Deployment diagram
- Network architecture (if your customer need specific network diagrams).
	- Private / public IP subnet
	- Firewall
- Enterprise architecture
	- Policy
	- Governance

**4. Construction**
- Choosing productivity tools
- Software estimation
- Apply coding standard
- Doing unit testing

**5. Validation and Verification**

![](attachments/Pasted%20image%2020210922113144.png)

- Test case, list things that you need to test based on the requirements or usage scenario.
- Test plan, how you test?
- Test report, the outcome


Validation: Validate user input with the standard or format.
i.e. email validation:
- Email must have @domain.com
- Email must be at least 4 characters.

Verification: Verify user input with the data. I.e. verify username and password in user table.

**6. Testing Activities**

![](attachments/Pasted%20image%2020210922113711.png)

- Unit testing: testing functions or methods, such as buying method, posting method, display function.
- Integration testing: testing components / modules, searching integration testing: call several methods in order to do seach: sorting, filter, and do search
- System testing: testing system / app, testing system in a certain scenario.
- Usability: testing the user when using our system, test any other activity you give customer to the system + user feedback.
- Regression testing: whether is change in codes or requirements. 

**7. Deployment**

![](attachments/Pasted%20image%2020210922114002.png)

Deploy in 3 environments, in order to minimize the risk (as different usage of environment), quick recovery (), 
- Development environment, lowest risk
- Testing environment / staging, moderate risk, reproduce bugs (isolate the error to know where is the bugs located)
- Production environment, highest risk, customer report bugs

**8. Migration Strategy**
- Cut off, the system A down the system B up
- Parallel, the system A still run the system B run (run together), i.e. classic version and modern version.
- Piloting: user volunteered to testing the beta version. If there is no complaint from these users, then you can migrate the system.
- Phased, 2 systems up, in order to migrate from classic version to modern one step-by-step. After fully migrate, the classic version will be shut down.


## Conclusion Diagram
![](attachments/Software%20Development%20Essence.png)


