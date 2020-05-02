# Industrial Network Security

> Securing Critical Infrastructure Network for Smart Grid, SCADA, and Other Industrial Control Systems

# 2. About Industrial Networks

## Attacks, Breaches and Incidents: Malware, Exploits and APT's

The focus of this book is how an attack might occur and subsequently how to best protect the Industrial Network and the connected ICS components against undesirable consequences that result from this action.
Did  the action result in some outcome—operational, health, safety or environment—that  must be reported to a federal agency according to some regulatory legislation? 
Did it  originate from another country? 
Was it a simple virus or a persistent root kit? 
Could it be achieved with free tools available on the Internet, or did it require the resources of a state-backed cyber espionage group? 
Do such groups even exist?

## Asset, Critical Asset, Cyber Asset, and Critical Cyber Assets

* *Asset:* Component that is used within an industrial control system. 
    * Often physical (Workstation, server, network switch)
    * Also logical (Process graphic, database, logic program, firewall slue set or firmware)
    * In this book, any component of the network is called an asset

* *CCA:* Critical Cyber Asset: device that uses a Routable protocol within a control center or is dial-up accessible. In version 5 of the standard, this change to take on a more holistic approach, taking into account BES (Bulk Electric Systems)

## Security controls and Security countermeasures

These terms simply refer to methods of enforcing cyber security in order to reduce risk

## Firewalls and IPS's

Basic firewalls may not be able to distinguish between what is a request and what is a response
* *Deep Packet Inspection system *is a device that can decode network traffic and look at the contents or payload of that traffic.
It is typically used by IDS's, IPS's, advanced firewalls and many other systems to detect signs of attacks.
* Industrial Networks support high availability making most general IPS appliances less common on critical networks; IPS is more often applied at upper level networks where high availability (>99.99%) is not such a high priority.

## Industrial Control System

* *An Industrial Control System (ICS)* is a broad class of automation systems used to provide control and monitoring functionality in manufacturing and industrial facilities.
Aggregate of a variety of different system types
    * *Process Control Systems (PCS)*
    * *Distributed Control Systems (DCS)*
    * *Supervisory control and data acquisition (SCADA) systems*
    * *Safety instrumented systems (SIS)*
    * And many others

## DJs or SCADA

Both systems are designed to monitor and to control manufacturing or industrial equipment.

ICS are often referred to in the media as SCADA, which is both inaccurate and misleading.
A SCADA system is a ICS, but not all ICS are SCADA.

## Industrial Networks

The various assets that comprise a ICS are interconnected over an industrial Network.

![Sample network connectivity of an ICS](./Images/SimpleIN.png)

Following Stuxnet, there has been a open source revision of the protocols that where in place. These protocols where found to have critical security bugs, which instigated the critical industry sector to migrate to proprietary protocols, often too cost-prohibitive for researches to procure and analyse.
    
## Networks, Routable Networks, and Nonroutable Networks

A *Nonroutable network* refers to those serial, bus and point-to-point communication links that utilize **Modbus/RTU**, DNP3, fieldbus and other networks.

A *Routable network* typically means a network utilizing the protocol TCP/IP or UDP/IP although other protocols such as AppleTalk, DEVnet and others certainly apply.

In a industrial network, it is common that Routable and Nonroutable networks interconnect or overlap.

All networks and all devices should be considered potentially accessible and vulnerable.


## Enterprise or business networks

> Network of systems that provide the information infrastructure to the business. They can be suppliers that provide the raw material, customers, that receive the finished product.

In the end, the business network and the industrial network interconnect to make up a single end-to-end network

It should be noted that there are several systems and services that exist in both networks, such as directory services, file servers and databases. 
These common services should not be shared, rather replicated, to minimize interconnectivity and reduce potential attack surfaces of both ICS and enterprise infrastructure.

## Zones and enclaves

> Closed group of assets or a functional group of devices, services and applications that make up a larger system. 

* *Zone:* A spatial network that has been created to expose a subset of resources to a larger, untrusted network.

While highly effective, there are times that they become unpractical, because of the complexity of controlling a single device over a network. (Smart grids)

## Network perimeters or electronic security perimeters

* *Perimeter:* The outermost boundary of any closed group of assets (zone) 
    * It is a logical point in which implement cyber security controls.
    * Typically consist of Firewalls, IPS or similar network-based filters

## Critical infrastructure

* *Industrial Networks:* are referred to as any network operating some sort of automated control system that communicates digitally over the network. 
* *Critical Infrastructure:* is referring to the critical *systems and assets* used within a network computing infrastructure.

### Utilities

Water, wastewater, gas, oil, electricity and communications are critical national infrastructures that rely heavily on industrial networks and automated control systems.
They are also clear examples of industrial networks.

### Nuclear facilities

High target for hackers, very secure and protected by law

### Bulk electric

Defined as critical infrastructure under HSPD-7 and highly regulated in North America by NERC.

### Smart Grid

Is a modernization of energy transmission, distribution, and consumption systems.
It will be used as an example in this book, because, as it has become "smart", the devices and components that make up the transmission, distribution, metering, and other components of the grid infrastructure have become sources of digital information, have been given distributed digital communication capability, and have been highly automated.

### Chemical facilities

Unlike the Utility networks, they have to secure their intellectual property as much as they do their control systems and manufacturing operations.

## Common Industrial Security Recommendations

1. Identify what systems need to be protected
1. Separating the systems logically into functional groups
1. Implementing a defense in depth strategy around each system or group
1. Controlling access into and between each group
1. Monitoring activities that occur within and between groups
1. Limiting the actions that can be executed within and between groups

### Identification of critical systems

The first step is determining what needs to be protected. 
Identifying the assets that need to be secured and their overall importance to the reliable operation of the overall Integrated System.
When determining what needs to be protected, we have to map every existing device, and determine if it is a critical asset or not. 
![Diagram to determine critical assets](./Images/DeterminingCriticalAsset.png)

### Network Segmentation / Isolation OS Systems

Segmentation of assets into functional groups allows specific services to be tightly locked down and controlled, and is one of the easiest methods of reducing the attack surface that is exposed to potential threat actors. 

![Functional Groups - Done right](./Images/FuntionalGroups.png)

### Defense in depth

A defense in depth strategy should be implemented.

![Defense in Depth](./Images/DefenseInDepth.png)

### Access Control

Most difficult, but important aspects of cyber security.
Considers 3 very important aspects of how a user interacts with resources.

* Identification
* Authentication
* Authorization

The successful implementation of access control is difficult because of the complexity of managing users and their roles and their mapping to specific devices and services that relate specifically to an employee's operational responsibilities.

![Access Control](./Images/AccessControl.png)

The strengths of Access Control increases as a user's identity is treated with the additional context of that user's roles and responsibilities within a functional group.

## Advanced Industrial Security Recommendations

* *Security Monitoring:* Recognized method of providing situational awareness, Decide what has to be monitored
* *Policy Whitelisting:* A policy white list defines the behaviour that is acceptable. This is important in a ICS architecture, where an industrial protocol is able to exhibit specific behaviours, such as issuing commands, collecting data, or shooting down a system.
* *Application Whitelisting:* Defines the applications and files that are known to be good on a device and prevents any other application from executing.

