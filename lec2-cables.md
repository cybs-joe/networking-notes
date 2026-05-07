# Lecture 2 — Cables

## Basics
- **RJ-45**: Registered Jack — the connector at the end of an ethernet cable
  - *Example: the connector you plug into your laptop's ethernet port or into a switch*
  - *Example: looks like a wider version of a phone jack*
- **Ethernet**: a collection of network protocols/standards
  - *Example: when you plug a cable into your PC and router, they're communicating using Ethernet standards*
  - *Example: defines how data is formatted and transmitted over a wired LAN*
- **Bit**: value represented by either 0 or 1
  - *Example: the letter "A" in binary is 01000001 — that's 8 bits*
- **8 bits = 1 byte**
  - *Example: a 1MB file = 8 million bits being transferred*
- **Speed measured in bits per second**
  - *Example: a 100 Mbps connection can transfer 100 million bits every second*
  - *Example: downloading a 1GB file on a 100 Mbps connection takes roughly 80 seconds*

| Unit | Value |
|---|---|
| 1 Kilobit (Kb) | 1,000 bits |
| 1 Megabit (Mb) | 1,000,000 bits |
| 1 Gigabit (Gb) | 1,000,000,000 bits |
| 1 Terabit (Tb) | 1,000,000,000,000 bits |

---

## Copper UTP Cables
- **UTP**: Unshielded Twisted Pair
  - *Example: the standard ethernet cable you use to connect your PC to a router at home*
  - *Example: the cables running through walls in offices connecting PCs to wall ports*
- Used in Ethernet (not all Ethernet uses all 8 wires)
  - *Example: older 100 Mbps Ethernet only uses 4 of the 8 wires, while Gigabit uses all 8*
- **Full duplex transmission**: receive and send at the same time using a straight-through cable
  - *Example: you can download a file and upload another simultaneously on the same cable*
  - *Example: a PC connected to a switch using a straight-through cable — both can talk at the same time*
- Connecting same device types → use a **crossover cable**
  - *Example: connecting two PCs directly together to transfer files without a switch*
  - *Example: connecting two switches together to expand the network*
  - *Example: connecting two routers directly together*

---

## Fiber-Optic Connections

A fiber-optic cable has four layers:

| Layer | Description | Example |
|---|---|---|
| 1 | Fiberglass core | the actual path light travels through |
| 2 | Cladding that reflects light | acts like a mirror keeping light inside the core |
| 3 | Protective buffer | absorbs physical shock if cable is bent or stepped on |
| 4 | Outer jacket | the plastic coating you see on the outside of the cable |

### Multi-mode vs Single-mode

| Property | Multi-mode | Single-mode |
|---|---|---|
| Core diameter | Wider | Narrower |
| Light entry | Multiple angles | Single angle (laser) |
| Cable length | Longer than UTP, shorter than single-mode | Longest |
| Cost | Cheaper than single-mode | Most expensive |
| Example | used inside buildings, data centers | used for long distances like city-to-city connections |

### UTP vs Fiber-Optic

| Feature | UTP | Fiber-Optic |
|---|---|---|
| Cost | Lower | Higher |
| Max Distance | ~100m | Much longer |
| EMI Vulnerability | Yes | No |
| Ports | RJ45 (cheaper) | SFP (expensive) |
| Example | office desk connections | connecting buildings or data centers |
