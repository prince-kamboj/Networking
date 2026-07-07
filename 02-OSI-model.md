# OSI Model (Open Systems Interconnection)

## Introduction

The **OSI (Open Systems Interconnection) Model** is a conceptual framework that explains how data travels from one computer to another over a network. It divides the communication process into **seven distinct layers**, where each layer has a specific responsibility.

Rather than being a protocol itself, the OSI Model acts as a **reference model** that helps developers, network engineers, and students understand how different networking technologies work together.

Although today's Internet primarily uses the **TCP/IP Model**, the OSI Model remains one of the most important concepts in computer networking because it provides a clear and structured way to study network communication.

---

# Why Was the OSI Model Developed?

Before the OSI Model was introduced, networking vendors developed their own communication methods.

For example:

- IBM computers communicated differently from DEC computers.
- Software designed for one vendor often could not communicate with another.
- There was no common standard for network communication.

To solve this problem, the **International Organization for Standardization (ISO)** introduced the OSI Model in **1984**.

Its purpose was to create a standard framework that allows devices from different manufacturers to communicate efficiently.

---

# Objectives of the OSI Model

The main objectives of the OSI Model are:

- Standardize network communication
- Divide networking into smaller manageable layers
- Simplify troubleshooting
- Promote interoperability between vendors
- Make network design easier
- Allow independent development of networking technologies

---

# Advantages of the OSI Model

The OSI Model offers several benefits:

### Standardization

Provides a universal reference for networking.

---

### Easier Troubleshooting

Problems can be isolated to a particular layer instead of checking the entire network.

Example:

- Unable to access a website?
- First check the Physical Layer.
- Then Data Link.
- Then Network.
- Continue upward until the issue is found.

---

### Modular Design

Each layer performs a specific task independently.

This makes network technologies easier to develop and maintain.

---

### Vendor Independence

Devices from different companies can communicate because they follow common standards.

---

### Simplified Learning

Breaking networking into seven layers makes it much easier to understand than learning everything at once.

---

# Structure of the OSI Model

The OSI Model consists of seven layers.

```text
+-----------------------------+
| 7. Application Layer        |
+-----------------------------+
| 6. Presentation Layer       |
+-----------------------------+
| 5. Session Layer            |
+-----------------------------+
| 4. Transport Layer          |
+-----------------------------+
| 3. Network Layer            |
+-----------------------------+
| 2. Data Link Layer          |
+-----------------------------+
| 1. Physical Layer           |
+-----------------------------+
```

Data moves **from the top layer to the bottom layer** while being transmitted.

At the receiving end, it moves **from the bottom layer back to the top**.

---

# Layer 7 – Application Layer

The **Application Layer** is the topmost layer of the OSI Model.

It acts as the interface between the user and the network.

When you perform activities such as browsing websites, sending emails, uploading files, or chatting online, you interact with this layer.

### Responsibilities

- Provides network services to users
- Enables communication between applications
- Starts the communication process
- Accepts user requests

### Common Protocols

- HTTP
- HTTPS
- FTP
- SMTP
- POP3
- IMAP
- DNS

### Real-Life Example

When you type:

```
https://www.google.com
```

into your browser and press **Enter**, the request begins at the Application Layer.

---

# Layer 6 – Presentation Layer

The Presentation Layer is responsible for **how data is represented**.

Different computers may store information differently.

This layer ensures that both sender and receiver understand the data correctly.

### Responsibilities

- Data translation
- Encryption
- Decryption
- Compression
- Decompression
- Character encoding

### Example

Suppose you send an encrypted email.

The Presentation Layer encrypts the message before transmission.

The receiver's Presentation Layer decrypts it before displaying the original content.

Without this layer, encrypted or compressed data would not be understandable by the receiving application.

---

# Layer 5 – Session Layer

The Session Layer establishes, manages, and terminates communication sessions between two devices.

A **session** refers to a continuous exchange of information between two systems.

### Responsibilities

- Session establishment
- Session maintenance
- Session termination
- Synchronization
- Recovery after interruptions

### Example

Imagine attending an online meeting.

The Session Layer:

- Starts the meeting session.
- Keeps it active while participants communicate.
- Ends the session when everyone leaves.

If the connection is interrupted, this layer helps resume communication from the last synchronization point.

---

# Layer 4 – Transport Layer

The Transport Layer ensures that data reaches the correct destination completely and reliably.

It is responsible for dividing large messages into smaller pieces called **segments** and reassembling them at the destination.

### Responsibilities

- End-to-end communication
- Segmentation
- Reassembly
- Flow control
- Error detection
- Error recovery

### Main Protocols

#### TCP (Transmission Control Protocol)

Features:

- Reliable
- Connection-oriented
- Error checking
- Packet sequencing
- Retransmission

Used by:

- HTTPS
- SSH
- FTP
- Email

---