### Common Miss perceptions About Industrial Network Security

* *Cyber security of industrial networks is not necessary:* There is no longer an air gap separating the ICS from any possible source of digital attack
* *Industrial security is an impossibility:* Even though devices in a ICS may not be patched, there are other measures to grant a intensive security
* *Cyber security is someone else's responsabilitie:* Cyber security is a end-to-end problem that requires a end-to-end solution
* *It is the same as a "regular" cyber security:* Industrial and business networks are different and require different security measures to adequately protect them.


# 3. Industrial Cyber Security History and Trends

Industrial Network systems differ from commercial network systems in that they are expected to operate for months or even years.
This is due to the network's requirements of availability.

## Importance of securing industrial networks

Before, physical security was a priority and there exists locked rooms and zones to prevent unauthorised people to enter the secure location.
Digital security wasn't a priority because the Industrial Network was air-gapped, but as more modern 'real-time' technology advanced, there needed to be a way of accessing air-tight restricted data, so it was broken.

## The evolution of the cyber threat

* *Cyber Threat:* numerous definitions exist, but all have in common

* Unauthorized access to a system
* Loss of confidentiality, integrity or availability of the system, it's data or applications

The initial penetration of industrial systems is getting easter through the evolution and deployment of increasingly complex and sophisticated malware.

The industrial systems at levels 2, 1 and 0 are being increasingly targeted.

The threats continue to evolve, learning from successful techniques from past malware while introducing new capabilities and complexity.

The industrial systems as they stand today simply don't stand a chance against a modern attack capability.
Their primary line of defense remains the business networks that surround them and network-based defenses between each security level of the network.

### Observations about the attacks

* Most attacks seem to be opportunistic
* Initial attacks, simpler exploits; Thwarted or discovered attacks, > sophisticated methods
* majority of cyber attacks -> Financially motivated
* Malware samples increase at an alarming rate
* Majority of attacks originate externally and leverage weak or stolen credentials
* Majority of incidents affecting industrial systems are unintentional
* New malware code samples are increasingly more sophisticated
* Percentage of cyber attacks is high, but has been steadily decreasing
* Auto-run malware has been rising steadily
* Malware and Hacking-as-a-service has become more prevalent
* Remote access incidents have been steadily increasing
* Pretty straightforward:
    * Spear phishing
    * Watering hole
    * Database Injection

## APT's and weaponed malware

> Advanced Persistent Threats

Stuxnet is an example of an APT and Weaponed malware
It replicated itself a number of times, and auto-removed itself from the system if it's host was no the preconfigured target.
It used 0-days to bypass IDS's and used Digital certificates (Stolen) to pretend it is a authorized program.

![Distinctions between Common APT and Weaponed Malware](./Images/APTWeaponizedComparison.png)

### Night Dragon

Discovered by McAfee, this weaponed malware targeted a series of Oil, Energy, and Petrochemical companies. 
The attack started with SQLi and pivoted it's way into internal network. 
They used Command and Control systems, and Remote Administration Toolkits, to recover sensitive information from the companies executives.
The goal of the attack, was to gain sensitive information.
This is a form of cyber-espionage.

### Stuxnet

Game-changer because it was the first targeted, weaponed cyber-attack against an industrial control system.

### Advanced Persistent Threats and Cyber Warfare

Important differences

* Cyber Warfare is higher in sophistication and in consequences, mostly due to available resources of the attacker and the ultimate goal of destruction versus profit.
* In many industrial networks, there is less profit available to a cyber-attacker than from others, and so it requires a different motive for attack (i.e. Socio-political)

### Defending against modern cyber-threat

Advanced Persistent Diligence requires a strong **defense-in-depth** approach, to reduce the available attack surface for a attacker and to provide a broader perspective of threat activity for use in Incident Response, Analysis, Remediation, Restoration and investigation.

Now, traditional security measures are not enough and we have to use new technologies, such as:

* **Next-generation firewalls (NGFW)**
* **Unified Threat Management (UTM)**
* **ICS protocol aware IPS's**

Having situational awareness of what is attempting to connect to the system as well as what is going on within the system is the only way to start to regain control of the network and the system connected to it.

## Insider Threats

> *Insider*: An individual who has approved access, privilege, or knowledge of information systems, information services, and missions.

This definition can be expanded to the unique operational aspect of ICS to include a wide range of individuals:

* Employees with direct access to ICS components for operation
* Employees with highly privileged access for administration and configuration
* Employees with direct access to ICS data
* Subcontractors with access to specific ICS components or subsystems for operation
* Services providers with access to specific ICS components or subsystems for support

Each of these individual can introduce unauthorised data to the system, which is, in turn focused heavily on preventing outside attack

The Repository of Industrial Security Incidents (RISI) showed in 2013 that only 35% of incidents originated from outsiders.
The reason is not a intentional will of causing harm to a system, but a result of unintentional or accidental actions directed on the overall security policies deployed within the architecture.

## Hacktivism, Cyber Crime, Cyber Terrorism, and Cyber War

There are vulnerable industrial systems, and because these systems are vulnerable, anyone willing to perform some research, download some freely available tools, and put forth some effort, can launch an attack. 
With a minimal knowledge of ICS, the likelihood of a successful attack with moderate consequences is significantly increased.
The real question is one of motive and resources.
The average person is not motivated enough, a hacktivist group is.
The average person nay not have the resources to develop a 0-day exploit or execute spear-phishing campaigns, but now, all of these services, are available for hire.
A fully weaponed attack on a critical infrastructure, no longer needs to be military, because it can be mercenary.

# 4. Industrial Control System and Operations

## System Assets

We have to understand the type of devices that are connected to the network:

* Sensors, Actuators, Motor, Drives, Gauges
* Programmable Logic Controllers (PLC)
* Remote Terminal Units (RTU)
* Intelligent Electronic Device
* Human-Machine Interface
* Supervisory Workstation
* Data Historian
* And others

### Programmable Logic Controller

* used to automate functions within manufacturing facilities.
* Typically hardened 
* specialized for a specific use
* Custom OS, with as little overhead as possible
* Typically control real-time processes


![Contents of a typical PLC](./Images/PLC.png)

#### Ladder Diagrams (LD) 

Is a simplistic programming language included with the IEC-61131-3 standard.
Can be thought of as a set of connections between inputs (relay contacts) and outputs (relay coils)
Ladder logic follows a relay function diagram. 
A path is traced from the left hand side, across "rungs" consisting of various inputs. 
If a input relay is true, the path continues.
If the path to the right side completes, the output coil will be set to true.
Every step is tested in each scan

![Example of a OR in a Ladder Diagram](./Images/LadderDiagramOR.png)

### Sequential Function Charts

*Sequential Logic:* Programming language used by PLC's and defined within the IEC-61131-3 standard 

* Sequential Logic Differs from ladder logic in that each step is executed in isolation and progresses to the next step only upon completion.
* Very common in batch-oriented operations
* Can be uploaded the logic by direct serial or ethernet
* PLC's can hold the code and the compiled logic

### Remote Terminal Unit

