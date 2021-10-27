# Software Development Method and Practices

## Software Development
**Definition**: detailed creation of working software through combination of coding, verification, unit testing, integration testing, and debugging. You need a predefined problem and to give solution, so you need the process in between.

![](Pasted%20image%2020210908102130.png)

Differentiate requirement and problem.
**Requirements** = Is something you have to do. Such as, to graduate you ==need== to finish your thesis. Need to is word for requirement.
**Problems** = what gives you difficulties, i.e. choosing topic.

Thesis generator software: requirement, problem, and output (solution).
![](Pasted%20image%2020210908102650.png)

**Software development**: you have predefined problem.
**Software engineering**: applying engineering principles to software development.
> Engineering principles is solving complex problem with structured way.
> complexity in this term, is something that you need to learn before applying solution, because there is:
> - several constraint: i.e. learn Linux to build environment in Linux.
> - several possibility of solution: i.e. mobile app? web app? API based solution?
> - multi domain consideration: i.e. environmental safety, economical value of the user, usability, education.
> 
> complexity can be simplified if you have predefined solution.

Software development is subset of software engineering.
Software development is the major activity in software engineering.
Software development is the discipline of software engineering.
> Go-Jek is software engineering, Go-Pay is the software development.

## Software Engineering Basics
![](Pasted%20image%2020210908114113.png)

- Customers: users of our system or people that are purchasing this system for the users.
	- Opportunity: chance to do something to provide value to customers, including fixing an existing problem via this software system.
	- Stakeholders: individuals, organizations, or groups that have some interest or concern either in the system to be developed or in its development.

- Solution: the outcome of this endeavor
	- Requirements: provide the stakeholder view of what they expect the software system to provide.
		- They indicate what the software system must do, but do not explicitly express how it must do it.
		- Among the biggest challenges software teams faces are changing requirements.
		
	- Software system: the primary outcome of software endeavor is software system itself. 3 important characteristics:
		- Functionality: the function itself
		- Quality: reliability, performance, rich user experience
		- Extensibility: from version to version and platform to platform
		
	- Endeavors: action to take to achieve an objective
		- Team: enough people with right skill mix, work collaboratevely, and adapting changing environments.
		- Work: bringing opportunity to reality, effort and time are limited.
		- Way of working: team members must agree on their way of working. I.e. the practice and tools will be used.

## Software Engineering Framework
In order to be more productive: 4 component in software engineering framework (SEI) / umbrella activities:
1. software process: aspect that we need to accomplish.
2. software method: how develop the software.
3. software practices: best practices and technical approach.
4. software tools: as enabler to make developer more productive.

![](Pasted%20image%2020210908104519.png)

## Question in Software Development
1. What tasks do we need perform? -> checklist to create quality software in structured way.
2. How do we ensure we will do a great job?
3. How do we measure the quality of what we have done?
4. How do we ensure that what we done is really matching the initial needs and requests?
5. How do we minimize the effort to accomplish the goal? -> due to bug fixing, recoding, etc.
6. What skill do we need?
7. What tools do we need?
8. How many people are needed?
9. Which skills, profiles, experience?
10. etc

Would you use the same approach to build cities, house, hospital, and cat house? **No** the quality is totally different, the result is also different.

## SDLC (Software Development Life Cycle)
**Definition** Structured process to build quality software based on predefined problem.

Why the name is not SELC? -> Completely operational structure and predefined step.
SDLC describes WHO does WHAT, HOW and WHEN to perform the ACTIVITIES that are needed to achieve the goal: Implement a Software System.
![](Pasted%20image%2020210908105556.png)

**Small program development**
![](Pasted%20image%2020210908111133.png)

## Waterfall
**Waterfall**, sequential, most famous and well defined process
- Most logical and easy to understand.
- Prescriptive and rigid
- But doesn't lead to great result, especially on new system.

Waterfall is implementation of formal software process, but it is not formal software process.

![](Pasted%20image%2020210908111152.png)

==Requirements==: understand and describe what to build.
==Analysis and design==: study the problem and design a solution that will fulfill the requirements.
==Implementation==: giving the solution
==Test and verify==: is your solution fulfill requirements and expectation?

Waterfall problem, dynamic issue especially when it has any changes and bugs, it must well defined first. In the implementation of First of a Kind (FOAK) systems, this approach doesn't work.
1. Projects delay are impacting future critical phases.
2. Risks are addressed late
3. Testing is performed only at the end.
4. Project progress is measured by document releases.
5. It doesn't allow to release preliminary version to evaluate stakeholder feedback.

## Dynamic Models
**Dynamic models**, iterative and incremental approach. This facilitates direct work and solving the delay problem in waterfall.
> Iterative: do similar activity inside the time box. For example each iterative has time box of 2 months before the increment.
![](Pasted%20image%2020210908112604.png)

Characteristics:
- Usually time boxed iterations are used and is better to add new iterations than extending the duration of an iteration.
- Risks are addressed in initial releases.
- If required a smaller system can be released during the project.
- Good for long project time, i.e. 6 months.

Problems in iterative project:
1. Exhaustion
2. Management complexity
3. Costly compared to waterfall

## Agile
**Agile** the evolution of dynamic models.

The process is to simplify things by reducing complexity of planning, by focusing on costumer value and shaping a fruitful climate of participation and collaboration

Methods: contemporary form of concurrent engineering, cross-functional teams, and overlapping development.
1. SADT
2. DeMarco method
3. Booch method
4. OMT
5. OOSE
6. RUP/UP
7. XP
8. Agile development
9. Etc

Practices:
1. Object Oriented Programming
2. OOAD
3. Use cases
4. User stories
5. UML
6. Components
7. SOA, EA, PLA
8. Etc

Formal software process
![](Pasted%20image%2020210908115628.png)

Agile manifesto
![](Pasted%20image%2020210908120001.png)

## Closing
**Process Pattern**
![](Pasted%20image%2020210908120119.png)

**Simple Process**
Personal Software Process (PSP)by Cernigemellon University
Developing software by himself, It is between agile and formal (hybrid).
![](Pasted%20image%2020210908120333.png)

**Waterfall**
![](Pasted%20image%2020210908120833.png)

**Iterative Waterfall**
![](Pasted%20image%2020210908121135.png)

**V- Model Process**
![](Pasted%20image%2020210908120905.png)

**Prototyping Process**
![](Pasted%20image%2020210908121058.png)

**Incremental Process** -> CI/CD
![](Pasted%20image%2020210908121207.png)

**Spiral Model** -> iteration model with delivered output
![](Pasted%20image%2020210908121241.png)

**Capability Maturity Model (CMM)**
To help a software organization define its level of maturity in software development.
![](Pasted%20image%2020210908121440.png)