#### UDP (User Datagram Protocol)

Features:

- Fast
- Connectionless
- Low latency
- No retransmission

Used by:

- DNS
- Online gaming
- Video streaming
- Voice over IP (VoIP)

---

### Example

Downloading a PDF from a website.

The file is divided into many smaller segments.

TCP ensures:

- No segment is lost.
- Segments arrive in order.
- Missing segments are retransmitted.

---

# Layer 3 – Network Layer

The Network Layer is responsible for moving data between different networks.

Its primary job is **routing**.

### Responsibilities

- Logical addressing
- Routing
- Path selection
- Packet forwarding

### Common Protocols

- IPv4
- IPv6
- ICMP
- IPsec

### Device

Router

### Example

Suppose your laptop in India accesses a server located in the United States.

The Network Layer determines the best route through multiple routers across the Internet.

Without routing, packets would never reach their destination.

---

# Layer 2 – Data Link Layer

The Data Link Layer provides communication between devices connected to the same physical network.

It organizes bits into **frames** and detects transmission errors.

### Responsibilities

- Framing
- Physical addressing (MAC Address)
- Error detection
- Flow control
- Media access control

### Device

- Switch
- Bridge

### Example

Your laptop sends data to your Wi-Fi router.

Both devices are connected to the same local network.

The Data Link Layer uses MAC addresses to deliver the frame to the correct device.

---

# Layer 1 – Physical Layer

The Physical Layer is the lowest layer of the OSI Model.

It is responsible for transmitting raw binary data over the communication medium.

Unlike other layers, it does not understand packets or frames—it simply transmits **bits (0s and 1s).**

### Responsibilities

- Transmission of bits
- Electrical signals
- Optical signals
- Wireless signals
- Cable specifications
- Connectors

### Devices

- Hub
- Repeater
- Network Cable
- Fiber Optic Cable

### Transmission Media

- Twisted Pair Cable
- Coaxial Cable
- Fiber Optic Cable
- Radio Waves
- Wi-Fi

### Example

When a binary sequence such as:

```text
10110010
```

is transmitted through an Ethernet cable, the Physical Layer converts it into electrical signals.

At the receiving side, those signals are converted back into binary bits.

---




## Protocol Data Unit (PDU)

As data moves through the layers of the OSI Model, each layer adds its own information to help deliver the data correctly. The data has a different name at different layers. These names are called **Protocol Data Units (PDUs)**.

| OSI Layer | PDU |
|-----------|-----|
| Application | Data |
| Presentation | Data |
| Session | Data |
| Transport | Segment (TCP) / Datagram (UDP) |
| Network | Packet |
| Data Link | Frame |
| Physical | Bits |

### Why PDUs Matter

Each layer performs a specific job and packages the data in a format that the next layer understands. This makes communication organized and reliable.

---

# Encapsulation

Encapsulation is the process of adding protocol information to data as it moves **down** the OSI Model.

Every layer adds its own header, and in some cases a trailer, before passing the data to the next layer.

Think of it like sending a parcel:

- The message is written.
- It is placed inside an envelope.
- The envelope is placed inside a package.
- A shipping label is attached.
- The package is transported to its destination.

Each step adds information without changing the original message.

---

## Encapsulation Process

```text
Application Layer
        │
        ▼
      DATA
        │
        ▼
Presentation Layer
        │
        ▼
      DATA
        │
        ▼
Session Layer
        │
        ▼
      DATA
        │
        ▼
Transport Layer
        │
Adds TCP/UDP Header
        ▼
     SEGMENT
        │
        ▼
Network Layer
        │
Adds IP Header
        ▼
      PACKET
        │
        ▼
Data Link Layer
        │
Adds MAC Header
Adds Trailer
        ▼
      FRAME
        │
        ▼
Physical Layer
        │
Converts to Bits
        ▼
101011001011010...
```

---

# Decapsulation

Decapsulation is the reverse of encapsulation.

As data reaches the receiving device, each layer removes the information added by its corresponding layer until the original message reaches the application.

```text
Bits

↓

Frame

↓

Packet

↓

Segment

↓

Data

↓

Application
```

Each layer removes only its own header before passing the remaining data upward.

---

# Communication Between Layers

Each layer communicates with:

- The layer directly above it.
- The layer directly below it.
- Its corresponding layer on the receiving computer.

Example:

```text
Computer A                  Computer B

Application  <----------->  Application

Presentation <----------->  Presentation

Session      <----------->  Session

Transport    <----------->  Transport

Network      <----------->  Network

Data Link    <----------->  Data Link

Physical     <----------->  Physical
```

This is called **peer-to-peer communication**.

---

# Example: Opening a Website

Suppose you type:

```
https://www.google.com
```

into your web browser.

The communication happens like this.

## Step 1 — Application Layer

The browser creates an HTTP or HTTPS request.

Example:

