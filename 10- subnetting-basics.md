# Subnetting Basics

## Introduction

As computer networks grow, managing them efficiently becomes more challenging. If all devices are placed on a single large network, it can lead to excessive broadcast traffic, reduced performance, and security concerns.

**Subnetting** is a technique used to divide a large network into multiple smaller and more manageable networks called **subnets**.

Subnetting is one of the most important concepts in networking and is widely used in enterprise networks, cloud environments, and cybersecurity.

---

# What is Subnetting?

**Subnetting** is the process of dividing a single IP network into multiple smaller logical networks (subnets).

Each subnet functions as an independent network while still being part of the original network.

Example:

```
Original Network

192.168.1.0/24

↓

Subnet 1
192.168.1.0/26

Subnet 2
192.168.1.64/26

Subnet 3
192.168.1.128/26

Subnet 4
192.168.1.192/26
```

---

# Why Do We Need Subnetting?

Subnetting provides several advantages:

- Reduces network congestion
- Reduces broadcast traffic
- Improves network performance
- Better network organization
- Easier troubleshooting
- Better security
- Efficient IP address utilization
- Supports large enterprise networks

---

# Key Terms

Before learning subnetting, understand these important terms.

---

## Network Address

The first address in a subnet.

It identifies the subnet itself.

Example

```
192.168.1.0
```

This address cannot be assigned to a device.

---

## Host Address

Host addresses are assigned to devices.

Example

```
192.168.1.10
192.168.1.25
192.168.1.100
```

---

## Broadcast Address

The last address in a subnet.

Used to send data to all devices within that subnet.

Example

```
192.168.1.255
```

---

## Subnet Mask

A subnet mask separates the **network portion** from the **host portion** of an IP address.

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

---

# CIDR (Classless Inter-Domain Routing)

CIDR uses slash notation to represent the subnet mask.

Examples

| CIDR | Subnet Mask |
|------|-------------|
| /8 | 255.0.0.0 |
| /16 | 255.255.0.0 |
| /24 | 255.255.255.0 |
| /25 | 255.255.255.128 |
| /26 | 255.255.255.192 |
| /27 | 255.255.255.224 |
| /28 | 255.255.255.240 |
| /29 | 255.255.255.248 |
| /30 | 255.255.255.252 |

---

# Understanding Network and Host Bits

Example

```
192.168.1.10/24
```

Network Bits

```
192.168.1
```

Host Bits

```
10
```

In binary:

```
11111111.11111111.11111111.00000000

↑ Network ↑        ↑ Host ↑
```

---

# Default Subnet Masks

| Class | Default Mask | CIDR |
|--------|--------------|------|
| A | 255.0.0.0 | /8 |
| B | 255.255.0.0 | /16 |
| C | 255.255.255.0 | /24 |

Although modern networking uses CIDR instead of classes, these defaults are useful for understanding subnetting basics.

---

# Borrowing Host Bits

Subnetting works by borrowing bits from the **host portion** of an IP address.

Example

Original Network

```
192.168.1.0/24
```

Borrow 2 Host Bits

```
192.168.1.0/26
```

Result

```
Network Bits ↑

11111111.11111111.11111111.11000000

Host Bits ↓
```

More borrowed bits create more subnets but fewer hosts per subnet.

---

# Number of Subnets

Formula

```
2^n
```

Where:

```
n = Number of Borrowed Bits
```

Example

Borrow

```
2 Bits
```

Subnets

```
2² = 4
```

---

# Number of Hosts

Formula

```
2^h − 2
```

Where

```
h = Host Bits Remaining
```

The subtraction of 2 accounts for:

- Network Address
- Broadcast Address

Example

Host Bits

```
6
```

Hosts

```
2⁶ − 2

64 − 2

62 Hosts
```

---

# Example 1

Network

```
192.168.1.0/24
```

Subnet

```
/26
```

Subnet Mask

```
255.255.255.192
```

Borrowed Bits

```
2
```

Subnets

```
4
```

Hosts Per Subnet

```
62
```

---

# Resulting Subnets

| Network | First Host | Last Host | Broadcast |
|---------|------------|-----------|-----------|
| 192.168.1.0/26 | 192.168.1.1 | 192.168.1.62 | 192.168.1.63 |
| 192.168.1.64/26 | 192.168.1.65 | 192.168.1.126 | 192.168.1.127 |
| 192.168.1.128/26 | 192.168.1.129 | 192.168.1.190 | 192.168.1.191 |
| 192.168.1.192/26 | 192.168.1.193 | 192.168.1.254 | 192.168.1.255 |

---

# Example 2

Network

```
10.0.0.0/24
```

Borrow

```
1 Bit
```

New Prefix

```
/25
```

Subnets

```
2
```

Hosts

```
126 Hosts Each
```

Subnet 1

```
10.0.0.0/25
```

Subnet 2

```
10.0.0.128/25
```

---

# Benefits of Subnetting

- Better bandwidth utilization
- Improved security
- Reduced broadcast domains
- Easier troubleshooting
- Better network management
- Efficient use of IP addresses
- Improved scalability

---

# Real-World Example

A company has three departments:

- HR
- Finance
- IT

Instead of placing all computers in one network:

```
192.168.1.0/24
```

The administrator creates separate subnets:

```
HR

192.168.1.0/26

Finance

192.168.1.64/26

IT

192.168.1.128/26
```

This reduces unnecessary broadcasts and improves security between departments.

---

# Summary

Subnetting divides a large network into smaller, more manageable subnets. It improves performance, reduces broadcast traffic, enhances security, and allows efficient use of IP addresses. Understanding subnetting is essential for network engineers, system administrators, cloud professionals, and cybersecurity analysts.

---