* Typically reside in a substation, along a pipeline or some other remote location
* Monitor field parameters and transmit the data back to the central monitoring station
* Commonly include a Modem, cellular data connection, radio or other wide area communication technology
* Typically stored in locations with no access to electricity and may be supplied with it by solar panels
* Commonly placed outdoors, subdued to extreme environmental conditions
* RTU's and PLC continue to overlap, to the point that a RCU can be thought of as a remote PLC

### Intelligent Electronic Devices

* Electric Utility Sector's take on RTU's.
* They manage electrical loads and provide local isolation when needed.
* They can also be installed in areas with high voltage and weather, such as a tower.

### Human Machine Interface

* Used as an operator's means to interact with PLC's, RTU's and IED's.
* Replace manually activated switches, dials and controls used to sense and influence the process.
* Come in two predominant form-factors
    * Runs on Modern OS and are capable of performing a variety of functions
    * Combine a Industrial Hardened computer, local touch panel and is packaged to support door on direct panel mounting. Typically use embedded OS and are programmed with a separate computer and associated engineering software.
* Used without password, because in a event of a emergency, using a password is unsafe.

### Supervisory Workstations

* Collects information from assets used within a control system and presents that information for supervisory purposes.
* Is primary read-only
* Change parameters such as alarm limits for a process

### Data Historian

* Specialized software that collects point values, alarm events, batch records, and systems and stores it in a purpose-built database.
* Data histories and stored within a historian is referred to as "tags" and can represent almost anything. ( From airflow in a vent to acceptable loss margins) 

Information used by both industrial operations and business management is often replicated across industrial and business networks. This represents a security risk, as a less secure network, such as a business network can provide access to a more secure zone. 

Properly isolating and securing data historian components that connect with assets in less trusted networks within a semi trusted DMZ significantly help to minimize accessibility.

### Business Information Consoles and Dashboards

Consist of the same data presented to a HMI or data historian system, but physically located elsewhere, such as a executive office. 
The physical display in this case, is controlled using a secure keyboard video mouse switching system (KVM)
It can also be presented, using intermediary steps, to a website inside a company's Intranet, or a excel sheet. Depending on the complexity of the BICAD's

## System Operations

A typical industrial operation consists of  several layers of programmed logic designed to manipulate mechanical controls in  order to automate the operation.
Each specific function is automated by what is com- only referred to as a control loop.
Multiple control loops are typically combined or  stacked together to automate larger processes

### Control Loops

One of the many automated processes that make up a Industrial Controller.
The term loop, derives of the ladder-logic widely used in these systems.
A closed loop is one in which its output, affects its input.
Closed loops provide automated control, open loops, provide manual control.

### Control Processes

General term used to define larger automated processes within an industrial operation.
One control process may be composed of one or more control loops.
Each process is typically managed using a HMI, which is used to interact with the process.

### Feedback loops

Feedback is generally provided directly from the HMI used to control a specific process.

### Production Information Management

Once histories, the information can be further analyzed using tools, such as Statistical Process Control (SPC) / Statistical Quality Control (SQC), either directly from within the data historian or by using an external analysis tool, such as a spreadsheet.
Historical data can be replayed at some point in the future to compare past and present plant operations.

### Business Information Management

Operational monitoring and analysis provides valuable information that can be used by plant management to fine-tune operations, improve efficiencies, minimize costs, and maximize profits.
This drives a need for replication of operational data into the business network.
By placing an HMI outside of the ICS DMZ, any firewalls, IDS/IPS, and other security monitoring devices that are in place need to be configured to allow the communication of the HMI into and out of the ICS DMZ.
This effectively reduces the strength of the security perimeter between the industrial and business networks to user authentication only.

## Process Management

An HMI is used by an operator to obtain real-time information about the state of the process to determine whether manual intervention is required to manage the control process by adjusting an output (open loop) or modifying established set points (closed loop).

## Safety Instrumented Systems

Safety instrumented systems (SIS) are deployed as part of a comprehensive risk management strategy utilizing layers of protection to prevent a manufacturing environment from reaching an unsafe operating condition.
The Basic Process Control System is in charge of maintaining a discrete and continuous control of the process, but I case the process reaches extreme, unstable states, the Safety Instrumented System is deployed. 
This typically manages a automated shutdown of the process.

There are two risks originate within the SIS related to cyber incidents:

* The prevention of the SIS from properly performing its control functions can allow the plant to transition into a dangerous state that could result in catastrophic events.
* The SIS can also be used maliciously to cause unintentional equipment or plant shutdowns

In both cases, the need to isolate the SIS  to the greatest extent is a reasonable approach to improving cyber security resilience.
The systems have to be checked periodically to ensure they work. 
This is a good time to perform security operations such as SW updates and patching.

## The smart grid

The smart grid is complex and highly interconnected. 
It is not the convergence of a few systems, but of many including customer information systems, billing systems or demand response systems.
Most of these systems interconnect and intercommunicate with many others.
The benefits of this allow for intelligent command and control of energy usage, distribution, and billing.
The disadvantage of such a system is that the same end-to-end command and control pathways could be exploited to attack one, any, or all of the connected systems.

## Network Architectures

The ICSs and operations discussed so far are typically limited to specific areas of a larger network design, which at a very high level consist of business networks, production networks, and control networks.  

In reality, industrial networks consist of multiple networks, and they are rarely so easily and neatly organized.

![Functional demarcation of industrial networks](./Images/IN.png)

# 5. Industrial Network Design and Architecture

There are many functions to be served in an industrial network in addition to the control system, along with consideration for many distinct network areas.
The supervisory components that oversee these basic controls systems are interconnected via a network of specialized embedded systems, workstations, and various types of servers.
Many supervisory networks may constitute a larger plant network.
In addition, the business network cannot be forsaken here.
Each area, depending upon it's function, capacity, system vendor, and owner/operator well have it's own topologies, performance considerations, remote access requirements and network services.
These must all be taken into account when considering one of the most important security design considerations.
Network segmentation.

> In ICS, network segmentation is most used in terms of *zone segmentation*.
Zone segmentation refers to the division of industrial systems into grouped subsystems, for the primary purpose of reducing the attack surface of a given system, as well as minimizing attack vectors into and out of that system.
This is accomplished by limiting the unnecessary flow of data between zones.

**A security zone is focused on the grouping of assets based purely on security requirements.**

## Introduction to industrial networking

In an industrial network, the availability of data is often prioritized over data integrity and confidentiality. 
As a result, there is a greater use of UDP protocols and fault-tolerant networks interconnecting endpoints and servers.
Bandwidth and latency are extremely important, as the applications and protocols in use support real-time operations that depend on deterministic communication, often with precise timing requirements.

![Differences in Industrial Network Architecture by form](./Images/DiferencesInINAbyForm.png)

## Common topologies

* **Bus topologies:** Linear, often used to support either serially connected devices, or multiple devices connected to a common bus via taps. Inexpensive, but limited in performance and reliability. Not very widely used.
* **Mesh topologies:** Used for critical devices that require performance and uptime. (Core ethernet switches, routers and servers). Many paths exist to a given point (redundant)
* **Wireless mesh:** Logically similar to wired mesh topologies.
* **Star topologies:** Point-to-multipoint networks. A centralized network resource supports many nodes or devices.
* **Branch/tree topologies:** Hierarchically connected topologies where a single topology (trunk) supports additional topologies (branches)
* **Ring topologies:** Each node connected serially, but the end node is connected to the first also. Normally used to interconnect network access switches
* **Multihoming or Dual-Homing:** Connection of a single node to > 1 networks. 

