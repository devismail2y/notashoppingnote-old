# Standards and Implementation of Pervasive Computing Applications

## Mobility
Physical mobility and logical mobility.

Paradigm:
- low cost
- targeted at relatively simple devices with limited resources

## Simple Classification of Wireless Networks
![](attachments/Pasted%20image%2020220405214948.png)

Spectrum Management:
- Manual: users configure their systems to avoid interfering with others (strength and frequency)
- Centralized: centralized entities that manage the use of frequencies and assign them to their nodes to avoid interference.
- Distributed assignation of frequencies: network senses the medium and gathers information about which channels (frequencies) are crowded. It then selects un-crowded channel in which to operate.

### Global Cell
- Radio coverage reach hundreds of kilometres.
- Suitable for communication with remote areas, where there is low traffic densities or between countries.
- Using satellites (no possibility of movement in their nodes)
- Data rates are very high, but the latency time are in in the order of dozens of seconds
- Great power consumption

Application: Satellite

Type of satellite service
- Geo-stationary satellite service (GSO): equal to earth's rotational period, located in 35.786 km above Earth's equator.
	- Permanent use of one satellite
	- Reachable in one specific geographic area

- Non geo-stationary satellite service (NGO): located between 700km - 1.500 km from the Earth.
	- Connections to non-stationary satellites
	- A receptor will be available in the satellite's coverage area sooner or later.
	- For this reason, a receptor must be used to deal with automatic connections and disconnections.

![](attachments/Pasted%20image%2020220405220234.png)

## Macro-Cellular
- Radio coverage reach dozens of kilometers
- Used to communicate between different cities, with low or medium traffic density.
- These networks are employed by cellular telephone systems
- Mobile nodes can migrate between fixed stations
- Can take speeds up to 250 Km/h
- Data rates are medium (up to 2Mbps with mobiles of 2.5 or 3G) or GSM

Application: GSM, GPRS, EDGE, UMTS, HSPA, LTE, 5G


## Micro-Cellular
The area is smaller, but it can build many infrastructure.
- Less expensive infrastructure.
- Can handle more users in specific area.
-  Radio message for less than 10 km.
- High or medium traffic density
- Mobile nodes can have speeds up to 50 km/h

Application: DECT, HIERACC, 802.16


## Pico-Cell
- Small radio coverage (less than 100 meters).
- Establish high speed data links between devices in the same building.
- Substitute of local area network.
- High data rates and limited movement speed (up to 10Km/h).
- Capability of roaming mobile nodes exists.
- High data rates of operation make them unsuitable for devices with small batteries.

Application: 802.11. HiperLAN, HomeRF

- Designed to extend LAN connectivity to laptop computers.
- Medium-high power consumption
- Reduced user mobility

### IEEE 802.11
- Wifi
- Location services
- Data rates from 1 Mbps up to 100 Mbps

### HIPERLAN
- Data rates up to 19 Mbps in centralized or distributed mode

## Personal Area Network
- Connect devices over a small coverage area (less than 10 meters)
- Designed for implementation in low power computing, better operation time than Pico-cell
- Mobility speed limited to 10 km/h

Application: Bluetooth, UWB

### Ultra Wide Band (UWB)
- Better signal error resistance
- Low cost transmitters and receptors
- Very high data rates (20 to 350 Mbps)

Cons:
- Low power transmission
- Very small coverage (less than 10m)

### Bluetooth
- Implementation in the same processor with very low additional cost
- Low power consumption

Evolution
- 1.2 : adaptive frequency hopping to avoud using busy frequencies, extended synchronous connections with packet retransmissions.
- 2.0: compatibility with v1.2, enhanced data rate up to 3.0 Mbps
- 2.1: security improvements
- 3.0: enhanced data rates up to 24 Mbps, based on an 802.11 link, video streaming available.

Bluetooth Low Energy (BLE)
- Industry standard for interoperability across platforms
- Ultra-low peak, average and idle mode power consumption
- Standardized application development eases development and deployment time and cost

## Wireless Sensor Networks
- Designed to connect low cost devices (i.e. physical magnitude sensors) spread over an extended area.
- Data rates up to 250 kbps
- Radio coverage are very small (up to 10 m, there also WSN with coverage up to 100m).
- Nodes are very resistant to disconnection
- Mobility speed is limited (up to 10 km/h)
- These networks can perform a very long operation time with ultra low power consumption
- Trends among researcher

Application: 802.15.4, Zigbee, nanoNet

### Zigbee
- Low rate
- Low power

![](attachments/Pasted%20image%2020220405222533.png)

802.15.4 defines the operation of low-rate wireless personal area network (LR-WPAN)

### nanoNET
- Technology for loss protection of animal and people
- Uses standard 802.15.4a (chirp spread spectrum) to achieve maximum range without loss
- Typical devices for this technology are location tags (mobile), anchor nodes (fixed), location gateways, and location server.

