# TCP/IP Model

## Introduction

The **TCP/IP (Transmission Control Protocol/Internet Protocol) Model** is the standard networking model used for communication over the Internet and most modern computer networks.

Unlike the OSI Model, which is mainly a reference model for learning and understanding networking concepts, the TCP/IP Model is a practical model that is implemented in real-world networks.

Every time you browse a website, send an email, watch a video, or use an online application, your data travels using the TCP/IP protocol suite.

---

# What is TCP/IP?

TCP/IP stands for:

- **TCP** – Transmission Control Protocol
- **IP** – Internet Protocol

These two protocols work together to ensure reliable communication between devices connected to a network.

Although the model is named after TCP and IP, it actually consists of many protocols working together.

Some examples include:

- HTTP
- HTTPS
- DNS
- FTP
- SSH
- DHCP
- TCP
- UDP
- IPv4
- IPv6
- ICMP

---


# Why Was the TCP/IP Model Developed?

The model was developed to solve several communication challenges.

### Main objectives

- Allow communication between different types of computers
- Support large-scale networks
- Provide reliable communication
- Handle packet routing efficiently
- Ensure interoperability between different vendors

---

# Advantages of the TCP/IP Model

- Open standard
- Scalable
- Reliable
- Platform independent
- Supports routing
- Used worldwide
- Easily expandable

---

# Layers of the TCP/IP Model

The TCP/IP Model consists of **four layers**.

```text
+------------------------------+
| 4. Application Layer         |
+------------------------------+
| 3. Transport Layer           |
+------------------------------+
| 2. Internet Layer            |
+------------------------------+
| 1. Network Access Layer      |
+------------------------------+
```

Unlike the OSI Model, the TCP/IP Model combines several responsibilities into fewer layers.

---

# Layer 4 – Application Layer

The Application Layer provides services directly to user applications.

This layer combines the responsibilities of the following OSI layers:

- Application
- Presentation
- Session

### Functions

- Network communication for applications
- Data formatting
- Authentication
- Encryption support
- File transfer
- Email services
- Name resolution

### Common Protocols

- HTTP
- HTTPS
- FTP
- SSH
- DNS
- SMTP
- IMAP
- POP3
- DHCP

### Example

When you open:

```
https://github.com
```

your browser communicates with GitHub using protocols from the Application Layer.

---

# Layer 3 – Transport Layer

The Transport Layer provides communication between two hosts.

Its primary responsibility is reliable data delivery.

### Functions

- End-to-end communication
- Segmentation
- Flow control
- Error detection
- Error recovery
- Port addressing

### Protocols

## TCP

Features:

- Reliable
- Connection-oriented
- Error checking
- Packet sequencing
- Retransmission

Common uses:

- HTTPS
- SSH
- FTP
- Email

---

## UDP

Features:

- Fast
- Connectionless
- No retransmission
- Low latency

Common uses:

- DNS
- Online gaming
- Live streaming
- VoIP

---

# Layer 2 – Internet Layer

The Internet Layer is responsible for delivering packets between networks.

Its primary task is routing.

### Functions

- Logical addressing
- Packet forwarding
- Routing
- Fragmentation

### Common Protocols

- IPv4
- IPv6
- ICMP
- ARP

### Device

Router

### Example

Your laptop sends a request to a server in another country.

Routers forward packets across multiple networks until they reach the destination.

---

# Layer 1 – Network Access Layer

This layer is responsible for transmitting data over the physical network.

It combines the responsibilities of the OSI:

- Data Link Layer
- Physical Layer

### Functions

- Framing
- MAC Addressing
- Error Detection
- Physical Transmission
- Media Access

### Common Technologies

- Ethernet
- Wi-Fi
- Fiber Optics
- Bluetooth

### Devices

- Switch
- Hub
- Bridge
- NIC

---

# Data Flow Through the TCP/IP Model

```text
User

↓

Application Layer

↓

Transport Layer

↓

Internet Layer

↓

Network Access Layer

↓

Physical Network

↓

Destination Device
```

The receiving device processes the data in reverse order.

---

# Protocol Data Units (PDU)

| Layer | PDU |
|---------|------|
| Application | Data |
| Transport | Segment / Datagram |
| Internet | Packet |
| Network Access | Frame / Bits |

---

# Addressing Used

Different layers use different types of addresses.

| Layer | Address Type |
|---------|-------------|
| Transport | Port Number |
| Internet | IP Address |
| Network Access | MAC Address |

---

# Encapsulation

As data moves downward, each layer adds its own header.

```text
Application

↓

Data

↓

Transport

↓

Segment

↓

Internet

↓

Packet

↓

Network Access

↓

Frame

↓

Bits
```

---

# Decapsulation

The receiving computer removes these headers in reverse order until the original data reaches the application.

---

# OSI Model vs TCP/IP Model

| OSI Model | TCP/IP Model |
|------------|--------------|
| 7 Layers | 4 Layers |
| Reference Model | Practical Model |
| Developed by ISO | Developed by DoD |
| Mainly for learning | Used on the Internet |
| Protocol independent | Based on TCP/IP protocols |

---

# Relationship Between OSI and TCP/IP

```text
OSI Model                  TCP/IP Model

Application  ┐
Presentation ├────────► Application
Session      ┘

Transport ───────────► Transport

Network ─────────────► Internet

Data Link ┐
Physical  ┘──────────► Network Access
```

---

# Real-World Example

Suppose you open:

```
https://github.com
```

The communication follows this order:

1. Browser creates an HTTPS request.
2. TCP divides the data into segments.
3. IP adds source and destination addresses.
4. Ethernet or Wi-Fi transmits the frame.
5. Routers forward packets.
6. GitHub's server receives the request.
7. The response follows the same path back to your browser.

---

# Summary

The TCP/IP Model is the foundation of modern networking and the Internet. It provides a practical framework for communication using four layers: Application, Transport, Internet, and Network Access.

Each layer has a specific role, from interacting with user applications to routing packets and transmitting data across physical media. Understanding the TCP/IP Model is essential because nearly all modern networks, including the Internet, are built on this architecture.

---
