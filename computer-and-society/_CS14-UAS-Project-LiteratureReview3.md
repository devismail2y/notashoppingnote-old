# Cyber-Attacks on the Oil & Gas Sector: A Survey on Incident Assessment and Attack Patterns
This research correlate with MITRE ATT&CK Framework

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

ICS in OG
Level 0 - Edge devices
work in the field, remote installations and directly connected to engineering infrastructure - to collect physical environment information or control physical engines with input.
- sensors: temperature, pressure, humidity, sound, rfid, gas, flow, smart sensors to capture the state of components. (standardized under EU ATEX Directive 2014/34/EU - for potentially explosive atmospheres and certified using ExIA for sensor protection)
- actuators: devices for moving or controlling mechanism or system, acts upon an environment - defined with NIST

128448




