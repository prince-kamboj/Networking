# Network Topologies

## Introduction

A **Network Topology** refers to the physical or logical arrangement of devices (nodes) and the communication links between them in a computer network.

It defines how computers, servers, switches, routers, and other network devices are connected and how data flows through the network.

Choosing the right topology affects:

- Network performance
- Reliability
- Scalability
- Maintenance
- Cost
- Security

Network topology is one of the fundamental concepts in networking and is commonly discussed in networking interviews and cybersecurity.

---

# What is a Node?

A **Node** is any device connected to a network.

Examples:

- Computer
- Laptop
- Server
- Printer
- Router
- Switch
- Mobile Phone

---

# Types of Network Topologies

There are two main categories of network topology:

## 1. Physical Topology

Physical topology describes the actual physical layout of cables and devices.

Example:

- Ethernet cable connections
- Fiber optic connections
- Switch placement

---

## 2. Logical Topology

Logical topology describes how data moves through the network regardless of the physical layout.

Example:

- Ethernet
- Token Ring

---

# Types of Physical Network Topologies

The most common network topologies are:

1. Bus Topology
2. Star Topology
3. Ring Topology
4. Mesh Topology
5. Tree Topology
6. Hybrid Topology

---

# 1. Bus Topology

In a Bus Topology, all devices are connected to a single communication cable called the **Backbone Cable**.

```
PC ---- PC ---- PC ---- PC
        |
   Backbone Cable
```

Every device shares the same communication medium.

---

## Working

- One device sends data.
- The signal travels along the backbone cable.
- Every device receives the signal.
- Only the intended receiver accepts it.

---

## Advantages

- Easy to install
- Requires less cable
- Low cost
- Suitable for small networks

---

## Disadvantages

- Backbone failure stops the entire network
- Difficult troubleshooting
- Performance decreases as more devices are added
- High collision rate

---

## Real-World Example

Small office networks (older Ethernet networks)

---

# 2. Star Topology

Star Topology is the most commonly used topology today.

All devices connect to a central device, usually a **Switch** or **Hub**.

```
        PC
         |
PC --- Switch --- PC
         |
       Server
         |
      Printer
```

---

## Working

- Data is first sent to the switch.
- The switch forwards the data only to the destination device.

---

## Advantages

- Easy to install
- Easy to troubleshoot
- High performance
- Easy to expand
- Failure of one cable affects only one device

---

## Disadvantages

- Central switch failure stops the network
- More cable required
- Higher installation cost

---

## Real-World Example

- Home Networks
- School Labs
- Offices
- Data Centers

---

# 3. Ring Topology

In Ring Topology, every device connects to exactly two neighboring devices, forming a closed loop.

```
PC ----- PC
|         |
|         |
PC ----- PC
```

---

## Working

Data travels around the ring until it reaches the destination.

Some ring networks use a **Token** to control communication.

---

## Advantages

- No data collisions
- Equal network access
- Predictable performance

---

## Disadvantages

- Failure of one device may affect the network
- Difficult maintenance
- Adding devices can interrupt communication

---

## Example

Older Token Ring Networks

---

# 4. Mesh Topology

Every device connects directly to every other device.

```
A ------- B
|\       /|
| \     / |
|  \   /  |
|   \ /   |
|   / \   |
|  /   \  |
| /     \ |
|/       \|
C ------- D
```

---

## Types

### Full Mesh

Every device connects to every other device.

### Partial Mesh

Only important devices have multiple connections.

---

## Advantages

- Very reliable
- Multiple communication paths
- Excellent fault tolerance
- Highly secure

---

## Disadvantages

- Very expensive
- Large amount of cabling
- Complex installation
- Difficult management

---

## Real-World Example

- Internet Backbone
- Military Networks
- Banking Networks

---

# 5. Tree Topology

Tree Topology combines multiple Star Topologies using a hierarchical structure.

```
           Core Switch
          /          \
      Switch1      Switch2
      /    \        /    \
    PC     PC     PC     PC
```

---

## Advantages

- Easy to expand
- Suitable for large organizations
- Good network management

---

## Disadvantages

- Backbone failure affects multiple networks
- Complex installation
- Higher cost

---

## Real-World Example

- Universities
- Corporate Offices
- Enterprise Networks

---

# 6. Hybrid Topology

Hybrid Topology combines two or more different topologies.

Example:

- Star + Bus
- Star + Ring
- Star + Mesh

```
 Star Network
      |
      |
   Router
      |
 Bus Network
```

---

## Advantages

- Flexible
- Scalable
- Reliable
- High performance

---

## Disadvantages

- Expensive
- Complex design
- Difficult maintenance

---

## Real-World Example

Large companies and cloud service providers often use hybrid topologies.

---

# Comparison Table

| Topology | Cost | Reliability | Performance | Scalability |
|----------|------|-------------|-------------|-------------|
| Bus | Low | Low | Low | Poor |
| Star | Medium | High | High | Excellent |
| Ring | Medium | Medium | Medium | Medium |
| Mesh | Very High | Very High | Excellent | Good |
| Tree | High | High | High | Excellent |
| Hybrid | High | Very High | Excellent | Excellent |

---

# Topology Selection

| Requirement | Best Choice |
|-------------|-------------|
| Home Network | Star |
| Small Office | Star |
| Large Enterprise | Tree |
| Data Center | Mesh |
| Internet Backbone | Mesh |
| University Campus | Tree |
| Cloud Infrastructure | Hybrid |

---

# Summary

Network topology defines how devices are connected and communicate within a network. Different topologies offer different advantages in terms of cost, performance, reliability, scalability, and fault tolerance. Star topology is the most widely used in modern LANs, while Mesh and Hybrid topologies are preferred for high-availability and enterprise environments.

---