![Common networks](./Images/CommonNetworks.png)

## Network Segmentation

Originally developed as a means to limit the broadcast domain of an Ethernet network that was designed at that time around 10MB connections typically using either a "hub" (10BaseT) or a shared "trunk" (10Base2) as an access medium.
**Segmentation typically occours at layer 3 (network layer), by a network device providing routing functions (routers, firewalls, switches)** but as networks became larger due to switched Ethernet technology becoming commodities and capabilities of network processing increased providing an alternative method of segmentation.
This relatively new development allowed broadcast to be contained at layer 2 using virtual LANs (VLANs), which utilize a tag in the Ethernet header to establish a VLAN ID (802.1Q). 
VLANs enable compatible Ethernet switches to forward or deny traffic (including broadcasts) based upon either the 802.1Q tag or the port’s VLAN ID (PVID).
To communicate between VLANs, traffic would need to be explicitly routed between VLANs at Layer 3, using a routing device.
Essentially, each VLAN behaved as if it were connected to a dedicated subinterface on the router, only the segmentation occurred at Layer 2, separating the function from the main physical router interface.
This meant that VLANs could segment traffic much more flexibly, and much more cost effectively as it minimized the amount of routers that needed to be deployed.

Today there are Layer 3 switches that combine the benefits of a VLAN switch with the added control of a layer 4 router, making VLANs much easier to implement and maintain.


* *Segmentation:* Division of networks or zones into smaller units. Segmented networks still intercommunicate over a common infrastructure
* *Segregation:* Elimination of communication or data flow in order to completely isolate systems.

Examples of network segmentation:

* Public networks (Internet)
* Business networks
* Operation networks
* Plant control networks
* Supervisory control networks (ICS, engineering workstations, and HMIs)
* Basic/Local control networks (Controllers, PLC's, RTU's, field devices, IED's and subsystems)
* Process networks (Device networks, analyzer networks, equipment monitoring networks and automation systems)
* Safety networks (safety instrumented systems (SIS) and devices)

Depending upon how the network infrastructure is configured, the division of the network can be: Absolute, Conditional, Bidirectional, Unidirectional.


![Types of communication flow](./Images/CommunicationFlow.png)

## Higher layer segmentation

Normally, network segmentation is enforced at layer 2 (VLANs) or 3 (subnets).
The containment of certain network activities can be implemented in any layer of the OSI model.
By limiting sessions and applications at OSI layer 4-7 instead of layers 2-3, it becomes possible to isolate certain communications between fully defined groups of devices, while allowing other communications to operate more freely.

![Types of segmentation 1](./Images/TypesOfSegmentation01.png)

![Types of segmentation 2](./Images/TypesOfSegmentation02.png)

### At what layer should security be implemented?

Risk and vulnerability assessments would help answer the dilemma.

1. Protect areas that represent the greatest risk first

### Relative benefits of various network segmentation methods

![Characteristics of segmentation](./Images/CharacteristicsOfSegmentation.png)

### Physical vs logical segmentation

* *Physical segmentation:* use of two separate physical network devices to perform the isolation between networks
* *Logical segmentation:* Use of logical functions within a single network to achieve the same result

Proper network segmentation is important for both process and control networks that often utilize UDP multicast to communicate between process devices with the least amount of latency.
Layer 2 network segmentation within a common process may be impossible because it would break up the required multicast domain.
Communication between control networks and process networks are handled at a higher tier of the overall architecture using layer 3 switching or routing.

Logical segmentation is only allowed between those segments/zones that require minimal security against cyber-threats. To address this risk:

* Implement defense-in-depth security controls at the demarcation points where networks can be segmented.
* Monitor process network activity

## Network services

When managing multiple networks (Ranging from business to industrial), Domain servers and other identity and access control systems should be maintained separately for the industrial network.

When providing for network network services in industrial systems, abide by the *Principle of least route* which states that in a purpose-built network, a node should only be given the connectivity to perform it's function. (a node must only posses the minimum level of network access that is required for it's individual function)

## Wireless Networks

Any device that is equipped with an appropriate receiver or transmitter and is within the range of an access point can physically receive or transmit wireless signals.

Industrial networks that implement outdoor wireless networks typically conduct thorough radio frequency surveys in order to place antennas in optimized positions and reduce unnecessary exposure to the network. 

In industrial networks, wireless communication is achieved with two implementations:

* *WirelassHART:* Wireless implementation of the HART protocol using IEEE 802.15.4 radio and TDMA communication between nodes
* *OneWireless:* Implementation of ISA 100.11a wireless mesh network based on IEEE 802.11 a/b/g/n standards and is used to transport common industrial protocols such as:
    * Modbus
    * HART
    * OPC
    * General Client Interface (GCI)
    * And other vendor-specific protocols

Both systems support mesh networks and use 2 devices: One for managing connected nodes and communications between nodes, and one to enforce access control and security.

![Wireless HART network](./Images/WirelessHARTNetwork.png)

## Remote access

Necessary evil that must be considered when designing the network. (Incident response and resolution, remote access to engineers for difficult access locations)
All access points should be considered an attack vector and therefore used only when necessary.

Strict security controls should be used:

* *Minimize attack vectors:* Provide one path over which remote access may occur when implementing a remote access solution.
* *Follow the principle of leas privilege:* Users only access systems or devices with which they have specific need or authority
* *segmentation and segregation:* to isolate the systems that allow remote access from other systems not accessed remotely
* *Application control:* to limit remote users to only those applications with which they are authorized.
* *Prevent direct access to critical system:* where the risk outweighs the benefits of remote access. Force remote access through a DMZ or proxy, to enforce further security measures.
* *Remote connection security policy should be >= to the physical connection policy:* Preferred approach is to create a *jump station*, which provides a landing point for the user before he connects to the physical trusted device.
* *Avoid storing credentials on the remote end of the connection:* even if then are transmitted via secure tunnel.
* *Ability to terminate and disconnect remote access mechanisms localy:* in the event of a cyber incident
* *Log everything:* All successful and unsuccessful remote access and activity.

### Performance and considerations

#### Latency and jitter

* *Latency:* The time it takes for a packet to traverse a network from it's source to it's destination host.
* *Jitter:* Variability of latency over time as large amounts of data are transmitted across the network.

#### Bandwidth and throughput

* *Bandwidth:* The total amount of data that can be carried from one point to another in a given period of time. (Typically measured in Mbps or Gbps)
  * Is not usually a concern in IN although it may occur in large flat (layer 2) networks (noisy)
* *Throughput:* volume of data that can flow through a network.
  * The correlation between bandwidth and throughput is dependent on the size of the packet.
  * A device is said to have *line rate* throughput when it can transfer data at the full capability of the network interface.

#### Types of service, class of service, and quality of service

