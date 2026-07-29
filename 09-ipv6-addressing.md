# IPv6 Addressing

## Introduction

As the Internet continued to grow, the available IPv4 addresses became insufficient for the increasing number of devices. To overcome this limitation, **IPv6 (Internet Protocol Version 6)** was developed by the Internet Engineering Task Force (IETF).

IPv6 is the successor to IPv4 and provides a much larger address space, improved security features, simplified packet headers, and better support for modern networking technologies such as IoT (Internet of Things), cloud computing, and mobile networks.

Today, IPv6 is gradually being adopted worldwide alongside IPv4.

---

# What is IPv6?

**IPv6 (Internet Protocol Version 6)** is the latest version of the Internet Protocol that uses **128-bit addresses** to uniquely identify devices on a network.

Unlike IPv4, IPv6 provides an enormous number of unique addresses, making address exhaustion practically impossible.

Example:

```
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

---

# Why IPv6 Was Introduced

IPv4 has approximately:

```
4.3 Billion Addresses
```

With billions of smartphones, computers, IoT devices, and servers connected to the Internet, IPv4 addresses became insufficient.

IPv6 solves this problem by providing approximately:

```
340 Undecillion Addresses

340,282,366,920,938,463,463,374,607,431,768,211,456
```

This is often written as:

```
2^128 Addresses
```

---

# Features of IPv6

- 128-bit addressing
- Huge address space
- Better routing efficiency
- Built-in IPsec support
- Simplified packet header
- No broadcast traffic
- Supports multicast and anycast
- Automatic address configuration
- Improved security
- Better Quality of Service (QoS)

---

# Structure of an IPv6 Address

An IPv6 address contains:

```
128 Bits
```

It is divided into:

```
8 Blocks
```

Each block contains:

```
16 Bits
```

Example

```
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

Structure

```
2001
0db8
85a3
0000
0000
8a2e
0370
7334
```

Each block is separated using a colon (`:`).

---

# Hexadecimal Number System

IPv6 uses hexadecimal digits.

Allowed characters:

```
0 1 2 3 4 5 6 7 8 9
A B C D E F
```

Example

```
2001
db8
abcd
ff10
```

---

# IPv6 Address Format

General format

```
xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx
```

Example

```
2405:201:8000:abcd:1234:5678:90ab:cdef
```

---

# Address Compression

IPv6 addresses are long, so they can be shortened.

---

## Rule 1 – Remove Leading Zeros

Original

```
2001:0db8:0000:0000:0000:ff00:0042:8329
```

Compressed

```
2001:db8:0:0:0:ff00:42:8329
```

---

## Rule 2 – Replace Consecutive Zero Blocks

Original

```
2001:db8:0:0:0:ff00:42:8329
```

Compressed

```
2001:db8::ff00:42:8329
```

**Important:** The `::` symbol can only be used **once** in a single IPv6 address.

---

# Types of IPv6 Addresses

## 1. Unicast Address

Used for communication between one sender and one receiver.

Example

```
2001:db8::10
```

---

## 2. Multicast Address

Used to send data to multiple devices simultaneously.

Starts with:

```
FF00::/8
```

Example

```
FF02::1
```

---

## 3. Anycast Address

An Anycast address is assigned to multiple devices, but packets are delivered to the **nearest** device based on routing distance.

Commonly used by:

- DNS Servers
- CDN Providers
- Cloud Services

---

# IPv6 Address Types

## Global Unicast

Public IPv6 addresses.

Prefix

```
2000::/3
```

Example

```
2001:4860:4860::8888
```

(Google Public DNS)

---

## Link-Local Address

Automatically assigned to every IPv6-enabled interface.

Prefix

```
FE80::/10
```

Example

```
FE80::25A:1B2C:34D5:6789
```

Used only within the local network.

Routers do not forward these addresses.

---

## Unique Local Address (ULA)

Private IPv6 addressing.

Prefix

```
FC00::/7
```

Commonly

```
FD00::/8
```

Used inside organizations.

---

## Loopback Address

Equivalent to IPv4:

```
127.0.0.1
```

IPv6 Loopback

```
::1
```

Used for testing the local machine.

---

## Unspecified Address

Equivalent to IPv4:

```
0.0.0.0
```

IPv6

```
::
```

Represents the absence of an address.

---

# Prefix Length

IPv6 uses **prefix length** instead of subnet masks.

Example

```
2001:db8:1234::15/64
```

Meaning

```
First 64 bits → Network

Remaining 64 bits → Host
```

Most IPv6 networks use:

```
/64
```

---

# IPv4 vs IPv6

| Feature | IPv4 | IPv6 |
|---------|------|------|
| Address Length | 32-bit | 128-bit |
| Address Format | Decimal | Hexadecimal |
| Address Size | 4.3 Billion | 2¹²⁸ Addresses |
| Broadcast | Supported | Not Supported |
| Header | Complex | Simpler |
| NAT | Required | Usually Not Required |
| Security | Optional | IPsec Support |
| Configuration | Manual/DHCP | SLAAC/DHCPv6 |

---

# IPv6 Address Configuration

IPv6 supports:

## Manual Configuration

Administrator assigns the address manually.

---

## Stateless Address Autoconfiguration (SLAAC)

The device automatically generates its own IPv6 address using information advertised by the router.

Advantages:

- No DHCP server required
- Easy deployment
- Automatic configuration

---

## DHCPv6

Similar to DHCP in IPv4.

Provides:

- IPv6 Address
- DNS Server
- Other Network Information

---

# Neighbor Discovery Protocol (NDP)

IPv6 replaces ARP with **Neighbor Discovery Protocol (NDP)**.

NDP is used for:

- Address Resolution
- Router Discovery
- Duplicate Address Detection
- Neighbor Discovery

---

# Advantages of IPv6

- Massive address space
- Faster routing
- Better security
- Improved multicast support
- No broadcast traffic
- Better performance
- Auto configuration
- Simplified packet header
- Better support for IoT
- Improved mobile networking

---

# Disadvantages of IPv6

- Migration from IPv4 is complex
- Older hardware may not support IPv6
- Learning curve for administrators
- Some legacy applications require updates

---

# Real-World Example

Home Network

```
Internet
      │
Router
      │
──────────────────────────
Laptop

2001:db8:1::10

Phone

2001:db8:1::20

Printer

2001:db8:1::30
```

Each device receives its own globally unique IPv6 address.

---

# Summary

IPv6 is the modern Internet Protocol designed to replace IPv4. It uses 128-bit hexadecimal addresses, offers an enormous address space, improves routing efficiency, supports automatic configuration, and removes the need for broadcast traffic. Understanding IPv6 is essential for networking, cloud computing, and cybersecurity professionals as adoption continues to increase.

---

