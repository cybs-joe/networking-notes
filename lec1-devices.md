# Lecture 1 — Network Devices

## Client & Server
- **Client**: a device that accesses a service made available by a server
  - *Example: your laptop requesting a webpage from Google*
- **Server**: a device that provides functions or services for clients
  - *Example: Google's web server sending back the webpage to your browser*

> **Note:** The same device can be a client or server in some situations
> *Example: your PC acts as a client when browsing the web, but acts as a server if you're hosting a website on it*

---

## Switches
- Connect end hosts within the same area (LAN)
  - *Example: all PCs, printers, and phones in an office connected to the same switch*
  - *Example: a gaming cafe where all PCs are connected to one switch to play on the same local network*

**Characteristics:**
- 24+ network interfaces/ports for end hosts to connect to
  - *Example: a 24-port switch in a university lab connecting all student PCs*
  - *Example: a small office switch with 48 ports connecting PCs, printers, and IP phones*
- Provide connectivity to hosts within the same LAN
  - *Example: PC-A sends a file to PC-B, both connected to the same switch*
  - *Example: a printer shared between 10 PCs all on the same switch — no router needed*
- Do **not** provide connectivity between LANs or over the internet
  - *Example: PC-A on switch 1 cannot reach PC-B on switch 2 without a router*
  - *Example: two different office floors each have their own switch — they can't communicate until both switches connect to a router*

---

## Routers
- Fewer network interfaces compared to switches
  - *Example: a home router typically has 4 LAN ports vs a switch with 24+*
  - *Example: an enterprise router may have 4-8 ports while the office switch it connects to has 48*
- Provide connectivity **between** LANs
  - *Example: floor 1 and floor 2 of an office each have their own switch — a router connects both floors so they can communicate*
  - *Example: your home network (192.168.1.x) connecting to your neighbor's network would require a router*
- Used to send data over the internet
  - *Example: when you open YouTube, your home router forwards your request from your local network to YouTube's servers across the internet*
  - *Example: your router is what connects your private home network to your ISP's network*

---

## Firewalls
- Monitor and control network traffic based on configured rules
  - *Example: a firewall blocking all incoming traffic on port 23 (Telnet) to prevent unencrypted remote access*
  - *Example: a company firewall allowing only port 443 (HTTPS) traffic from outside*
- Can be placed inside or outside the network
  - *Example: placed outside — filters traffic before it even enters the network*
  - *Example: placed inside — sits between departments so the HR network can't access the engineering network*
- **Next-gen firewalls**: include more modern advanced filtering capabilities
  - *Example: instead of just blocking ports, it can identify and block specific apps like BitTorrent even if they use normal ports*
  - *Example: can detect malware patterns in traffic, not just block by IP or port*

> **Host-based firewalls**: software that filters traffic entering or exiting a host machine
> - *Example: Windows Defender Firewall on your PC blocking an app from accessing the internet*
> - *Example: iptables on your Arch Linux machine controlling which ports accept incoming connections*
