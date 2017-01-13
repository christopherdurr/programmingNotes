# Computer Networking

## Chapter 1: Computer Networks and The Internet

## 1.1

Devices hooked up to the internet are called **hosts** or **end systems**. 

These end systems are connected by **communication links** and **packet switches**

**Transmission Rate**: How fast a system can transmit data in bits/second

**Packet Switch**: takes a packet arriving on one of its incoming communication
links and forwards that packet on one of its outgoing communication links. 

Two types of packet switches:

* Routers: Used in network core
* Link-Layer switches: Used in access networks 

**Route/Path**: The sequence of communication links and packet switches traversed by a packet from
the sending end system to the receiving end system

**Internet Service Provider**: How end systems access the internet

**Protocol**: Controls the sending and receiving of information within the internet

* **Transmission Control Protocol(TCP)**:
* **Internet Protocol(IP)**: Specifies the format of the packets that are sent and received. **TCP/IP**

**Internet Standards**: Created by the IETF (Internet Engineering Task Force). Standard documents are called requests for comments (**RFC**)

**Application Programming Interface (API)**: Specifies how a program running on one end system asks
the Internet infrastructure to deliver data to a specific destination program running on another end system. 

**Network Protocol**: Defines the format and the order of messages exchanged between
two or more communicating entities

## 1.2

Host

* **Client**: Desktops and Mobile PCs
* **Server**: Store and distribute webpages, stream video, relay email etc. 

Many servers reside in **Data Centers**, each having more than thousands of servers

Access Network: Network that connects and end system to the first router ("edge router")

If downstream and upstream rates are different, access is "asymmetric"

**Cable Internet Access**: Uses cable television existing infrastructure

Cable internet access requires cable modems, which is an external device, connecting to the home PC through an ethernet port. If multiple people download/upload at the same time, the upstream and downstream rate will be lower than normal. 

**Fiber To The Home (FTTH)**: Provide an optical fiber path from the CO directly to the home. 

Two optical distribution Network Architectures

1. Active Optical Networks (AON): Switched Ethernet
2. Passive Optical Networks (PON): Verizon's FIOS Service

PON Explained

Each home has an Optical Network Terminator (ONT) which is connected to a neighborhood splitter. 

The splitter combines the homes onto a single optical fiber, which connects to an Optical Line Terminator (OLT) in the CO. A home router connects to the ONT. 

Local Area Networks (LAN) are used in university and corporate settings. Ethernet is the most prevalent LAN. End system users connect to the Ethernet Switch, which then connects to the larger internet

Wireless LAN (WiFi)

3G: Provides Packet-switched WAN speeds of 1Mbps. 

**Physical Medium**: What bits are sent across. 

Two types of Physical Mediums:

1. **Guided Media**: Data travels on a solid medium, such as a fiber-optic cable or a coaxial cable
2. **Unguided Media**: Data travels in the atmosphere and in outer space, such as wireless LAN or a digital satellite channel

* **Unshielded Twisted Pair (UTP)**: Most common guided transmission medium. Used for LAN. 
* **Coaxial Cable**: Used in cable TV systems. It is a **Shared Medium**, a medium that serves more than one user at a time. 
* **Fiber Optics**: Can support tremendous bit rates. 
* Terrestrial Radio Channel: Require no physical wires to be installed, can penetrate walls, and can carry a signal over long distances 
* Satellite Radio Channel
*   **Geostationary Satellite**: Reamin above the same spot on the earth
*   **Low-earth Orbiting (LEO) Satellite**: Don't permanently remain above one spot. They rotate around the earth. 

## 1.3

Packet Switches use **store-and-forward** transmission. This means they must receive the entire packet before it can begin to transmit the data on the outbound link. This is what causes "buffering"

At L/R seconds,the entire packet has been transmitted. Total delay is 2L/R. 

N(L/R)

**Output Buffer/Output Queue**: Stores packets that the router is about to send into that link. 

Packets suffer **queueing delays**, which are variable and depend on level of congestion in network. 

Every router has a **Forwarding Table** that maps destination addresses to the router's outbound links. Routers have **routing protocols** that are used to automatically set the forwarding tables. 

How data moves through a network of links and switches:

1. **Circuit Switching**: The resources needed along a path are reserved for the duration of the communication between end systems
2. **Packet Switching**: Resources are not reserved, and we have to wait for access to a communication link

For circuit switching, when two hosts want to communicate the network establishes an **end-to-end connection** between two hosts. 

Circuits are implemented by:
* **Frequency-Division Multiplexing (FDM)**: The link dedicates a frequency band for each connection. The width of the band is called *bandwidth*
* **Time-division multiplexing (TDM)**: Time is divided into fixed durations

The problem with circuit switching is that it is wasteful because dedicated circuits are idle during **silent periods**


