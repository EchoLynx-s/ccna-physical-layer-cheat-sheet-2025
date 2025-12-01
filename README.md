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