```
GET /
```

---

## Step 2 — Presentation Layer

The request is prepared.

Possible operations include:

- Encryption (TLS)
- Compression
- Character encoding

---

## Step 3 — Session Layer

A communication session is established between your browser and Google's server.

The session is maintained until communication finishes.

---

## Step 4 — Transport Layer

TCP divides the request into segments.

Each segment contains:

- Source Port
- Destination Port
- Sequence Number
- Checksum

TCP guarantees reliable delivery.

---

## Step 5 — Network Layer

The IP header is added.

Example:

```
Source IP

192.168.1.20

Destination IP

142.250.xxx.xxx
```

The router uses these addresses to forward packets toward Google.

---

## Step 6 — Data Link Layer

The packet is converted into a frame.

MAC addresses are added.

Example:

```
Source MAC

00:11:22:33:44:55

Destination MAC

AA:BB:CC:DD:EE:FF
```

---

## Step 7 — Physical Layer

The frame becomes electrical, optical, or wireless signals.

Example:

```
101001101010110...
```

The data travels through cables or wireless media.

---

# Receiving Process

Google's server performs the opposite operation.

```text
Bits

↓

Frame

↓

Packet

↓

Segment

↓

Data

↓

Web Server
```

This reverse process is called **Decapsulation**.

---

# Encapsulation vs Decapsulation

| Encapsulation | Decapsulation |
|---------------|---------------|
| Sender Side | Receiver Side |
| Adds Headers | Removes Headers |
| Top → Bottom | Bottom → Top |
| Prepares Data for Transmission | Restores Original Data |

---

# Devices Used at Each Layer

| Layer | Common Device |
|---------|--------------|
| Application | Gateway, Proxy Server |
| Presentation | Gateway |
| Session | Gateway |
| Transport | Gateway, Firewall |
| Network | Router, Layer 3 Switch |
| Data Link | Switch, Bridge, NIC |
| Physical | Hub, Repeater, Cable |

---

# Addressing at Different Layers

Different layers use different types of addresses.

| Layer | Address |
|---------|----------|
| Transport | Port Number |
| Network | IP Address |
| Data Link | MAC Address |

Example:

```
Port Number

443

↓

IP Address

142.250.xxx.xxx

↓

MAC Address

00:11:22:33:44:55
```

---

# Flow of Data

```text
User

↓

Browser

↓

Application Layer

↓

Presentation Layer

↓

Session Layer

↓

Transport Layer

↓

Network Layer

↓

Data Link Layer

↓

Physical Layer

↓

Internet

↓

Destination Computer

↓

Physical Layer

↓

Data Link Layer

↓

Network Layer

↓

Transport Layer

↓

Session Layer

↓

Presentation Layer

↓

Application Layer

↓

Website Opens
```

---

# Remembering the OSI Layers

### Top to Bottom

```
All

People

Seem

To

Need

Data

Processing
```

Application

Presentation

Session

Transport

Network

Data Link

Physical

---

### Bottom to Top

```
Please

Do

Not

Throw

Sausage

Pizza

Away
```

Physical

Data Link

Network

Transport

Session

Presentation

Application

---

# OSI Model at a Glance

| Layer | Main Function |
|---------|---------------|
| Application | User Services |
| Presentation | Translation & Encryption |
| Session | Session Management |
| Transport | Reliable Delivery |
| Network | Routing |
| Data Link | Framing & MAC Addressing |
| Physical | Transmission of Bits |

---

# Common Misconceptions

### OSI Model is not a protocol.

It is only a reference model used to understand network communication.

---

### The Internet does not directly use the OSI Model.

Modern networks primarily use the **TCP/IP Model**, but the OSI Model is still widely used for learning, troubleshooting, and designing networks.

---

### Layers are independent.

Each layer performs its own task without needing to know how other layers work internally.

This modular approach makes networking easier to design and maintain.

---



# Layer Summary

| Layer | Main Responsibility | Common Device |
|--------|---------------------|---------------|
| Application | Network services for applications | Gateway |
| Presentation | Translation, Encryption, Compression | Gateway |
| Session | Session Management | Gateway |
| Transport | Reliable Delivery | Gateway |
| Network | Routing & Logical Addressing | Router |
| Data Link | Framing & MAC Addressing | Switch |
| Physical | Bit Transmission | Hub, Repeater |

---



# Summary

The OSI Model provides a structured way to understand how devices communicate over a network.

Each of the seven layers performs a specific function, from interacting with user applications to transmitting bits over physical media.

During transmission, data is encapsulated as it moves down the layers, gaining headers and other control information. At the destination, the process is reversed through decapsulation, allowing the original data to be delivered to the receiving application.

Although modern networks rely on the TCP/IP Model, the OSI Model remains one of the most important concepts in networking because it simplifies learning, troubleshooting, and understanding how communication works between devices.



