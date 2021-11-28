# Cyber-Attacks on the Oil & Gas Sector: A Survey on Incident Assessment and Attack Patterns
This research correlate with MITRE ATT&CK Framework, based on TTP, 

SCADA system usually apply to diverse systems and components

Cyber-Physical System (CPS) computer system in which a mechanism is controlled or monitored by computer-based algorithm. CPS is similar to IoT, sharing the basic architecture, nevertheless, CPS presents a higher combination and coordination between physical and computational elements. I.e. smart grid, autonomous mobile, medical monitoring, ICS, robotics systems, and automatic pilot.

Academic studies 4,5,8,52,115,117, 93

4, vulns and potential threats in CPS
122, ICS security and protocol-related (Modbus/TCP, DNP3, IEC 61850) and sensor related vulnerabilities.
118, classification of attack in SCADA
8, 18, 21 ,240, 47, 71 ICS security issues and vulnerabilities.
8, 47, 61 systematic analysis of realworld cyber security incidents.


121, CPS research efforts
93, security challenges and approaches in the CPS Security.
8, explore ICS security landscape

123, security and privacy concerns

Downstream infrastructures utilize SCADA as a focal point for system input and control all components (Inlet system, condensate tanks, dryer units, dehydrators, compressor, storage units, dispensers, recovery systems, station control systems)

Midstream & upstream attack follow the same general architecture

Midstream mostly below ground and have low ratios of ICS per pipeline kilometers, but Above Ground Installation (AGI) may have numerous ICS assets installed (Block valve stations, primary and secondary pump, metering stations, remote distribution stations, and critical distribution point)

Upstream infrastructures deploy SCADA systems for monitoring purposes. during well extraction, separation of oil and gas, exporting to pipes. 

ICS architecture (PLC, RTU, relays,), connectivity (protocols, routing devices, communication media), use-cases(HMI, server types,) largely the same for midstream AGIs and upstream facilities

5,29 Smart sensors and devices can be defined as nonstandard computing device able to gather, analyze,  and send data over a network for decision support 

30 OG mostly applies automated tank gauges, smart sensors and valves to monitor or influence fuel tank inventory levels and raise alarms.

Using network protocols - MITM, injection attacks eavesdropping attacks

![](attachments/Pasted%20image%2020211128213654.png)

![](attachments/Pasted%20image%2020211128213701.png)

ICS in OG, each level includes specific asset types and relevant devices

Level 0 - Edge devices
work in the field, remote installations and directly connected to engineering infrastructure - to collect physical environment information or control physical engines with input.
- sensors: temperature, pressure, humidity, sound, rfid, gas, flow, smart sensors to capture the state of components. (standardized under EU ATEX Directive 2014/34/EU - for potentially explosive atmospheres and certified using ExIA for sensor protection)
- actuators: devices for moving or controlling mechanism or system, acts upon an environment - defined with NIST

Level 1 - Intelligent control devices
supervisory systems to control infrastructures, such as actuators and monitor component status for decision making. Such as Remote Terminal Units (RTU) and Programmable Logic Controllers (PLC)

Level 1 - Network Infrastructure: Network hardware
Middleware between the substation and control center.

Level 2 - SCADA Control Center
Human Machine Interface (HMI): user input system that allows a human operator to control and monitor the systems.
ICS servers: ICS often use multiple servers for granular control and resilience. - Supervisory systems, MTU, database server

MTU = Master Terminal Units, device that issues the commands to RTUs, which located at remote places from control, gathers the required data, stores the information, and process the information.

Level 2 - Network Infrastructure: Communication protocols
How to communicate real-time to pass critical information using protocols such as DNP3, ZigBee, FINS, ModBus, RS-232

![](attachments/Pasted%20image%2020211128235259.png)

IoT and Digitization of O&G Systems
Digitization of O&G mostly involves the use of IoT smart meters (Level 0) that cooperate in closed loopswith smart relays (Level 1) and relevant software (Level 2). Benefits of IoT
- minimize operational risks during drilling
- real time monitoring of infra states 128
- improve production using data mining and aggregation 124, 135

Digitization unifies systems, but introduce major overhead in processing, storing, and securing data.
- operating facilities like offshore rigs, pipelines, stations or refineries can pave way to increased damage from security incidents 94, 95
- disruptions
- result in injuries to employees or civilians
- environmental hazards 114
- aggregation in big data result in increased privacy risks for personnel information.
- smart meter implementation sometimes bypasses layer 1. directly communicate to layer 2 through 4G

Generic attacks
1. affect physical security and safety
2. target facility


Malware infiltration may steal data or manipulate valve and cause gas leakage.

Attack can be distinguished on the location of the attacker, the close the hacker, the more dangerous

Common Attack Pattern Enumeration and Classification (CAPEC) 26
![](attachments/Pasted%20image%2020211129001149.png)

Attack based on OG facilities per layer 7,8,23,38
![](attachments/Pasted%20image%2020211129001628.png)

hardware layer : 
- low level equipment that connects to the ICS: field devices, sensors, processors, memories, slaves, RTU, PLC, relays

Firmware: software that enables low-level control of devices and hardware, stored in non-volatile memory. Interface between hardware and software.

Software: computer software used in ICS for monitoring and control. 

Process: abstract layer tht describes overall ICS and process, mapping business logic, system architecture.