* *Quality of Service (QoS):* the ability to differentiate and prioritize some traffic over other traffic.
* *Type of Service (ToS) and Class of Service (CoS):* provide the mechanisms for identifying the different types of traffic.
    * CoS is identified at a layer 2  using the 802.1p protocol (Provides a field in the header to differentiate)
    * ToS is identified in a layer 3 using the 6-bit ToS field in the IPv4 header.

Both ToS and CoS values are used by QoS mechanisms to shape the overall network traffic.

#### Network hops

Every network device the packet encounters must process the packet.
This adds latency, although most modern network devices are very high performance, and no not add much latency.
Routers and some security devices that operate at layer 4-7 may incur measurable amounts of latency.

#### Network security controls

Introduce latency to a greater degree than network switches and routers.
The deeper the inspection, the greater the imposed latency.

### Safety instrumented systems (SIS)

Consists of many of the same types of devices as a ICS.
Functionally, the SIS is intended to detect a potentially hazardous state of operation, and place the system into a "safe state" before the hazardous state can occur.
Designed for maximum reliability and include redundancy and self-diagnostics to ensure the SIS is fully functional.
This requirement is measured as a statistical value called the *Average Probability of Failure on Demand* (PFD).
This probability is stated as a Safety Integrity Level (SIL) ranging from 1 (PFD of < 10 ^-1)to 4 (PFD of < 10 ^-4)

While SIS cannot protect against cyber attacks directly, they should be able to prevent catastrophe from being caused by a cyber-attack against an industrial process by putting the system into a secure state before the catastrophe can occur.
General advice:

* When implementing a SIS, do so in a way that a malicious actor who successfully compromises control and process zones will not be able to compromise the SIS.
* Comply with the Principle of Least Privilege
* Consider failures and unsafe states when implementing an SIS

### Special considerations

As systems are tuned to specific purposes -such as the advanced metering requirements for the smart grid- specialized networks such as the advanced metering infrastructure (AMI), will evolve to accommodate them.
It is important to give specialized system their due consideration while continuing to apply the fundamental principles of secure network design.

#### Wide area connectivity

Can be provided by private infrastructure or by leased connectivity from public carriers.
These connections should therefore be considered higher risk, and extra measures should be taken to ensure confidentiality, integrity, and availability of a WAN connection.

#### Smart grid network considerations

There is one primary quality that is consistent across any smart grid deployment, and that is the scale and accessibility.
The scale of the smart grid requires the use of some mechanisms to "tier" or hierarchically distribute the nodes.

Scalability also plays a role in the development of smart grid devices, putting significant cost pressure on the end-node devices (smart meters).
Ant device used at such a large scale needs to be as efficient to build, deploy, operate, and maintain as possible.
This business driver is a real concern because of the costs ans complexity of providing security assurances and testing throughput the supply, design, and manufacturing stages of smart meter development.

![Smart Grid Attack Surface](./Images/SGAttackSurface.png)

#### Advanced metering infrastructure

Are used by electric, water and gas utilities.
Highly Distributed, Massively scalable, uses specialized systems and protocols, presents a number of security and privacy considerations, and extremely accessible.

Advanced metering infrastructure architecture consists of smart meters, a communication network, and a AMI server or headend. 

* Smart meter: digital device for real time data collection, a microprocessor and a local memory, and a network interface to connect to the headend.
* Headend: AMI server (Collection of metered data), Meter Data Management System (MDMS) (shares with billing systems, historians). Intercommunicates with many other systems in the smart grid (Transmission and distribution ICS servers, energy management systems (EMS), in home networks and many others).
* The potential for exploitability is big, given the business requirements, low cost, and number of devices. Also it's proprietary protocols.


# 6. Industrial Network Protocols

Industrial Protocols are designed for real-time operation to support precision operations involving deterministic communication of both monitoring and control data.
This means that most industrial protocols forgo any feature (Authentication / encryption) or function that is not absolutely necessary for the sake of efficiency.
Many of these protocols have been modified to run over Ethernet and Internet Protocol (IP) networks as suppliers moved away from proprietary networks.

## Overview of industrial network protocols

> Real-time communications protocols, developed to interconnect the systems, interfaces, and instruments that make up an industrial control system. 

Will be divided into:

* Fieldbus protocols
    * FOUNDATION Fieldbus, CIP, PROFIBUS/PROFINET, P-NET, WorldFIP, INTERBUS, CC-Link, HART, SERCOS
    * Commonly used to connect process-connected devices (e.g. Sensors) to basic control devices (e.g. PLC), and control devices to supervisory systems (e.g. ICS server, HMI, historian)
* Backend protocols
    * Deployed on or above supervisory networks, and are used to provide efficient system-to-system communication as opposed to data access.
    * Commonly used to connect a historian to an ICS server, connecting a ICS from one supplier to another supplier's systems, or connecting two ICS operation control centers.

The most important protocols:

* **Fieldbus**:
    * Modicon Communication Bus (Modbus)
    * Distributed Network Protocol (DNP)
* **Backend**:
    * Open Process Communications (OPC)
    * Inter-Control Center Protocol (ICCP)

Because they represent some unique qualities:

* Each is used in different areas within an industrial network
* Each provides different methods of verifying data integrity and/or security
* The specialized requirements of Industrial Network (Rea-time synchronous communication) often make them highly susceptible to disruption

### Fieldbus Protocols

#### Modicon Communications bus

Designed in 1979 to enable process controllers to communicate with real-time computers, and remains one of the most popular protocols used in ICS architectures.

##### What it does:

Operates at layer 7 of the OSI model.
Extremely simple devices, such as sensors or motors, use Modbus to communicate with more complex computers

##### How it works:

Request/response protocol using 3 distinct protocol data units (PDU):

* Modbus Request 
* Modbus Response
* Modbus Exception Response

![Modbus protocol transaction](./Images/Modbus protocol transaction.png)

Function codes and data requests can be used to perform a wide range of commands:

* Read the value of a single register
* Write the value of a single register
* Read a block of values from a group of registers
* Write a block of values from a group of registers
* Read files
* Write files
* Obtain device diagnostic data

##### Variants:

* Mobdus RTU and Modbus ASCII

> Variants of Modbus made to work in asynchronous serial communications.

> * Modbus RTU: Supports Binary
* ModbusASCII: Supports ASCII (X2 the size of Modbus RTU (Due to Hex encoding vs Binary))

* Modbus TCP: 

> * Modbus TCP: Supports IP

> Come in two forms, the *basic* form takes the original protocol and applies a Modbus Application Protocol (MBAP) to create a new frame. Common with old, legacy HW.
ModbusTCP is the more common and removes the legacy address and error checking and uses only the Modbus PDU with a MBAP header.

* Modbus Plus or Modbus+: 

> Uses token passing mechanisms to send embedded Modbus messages

##### Where is is used:

Typically deployed between PLC's (slave) and HMI's (Master), or between a master PLC and several slave devices.

![Modbus use within a IN](./Images/ModbusUseWithIN.png)

##### Security concerns:

* Lack of authentication - Only require the use of valid Modbus address, function code, and associated data.
* Lack of encryption - Commands and address are transmitted in clear text
* Lack of message checksum (Modbus/TCP only) - Command can easily be spoofed
* Lack of broadcast suppression - All serially connected devices will receive all messages

##### Security recommendations:

