# 🌐 Networking Notes
> Credits to Jeremy's Lab & written by cybs-joe

## Table of Contents

| Lecture | Topic |
|---|---|
| [Lecture 1](lec1-devices.md) | Network Devices — Clients, Servers, Switches, Routers, Firewalls |
| [Lecture 2](lec2-cables.md) | Cables — UTP, Fiber-Optic, Connectors |
| [Lecture 3](lec3-tcpip.md) | TCP/IP Model — Layers, Encapsulation, PDUs, OSI Model |

---

## Lecture 1 — Network Devices

### Client & Server
- **Client**: a device that accesses a service made available by a server
- **Server**: a device that provides functions or services for clients
- > **Note:** The same device can be a client or server in some situations

---

### Switches
- Connect end hosts within the same area (LAN)

**Characteristics:**
- 24+ network interfaces/ports for end hosts to connect to
- Provide connectivity to hosts within the same LAN
- Do **not** provide connectivity between LANs or over the internet → need a router for that

---

### Routers
- Fewer network interfaces compared to switches
- Provide connectivity **between** LANs
- Used to send data over the internet

---

### Firewalls
- Monitor and control network traffic based on configured rules
- Can be placed inside or outside the network
- **Next-gen firewalls**: include more modern advanced filtering capabilities

> **Host-based firewalls**: software applications that filter traffic entering or exiting a host machine (e.g. a PC)

---

### Quiz Results ✅
| Question | Answer |
|---|---|
| Q1 | Switch |
| Q2 | Server |
| Q3 | Client |
| Q4 | Router |
| Q5 | Next-gen Firewall |

---

## Lecture 2 — Cables

### Basics
- **RJ-45**: Registered Jack
- **Ethernet**: collection of network protocols/standards
- **Bit**: value represented by either 0 or 1
- 8 bits = 1 byte
- Speed is measured in **bits per second**

| Unit | Value |
|---|---|
| 1 Kilobit (Kb) | 1,000 bits |
| 1 Megabit (Mb) | 1,000,000 bits |
| 1 Gigabit (Gb) | 1,000,000,000 bits |
| 1 Terabit (Tb) | 1,000,000,000,000 bits |

---

### Copper UTP Cables
- **UTP**: Unshielded Twisted Pair
- Used in Ethernet (not all Ethernet uses all 8 wires)
- **Full duplex transmission**: receive and send at the same time using a straight-through cable
- Same applies when a router transmits/receives from a switch
- Connecting router↔router, switch↔switch, or PC↔PC → use a **crossover cable**

---

### Fiber-Optic Connections

A fiber-optic cable has four layers:

| Layer | Description |
|---|---|
| 1 | Fiberglass core |
| 2 | Cladding that reflects light |
| 3 | Protective buffer |
| 4 | Outer jacket |

#### Multi-mode vs Single-mode

| Property | Multi-mode | Single-mode |
|---|---|---|
| Core diameter | Wider | Narrower |
| Light entry | Multiple angles | Single angle (laser) |
| Cable length | Longer than UTP, shorter than single-mode | Longest |
| Cost | Cheaper than single-mode | Most expensive |

#### UTP vs Fiber-Optic

| Feature | UTP | Fiber-Optic |
|---|---|---|
| Cost | Lower | Higher |
| Max Distance | ~100m | Much longer |
| EMI Vulnerability | Yes | No |
| Ports | RJ45 (cheaper) | SFP (expensive) |

---

## Lecture 3 — TCP/IP Model

### Protocols & Standards
- **Protocol**: a set of rules defining how data should be communicated between devices over a network
- Examples: IP, TCP, HTTP

---

### TCP/IP Layers (5-Layer Model)

| Layer | Name | Protocols | Function |
|---|---|---|---|
| 5 | Application | Telnet, FTP, TFTP | Create and interpret data for applications |
| 4 | Transport | TCP, UDP | End-to-end communication using port numbers |
| 3 | Internet | IPv4, IPv6 | End-to-end delivery across networks using IP addresses |
| 2 | Link (Local Network) | Ethernet, WiFi | Hop-to-hop delivery within LAN using MAC addresses |
| 1 | Physical | — | Sends bits as electrical, optical, or radio signals |

---

### Encapsulation & Decapsulation

#### Encapsulation (Sending)
1. **Application layer** — prepares data
2. **Transport layer** — adds L4 header (port numbers)
3. **Internet layer** — adds L3 header (source/destination IP)
4. **Link layer** — adds L2 header + trailer (MAC addresses, error checking)
5. **Physical layer** — transmits bits as signals

#### Decapsulation (Receiving)
1. **Physical layer** — receives bits
2. **Link layer** — examines and removes L2 header/trailer
3. **Internet layer** — examines and removes L3 header
4. **Transport layer** — examines and removes L4 header
5. **Application layer** — processes the data, generates response if needed

---

### Protocol Data Units (PDUs)

| Layer | PDU Name | Contents |
|---|---|---|
| Layer 4 | Segment (TCP) / Datagram (UDP) | Data + L4 header |
| Layer 3 | Packet | Segment/Datagram + L3 header |
| Layer 2 | Frame | Packet + L2 header + trailer |

- **Payload**: the content inside each PDU
- A packet's payload = segment or datagram
- A frame's payload = packet
- **Same-layer interaction**: each layer communicates with its peer layer on the other device

---

### OSI Model (7 Layers)

| Layer | Name |
|---|---|
| 7 | Application |
| 6 | Presentation |
| 5 | Session |
| 4 | Transport |
| 3 | Network |
| 2 | Data Link |
| 1 | Physical |
