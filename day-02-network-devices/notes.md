# CCNA Day 2 – Interfaces and Cables

## Objective
Learn about network interfaces, Ethernet ports, console connections, cable types, and when each cable is used.

---

# What is a Network Interface?

A **network interface** is the connection point through which a device sends and receives data on a network.

Examples:
- Ethernet port
- Console port
- Serial port
- Fiber port

---

# Interface Naming in Cisco Devices

Cisco names interfaces using:

`InterfaceType Slot/Port`

Examples:
- `FastEthernet0/1`
- `GigabitEthernet0/0`
- `GigabitEthernet0/1`

### Meaning of Slot and Port

- **Slot** = Module location in the device.
- **Port** = Physical connector on that module.

Example:
- `Fa0/1` → Slot 0, Port 1
- `Gi0/2` → Slot 0, Port 2

---

# FastEthernet vs GigabitEthernet

| Interface | Speed |
|-----------|-------|
| FastEthernet (Fa) | 100 Mbps |
| GigabitEthernet (Gi) | 1000 Mbps (1 Gbps) |
| TenGigabitEthernet | 10 Gbps |

---

# Console Port

The **Console Port** is used to configure a Cisco device directly.

- Does not carry normal network traffic.
- Uses a **Console (Rollover) Cable**.
- Connects a PC to a router or switch for CLI access.

---

# Ethernet Ports

Ethernet ports are used for normal network communication.

Devices connected:
- PC
- Switch
- Router
- Server

---

# Cable Types

## 1. Console (Rollover) Cable

**Purpose:** Device configuration.

Connection:
- PC ↔ Router/Switch Console Port

Color in Packet Tracer:
- Light Blue

---

## 2. Copper Straight-Through Cable

Used for connecting **different types of devices**.

Examples:
- PC → Switch
- Switch → Router
- Router → PC

Most common Ethernet cable.

---

## 3. Copper Cross-Over Cable

Used for connecting **similar devices**.

Examples:
- Switch → Switch
- Router → Router
- PC → PC

Modern devices often use **Auto-MDIX**, so straight-through cables usually work as well.

---

## 4. Fiber Optic Cable

Used for:
- High-speed communication
- Long-distance connections

Advantages:
- Faster
- Less interference
- Longer range

---

# Serial Cable

Used mainly in WAN connections between routers.

- DCE side provides clocking.
- DTE side receives clocking.

---

# Auto-MDIX

**Auto-MDIX** automatically detects whether a straight-through or cross-over connection is needed.

Benefit:
- No need to manually choose cable type on most modern Cisco devices.

---

# Interface Status

Common interface states:

| Status | Meaning |
|---------|---------|
| Up/Up | Interface is working |
| Administratively Down | Disabled with `shutdown` |
| Down | Physical connection problem |

Enable an interface:

```text
Router(config)# interface g0/0
Router(config-if)# no shutdown
```

---

# Packet Tracer Cable Selection

When clicking a switch after selecting a cable:

- **Console** → For CLI configuration.
- **FastEthernet/GigabitEthernet ports** → For normal network connections.

---

# Quick Revision

- **Interface** = Connection point on a network device.
- `Fa0/1` means **Slot 0, Port 1**.
- **Console cable** is used for configuration.
- **Straight-through** connects different devices.
- **Cross-over** connects similar devices.
- **Fiber** is used for high-speed, long-distance links.
- **Auto-MDIX** automatically detects cable requirements.
- Use `no shutdown` to enable an interface.