* Should be used to communicate within a set of known devices
* Provide access control with filtering capabilities and filter:
    * Modbus TCP packets are the wrong size
    * Function codes that force devices into a "listen only" mode
    * Function codes that restart communications
    * Function codes clear, erase or reset diagnostic information, such as counters and diagnostic registers
    * Function codes that request information about Modbus server
    * Any message with an Exception code PDU
    * Modbus traffic from a server to many slaves
    * Modbus requests for lists of defined ports and their values (Conf scan)
    * Commands to list all available function codes (Conf scan)

#### Distributed network protocol (DNP / DNP3)

Serial protocol designed for use between master stations and slave devices (Outstations).
The primary motivation for this protocol is to provide reliable communication in environments common with the electric utility industry that include high levels of electromagnetic frequency and poor transmission media.
Extended to work over TCP/IP.
Now used by electric, oil, gas, water and wastewater industries.
Unlike Modbus and ICCP, DNP3 is bidirectional (Supporting communications from master to slave and from slave to master) and supports exception-based reporting

##### What it does:

Used to send and receive messages between control system devices.
The link-layer frame ( or LPDU) header and the data payload contain CRC's and the data payload actually contains a pair of CRC octets for every 16 data octets. 
This provides a high degree of assurance that any communication errors will be detected.
It is still possible to loose a packet
Each frame consists of a multi-part header and a data payload.
The frame header contains well-defined function code, which can tell the recipient whether it should confirm, read, write, select a specific point, operate a point, and more.
The data payload of the frame support analog data, binary data, files, counters and other types of data objects.

##### How it works:

DNP3 provides a method to identify the remote device's parameters and then use message buffers corresponding to event data classes 1 - 3 in order to identify incoming messages and compare them to known point data.
In this way the paster station is only required to retrieve new information resulting from a point change or changes event on the outstation.

When a change occurs on an outstation, a flag is set to the appropriate data class.
The master station is then able to poll only those outstations where there is new information to be reported.
This directly results in improved responsiveness and more efficient data exchange.

##### Secure DNP3:

Adds authentication to the response/request process
Authentication occurs using a unique session key that is hashed together with message data from the sender and from the challenger.
The result is an authentication method that verifies authority, integrity, and pairing at the same time.

![DN3 protocol framing](./Images/DN3ProtocolFraming.png)

##### Where is is used:

Between a master control station and a RTU in a remote station.
Transmission medium can include wireless, ratio and dial-up.
Also widely used to interconnect RTU and IED.

![DN3 Use](./Images/DN3Use.png)

##### Security concerns:

No inherent authentication or encryption within DNP3.
Examples of manipulations:

* Turning off unsolicited reporting to suppress alarms
* Spoofing unsolicited responses to the master, to trick the operator into performing inappropriate actions.
* Issuing unauthorised stops, restarts, or other functions that could disrupt operations

##### Security recommendations:

Implement only secure DNP3 or TLS if not possible.
DNP3 stations and outstations should be isolated into a unique zone consisting only of authorized devices and the zones should be thoroughly secured using standard defense-in-depth best practices, including a industrial firewall.
Look for, and decline access with specific function calls and behaviours:

* Use of any non-DNP3 communication on a DNP3 port
* Use of configuration function 23 (Disable unsolicited response)
* Use of control function codes 4, 5 or 6 (Operate, Direct Operate, and Direct Operate without Acknowledgement)
* Use of application control function 18 (Stop Application)
* Multiple unsolicited responses over time (Response storm)
* Any unauthorised attempt to perform an action requiring authentication
* Any Authentication failures

#### Process fieldbus

Most used variant is PROFIBUS DP, which has 3 variants PROFIBUS DP-V{0..2}.
There are also three profiles for PROFIBUS communication: asynchronous, synchronous and over Ethernet (PROFINET).
PROFIBUS is a master-slave protocol that supports multiple master nodes through the use of token sharing (When a master has control of the token, it can communicate with the slaves)
A master PROFIBUS node is typically a PLC or RTU, and a slave is a sensor, motor, or some other control system device.

![PROFIBUS DP communications](./Images/PROFIBUSCommunications.png)

##### Security concerns:

PROFIBUS lacks authentication inherent to many of its functions, allowing a spoofed node to impersonate a master node, which in turn provides control over all configured slaves.
(PROFIBUS DP utilizes DP network, therefore, the attacker has to physically there. This reduces the attack options)

##### Security recommendations:

The network and connected devices are very susceptible of attack if unauthorised physical access is obtained.

### Industrial ethernet protocols

Term used to reference the adaptation of the IEEE 802.3 Ethernet standard to real-time industrial automation applications.
One of the goals was to go from a asynchronous standard to a synchronous one.
Industrial Ethernet also provides physical enhancements to "harden" the office grade nature of standard Ethernet technologies with ruggedized wiring, connectors and hardware designed for industrial use.

![Real-time Ethernet Implementations](./Images/Real-timeEthernetImplementations.png)

#### Ethernet Industrial Protocol:

CIP, also known as Control and Information Protocol, is a publicly available protocol managed through the Open Device Vendors Association (ODVA).
CIP is an application layer protocol that provides a consistent set of messages and services that can be implemented in a variety of ways using different network and link layer techniques, all supporting interoperability.
CIP supports integration of I/O, control, data collection, and device configuration on a single network.

![Overview of CIP](./Images/CIP.png)

EtherNet/IP uses standard Ethernet frames in conjunction with the CIP suite to communicate with nodes.
EIP supports everything CIP implements.

CIP uses object models to define the various qualities of a device.
Each CIP object possesses attributes (data), services (commands), connections, and behaviours (relationships between attributes, values and services)
There are 3 types of objects:

* Required objects

> Define attributes such as device identifiers (Manufacturer, serial number, date of manufacture) (Identity object), routing identifiers, and physical connection data.

* Application objects

> Define input and output profiles for devices

* vendor-specific Objects

> Enable vendors to add proprietary objects to a device

The wide adaptation and standardization of CIP has resulted in an extensive library of device models which can facilitate interoperability, but can also aid in control network scanning and enumeration.

##### Security concerns:

* Susceptible to any of the vulnerabilities of Ethernet.
* The CIP does not define any implicit or explicit mechanisms for security
* Use of common device objects can facilitate device identification and enumeration

##### Security recommendations:

* Real-time ethernet protocol using TCP and UDP transports making it necessary to provide Ethernet and IP-based security at the perimeter of any EIP network.
* Consideration to put EIP devices inside a dedicated zone with packet monitoring.

#### PROFINET:

Designed for scalability.
3 versions.

> 1 - built on top of TCP/IP
2 - RT technology bypasses OSI layers 3 and 4
3 - requires specific hardware, and is a OSI layer 2.

![PROFINET versions](./Images/PROFINET.png)

##### Security concerns:

Real-time Ethernet protocol, therefore is susceptible to any of the vulnerabilities of Ethernet.

##### Security recommendations:

* Lack of authentication protocols requires strong isolation of the bus.
* Careful consideration of the zones and conduits.
* Monitoring of the network: Firewalls, ICS-aware IPS's. 

#### Ether cat:

