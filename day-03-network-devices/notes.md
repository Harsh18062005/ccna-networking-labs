# Day 3 — TCP/IP Model

## 1. Networking Models

A **networking model** is a framework that divides network communication into different layers.

### Why use layers?

- Makes networking easier to understand
- Helps with troubleshooting
- Provides standardization
- Allows different technologies to work together
- Separates different networking functions

---

# 2. Protocol

A **protocol** is a set of rules that devices follow to communicate with each other.

Examples:

- HTTP
- HTTPS
- DNS
- DHCP
- TCP
- UDP
- IP
- Ethernet
- SSH

---

# 3. OSI Model — Introduction

The **OSI (Open Systems Interconnection) model** is a conceptual/reference model used to understand how network communication works.

It divides networking functions into **7 layers**.

The seven layers are:

1. Application
2. Presentation
3. Session
4. Transport
5. Network
6. Data Link
7. Physical

> Detailed functions of each OSI layer are covered separately in the OSI Model topic.

---

# 4. TCP/IP Model

The **TCP/IP model** is a practical networking model used to describe how devices communicate over networks, including the Internet.

A common 5-layer version consists of:

| Layer | Name |
|---|---|
| 5 | Application |
| 4 | Transport |
| 3 | Internet |
| 2 | Local Network |
| 1 | Physical |

---

# 5. TCP/IP Layers

## Layer 5 — Application

Provides network services used by applications.

Examples:

- HTTP
- HTTPS
- DNS
- DHCP
- FTP
- SSH

---

## Layer 4 — Transport

Provides communication between applications on different devices.

Main protocols:

- TCP
- UDP

Transport layer also uses **port numbers** to identify applications/services.

---

## Layer 3 — Internet

Responsible for communication between different networks.

Main protocol:

- IP

Main functions:

- Logical addressing
- Routing
- Packet forwarding

---

## Layer 2 — Local Network

Responsible for communication over the local network.

Examples:

- Ethernet
- Wi-Fi

Important concepts:

- MAC addresses
- Frames
- Local delivery

---

## Layer 1 — Physical

Responsible for transmitting data as signals over a physical medium.

Examples:

- Copper cables
- Fiber-optic cables
- Wireless signals

---

# 6. TCP/IP Model — Quick View

```text
┌─────────────────────────┐
│  Application            │
├─────────────────────────┤
│  Transport              │
├─────────────────────────┤
│  Internet               │
├─────────────────────────┤
│  Local Network          │
├─────────────────────────┤
│  Physical               │
└─────────────────────────┘
```

---

# 7. Data Encapsulation

When data is sent through a network, information is added at different layers.

The basic flow is:

```text
Data
  ↓
Segment / Datagram
  ↓
Packet
  ↓
Frame
  ↓
Bits
```

This process is called **encapsulation**.

---

# 8. Data Decapsulation

At the receiving device, the process happens in the opposite direction.

```text
Bits
  ↓
Frame
  ↓
Packet
  ↓
Segment / Datagram
  ↓
Data
```

This process is called **decapsulation**.

---

# 9. Protocol Data Units (PDU)

Different layers use different names for the data being transmitted.

| TCP/IP Layer | PDU |
|---|---|
| Application | Data |
| Transport | Segment / Datagram |
| Internet | Packet |
| Local Network | Frame |
| Physical | Bits |

### Remember

```text
TCP       → Segment
UDP       → Datagram
IP        → Packet
Ethernet  → Frame
Physical  → Bits
```

---

# 10. OSI and TCP/IP

The OSI model and TCP/IP model both help us understand network communication using layers.

The OSI model has **7 layers**, while the 5-layer TCP/IP model has **5 layers**.

Basic relationship:

```text
OSI                     TCP/IP

Application ──────┐
Presentation ─────┼──→ Application
Session ──────────┘

Transport ───────────→ Transport

Network ─────────────→ Internet

Data Link ───────────→ Local Network

Physical ────────────→ Physical
```

> The detailed OSI model and its individual layer functions will be covered in the separate OSI lesson.

---

# 11. Key Takeaways

- A networking model divides networking functions into layers.
- A protocol is a set of rules used for communication.
- The OSI model has **7 layers**.
- The TCP/IP model can be represented using **5 layers**.
- TCP/IP layers are:
  - Application
  - Transport
  - Internet
  - Local Network
  - Physical
- Encapsulation happens when data moves down the stack.
- Decapsulation happens when data moves up the stack.
- TCP uses **segments**.
- UDP uses **datagrams**.
- IP uses **packets**.
- Ethernet uses **frames**.
- The Physical layer transmits **bits**.