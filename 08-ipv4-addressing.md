# IPv4 Addressing

## Introduction

Every device connected to a network needs a unique address so that it can communicate with other devices. This unique identifier is known as an **IP (Internet Protocol) Address**.

**IPv4 (Internet Protocol Version 4)** is the most widely used version of the Internet Protocol. It identifies devices on a network and helps routers deliver data packets to the correct destination.

Although IPv6 was introduced to solve the shortage of IPv4 addresses, IPv4 is still extensively used in home networks, enterprise environments, and the Internet.

---

# What is an IPv4 Address?

An IPv4 address is a **32-bit logical address** assigned to a device on a network.

It uniquely identifies a device and allows communication between networks.

Example:

```
192.168.1.10
```

Each IPv4 address consists of **32 bits**, divided into **4 octets**.

Each octet contains **8 bits**.

```
192.168.1.10

↓

192    168     1      10
|-------|-------|-------|
8 bits  8 bits  8 bits  8 bits
```

Total:

```
8 + 8 + 8 + 8 = 32 bits
```

---

# Binary Representation

Every decimal number is converted into binary.

Example

```
Decimal

192.168.1.10
```

Binary

```
11000000.10101000.00000001.00001010
```

Each octet ranges from

```
00000000

to

11111111
```

Decimal Range

```
0 – 255
```

---

# Structure of an IPv4 Address

An IPv4 address has two parts:

```
Network Portion
Host Portion
```

Example

```
192.168.1.25/24
```

Network

```
192.168.1
```

Host

```
25
```

The network portion identifies the network, while the host portion identifies a specific device on that network.

---

# Dotted Decimal Notation

IPv4 addresses are written using dots between each octet.

Example

```
10.0.0.5

172.16.1.20

192.168.10.50
```

This format is called **Dotted Decimal Notation**.

---

# Address Classes

Originally, IPv4 addresses were divided into five classes.

---

## Class A

First Octet Range

```
1 – 126
```

Default Subnet Mask

```
255.0.0.0
```

Binary Prefix

```
0
```

Example

```
25.100.10.5
```

Large organizations commonly used Class A networks.

---

## Class B

First Octet

```
128 – 191
```

Default Mask

```
255.255.0.0
```

Binary Prefix

```
10
```

Example

```
172.16.10.5
```

Used by medium-sized organizations.

---

## Class C

First Octet

```
192 – 223
```

Default Mask

```
255.255.255.0
```

Binary Prefix

```
110
```

Example

```
192.168.1.25
```

Most common in home and office networks.

---

## Class D

Range

```
224 – 239
```

Purpose

```
Multicast
```

---

## Class E

Range

```
240 – 255
```

Purpose

```
Research and Experimental
```

---

# Reserved Addresses

Certain IPv4 addresses are reserved for special purposes.

---

## Loopback Address

```
127.0.0.1
```

Purpose

Testing the local computer's networking stack.

Command

```bash
ping 127.0.0.1
```

---

## Default Route

```
0.0.0.0
```

Represents an unknown or default network.

---

## Broadcast Address

Example

```
192.168.1.255
```

Sends data to all devices on the same network.

---

# Private IP Addresses

Private addresses are used inside local networks and are **not routable on the public Internet**.

| Class | Range |
|--------|-------|
| A | 10.0.0.0 – 10.255.255.255 |
| B | 172.16.0.0 – 172.31.255.255 |
| C | 192.168.0.0 – 192.168.255.255 |

Example

```
192.168.1.100
```

Home routers commonly assign these addresses using DHCP.

---

# Public IP Addresses

Public IP addresses are globally unique and can be reached over the Internet.

Example

```
8.8.8.8
```

(Google Public DNS)

Public IP addresses are assigned by Internet Service Providers (ISPs).

---

# Static IP Address

A Static IP Address never changes unless manually modified.

Advantages

- Stable connection
- Suitable for servers
- Easier remote access

Examples

- Web Server
- DNS Server
- Mail Server

---

# Dynamic IP Address

A Dynamic IP Address is assigned automatically by a DHCP server.

Advantages

- Automatic configuration
- Efficient use of IP addresses
- Easier network management

Most home devices use dynamic IP addresses.

---

# APIPA (Automatic Private IP Addressing)

If a DHCP server is unavailable, Windows may automatically assign an address from the following range:

```
169.254.0.0 – 169.254.255.255
```

This is called **APIPA**.

It allows communication only within the local network segment.

---

# Subnet Mask

A subnet mask separates the network portion from the host portion of an IP address.

Example

```
IP Address

192.168.1.10

Subnet Mask

255.255.255.0
```

CIDR Notation

```
192.168.1.10/24
```

Here, **/24** means the first 24 bits identify the network.

---

# Default Gateway

A default gateway is the router that forwards traffic to other networks.

Example

```
IP Address

192.168.1.25

Gateway

192.168.1.1
```

Without a gateway, a device can communicate only with devices on the same network.

---

# DNS Server

DNS converts domain names into IP addresses.

Example

```
www.google.com

↓

142.250.x.x
```

Common Public DNS Servers

Google

```
8.8.8.8
8.8.4.4
```

Cloudflare

```
1.1.1.1
1.0.0.1
```

---

# Example Network Configuration

```
IP Address

192.168.1.25

Subnet Mask

255.255.255.0

Gateway

192.168.1.1

DNS

8.8.8.8
```

---

# Real-World Example

Home Network

```
Internet
      │
 ISP
      │
Router
192.168.1.1
      │
 ┌──────────────┐
 │              │
Laptop      Smartphone
192.168.1.10   192.168.1.20
```

Each device has a unique IPv4 address, while the router uses NAT to communicate with the Internet.

---

# Summary

IPv4 addressing is the foundation of modern networking. It uses 32-bit logical addresses to identify devices, enabling communication within local networks and across the Internet. Understanding address classes, private and public IP addresses, subnet masks, gateways, and DNS is essential for networking, system administration, and cybersecurity.

---

