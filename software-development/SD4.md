# Key Elements of Software Development
Kuliah by Ridi Ferdiana

## Key Elements
1. Business point of view (requirement & analysis)
2. Technical Point of view (design, development, deployment)

![](Pasted%20image%2020210908154242.png)
## Technology Consideration
Technology as the enablers
1. Is your customer already has legacy system (existing system)?
2. What license that customer had? Is your client have resource to buy another technology? Or do you want to use open source technology?
3. What technology/framework is your team capable of doing?.
4. Where your app will be deployed? Web app(chrome, mozilla, etc)? Mobile app? etc..	
	What do you choose desktop vs web application? -> but it really depends on the capability of your human resources.
5. Market/current trend. I.e. low codes development, power platform by Microsoft.

The most important: is your customer agree with your technology choice?

![](Pasted%20image%2020210908154651.png)

## From Business Problems to Requirement

Using legacy system or using new system? -> depends whether your developer understand that legacy system or not. Even if your customer insists to use legacy system or not.

Visibility: using open source software is a charm because you can modify it freely.

Buy or build? 
- Do customer has the money?
- If you buy, can you integrate it to legacy system? Actually if you buy, you buy for the customer support (i.e. if you find bugs, or difficulties.), updates, etc. It will be helpful for long term run.

![](Pasted%20image%2020210908162224.png)

**From analysis to design**

![](Pasted%20image%2020210908162730.png)

Interoperability, capable to communicate between different systems.

Software development tool:
1. Computer aided software engineering (CASE tools) is the domain of software tools used to design and implement applications. i.e. diagramming tools to represents data in diagram, the most acceptable standard is UML (Unified Modeling Language). Apps that use UML: Microsoft Visio, Power Designer, etc. 
2. Integrated development environment, i.e. Visual Studio, Eclipse, etc. Differentiate with code editor.
3. Codes editor, VS Code, Atom, Sublime, Notepad, etc.
4. Build and compiler, Java SDK
5. Package provider, install shield

DevOps tool
1. Source code versioning: Git
2. Project management software: MS Project
3. Computer supported collaborative work, Teams, Webex, Zoom
4. Integration pipeline: Helps you integrate between each systems using one integration step. It helps you to automate streamline activity. I.e.Jenkins
5. Deployment support, helps you to deploy the source code. I.e. IAAC (Infrastructure As A Code), i.e. Terraform, AWS Cloudformation, Chef, Ansible, Puppet, Vagrant.

Now we also have the integrated tools for DevOps: Jira, Azure DevOps, etc.


## Key Development Decision
**Technology wave**
1. Desktop App
2. Web App
3. Mobile App
4. Multiplatform App

**Choice of Programming Language**
1. Complied (Java, C, C#)
2. Interpreted (JavaScript, Python)

**Programming Conventions**
1. camelCase
2. PascalCase
3. Hungarian Case (strCase), you define the data type before the variable name, a bit old method.

## Software Development Practices
- Coding
	- Coding design/design patterns
	- Coding conventions
	- Coding practices (Open source, 3rd party, framework)
	- Low codes and no codes development

- Teamwork
	- Planning game
	- Integration procedure (daily build)
	- Development techniques (task based, pair)

- QA
	- Creating test case by developer/by tester
	- Unit test/without unit test
	- Step through/trial and error
	- Review or debug

- Tools
	- Choose version control
	- Language and compiler version
	- Software development framework
	- Integrated development tools

## From Development to Deployment
![](Pasted%20image%2020210908170749.png)

**Release management**
Publishing tools = converting source code to binary that specific to certain platform.
Configuration management = help you deploy the code to existing infrastructure using automation, such as IAAC

## From Deployment to Maintenance
![](Pasted%20image%2020210908171015.png)

**Commerce system**
Perpetual: one term payment for long term need.

Subscription: recurring payment.

Freemium payment system:
1. Ads
2. Selling data
3. Micro transaction (i.e. in online game)

## Developers Learning Path
![](Pasted%20image%2020210908171419.png)

1. If you want to build web app, learn about web app first and current technology
2. Programming language based on the web app
3. Ready to use software development framework
4. Software architecture, i.e. client server, clustering, scalability, layered architecture
5. Life cycle management i.e. devops, scrum, cloudformation.


## Key Contemporer Technology
![](Pasted%20image%2020210908171846.png)


## Addition 
Integration vs Interoperability
Integration is a way to unite.
Interoperability is a way to communicate.

**Integration**: process of combining multiple applications to function together as unified whole. I.e. company combining multiple purchased technologies into a singular application that solves a focused problem or set of problems.
 
 two types of integration:
 1. Tight coupling
 2. Loose coupling

In the real world, deploying multiple applications to do focused jobs the enterprise is the norm, but in order to solve the complex problems, these solutions need to work together in an efficient and cost effective manner (interoperability).

**Interoperability**: incorporates content from multiple disparate and entirely independent systems to advance the effective delivery of solution to the market. It doesn't need to become one, but they communicate each other.

-   Bidirectionally sharing contact information between a [clinical communication platform](https://www.spok.com/spok-care-connect "Spok Care Connect") and a third-party scheduling solution or the EHR to ensure both solutions have the most up-to-date information via a standardized method
-   Incorporating location content from a location services device attached to an ambulatory monitor to more accurately track location information in an event or data capture
-   An alert management system combining important patient information—such as fall indicators or procedures from the EHR—into a nurse call message going to a clinician on any device, while still allowing responses to be passed back to the nurse call system for call escalations or reporting

