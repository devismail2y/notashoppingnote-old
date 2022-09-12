# Vulnerability Threat and Countermeasures

## Pillar of Information Security
Five pillars of cybersecurtiy:
- Confidentiality
- Integrity
- Availability
- Authentication
- Non-repudiation

Plus two more in IoT
- **Resilience**: maintain state of awareness and an accepted level of operational normalcy in response to disturbances including from the nature.
- **Safety**: safe from causing hurt, injury, or loss.

## TVR (Threat Vulnerability Risk)
- Threat: potential of attacks/exploit. 
	- Threat actor (source): who do the threat.
	- Threat: hardware, software, environmental, supply chain, degradation, etc.
	- Can target safety: transfer functions, state filters (kalman filters) and other inner control loop artifacts.
	- Malicious hacking drives for-profit marketplace of its own in dark web.
- Vulnerability: weakness either in design, integration, or operation.
	- Deficiencies in a device's physical protection
	- Software quality
	- Configuration
	- Suitability of protocol security for its environment
	- Appropriateness of the protocols themselves.
- Risks: quantitative or qualitative methods of evaluation. It one's exposure to loss.
	- How large the impact of attack?
	- How valuable the target may be to attackers?
	- Anticipated skill and motivations of the attackers.
	- A prior knowledge of a system's vulnerabilities (those discovered during threat modelling, public advisories, penetration testing, and so on).

Common IoT Attack
- Wired and wireless scanning
- Protocol attacks
- Eavesdropping
- Cryptographic and key management attacks
- Spoofing and masquerading
- Operating system and application integrity attacks
- Denial of service and jamming
- Physical security attacks
- Access control attacks (Privilege Escalation)

Countermeasures:  
![](attachments/Pasted%20image%2020220905141501.png)  

## Attack Trees
Using SecurlTree tools build by [Amenaza](https://www.amenaza.com)

Attacker has goal to re-directing Unmanned Aircraft Systems (UAS), which is a drone while in flight. There are top-level activities of attack tree.  
![](attachments/Pasted%20image%2020220905142229.png)  
- Corrupting navigation database: 
Apa?

## Fault Trees
Safety and reliability engineering's principal modeling tool is called Fault Tree Analysis (FTA). For example, FAA safety requirements for aircraft needs significant levels of redundancy. This risk management of FAA for example lean heavily on FTA.

Fault tree and attack tree differences:
- Fault tree are not based on intelligently planned attacks.
- Fault trees are traversed based on stocahstic process (failure/fault rates) from each leaf through the dependent, intermediate nodes.
- Each fault tree leaf is completely independent (fault occur randomly AND independently of each other) of all other leaves of the tree.

In essence a fault tree can account for the rate at which an aircraft's braking system may fail naturally.

Merging fault and attack tree
apa?

## De