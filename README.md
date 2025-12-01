# CCNA – Physical Layer (Module 4)

Quick-reference notes for NetAcad CCNA – **Module 4: Physical Layer**.  
Focus is on how bits actually travel over copper, fiber, and wireless – and how physical characteristics (distance, noise, bandwidth, connectors) impact network design.

I use it to revise concepts and remember key ideas for labs, Packet Tracer, and exams.

---

## Table of Contents

- [Module 4 Overview](#module-4-overview)
- [Module Map](#module-map)
- [4.0 Introduction](#40-introduction)  
  - [4.0.1 Why should I take this module?](#401-why-should-i-take-this-module)  
  - [4.0.2 What will I learn to do in this module?](#402-what-will-i-learn-to-do-in-this-module)
 
- [4.1 Purpose of the Physical Layer](#41-purpose-of-the-physical-layer)
  - [4.1.1 The Physical Connection](#411-the-physical-connection)  
  - [4.1.2 The Physical Layer](#412-the-physical-layer)  
  - [4.1.3 Check Your Understanding – Purpose of the Physical Layer](#413-check-your-understanding--purpose-of-the-physical-layer)
    
- [4.2 Physical Layer Characteristics](#42-physical-layer-characteristics)  
  - [4.2.1 Physical Layer Standards](#421-physical-layer-standards)  
  - [4.2.2 Physical Components](#422-physical-components)  
  - [4.2.3 Encoding](#423-encoding)  
  - [4.2.4 Signaling](#424-signaling)  
  - [4.2.5 Bandwidth](#425-bandwidth)  
  - [4.2.6 Bandwidth Terminology](#426-bandwidth-terminology)  
  - [4.2.7 Check Your Understanding – Physical Layer Characteristics](#427-check-your-understanding--physical-layer-characteristics)
    
- [4.3 Copper Cabling](#43-copper-cabling)  
  - [4.3.1 Characteristics of Copper Cabling](#431-characteristics-of-copper-cabling)  
  - [4.3.2 Types of Copper Cabling](#432-types-of-copper-cabling)  
  - [4.3.3 Unshielded Twisted-Pair (UTP)](#433-unshielded-twisted-pair-utp)  
  - [4.3.4 Shielded Twisted-Pair (STP)](#434-shielded-twisted-pair-stp)  
  - [4.3.5 Coaxial Cable](#435-coaxial-cable)  
  - [4.3.6 Check Your Understanding – Copper Cabling](#436-check-your-understanding--copper-cabling)
    
- [4.4 UTP Cabling](#44-utp-cabling)  
  - [4.4.1 Properties of UTP Cabling](#441-properties-of-utp-cabling)  
  - [4.4.2 UTP Cabling Standards and Connectors](#442-utp-cabling-standards-and-connectors)  
  - [4.4.3 Straight-through and Crossover UTP Cables](#443-straight-through-and-crossover-utp-cables)  
  - [4.4.4 Activity – Cable Pinouts](#444-activity--cable-pinouts)
    
- [4.5 Fiber-Optic Cabling](#45-fiber-optic-cabling)  
  - [4.5.1 Properties of Fiber-Optic Cabling](#451-properties-of-fiber-optic-cabling)  
  - [4.5.2 Types of Fiber Media](#452-types-of-fiber-media)  
  - [4.5.3 Fiber-Optic Cabling Usage](#453-fiber-optic-cabling-usage)  
  - [4.5.4 Fiber-Optic Connectors](#454-fiber-optic-connectors)  
  - [4.5.5 Fiber Patch Cords](#455-fiber-patch-cords)  
  - [4.5.6 Fiber versus Copper](#456-fiber-versus-copper)  
  - [4.5.7 Check Your Understanding – Fiber-Optic Cabling](#457-check-your-understanding--fiber-optic-cabling)
    
- [4.6 Wireless Media](#46-wireless-media)  
  - [4.6.1 Properties of Wireless Media](#461-properties-of-wireless-media)  
  - [4.6.2 Types of Wireless Media](#462-types-of-wireless-media)  
  - [4.6.3 Wireless LAN](#463-wireless-lan)  
  - [4.6.4 Check Your Understanding – Wireless Media](#464-check-your-understanding--wireless-media)  
  - [4.6.5 Packet Tracer – Connect a Wired and Wireless LAN](#465-packet-tracer--connect-a-wired-and-wireless-lan)  
  - [4.6.6 Lab – View Wired and Wireless NIC Information](#466-lab--view-wired-and-wireless-nic-information)
    
- [4.7 Module Practice and Quiz](#47-module-practice-and-quiz)  
  - [4.7.1 Packet Tracer – Physical Layer Exploration](#471-packet-tracer--physical-layer-exploration)  
  - [4.7.2 Packet Tracer – Connect the Physical Layer](#472-packet-tracer--connect-the-physical-layer)  
  - [4.7.3 What did I learn in this module?](#473-what-did-i-learn-in-this-module)  
  - [4.7.4 Module Quiz – Physical Layer](#474-module-quiz--physical-layer)

---

## Module 4 Overview

### Goal of the module

Understand **how bits actually move** over physical media:

- What the **Physical layer** does in the OSI model.
- How copper, fiber, and wireless links are built and specified.
- How **encoding, signaling, and bandwidth** affect performance.
- When to choose **UTP vs STP vs fiber vs wireless** in real designs.
- How to recognize common **cable types, connectors, and pinouts**.

This repo is my personal brain-dump for Module 4 so I can quickly find:

- Definitions of **physical media types** and their pros/cons.
- Encoding/signaling terms (NRZ, Manchester, baseband, broadband, etc.).
- Key **standards** (TIA/EIA, IEEE) and **cable categories**.
- Practical notes from the Packet Tracer activities and labs.

---

## 4.0 Introduction

This module drops all the way down to **Layer 1 – the Physical Layer**.  
It lives at the bottom of the OSI stack and maps to the **Network Access layer** in TCP/IP.  
Here you focus on the actual **media and signals** that move bits between devices: copper, fiber, and wireless.

Packet Tracer activities and hands-on labs for this module are all about **cabling, connectors, and interfaces**, so by the end you should feel comfortable wiring and checking a small network on your own.

---

### 4.0.1 Why should I take this module?

Everything else in networking (IP, routing, VLANs, security, etc.) assumes one thing:  
**the bits can physically get from A to B.**

This module is important because it helps me:

- See how the **physical layer** fits under the data link and the rest of the stack.  
- Understand the differences between **wired** and **wireless** connections and when to use each.  
- Recognize the main components of a home or small-office setup  
  (wireless router, Ethernet switchports, Internet/WAN port, NICs in PCs and laptops).  
- Read and follow **basic cabling standards**, so I don’t just “plug things in” at random.  

After this section, I should be able to look at a network diagram or a real rack and say:
> “I know exactly which media, connectors, and interfaces are needed here for Layer 1.”

---

### 4.0.2 What will I learn to do in this module?

**Module Title:** Physical Layer  

**Module Objective:** Explain how physical layer protocols, services, and network media support communication across data networks.

| Topic Title                    | Topic Objective                                                                 |
| ------------------------------ | ------------------------------------------------------------------------------- |
| **Purpose of the Physical Layer**      | Describe what the physical layer does and why it is required in a network.       |
| **Physical Layer Characteristics**     | Describe key characteristics of the physical layer (bandwidth, throughput, etc.).|
| **Copper Cabling**                    | Identify the basic features and limitations of copper network cabling.           |
| **UTP Cabling**                       | Explain how UTP cables and connectors are used in Ethernet networks.             |
| **Fiber-Optic Cabling**              | Describe fiber-optic media and its main advantages compared to other cabling.    |
| **Wireless Media**                   | Explain how devices connect using wired and wireless media on modern networks.   |



### 4.1 Purpose of the Physical Layer

All the higher-layer protocols (Ethernet, IP, TCP, HTTP, etc.) eventually need to become **electrical, optical, or radio signals** on some medium. The **physical layer (Layer 1)** is the part of the stack that actually moves these bits between devices.

It does **not** care about MAC addresses or IP addresses. Its job is:

- Take a **complete frame from Layer 2**,  
- Encode the bits into signals on a specific medium (copper, fiber, or wireless),  
- Send those bits **one after another** across the link,  
- Receive signals on the other side and turn them back into bits,  
- Hand the clean bit stream back up to the **data link layer**.

---

#### 4.1.1 The Physical Connection

Before any network communication can happen, a device needs a **physical connection** to the local network. That can be:

- **Wired connection**
  - Uses a **cable** (typically UTP Ethernet or fiber) to connect to a switch or a router.
  - Common in offices where desktops and some laptops plug into a switch for stable, high-spe
- **Wireless connection**
  - Uses **radio waves** between a device and a **wireless access point (AP)** or a wireless router.
  - Typical at home and in public spaces (Wi-Fi).

**Home/small office example – wireless router**

A typical home “Wi-Fi router” usually contains:

1. **Wireless antennas** – built-in or external, providing WLAN coverage.
2. **Multiple Ethernet switchports** – for wired devices (PCs, printers, consoles).
3. **Internet/WAN port** – uplink to the ISP modem or fiber ONT.

**Network Interface Cards (NICs)**

End devices need a NIC to connect at Layer 1:

- **Ethernet NIC** – for **wired** connections (RJ-45 port, UTP cable).
- **WLAN NIC** – for **wireless** connections (built-in Wi-Fi adapter).

Some devices have:

- Only Ethernet NIC → must use a cable.  
- Only WLAN NIC → can *only* connect wirelessly.  
- Both → user can choose wired vs wireless depending on performance and mobility needs.

Not all physical connections provide the same performance – cable type, distance, interference, and wireless signal quality all affect bandwidth and reliability.

---

#### 4.1.2 The Physical Layer

The **OSI physical layer** is responsible for actually transporting the bits that make up a data link frame.

From the **sending** device’s point of view:

1. Layer 2 (Data Link) hands down a **complete frame**.
2. The physical layer:
   - **Encodes** the bits of that frame into signals (voltages, light pulses, or radio waves).
   - Sends those signals **one bit at a time** over the medium.

From the **receiving** device’s point of view:

1. The physical layer:
   - Receives the incoming signals from the medium.
   - Converts them back into a **stream of bits**.
2. It passes the bit stream **up to the data link layer**, which re-assembles the full frame and checks it (FCS, MAC addresses, etc.).

Key points to remember:

- Layer 1 works with **bits and signals**, not addresses or protocols.
- It defines:
  - How 0s and 1s are represented on a given medium,
  - Timing and synchronization of signals,
  - Physical characteristics of connectors, cables, and wireless channels.
- The PDU that arrives at the physical layer for transmission is always a **frame** (from Layer 2).

---

#### 4.1.3 Check Your Understanding – Purpose of the Physical Layer

**Question 1**  
*True or false? The physical layer is only concerned with wired network connections.*  

- **Answer:** `False`  
- **Why:** Layer 1 covers **any** physical media – **wired (copper/fiber)** *and* **wireless (radio)**. Wi-Fi is still the physical layer, just using radio waves instead of a cable.

---

**Question 2**  
*True or false? When a frame is encoded by the physical layer, all bits are sent over the media at the same time.*  

- **Answer:** `False`  
- **Why:** On typical data networks, bits are sent **serially**, one after another, along the medium. The physical layer does **not** blast all bits simultaneously; it clocks them out in sequence.

---

**Question 3**  
*The physical layer of the receiving device passes bits up to which higher-level layer?*  

- **Answer:** `Data link layer`  
- **Why:** Layer 1 only cares about bits. Once the bit stream is recovered, it is handed to **Layer 2 (Data Link)**, which rebuilds the full frame and checks MAC/FCS fields.

---

**Question 4**  
*What PDU is received by the physical layer for encoding and transmission?*  

- **Answer:** `Frame`  
- **Why:** The data link layer creates the **frame** (header + payload + trailer). That complete frame is then given to the physical layer, which encodes its bits onto the medium.

---

### 4.2 Physical Layer Characteristics

This topic looks at what defines the physical layer: the **standards bodies**, the **hardware components**, how bits are **encoded** and **signaled**, and how we measure **bandwidth**.

---

#### 4.2.1 Physical Layer Standards

- Upper OSI layers (and the TCP/IP suite) are implemented in **software** and defined by the **IETF**.
- The **physical layer** is implemented in **hardware**: electronic circuitry, media, and connectors.
- Because it is hardware, its standards are created and maintained by electrical and communications engineering organizations, including:

  - International Organization for Standardization (**ISO**)  
  - Telecommunications Industry Association / Electronic Industries Association (**TIA/EIA**)  
  - International Telecommunication Union (**ITU**)  
  - American National Standards Institute (**ANSI**)  
  - Institute of Electrical and Electronics Engineers (**IEEE**)  
  - National telecom regulators such as the **FCC** (USA) and **ETSI** (Europe)

- Regional cabling standards groups also exist, such as **CSA**, **CENELEC**, and **JSA/JIS**, which define local specifications.

---

#### 4.2.2 Physical Components

Physical layer standards address three functional areas:

- **Physical components**
- **Encoding**
- **Signaling**

**Physical components** are the electronic hardware devices, media, and connectors that transmit the signals representing bits, for example:

- **NICs**  
- Interfaces and connectors  
- Cable materials and designs  
- Ports and interfaces on routers and switches

All of these are specified in physical layer standards.

---

#### 4.2.3 Encoding

- **Encoding (line encoding)** converts a stream of bits into a predefined **code**.
- The code is a predictable pattern that both sender and receiver recognize.
- Encoding is the **method or pattern used to represent digital information**, similar to **Morse code** using dots and dashes.

Example from the module:

- **Manchester encoding**  
  - `0` bit = high → low voltage transition  
  - `1` bit = low → high voltage transition  
  - Used in **10 Mbps Ethernet**.

Other Ethernet examples mentioned:

- **100BASE-TX** uses **4B/5B** encoding.  
- **1000BASE-T** uses **8B/10B** encoding.

---

#### 4.2.4 Signaling

- The physical layer generates **electrical, optical, or wireless signals** that represent `1` and `0` on the medium.
- The way bits are represented is the **signaling method**.
- Standards must define which signal represents a `1` and which represents a `0`.  
  Examples:
  - Change in **voltage** for copper cable.  
  - **Light pulses** for fiber-optic cable.  
  - Changes to a **wireless carrier wave** (microwave) for wireless media.

This is similar to Morse code, which uses on/off tones, lights, or clicks to send information.

Figures in the module show:

- **Copper cable** – varying electrical voltage over time.  
- **Fiber-optic cable** – a sequence of light pulses over time.  
- **Wireless media** – a digital signal carried using:
  - **AM** (Amplitude Modulation)  
  - **FM** (Frequency Modulation)  
  - **PM** (Phase Modulation)

---

#### 4.2.5 Bandwidth

- Different physical media support different **bit transfer rates**.
- **Bandwidth** = capacity of a medium to carry data; amount of data that can flow from one point to another in a given time.

Common units used in the table:

- **bps** – bits per second (fundamental unit)  
- **Kbps** – kilobits per second (1 Kbps = 1,000 bps)  
- **Mbps** – megabits per second (1 Mbps = 1,000,000 bps)  
- **Gbps** – gigabits per second (1 Gbps = 1,000,000,000 bps)  
- **Tbps** – terabits per second (1 Tbps = 1,000,000,000,000 bps)

Notes from the text:

- In both **10 Mbps** and **100 Mbps Ethernet**, bits travel at the speed of electricity.  
  The difference is **how many bits per second** can be transmitted.
- Practical bandwidth depends on:
  - Properties of the **physical media**  
  - Technologies used for **signaling** and **detecting** network signals  

---

#### 4.2.6 Bandwidth Terminology

The module uses three terms to describe bandwidth quality:

- **Latency**
- **Throughput**
- **Goodput**

**Latency**

- Time (including delays) for data to travel from one point to another.  
- In a multi-segment network, overall performance is limited by the **slowest link**.

**Throughput**

- Measure of how many bits are actually transferred across the media over a period of time.  
- Throughput is usually **less than the specified bandwidth** because of:
  - Amount of traffic  
  - Type of traffic  
  - Latency introduced by the number of network devices between source and destination

**Goodput**

- Measure of **usable data** transferred over a period of time.  
- Defined as:

  > **Goodput = throughput − protocol overhead**

- Overhead includes:
  - Traffic used to establish sessions  
  - Acknowledgments  
  - Encapsulation headers/trailers  
  - Retransmitted bits
- Therefore, **goodput is always lower than throughput**, which is generally lower than raw bandwidth.

---
### 4.2.7 Check Your Understanding – Physical Layer Characteristics

**Question 1**  
*Which media uses patterns of microwaves to represent bits?*  
**Answer:** `Wireless`  
Microwave / radio waves are used in wireless links and are modulated to represent 0s and 1s.

---

**Question 2**  
*Which media uses patterns of light to represent bits?*  
**Answer:** `Fiber-optic`  
Fiber-optic cable uses pulses of light to carry digital data.

---

**Question 3**  
*Which media uses electrical pulses to represent bits?*  
**Answer:** `Copper`  
Copper cabling (UTP, coax, etc.) carries data as changes in electrical voltage.

---

**Question 4**  
*Which of these is the name for the capacity of a medium to carry data?*  
**Answer:** `Bandwidth`  
Bandwidth is the **maximum capacity** of a medium to carry data, usually in bps, Kbps, Mbps, or Gbps.

---

**Question 5**  
*Which of these is a measure of the transfer of bits across the media?*  
**Answer:** `Throughput`  
Throughput is the **actual rate of bit transfer** across the medium over time (usually lower than the bandwidth).


