# Protocols and Standards

## Introduction

Communication between computers is only possible when all devices follow the same set of rules. These rules are known as **protocols**, while the organizations that define these rules create **standards**.

Protocols ensure that devices from different manufacturers can communicate reliably and securely over a network.

Examples include:

- Browsing websites
- Sending emails
- Downloading files
- Video conferencing
- Online gaming

Without protocols and standards, modern computer networks and the Internet would not exist.

---

# What is a Protocol?

A **protocol** is a set of rules and procedures that define how data is transmitted, received, and interpreted between devices.

Protocols specify:

- How communication begins
- Data format
- Error handling
- Transmission speed
- Connection termination

### Example

When you visit:

```
https://www.google.com
```

Your browser and Google's server communicate using the **HTTP/HTTPS protocol**.

---

# Why are Protocols Important?

Protocols ensure:

- Reliable communication
- Compatibility between devices
- Error detection
- Data integrity
- Security
- Efficient data transfer

Without protocols:

- Devices could not understand each other.
- Data would be corrupted.
- Networks would become unreliable.

---

# Characteristics of Protocols

Every protocol defines three important characteristics.

## 1. Syntax

Defines the structure and format of data.

Example:

```
Header | Data | Trailer
```

---

## 2. Semantics

Defines the meaning of each field in a message.

Example:

- Source Address
- Destination Address
- Error Information

---

## 3. Timing

Defines:

- When data should be sent
- Data transmission speed
- Synchronization

---

# Types of Protocols

Protocols operate at different layers of the networking stack.

Examples include:

- Application Layer Protocols
- Transport Layer Protocols
- Internet Layer Protocols
- Network Access Layer Protocols

---

# Common Network Protocols

---

# HTTP (HyperText Transfer Protocol)

Used for transferring web pages.

Default Port:

```
80
```

Characteristics:

- Stateless
- Unencrypted
- Fast

Example:

```
http://example.com
```

---

# HTTPS (HyperText Transfer Protocol Secure)

Secure version of HTTP.

Default Port:

```
443
```

Features:

- Encryption
- SSL/TLS
- Authentication
- Data Integrity

Example:

```
https://example.com
```

---

# FTP (File Transfer Protocol)

Transfers files between computers.

Default Ports:

```
20
21
```

Uses:

- Uploading websites
- Downloading files

Limitation:

Passwords are transmitted in plain text.

---

# SFTP (SSH File Transfer Protocol)

Secure file transfer protocol.

Default Port:

```
22
```

Advantages:

- Encrypted communication
- Secure authentication

---

# SSH (Secure Shell)

Provides secure remote login.

Default Port:

```
22
```

Common Uses:

- Remote server administration
- Secure command execution
- File transfer

Example:

```bash
ssh user@192.168.1.10
```

---

# Telnet

Remote login protocol.

Default Port:

```
23
```

Disadvantages:

- No encryption
- Insecure

SSH has replaced Telnet in most environments.

---

# DNS (Domain Name System)

Converts domain names into IP addresses.

Default Port:

```
53
```

Example:

```
google.com

↓

142.250.xxx.xxx
```

---

# DHCP (Dynamic Host Configuration Protocol)

Automatically assigns:

- IP Address
- Gateway
- DNS Server
- Subnet Mask

Ports:

```
67
68
```

---

# SMTP (Simple Mail Transfer Protocol)

Used to send emails.

Default Port:

```
25

587

465 (SSL)
```

---

# POP3 (Post Office Protocol v3)

Downloads emails from the mail server.

Default Port:

```
110
```

Encrypted:

```
995
```

---

# IMAP (Internet Message Access Protocol)

Accesses emails while keeping them on the server.

Default Port:

```
143
```

Encrypted:

```
993
```

---

# TCP (Transmission Control Protocol)

Reliable transport protocol.

Features:

- Connection-oriented
- Error checking
- Packet ordering
- Retransmission

Applications:

- HTTPS
- FTP
- SSH
- SMTP

---

# UDP (User Datagram Protocol)

Fast but unreliable protocol.

Features:

- Connectionless
- Low latency
- No retransmission

Applications:

- DNS
- Streaming
- VoIP
- Online Gaming

---

# ICMP (Internet Control Message Protocol)

Used for:

- Diagnostics
- Error reporting

Common Command:

```bash
ping google.com
```

---

# ARP (Address Resolution Protocol)

Converts:

```
IP Address

↓

MAC Address
```

Used inside Local Area Networks.

---

# Common Port Numbers

| Protocol | Port |
|----------|------|
| HTTP | 80 |
| HTTPS | 443 |
| FTP | 20,21 |
| SSH | 22 |
| Telnet | 23 |
| DNS | 53 |
| DHCP | 67,68 |
| SMTP | 25 |
| POP3 | 110 |
| IMAP | 143 |
| SFTP | 22 |

---

# Standards

A **standard** is an agreed-upon specification that ensures compatibility between hardware, software, and communication systems.

Standards allow products from different companies to work together.

---

# Standard Organizations

---

## IEEE

**Institute of Electrical and Electronics Engineers**

Develops networking standards.

Examples:

- Ethernet (802.3)
- Wi-Fi (802.11)

Website:

https://www.ieee.org

---

## ISO

**International Organization for Standardization**

Created the:

- OSI Model

Develops international technology standards.

---

## IETF

**Internet Engineering Task Force**

Responsible for Internet protocols.

Examples:

- TCP
- UDP
- IPv4
- IPv6
- HTTP

---

## ANSI

**American National Standards Institute**

Coordinates standards in the United States.

---

## ITU

**International Telecommunication Union**

Develops global telecommunications standards.

---

# RFC (Request for Comments)

RFCs are official technical documents describing Internet standards and protocols.

Examples:

- TCP
- IP
- HTTP
- DNS

RFCs are maintained by the IETF.

---

# Open Standards vs Proprietary Standards

| Open Standards | Proprietary Standards |
|---------------|-----------------------|
| Public | Private |
| Free to implement | Owned by companies |
| Community-driven | Vendor-controlled |

Example:

Open:

- TCP/IP
- HTTP
- DNS

Proprietary:

- Microsoft SMB (original versions)
- Apple's AirDrop (implementation)

---

# Protocol Stack

Protocols work together in layers.

Example:

```
Application
↓

Transport

↓

Internet

↓

Network Access
```

Each layer performs a specific function.

---

# Real-World Example

Opening a website:

```
Browser

↓

HTTPS

↓

TCP

↓

IP

↓

Ethernet

↓

Internet

↓

Server
```

Each protocol contributes to successful communication.

---



# Summary

- Protocols define the rules for communication.
- Standards ensure compatibility between devices and vendors.
- HTTP, HTTPS, FTP, SSH, DNS, DHCP, TCP, UDP, ICMP, and ARP are among the most important networking protocols.
- Organizations such as IEEE, ISO, IETF, ANSI, and ITU develop and maintain networking standards.
- Understanding protocols is fundamental for networking and cybersecurity.

---
