# Opening
## Create Groups
At least 2 students.

Books:
https://www.wiley.com/en-sg/Pervasive+Computing+and+Networking-p-9780470747728

## Computing Eras
- Mainframe
	- Many people, one computer
	- Fixed, central location
- PC
	- One person, one computer
	- Fixed location, decentralized
- Pervasive (Ubiquitous)
	- One person, many computers
	- Maybe a smart devices or mobile
	- Sometimes invisible directly to the users

## Pervasive Computing
An environment which people interact with embedded (and mostly invisible) computers and in which networked devices are aware of their surroundings and peers and are able to provide services or use services from peers effectively.


Characteristics
1. Physical integration: integration between computing nodes and the physical worlds, e.g. white board that records what's on.
2. Instantaneous interoperation (interoperate in changing environments)

Non-Examples of Pervasive Applications
1. Accessing email over a phone line from a laptop
2. Collecting of wirelessly connected laptops based on IEEE 802.11 at a conference

Borderline:
- A web-based object discovery system
- Physical integration
- Instantaneous operation

## Characteristics
- Always running and available
- Composed of collaborating parts spared over the network - distributed components
- Adapt to environments when the users/devices move -reconfigure to use available services
- Users are not aware of the computing embedded in the device - transparent interaction
- Information pursues the user rather than user pursues the information

## Challenges
- Invisibility - disappear from users; consciousness; by embedding/combining computing infrastructure with building infrastructure.
- Scalability
- Availability - anytime and anywhere
- Dynamic - users and devices are mobile, services are provided by collaborating distributed components
- Heterogeneity - variety of hardware, software, network protocols, and service providers.
- Integration with people - personal privacy, user intentions, access control.

## Design and Implementation Problem
- User intent, to be effective it is important to track this. Otherwise it will be almost impossible to determine which system actions will help rather than hinder the user.
	- Example: user is viewing video over a network that suddenly has a bandwidth limitation. Should the system reduce the fidelity of the video? Pause briefly to find another higher-bandwidth connection? Or advice user that task can no longer be accomplished? **The correct choice will depend on what the user is trying to accomplish**

- Context awareness, pervasive system must be cognizant of its user's state and surroundings, and must modify its behaviour based on this information.
	- Such as physical location, psychological state, emotional state, personal history, daily behavioural patterns, etc.

- Balancing proactivity and transparency, unless carefully designed, a proactive system can annoy a user and thus defeat the goal of invisibility.
	- The tolerance level are likely to be close with the level of expertise on a task and familiarity with the environment. 
	- For transparency, *auser patience model* can be implemented to predict whether the user will respond positively to fetch request. So the user interaction is suppressed and the fetch is handled transparently.

- Privacy and trust, the more user depend on a pervasive system, it becomes more knowledgeable about the user's behaviours. User must trust the infrastructure to a considerable extent and the infrastructure needs to be confident of user's identity.


## Mobile Agent Technology
Agent is a computer program that acts independently on behalf of a person or organization. Mobile agent is an agent that can autonomously migrate from host to host through a potentially heterogeneous computing infrastructure, and interact with other agents.

Mobile agent composed of:
- The execution environment provided by the host.
- The mobile agents that travel to various environments on a network.

Mobile agent security:
- Confidentiality: protection of information against the possibility of being disclosed to unauthorized party.
- Integrity: unauthorized parties cannot modify relayed information.
- Availability: attacks do not prevent information and system resources from performing their intended purposes.
- Authentication: ensuring the identity of any entity in the system.
- Non-repudiation: prevent any party from being able to deny accountability for an action.

![](attachments/Pasted%20image%2020220405212938.png)


## Sensor Networks
Most often utilized in monitoring designated physical parameters.
- sensor nodes, which are equipped with sensors for one or more physical phenomena (seismic, heat, motion, etc)
- networking infrastructure, typically wireless
- sink or base station, which collect information
- computing resources at the sink, or beyond, which perform data mining and correlation


