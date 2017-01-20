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

Point of Presence (**POP**): A group of one or more routers (at the same location) in the provider’s network where customer ISPs can connect into the provider ISP

Internet Exchange Point (**IXP**): A meeting point where multiple ISPs can peer together

As a packet travels from host to host, it suffers from several delays:

1. Nodal Processing Delay: The time required to examine a packet's header and determine where to direct the packet
2. Queueing Delay: Happens as a packet waits to be transmitted on a link
3. Transmission Delay: The amount of time required to push (that is, transmit) all of the packet’s bits into the link. 
4. Propagation Delay: The time required to propagate from the beginning of the link to router B. It depends on the physical medium of the link 

Transmission vs. Propagation delays: Transmission delays are a function of the packet's length and the transmission rate of the link. Propagation delays are a function of the distance between two routers

d<sub>nodal</sub> = d<sub>proc</sub> + d<sub>queue</sub> + d<sub>trans</sub> + d<sub>prop</sub>

Design your system so that the traffic intensity is no greater than 1!

When a packet comes and there is a full queue, the router will **drop** the packet and the packet will be **lost**

## 1.5

Each protocol belongs to one of the **layers**. 

The **service** that a layer offers to a layer above is referred to as the **service model** of a layer. 

Layering provides a structured way to discuss system components and makes it easy to update system components. 

Several drawbacks to layer:

* one layer may duplicate lower-layer functionality
* functionality at one layer may need information (e.g. a timestamp value) that is present only in another layer

A **protocol stack** are the protocols of various layers. 

**Message**: Packet of information at the application layer 

**Segment**: Transport layer packet

**Datagrams**: Network-Layer packets

**Frames**: Link-layer packets

The OSI (Open systems interconnection) Model

7 layers of the OSI model:

1. Application Layer
2. Presentation Layer
3. Session Layer
4. Transport Layer
5. Network Layer
6. Data link layer
7. Physical laye

A packet has two types of fields:
* Header fields
* Payload fields: Typically a packet from the layer above

## 1.6

**botnet**: A network of thousands of compromised devices 

A lot of malware is *self-replicating*, where once it infects a host it seeks entry into other hosts 

Virus vs. Worm: Virus requires human interaction while worms can enter devices without explicit user interaction.

**Packet Sniffer**: A packet receiver that records a copy of every packet that flies by. They are difficult to detect because they are passive. 

Injecting a packet with a false source address is known as **IP spoofing**

## Chapter 2: Application Layer

Two main architectural paradigms:

* **Client-server Architecture**: There is an always-on host, called the *server*, which services requests to its *clients*. Also has a fixed, well known address. 
* **P2P Architecture**: Minimal reliance on servers. Direct communication between pairs of hosts

Applications can have hybrid architectures. 

One of the advantages of P2P architecture is its *self-scalability*. 

Several challenges for P2P architecture:

1. Not ISP Friendly
2. Lack of security 
3. Convincing users to volunteer bandwidth to the application

A **process** is a program running in an end system. Processes communicate with each other by sending **messages** across the network. 

For the internet, the browser is the *client process* and the web server is the *server process*

A process sends messages through a **socket**, also referred to as the **application programming interface** between the application and the network. 

There are four possible services that a transport-layer protocol can solve:

1. **Reliable Data Transfer**. If not a big deal, then the application is *loss-tolerant*
2. **Throughput**. *bandwidth-sensitive* applications require throughput. *Elastic* applications can use as much throughput as available
3. **Timing**: Useful for real-time interactive applications. 
4. **Security**: Encrypt all data in the sending process. 

Two available transport protocols are UDP and TCP. 

TCP is a *connection-oriented service*. It also has a congestion-control mechanism. 

UDP is *connectionless*, and there's no guarantee the message will reach the receiving process.  


**HyperTextTransfer Protocol (HTTP)**: The web's application layer protocol. 

**Non-persistent connection**: Each TCP connection is closed after the server sends the object

**Persistent Connection**: Stays on the same TCP connection even after sending object. 

First-line of an HTTP request message is the **request line**. Subsequent fields are the **header lines**.

Response message has 3 sections:
* **Status Line**
* **Six Header Lines**
* **Entity Body**: The meat of the message

List of status codes:

* 200 OK: Request succeeded and the information is returned in the response
* 301 Moved Permanently: Requested object has been permanently moved; the new URL is specified in Location: header of the response message.
* 400 Bad Request: a generic error code indicating that the request could not be understood by the server.
* 404 Not Found: The requested document does not exist on this server
* 505 HTTP Version not supported: The requested HTTP protocol version is not supported by the server

Cookies can be used to identify a user. 

**Web Cache/Proxy Server**: A network entity that satisfies HTTP requests on behalf of an origin Web server. 

A cache is both a server and a client at the same time. It can reduce traffic and costs and improve performance of applications. 

Traffic intensity: (requests/second) x (length of request)/ speed of connection

Hit rates: Fraction of requests satisfied by cache

**Content Distribution Network (CDN)**: Installs geographically distributed caches throughout the internet

**Conditional GET**: Request message uses GET method and request message uses *if-modified-since* header line. 

FTP uses two parallel connections to transfer a file, a **control connection** and a **data connection**

 Because FTP uses a separate control connection, FTP is
said to send its control information **out-of-band**

 HTTP is said to send its control information **in-band**
 
 With FTP, the control connection
remains open throughout the duration of the user session, but a new data connection
is created for each file transferred within a session

The FTP server must associate the control connection with a specific user account,

Commonly used FTP commands:

* USER username: sends user identification to the server
* PASS password: sends password to server
* LIST: List all the files in the current directory
* RETR filename: Get a file (download) from current directory
* STOR filename: Used to store a file (upload) into the current directory 

An internet mail system has three major components: 

* User Agents
* Mail Servers
* Simple Mail Transfer Protocol (SMTP)

SMTP has several restrictions. For example, it restricts the body of an email message to 7-bit ASCII

SMTP can count on the reliable data transfer service of TCP to get the message
to the server without error

HTTP vs SMTP:

HTTP is a **pull protocol** -- Someone loads information on a web server

SMTP is a **push protocol** -- The mail server pushes the file to receiving mail server

There are several popular mail access protocols, including:

* **Post office protocol -- version 3 (POP3)**: Simple protocol, limited functionality. 
* **Internet Mail Access Protocol (IMAP)**: Many more features than POP3. Create and search folders
* HTTP




