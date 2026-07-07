# Networks

## Introduction

A **computer network** is a collection of two or more devices connected together to share data, resources, and services. These devices communicate using communication media and networking protocols.

Examples of connected devices include:

- Computers
- Laptops
- Smartphones
- Servers
- Printers
- Routers
- Switches
- IoT Devices

Networks are the backbone of modern communication, enabling everything from web browsing and cloud services to online banking and video conferencing.

---

# What is a Computer Network?

A computer network is a system in which multiple devices are connected to exchange information and share resources.

Example:

```text
      Internet
          |
      +---------+
      | Router  |
      +---------+
      /    |    \
 Laptop  Phone  Printer
```

All connected devices can communicate with each other.

---

# Why Do We Need Networks?

Networks provide many advantages:

- Share files
- Share printers
- Access the Internet
- Communication (Email, Chat, Video Calls)
- Resource Sharing
- Remote Access
- Cloud Computing

---

# Advantages of Networking

## 1. Resource Sharing

Users can share:

- Printers
- Storage
- Internet
- Applications

---

## 2. File Sharing

Files can be transferred quickly between devices.

Example:

```
Laptop → Shared Folder → Desktop
```

---

## 3. Communication

Networks enable:

- Email
- Video Calls
- Instant Messaging
- Voice Calls

---

## 4. Cost Saving

Organizations reduce costs by sharing hardware and software resources.

---

## 5. Centralized Management

Administrators can manage all devices from one location.

---

# Network Criteria

A good network should satisfy three important criteria.

## 1. Performance

Performance measures how efficiently a network transfers data.

Factors affecting performance:

- Bandwidth
- Number of users
- Hardware
- Transmission medium

---

## 2. Reliability

Reliability refers to how consistently the network operates.

Reliable networks:

- Have minimal downtime
- Recover quickly from failures
- Deliver packets correctly

---

## 3. Security

A secure network protects:

- Confidentiality
- Integrity
- Availability

Security measures include:

- Firewalls
- Encryption
- Authentication
- Access Control

---

# Physical Structures

Physical structure refers to how devices are physically connected.

---

## Point-to-Point Connection

Only two devices are directly connected.

```text
Computer -------- Printer
```

Advantages:

- Simple
- Fast
- Secure

Disadvantages:

- Limited scalability

---

## Multipoint Connection

Multiple devices share the same communication channel.

```text
Computer
      \
Laptop ---- Switch ---- Server
      /
 Phone
```

Advantages:

- Cost-effective
- Supports many devices

Disadvantages:

- Shared bandwidth

---

# Network Topologies

A topology defines how devices are arranged.

---

## 1. Bus Topology

```text
PC ---- PC ---- PC ---- PC
```

Advantages:

- Easy installation
- Low cost

Disadvantages:

- Backbone failure affects entire network
- Difficult troubleshooting

---

## 2. Star Topology

```text
       Switch
      /  |  \
    PC  PC  PC
```

Advantages:

- Easy management
- Easy troubleshooting
- Most commonly used today

Disadvantages:

- Switch failure affects all devices

---

## 3. Ring Topology

```text
PC ---- PC
|        |
PC ---- PC
```

Advantages:

- Predictable performance

Disadvantages:

- Failure of one device may affect the network

---

## 4. Mesh Topology

```text
A------B
|\    /|
| \  / |
|  \/  |
|  /\  |
| /  \ |
|/    \|
C------D
```

Advantages:

- Highly reliable
- Multiple communication paths

Disadvantages:

- Expensive
- Complex

---

## 5. Tree Topology

```text
        Core
       /    \
   Switch  Switch
   /   \      \
 PC   PC      PC
```

Advantages:

- Scalable
- Organized

Disadvantages:

- Backbone failure affects branches

---

## 6. Hybrid Topology

Combination of two or more topologies.

Example:

Star + Bus

Used in enterprise networks.

---

# Categories of Networks

---

## PAN (Personal Area Network)

Range:

- 1–10 meters

Examples:

- Bluetooth
- Smartwatch
- Wireless Earbuds

---

## LAN (Local Area Network)

Small geographical area.

Examples:

- Home
- Office
- School

Advantages:

- High speed
- Low cost

---

## CAN (Campus Area Network)

Connects multiple LANs within a campus.

Example:

University network.

---

## MAN (Metropolitan Area Network)

Covers a city.

Example:

City-wide ISP network.

---

## WAN (Wide Area Network)

Covers countries or continents.

Example:

The Internet.

---

# Network Models

A network model describes how communication occurs between devices.

---

## OSI Model

Seven Layers:

1. Physical
2. Data Link
3. Network
4. Transport
5. Session
6. Presentation
7. Application

Purpose:

Provides a standard framework for network communication.

---

## TCP/IP Model

Four Layers:

1. Network Access
2. Internet
3. Transport
4. Application

Used by the Internet.

---

# Internetwork

An internetwork is a collection of multiple interconnected networks.

Example:

```
LAN → Router → Internet → Router → LAN
```

Routers connect different networks.

---

# Common Network Devices

## Hub

- Broadcasts data to every device.
- Works at the Physical Layer.

---

## Switch

- Sends data only to the intended device.
- Works at the Data Link Layer.

---

## Router

- Connects different networks.
- Routes packets.
- Works at the Network Layer.

---

## Access Point

Provides wireless connectivity.

---

## Firewall

Monitors and filters network traffic.

Can allow or block packets based on security rules.

---

# Real-World Example

Suppose you access:

```
https://google.com
```

Flow:

```
Laptop

↓

Wi-Fi

↓

Router

↓

ISP

↓

Internet

↓

Google Server

↓

Response

↓

Laptop
```

---


# Summary

- A computer network connects devices for communication and resource sharing.
- Networks improve collaboration, communication, and efficiency.
- Good networks provide high performance, reliability, and security.
- Common topologies include Bus, Star, Ring, Mesh, Tree, and Hybrid.
- Networks are categorized as PAN, LAN, CAN, MAN, and WAN.
- Routers, switches, hubs, access points, and firewalls play important roles.
- Understanding networking is essential for cybersecurity professionals.

---