Real-time Ethernet-based fieldbus protocol classified as "Industrial Ethernet"
Can be used directly in a Ethernet frame or encapsulated as a UDP payload over port 34980.
Only 1-2 Ethernet frames are required for a complete cycle, allowing for very short cycle times. (Meeting IEEE Precision Time Protocol (PTP) requirements without specific HW)

##### Security concerns:

* Susceptible to any vulnerabilities found in standard Ethernet.
* No inherent network-layer mechanism for reliability, ordering, or data integrity checks.
* Susceptible to DoS, and MitM attacks.

##### Security recommendations:

* Provide Ethernet-based security at the perimeter of the network
* Use passive network monitoring
* ICS-aware IPS

#### Ethernet Power link:

* Fast Ethernet as the basis for real-time transmission of control messages via direct encapsulation of ethernet frames.
* Communication is divided into 3 time periods:
    * Transmission of a Master "Start of cycle" frame
    * Slave response if received a poll request frame
    * Asynchronous communication

##### Security concerns:

* Susceptible to any vulnerability of Ethernet communication
* Susceptible to DoS attacks

##### Security recommendations:

* Clear demarcation, based on the cyclic polling mechanism.
* Static Ethernet address tables
* Establish appropriate security zones

#### SERCOS III:

> Serial Real-time Communication System is a standardized open digital interface for communication between industrial controls, motion devices, and I/O devices. 

* Version 3 is a "Industrial Ethernet"-based implementation of the SERCOS interface that supports deterministic real-time control of motion and I/O applications.
* Master - slave protocol that operates cyclically

##### Security concerns:

* Susceptible to any of the vulnerabilities of other forms of Ethernet communication.
* Introduces new security concerns through the option to perform embedded TCP or UDP communications.

##### Security recommendations:

* Deploy static Ethernet-based tables 
* IP channel should be restricted or avoided
* Strong perimeter defenses
* Active monitoring

### Backend Protocols

#### Open Process Communications:

OLE (Object Linking and Embedded) for Process Control is not an Industrial Protocol, but "a series of standard specifications" designed to simplify integrations of various forms of data on the systems from different vendors.
Most embedded systems don't use Microsoft technology, but until the creation of OPC, they had to.
This protocol enhances the communication model, and adds better security.

##### What it does:

Designed to provide a higher level of integration between systems and subsystems, vs a fieldbus, that generally provides low-level data access and configuration.
OPC was motivated by the needs of end "users" and not system "vendors" to provide a common communication interface between diverse ICS components.

##### How it works:

Client-server manner, a client application calls a local process, bot instead of executing the process using local code, the process is executed on a remote server.
The remote process is linked to the client application and is responsible for providing the necessary parameters and functions to the server, utilizing a remote procedure call (RPC)

![OPC protocol operation](./Images/OPC.png)

OPC makes it difficult for Industrial Networks, because it has de ability to change ports.

##### Where is is used:

Commonly used within industrial networks, including data transfers to historians, data connection within HMI's, connectivity between serial fieldbus protocols like Modbus and DNP3 and ICS servers and other supervisory controls.

##### Security concerns:

* Highly vulnerable to attack using multiple vectors as it is subject to the same vulnerabilities as the more ubiquitously used OLE.
* Difficult to upgrade
* RPC vulnerabilities - OPC uses RPC making it susceptible to all RPC-related vulnerabilities
* Unnecessary ports and services
* OPC server integrity - Can create a rogue server and use to disrupt service and DoS.

##### Security recommendations:

* Use OPC-UA when possible
* All unnecessary ports and services should be removed from the OPC server
* OPC servers should be isolated into a unique zone consisting only of authorized devices
* Secure zones with Defense-in-depth practices
* Use Firewalls

#### Inter-control center Communications Protocol (ICCP):

Designed for communication between control centers within the electric utility industry.
Designed for bidirectional Wide Area Network (WAN) communication between a utility control center and other control centers, power plants, substations, and even other utilities.
A common protocol was needed to allow for reliable and standardized data exchange between utility control centers. 
Especially when the control centers are operated by different owners.

##### What it does:

* Establishes a connection
* Accesses information (read requests)
* Information transmission
* Notification of changes / alarms and other exceptional conditions
* Configuration of remote devices
* Control of operating programs

##### How it works:

Client-server model.
One control center is the client and another, the server.
ICCP is a unidirectional protocol, but most implementations, support both functions, allowing a single ICCP device to function as both client and server

##### Where is is used:

* Widely used between control system zones and between distinct control centers.

![ICCP use example](./Images/ICCPUse.png)

##### Security concerns:

Susceptible to spoofing and session hijacking because of:

* Lack of authentication and encryption
* Explicitly defined trust relationships

##### Security improvements over Modbus and DNP:

* Uses bilateral tables. Provides more control
* Secure version of ICCP exists that incorporates digital certificate and encryption

##### Security recommendations:

* Use Secure ICCP variants whenever possible
* Patch known vulnerabilities
* Isolated into a unique zone consisting of only client-server pairs
* Monitor ICCP traffic (Deep packet inspection)

### Advanced Metering Infrastructure and the Smart Grid

The smart grid is a widely distributed communication network that touches power generation and transmission systems, along with many end-user networks.

An example of the protocols in use by a smart-grid:

![Smart grid operational areas and protocols](./Images/Smart-grid.png)

##### Security concerns:

* Smart meters are readily available and therefore require board- and chip-level security in addition to network security.
* Smart grid protocols vary widely in their inherent security and vulnerabilities
* Neighborhood, home, and business LANs can be used to ingress to the AMI

##### Security recommendations:

* Perform risk and threat analysis in the planning stages
* Same for end users (Power plants, factories, homes)
* Strong defense-in-depth and in perimeter will help mitigate the risk

### Industrial Protocol Simulators

##### Modbus:

* Modus Pal 
* Triangle Microworks Communication Protocol Test Harness
* Modsak

##### DNP3/IEC60870-5:

* The Axon Group
* Communication Test Harness, from Triangle Microworks

##### OPC:

* Matrikon
* Kepware

##### ICCP/IEC60870-6:

* Triangle Microworks IEC 6087-6 (TASE.2/ICCP) Test Tool

##### Physical Hardware:

* Not overly expensive, if you want to test, but can't reproduce a entire network, like with simulators
* Purchasing through eBay might help

# 7. Hacking Industrial Control Systems

## Motives and consequences

### Consequences of a successful cyber incident

* Delay, block or alter the intended process: Amount of energy produced
* Delay, block or alter information related to a process: Preventing efficient production metrics
* Unauthorized changes to instructions or alarm thresholds: Damage, disable plant
* Inaccurate information sent to operators: Disguise changes or cause the operator to initiate inappropriate actions

![Potential impact of a successful Cyber-Attack](./Images/7 - impactOfCyberAttack.png)

There are studies that show the successful hacking of a ICS

* *Sandia National Laboratories:* Showed that a simple man-in-the-middle attack can alter values, which can reduce expected output.
* *VIKING:* Investigate whether the manipulation of input data can alter the normal control loop functions, ultimately causing a disturbance.

## Common Industrial Targets

Despite being different, there are several systems that are prone to be targeted:

