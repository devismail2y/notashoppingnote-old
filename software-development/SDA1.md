# Paper Review, A Framework For Transitioning Of Traditional Software Development Method To Distributed Agile Software Development

Madan Singh1 , Naresh Chauhan2 , Rashmi Popli3 1KIET Group of Institutions, Ghaziabad, 2,3YMCA University, Faridabad

Output:
The framework to transition traditional to Distributed Agile Software Development and address time-zone based problems in Distributed Environment.

## Intro
### Build and Fix Model
- No pre planning or pre designing
- resolves bugs at later stages.
- Not a planned approach.


In the challenging world of software development where customer opinion and demands are changing on day to day basis, these traditional methods cause project failures due to poor customer communication and rigid time frame structures

Early stages of software development followed “build and fix model and code – some – more model”. It is referred as first generation in the history of software development. In this development mechanism the idea is to write the code without pre – planning or pre – designing. It resolves bugs at later stages.

Lack of efficiency and predictability

### Heavy Weight Method
- called plan driven methods
- disciplined approach for large-sized projects.
- predictive in nature due to contest of a fixed schedule
- customer communication in the beginning and when the final product is delivered.
- But customer does not remain an integral part of such systems.
- It works well for the projects where requirements are very obvious and implicit.
- But these models face higher rate of project non reception, customer disagreement due to complex and dynamic nature of requirements.


### Agile Software Development (ASD)
- collection of software development approaches based on incremental development.
- Prominence, malleability, adaptive planning, frequent and incremental release, time-boxed development, continous customer communication.
- Effectual communication between team members is key aspect of ASD
- Iterative delivery is key process in agile environment, and may vary from one week to four weeks (sprint).\
- Gain attractiveness, because more action rather than plans, minimum documentation, minimum sized team performing all tasks, nose to nose contact, contribution of all the stakeholder in development process, applying changes at whatever time, good blueprint, eminent focus, and iterative delivery of shippable manufactured goods to the customer.

Agile Software Development (ASD) is software development methodology that emphasizes on adaptability. Due to which it satisfies customer - centered development that supports quick and flexible response to change. Distributed Agile software development (DASD), is a methodology in software development paradigm where development teams are distributed in different countries across the globe. 

### Distributed ASD (DASD)
- When any of the stakeholders is not available at the development site.
- Communication challenge to be addressed.
- language, cultural barriers, timezone barriers.
- homogeneous vs heterogeneous distributed system
	- homogeneous: all of them have same hardware, architecture, OS
	- heterogeneous: each computer has its own OS and machine infrastructure
- Resources are shared in distributed environment either in cooperating or competitive mode.
- Reduced cost, development time, enhanced quality
- But at the cost of team dynamics and certain dependencies problem.
- 
![](Agile%20vs%20Distributed%20Agile.png)

## Problems
- Communication between members is crucial, so leading the team is the main concern. -> designating a leader at every location can allow an helpful and alert communication to achieve goals. The onsite leader is supposed to direct the onsite team by communication with them and can be set as a point of contact for the main project and the client. The leader will be liable for running the communication channels and make sure the team is in receipt of course of action appropriately on the deliverables.
- In DA environment, tasks cannot be assigned based on expertise set, competence, ease of use, and goals due to different problems. Allocation strategy need to be addressed which solves the problem of task allocation in distributed environment qualitatively.
- Backlog prioritization in Agile environment need to be addressed properly. Properly managed backlogs can only help in faster completion of projects and faster delivery of the product.
- These team members have to fulfill some real time activities (locking a process, submitting a project at critical time, which faces some delay due to differences in logical clocks due to timezone difference)

## Content
- Distributed Software Development has grown rapidly die to cheaper manual labor, access to worldwide capacity, increase in trade and faster delivery. This is possible because business activities are performed at remote sites with remote teams who work all together to achieve common goals. In this way, a network of sub-teams is formed who work together to achieve the desired goals, i.e. to deliver the product successfully to the customer.
- Characteristics of distributed development: multi sourcing, geographic distribution, temporal variety, socio - cultural variety, linguistic variety and contextual variety, political and linguistic variety.
- Basic problem: design challenges, concurrency, openness, load balancing, security, complexities, dependencies, and required abilities for development.
- Three categories of distributed systems:
	- where hardware and software are kept distributed
	- where developers are kept distributed
	- where hardware, software, and developers are kept distributed.

- In all these three categories the problems persist but the first intent is to move the people from traditional software development to Agile software development and further to distributed Agile software development.
- This transition has to be made in such a way that the people working on traditional platforms do not face many problems.
- Further distributed development model is difficult to build in the absence of accurate people, exact processes and right tools.
- For this transitioning task, ownership is assigned to each team member, testing practices and development standards are implemented, effective communication channels are built which help in meetings and interactions, trainings, reviews and feedbacks.

### Framework
![](Framework%20from%20traditional%20to%20DASD.png)
- authentication for trustworthiness of the users.
- auto check to know whether the devices are lying in same timezone, if not, time zone adjustment algorithm are applied to reset the clocks of all active users.
- prioritize the task set which exists in the form of user stories
- task allocation algorithm is run which allocates the tasks to different developers
- the development starts in Agile environment that means that all the development work are done in specific time based environment called as Sprints which run for four to six week time for development. During each sprint developers meet either directly or through other means like video conferencing or video calling to discuss the progress or the hurdles encountered during the development process
- In this fashion development work continues for the entire sprint period after which shippable products are made available to the customer.
- But after each sprint, some backlog is always there which occurs due to a specific set of reasons. This backlog may cause severe problems to project completion if it is not handled properly. So the backlog available after each sprint is prioritized and reallocated to developers during other sprints or separately.
- Once all the sprints are over the product goes through regression testing phase where test cases are prepared.
- alpha – beta testing
- Delivered to customer