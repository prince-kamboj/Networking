# Private IP vs Public IP Address

## Introduction

Every device connected to a network requires an **IP (Internet Protocol) address** for communication. However, not all IP addresses are the same. Some are used only within local networks, while others are accessible over the Internet.

Based on their accessibility, IP addresses are classified into two main types:

- **Private IP Address**
- **Public IP Address**

Understanding the difference between private and public IP addresses is essential for networking, cloud computing, system administration, and cybersecurity.

---

# What is a Private IP Address?

A **Private IP Address** is an IP address that is used **inside a local network (LAN)** and **cannot be accessed directly from the Internet**.

Private IP addresses are assigned by routers or DHCP servers to devices within homes, schools, offices, and organizations.

Example:

```
192.168.1.10
```

---

# Features of Private IP Addresses

- Used within local networks
- Not routable on the Internet
- Can be reused by different organizations
- Assigned by a router or DHCP server
- Free to use
- Requires NAT to access the Internet

---

# Private IP Address Ranges

The Internet Assigned Numbers Authority (IANA) reserves three IPv4 ranges for private networks.

| Class | Address Range | CIDR |
|--------|---------------|------|
| Class A | 10.0.0.0 – 10.255.255.255 | 10.0.0.0/8 |
| Class B | 172.16.0.0 – 172.31.255.255 | 172.16.0.0/12 |
| Class C | 192.168.0.0 – 192.168.255.255 | 192.168.0.0/16 |

---

# Examples of Private IP Addresses

```
10.0.0.15

172.20.15.100

192.168.1.25
```

All of these addresses are valid private IPv4 addresses.

---

# What is a Public IP Address?

A **Public IP Address** is a globally unique IP address assigned by an **Internet Service Provider (ISP)**. It allows a device or router to communicate over the Internet.

Unlike private IP addresses, public IP addresses are routable on the Internet.

Example:

```
142.250.183.14
```

---

# Features of Public IP Addresses

- Globally unique
- Accessible from the Internet
- Assigned by an ISP
- Used for communication between networks
- Required for Internet access
- Can be static or dynamic

---

# Examples of Public IP Addresses

```
8.8.8.8
```

Google Public DNS

```
1.1.1.1
```

Cloudflare Public DNS

```
208.67.222.222
```

OpenDNS

---

# Difference Between Private and Public IP

| Feature | Private IP | Public IP |
|----------|------------|-----------|
| Scope | Local Network | Internet |
| Assigned By | Router / DHCP | ISP |
| Internet Accessible | No | Yes |
| Globally Unique | No | Yes |
| Cost | Free | Usually included with Internet service |
| NAT Required | Yes | No (already Internet-routable) |

---

# Static vs Dynamic Public IP

## Static Public IP

A **Static Public IP** remains the same unless changed manually or by the ISP.

Advantages:

- Ideal for web servers
- Remote access
- Hosting websites
- VPN servers
- CCTV remote viewing

Example:

```
103.25.120.10
```

---

## Dynamic Public IP

A **Dynamic Public IP** changes periodically and is assigned automatically by the ISP.

Advantages:

- More common
- Easier to manage
- Efficient use of IP addresses
- Usually included in residential Internet plans

Most home Internet connections use dynamic public IP addresses.

---

# Network Address Translation (NAT)

**Network Address Translation (NAT)** is a technique used by routers to allow multiple private IP addresses to share a single public IP address.

Without NAT, every device would require its own public IP address.

Example:

```
Laptop
192.168.1.10

Phone
192.168.1.20

Printer
192.168.1.30

        │
        ▼

Home Router
Private → Public Translation

        │

Public IP
49.36.120.15

        │

Internet
```

The router translates private IP addresses into its public IP when devices access the Internet.

---

# Why NAT is Important

- Conserves public IPv4 addresses
- Allows multiple devices to share one public IP
- Hides internal network structure
- Provides a basic layer of security
- Simplifies home and office networking

---

# How Communication Works

Suppose your laptop has:

```
Private IP

192.168.1.25
```

Router's Public IP:

```
49.36.120.15
```

When you visit:

```
www.google.com
```

The communication flow is:

```
Laptop

192.168.1.25

↓

Router

49.36.120.15

↓

Internet

↓

Google Server

↓

Router

↓

Laptop
```

The router performs NAT so that responses from the Internet return to the correct device.

---

# How to Check Your Private IP

## Windows

```cmd
ipconfig
```

Look for:

```
IPv4 Address
```

---

## Linux

```bash
ip addr
```

or

```bash
ifconfig
```

---

# How to Check Your Public IP

You can use a browser and search:

```
What is my IP
```

Or use:

```bash
curl ifconfig.me
```

---

# Real-World Example

Imagine a company with 200 employees.

Each employee receives a private IP address such as:

```
192.168.10.x
```

The company's Internet connection has only one public IP:

```
103.75.25.10
```

All employees access the Internet through that single public IP using NAT.

---

# Summary

Private IP addresses are used for communication within local networks, while public IP addresses enable communication over the Internet. Routers use NAT to translate private addresses into a public address, allowing multiple devices to share a single Internet connection. Understanding these concepts is fundamental for networking, cloud computing, and cybersecurity.

---