* *Network Services:* Active directory, Identity and Access management servers. Because they may be shared between business ans ICS networks.
* *Engineering workstations:* Used to exfiltrate or alter process logic.
* *Operator Consoles:* Used to trick human operators into performing unintended task
* *Industrial Applications:* SCADA servers, Historians, asset management
* *Protocols (Modbus, DNP3, EtherNet, etc.):* Used to alter, manipulate, blind or destroy almost any aspect of a ICS

![Attack Targets](./Images/7 - AttackTargets01.png)

![Attack Targets](./Images/7 - AttackTargets02.png)

![Attack Targets](./Images/7 - AttackTargets03.png)

![Attack Targets](./Images/7 - AttackTargets04.png)

![Attack Targets](./Images/7 - AttackTargets05.png)

![Attack Targets](./Images/7 - AttackTargets06.png)

![Attack Targets](./Images/7 - AttackTargets07.png)

![Attack Targets](./Images/7 - AttackTargets08.png)

![Attack Targets](./Images/7 - AttackTargets09.png)

![Attack Targets](./Images/7 - AttackTargets10.png)

![Attack Targets](./Images/7 - AttackTargets11.png)

## Common Attack Methods

Important to know the Difference between compromising, and attacking a target.

* *Compromising:* Ability to exploit a target and perform an *unknown* action
* *Attacking:* Causing the target to perform a *undesirable* action

Many ICS devices can be attacked via the *exploitation of functionality* versus the *exploitation of vulnerabilities*. (Issuing a *Shutdown* command)

### Man-in-the-middle attacks

Very straightforward process if the communication between systems runs on unencrypted protocols.
The biggest challenge to a successful MitM attack is to successfully insert oneself into the message stream, which requires establishing trust.

### Denial-of-service attacks

When a malicious event attempts to make a resource unavailable.
A Well targeted DoS can trigger a shutdown given that the controller enters a state called LoC (Loss of Control) which in turn forces it to enter a safe state: Shutdown.
If the DoS is performed against a HMI, this is called LoV (Loss of View) and can also trigger a shutdown given the operators can not monitor what is happening.

### Replay attacks

It is possible to capture packets and then replay them to accomplish the same action.
If these packets are part of a authentication mechanism, they provide the hacker a authentication mechanism.
Now he can authenticate in the network and be regarded as a trusted peer
This is called: *Exploitation of functionality*

Replay attacks are useful given the command-and-control nature of the ICS.

For the subtle manipulation of industrial systems, knowledge of specific ICS operations is required, but to sabotage a system, almost anything can be used to disrupt operations.

### Compromising the HMI

One of the easiest ways to obtain unauthorised Command and Control of an ICS is to leverage the capabilities of human-machine interface (HMI) console.

A known device vulnerability is exploited to install remote access to the console leading to the host *compromise*. (Use MSf to exploit the target system and install a remote VNC server.

### Compromising the Engineering Workstation (EWS)

Similar to HMI
Important to realise the EWS has important confidential documentation (Design, configuration, plant operation) that make the target a much higher-valued asset than a HMI.

### Blended attacks

A *Blended threat* is an exploit that combines elements of multiple types of malware and usually employs multiple attack vectors to increase the severity of damage and the speed of contagion

Recently blended attacks have increased in complexity (Stuxnet).
They are capable to mutate and adapt to specific situations in a specific environment.

### Examples of weaponized industrial cyber threats

* *Stuxnet:* First, complicated, highly specific
* *Shamoon:* Destructive, wiped systems clean
* *Flame:* More complex derivative of Stuxnet, cyberespionage

#### Stuxnet

The book describes it's abilities and goals

##### Lessons learned

![Lessons Learned - Stuxnet](./Images/7 - Stuxnet.png)

* To defend the ICS, we have to adopt a new "Need to know" mentality.
* If something is not explicitly defined, approved and allowed to execute and/or communicate, it is denied.
* Such high SW complexity and implementation requires above-average monitoring.
    * These measures include Layer 7 application session monitoring to discover zero-day threats and to detect covert communications over allowed "overt" channels.
    * More clearly defined security policies
    * Network whitelisting to control behaviour in and between zones.

#### SHAMOON/DistTrack

Information gatherer and destructive capabilities.
Constructed of 3 parts: Dropper, Wiper and Reporter.


#### Flame/Flamer/Skywiper

APT targeting middle-eastern countries.
Consists of modules:

* *Flame:* AutoRun infection routines
* *Gadget:* Update modules
* *Weasel:* Disk and file parsing
* *Telemetry:* handle C2 routines
* *Suicide:* self-termination
* *Frog:* steal passwords
* *Viper:* Capture screenshots
* *Munch:* capture network traffic

## Attack Trends

Shift from exploiting network layer and protocol layer vulnerabilities to application-specific exploits.
More recent: Shift from OS exploitation to the almost ubiquitously deployed client-side applications like web browsers, Adobe Acrobat Reader, etc.

Web based applications are also used heavily both for infection and for C2.
Employees in ICS use these services and they can't be monitored by the company, due to privacy.
Some companies even allow social media access through corporate firewalls.

### Evolving vulnerabilities: The Adobe exploits

Example of perspective shift, from low-level protocol to high level application.

The exploits use the ability within PDF's to execute code to perform malicious actions.

### Industrial application layer attacks

Adobe reader exploits are highly relevant because many computing products -Including ICS products- distribute manuals and other reference materials using PDF files and preinstall Adobe Reader.
This application remains unpatched, ergo possible vulnerability exploitation.

*Industrial Applications* are the applications and protocols that communicate to, from, and between supervisory, control, and process system components.

These applications are designed to control, either directly or indirectly, and therefore do not need to be infected with malware.
They can simply be used with malicious intent. (*Exploitation of functionality*)
They represent a problem that is not typically addressed through traditional IT security controls.

To mitigate this risk, it is going to be a lot easier and less costly to deploy appropriate security controls versus attempting to retrofit and/or replace the affected ICS equipment.

### Antisocial networks: A new playground for malware

People are subject to social engineering exploitation.
A attack targeting a specific ICS worker that, when opened, downloads and infects his computer is totally plausible.
Users at Pharmaceutical and Chemical sectors are highly probable of web-based malware encounters.
The best way to protect from these attacks is to block social media access within the network.

#### Cannibalistic mutant underground malware

Malware mutation is the ability of malware to auto-update itself. (Stuxnet and it's P2P network is a example of this)

## Dealing with an infection

Upon a infection do not immediately clean the system of infected malware.
There may be subsequent levels of infection that exist, yet dormant and may be activated as a result.

* The first step should be to logically isolate the infected machine from the network.
* Consider the safe and reliable operation of the manufacturing process as the primary objective.
* Always monitor everything
* Analyze available logs to help identify scope, infected hosts, propagation vectors and so on.
    * Retrieve legs from systems that have not been compromised, to perform comparative analysis.
* Sandbox and investigate infected systems.
* Be careful not to unnecessarily power-down infected hosts, as valuable data might be lost.
* Clone disk images for off-line analysis.
* Reverse-engineer detected malware
* Retain all info, for disclosure to authorities

If you have to reinstall OS, the initial copy should have been generated upon the system's arrival, and stored in a remote (off-site) secure location.
