# Lecture 3 — TCP/IP Model

## Protocols & Standards
- **Protocol**: a set of rules defining how data should be communicated between devices
  - *Example: HTTP defines how your browser requests and receives webpages*
  - *Example: just like how humans agree to speak the same language to communicate, devices agree on protocols*

---

## TCP/IP Layers (5-Layer Model)

| Layer | Name | Protocols | Function | Example |
|---|---|---|---|---|
| 5 | Application | Telnet, FTP, TFTP | Create and interpret data | your browser sending an HTTP request to Google |
| 4 | Transport | TCP, UDP | End-to-end communication using port numbers | TCP ensuring your file download arrives complete and in order |
| 3 | Internet | IPv4, IPv6 | Delivery across networks using IP addresses | your packet being routed from Cairo to a server in the US |
| 2 | Link | Ethernet, WiFi | Hop-to-hop delivery using MAC addresses | your PC sending a frame to your router on your home network |
| 1 | Physical | — | Sends bits as signals | electrical signals traveling through your ethernet cable |

---

## Encapsulation & Decapsulation

> Think of it like sending a letter:
> - You write the letter (data)
> - Put it in an envelope with a name (L4 header)
> - Put that envelope in a box with an address (L3 header)
> - Wrap the box for shipping with tracking info (L2 header + trailer)
> - Hand it to the delivery truck (Physical layer)

### Encapsulation (Sending)

| Step | Layer | What happens | Example |
|---|---|---|---|
| 1 | Application | prepares data | your browser prepares an HTTP request for google.com |
| 2 | Transport | adds L4 header | adds source/destination port numbers (your PC: port 443) |
| 3 | Internet | adds L3 header | adds source/destination IP (your IP → Google's IP) |
| 4 | Link | adds L2 header + trailer | adds MAC addresses and error checking |
| 5 | Physical | transmits bits | sends electrical signals through your ethernet cable |

### Decapsulation (Receiving)

| Step | Layer | What happens | Example |
|---|---|---|---|
| 1 | Physical | receives bits | Google's server receives electrical signals |
| 2 | Link | removes L2 header/trailer | checks for errors, removes MAC info |
| 3 | Internet | removes L3 header | reads destination IP, removes it |
| 4 | Transport | removes L4 header | reads port number, removes it |
| 5 | Application | processes data | Google's web server reads your HTTP request and responds |

---

## Protocol Data Units (PDUs)

| Layer | PDU Name | Contents | Example |
|---|---|---|---|
| Layer 4 | Segment (TCP) / Datagram (UDP) | Data + L4 header | your browser's HTTP request + port numbers |
| Layer 3 | Packet | Segment/Datagram + L3 header | the segment above + source/destination IP addresses |
| Layer 2 | Frame | Packet + L2 header + trailer | the packet above + MAC addresses + error checking |

- **Payload**: the content carried inside each PDU
  - *Example: a frame's payload is the packet inside it*
  - *Example: a packet's payload is the segment or datagram inside it*
  - *Example: think of it like Russian dolls — each layer wraps around the one inside it*

- **Same-layer interaction**: each layer communicates with its peer layer on the other device
  - *Example: the Transport layer on your PC talks directly to the Transport layer on Google's server, even though the data passes through many routers in between*
  - *Example: routers only care about Layer 3 (IP addresses) — they don't look at Layer 4 or above*

---

## OSI Model (7 Layers)

| Layer | Name | Function | Example |
|---|---|---|---|
| 7 | Application | interface between user and network | your browser, email client, FTP |
| 6 | Presentation | data formatting, encryption, compression | SSL/TLS encrypting your HTTPS traffic |
| 5 | Session | managing sessions between devices | keeping your login session alive on a website |
| 4 | Transport | end-to-end communication | TCP ensuring your file arrives complete |
| 3 | Network | routing between networks | IP addresses, routers forwarding packets |
| 2 | Data Link | hop-to-hop delivery on local network | MAC addresses, switches forwarding frames |
| 1 | Physical | transmitting raw bits | cables, signals, wireless radio waves |

> **OSI vs TCP/IP:**
> - OSI has 7 layers, TCP/IP has 5
> - OSI layers 5, 6, 7 are combined into the single Application layer in TCP/IP
> - *Example: when people say "Layer 3 switch" or "Layer 7 firewall" they are referring to OSI layers*
> - *Example: a Layer 7 firewall can inspect HTTP traffic and block specific URLs, while a Layer 3 firewall only works with IP addresses*