## Middleware
- Used to solve the complexity and heterogeneity of distributed systems.
- Placed between applications and the operating system

![](attachments/Pasted%20image%2020220405223108.png)

### Classes of Middleware
- Distributed tuples: offers abstraction for distributed tuples. i.e. L2IMBO, LINDA
- Remote Procedure Call: abstraction of external procedure invocation: Java Remote Method Invocation, Modula-3, XML-RPC, .NET Remoting
- Message-Oriented Middleware: message queue abstraction for messages between distributed applications. i.e. Advanced Message Queuing protocol, Java Message Service.
- Object Request Broker: remote object management abstraction allows using remote objects as if they were in the user's own space. I.e. DCOM, CORBA, COM.

### Challenges in Middleware
- All those types middleware are for large system with powerful computer.
- No network heterogeneity was considered
- Need network that is permanent, high speed, and reliable

Heterogeneity:
- Devices
- Networks
- Operating systems

## Middleware: Home Audio Video Interoperability (HAVi)
- Seamless interoperability among home entertainment products
- Allows registration of new devices as they add to the network
- Have some standard APIs to be used by other devices
- Operating system neutral middleware
	- Multi-directional AV streams
	- Event schedule
	- Registries
- Take advantage of chips built into modern audio and video appliacnes
- IEEE 1394 (i. LINK or FireWire) as the interconnection medium


![](attachments/Pasted%20image%2020220405224440.png)

Message system is responsible for passing messages between all HAVi software components.

Registry serves as a location directory service that allows other software, elements on the network to be found.

Event manager is responsible for sending status messages between software elements or sending HAVi network configuration messages.

Resource manager abstracts shared resources such as DCM or Device Control Modules, which are the central point of HAVi

### Classes of HAVi Devices
![](attachments/Pasted%20image%2020220405225610.png)

**Full AV**
- contains a complete HAVi architecture
- Run JAVA BYTE-code, can upload and execute
- Java bytecode from other devices, providing extended control capabilities to this kind of device
- Example: residential gateway controlling all devices at home

**Intermediate AV**
- Don't provide Java bytecode execution
- Cannot be controllers for any kind of devices but can control specific devices

**Base AV**
Only have DCM (Digital Control Module) in their memory that can export its code to other devices for being controlled through an AV controlling protocol.

**Legacy AV**
Don't implement HAVi architecture, and use proprietary protocols to control functionality


## Middleware: JINI
- Heavy dependent on Java.
- There is a look-up service acts as middleware

![](attachments/Pasted%20image%2020220405230541.png)

Running continuously to allow device discovery services, register devices, and give operation licences to their connected devices.

Registered in serveral look-up services that store information about device functionality, a Java bytecode needed to interact with the device and a set of properties and methods.

Devices are controlled using RMI (Remote Method Invocation)

## Middleware: Universal Plug and Play
- Dynamic connection of a device to a network, service offering and discovery, everything based on a unified description of functions and attributes of services through XML.
- Enable networked devices: PC, printers, Gateways, WiFi Access Points, and mobile devices to seamlessly discover each other's presence on the network.
- There are two factors that make UPnP especially attractive:
	- Using IP protocols at the lowest level.
	- Using open and standard protocols.

**Open Standard**
- Using HTTP protocols (asynchronous communciatiion)
- Can use HTTPU (HTTP using UDP) to be simpler and non-connection oriented. This is adequate solution for asynchronous communication in pervasive systems.

**First Phase**: Addressing
1. All UPnP devices incorporate a DHCP client to obtain an IP address.
2. If there is no answer from a DHCP server, it chooses an address and checks it wasn't used through ARP.
3. If the device has an IP address, it can proceed with discovery functions and service controls. This can be done by using protocol named SSDP (Simple Service Discovery Protocol)

![](attachments/Pasted%20image%2020220405231415.png)

**Control Point**
- Retrieve device description and get a list of associated services
- Retrieve service description for interesting services.
- Invoke actions to control the service
- Subscribe to the service's event source. Anytime the state of the service changes, the event server will send an event to the control point.

## Middleware: Universal Remote Console Control Protocol (URCC)
- Focused on the control of household appliances
- Device capable of talking with all kind of devices that implement URCC
- Components
	- Controller
	- Target device
	- Network to communicata

- URC was focused initially on IRDa but it can now use any other RF or wired network technology
- URCC has a provision for implementing natural language user interfaces and also multilingual interaction.


## Middleware: Open Services Gateway Specification (OSGi)
- Provides a common structure at application level that is independent of the middleware technology used.
- Allows the use of different technologies, i.e. Jini, UPnP because heterogeneity at middleware level.
- Developed in Java or C

![](attachments/Pasted%20image%2020220405232606.png)