Networks(Credits to Jeremy lab & written by cybs-joe)


Client:
its a device that accesses a service made available by a server.

Server:
a device that provides functions or services for clients.

Note: The same device can be a client or server in some situations.

Switches:
end hosts within the same area

characteristics:
1- have many network interfaces/ports for end hosts to connect to(usually 24+)
2- provide connectivity to hosts within the same LAN(local area network)

3- do not provide connectivity between LANs/over the internet
---> to do this we need a router

Routers:
1- Have fewer network interfaces compared to switches
2-They are used to provide connectivity between LANs
3-Used to send data over the internet

Firewalls(Network firewalls):
1-Monitor and control network traffic based on configured rules
2-can be placed inside or outside the network
(general note: known as next gen firewalls when they include more modern advanced filtering capabilities)

---> firewall on computer?
called host-based firewalls which are software applications that filter traffic entering or exiting a host machine (like a pc).

quiz q1) switch --> correct

quiz q2) Server --> correct

quiz q3) client --> correct

quiz q4) Router --> correct

quiz q5)  next gen firewall --> correct


lec 2 :

Cables:


RJ-45 = Registered jack

Ethernet :
collection of network protocols/standards

bit:
value represented by either a 0 or 1

8 bits = 1 byte

speed is measured in bits per second

	1 kilobit (Kb) --> 1,000 bits
	1 megabit (Mb) --> 1,000,000 bits
	1 gigabit (Gb) --> 1,000,000,000 bits
	1 terabit (Tb) --> 1,000,000,000,000 bits


Copper UTP cables --> unshielded twisted pair (Used in ethernet , not all ethernet use the 8 wires)

Full duplex transmission --> receive and send at the same time
using straight-though cable.

This process happens the same when a router is transmitting or receiving from a switch.

When connecting router to router , switch to switch , pc to pc we use 
a crossover cable


## 11. Fiber-Optic Connections

A fiber-optic cable has four layers:

| Layer | Description |
|---|---|
| 1 | Fiberglass core |
| 2 | Cladding that reflects light |
| 3 | Protective buffer |
| 4 | Outer jacket |

![Fiber-optic layers](images/fiber-optic-layers.png)

## Multi-mode vs Single-mode

| Property | Multi-mode | Single-mode |
|---|---|---|
| Core diameter | Wider | Narrower |
| Light entry | Multiple angles | Single angle (laser) |
| Cable length | Longer than UTP, shorter than single-mode | Longest |
| Cost | Cheaper than single-mode | Most expensive |

| Feature | UTP | Fiber-Optic |
|---|---|---|
| Cost | Lower | Higher |
| Max Distance | ~100m | Much longer |
| EMI Vulnerability | Yes | No |
| Ports | RJ45 (cheaper) | SFP (expensive) |


lec3:

TCP/IP Model

Protocol and Standards:

protocol is a set of rules defining how data should be communicated between devices over a network

protocols --> IP/TCP/HTTP and more


layered models --> 5 layers

Application layer --> includes protocols Telnet/FTP/TFTP
Transport Layer --> TCP/UDP
Internet Layer --> IPV4/IPV6
Link layer --> Ethernet/WiFi


Application layer --> Protocols for communication between application processes (Create and interpret the data)

Transport layer --> Provides end-to-end communication between application processes using port numbers

Internet layer --> Provides end-to-end communication between hosts across networks using IP address and routers

local network layer --> Provides hop-to-hop delivery within a local network using MAC addresses and switches

physical layer --> sends bits as electrical , optical , radio signals over the physical medium


How layers combine into a stack:

Encapsulation & decapsulation:

Encapsulation process:

The application layer prepares the data to be sent over the network
then the transport layer encapsulates the the data with its header which includes the info needed for that layer , then the internet layer encapsulates data with its sources and destination addresses
then local network layer encapsulates by adding the trailer that the receiving device uses to check for transmission errors , finally the physical layer transmits the bits as signals over the physical medium.

decapsulation process:

The device receives the message as a stream of bits in the physical layer
the it passes these bits to the next layer local network layer , the device examines the information in local network layer header and trailer and then removes them ,then the internet layer examines and removes the layer 3 header same for transport layer it removes header 4 , and then the data i delivered to the application layer, the application layer processes the data and if needed , generates a response that goes back down the stack

Protocol Data units:

in layer 4 header (Transport layer) the combination of data and l4 header is called segment(TCP) or datagram(UDP)

the combination of a segment/datagram and l3 header (Internet layer) is called a packet

the combination of a segment/datagram and l2 header (Iocal network layer) is called a frame which is what actually sent over the wire

Protocol data unit is name that is used to describe a message at each stage 

A segment or datagram is a layer 4 PDU(L4PDU)

Packet = (L3PDU)

frame = (L2PDU)

content of each PDU is called a payload 

packet's payload is a segment or datagram

frame's payload is a packet

same-layer interaction --> each same layer interact with each other

OSI Model:
1-Physical layer
2-Data link layer
3-Network Layer
4-Transport layer
5-Session layer
6-Presentation layer
7-application layer
