# CCNA – Basic Switch & End Device Configuration (Module 2)  
> Repo: `ccna-basic-switch-end-device-config-cheat-sheet-2025`

Quick-reference notes for **NetAcad CCNA – Module 2: Basic Switch and End Device Configuration**.  
Focus is on **IOS basics, device setup, IP addressing, and connectivity testing**.

> ⚠️ This is a **study helper**, not an answer key.  
> I use it to revise concepts and remember commands for labs, Packet Tracer, and exams.

---

## Table of Contents

- [Module 2 Overview](#module-2-overview)
- [How to Use This Cheat Sheet](#how-to-use-this-cheat-sheet)
- [Module Map](#module-map)
- [2.0 Introduction](#20-introduction)
  - [2.0.1 Why should I take this module?](#201-why-should-i-take-this-module)
  - [2.0.2 What will I learn to do in this module?](#202-what-will-i-learn-to-do-in-this-module)
- [2.1 Cisco IOS Access](#21-cisco-ios-access)
- [2.2 IOS Navigation](#22-ios-navigation)
- [2.3 The Command Structure](#23-the-command-structure)
- [2.4 Basic Device Configuration](#24-basic-device-configuration)
- [2.5 Save Configurations](#25-save-configurations)
- [2.6 Ports and Addresses](#26-ports-and-addresses)
- [2.7 Configure IP Addressing](#27-configure-ip-addressing)
- [2.8 Verify Connectivity](#28-verify-connectivity)
- [2.9 Practice Ideas](#29-practice-ideas)

---

## Module 2 Overview

**Goal of the module**

Get comfortable working with **Cisco IOS** on switches and end devices:

- Access and navigate IOS using **console** and **remote** methods.
- Understand **user EXEC**, **privileged EXEC**, and **configuration** modes.
- Apply **basic configuration** to switches and PCs.
- Configure **IP addressing** and **default gateways**.
- Use tools like **ping** and **traceroute** to verify connectivity.
- Understand the difference between **running-config** and **startup-config** and how to save configs.

This repo is just my **personal brain-dump** for Module 2 so I can quickly find:

- The **exact commands** I always forget.
- A short reminder of **what each section is about**.
- Small **lab snippets** I can paste into Packet Tracer.

---

## How to Use This Cheat Sheet

- The **section numbers (2.1, 2.2, 2.3, …)** match NetAcad, so you can follow along while watching/reading.
- When I do a lab, I scroll to that section and use:
  - **🧠 Big idea** → one-paragraph concept reminder.
  - **💻 Core commands** → copy/paste CLI blocks.
  - **✅ Checklist** → what I should be able to do before moving on.
- Before quizzes/exams, I skim all **🧠 Big idea** blocks and some key commands.

> For now this file is mostly a **skeleton**. I’ll fill each section as I progress through the module.

---

## Module Map

High-level view of what’s in this module:

- **2.0 – Introduction**  
  Why this module exists and what skills I should have at the end.

- **2.1 – Cisco IOS Access**  
  How to reach a device: console, SSH, Telnet, and terminal emulators.

- **2.2 – IOS Navigation**  
  Modes (user, privileged, global config, interface, etc.) and how to move between them.

- **2.3 – Command Structure**  
  Command syntax, context-sensitive help, shortcuts, and how IOS parses commands.

- **2.4 – Basic Device Configuration**  
  Hostnames, passwords, banners, and basic security hardening for switches.

- **2.5 – Save Configurations**  
  `running-config` vs `startup-config`, saving, and wiping configs.

- **2.6 – Ports and Addresses**  
  Switch ports, interfaces, MAC addresses, and where IP addressing actually lives.

- **2.7 – Configure IP Addressing**  
  IPv4/IPv6 addressing on PCs and switches, plus default gateway configuration.

- **2.8 – Verify Connectivity**  
  Using `ping`, `tracert/traceroute`, and basic `show` commands to confirm everything works.

- **2.9 – Practice Ideas**  
  Small Packet Tracer lab ideas for extra repetition.

---

## 2.0 Introduction

### 2.0.1 Why should I take this module?

In Module 1 you looked at what networks are and why they matter.  
In Module 2 you actually start **configuring real devices**.

As a network technician/engineer you will:

- Set up **new networks** or maintain and upgrade existing ones.
- Configure **switches and end devices** so they are **secure** and **fit the requirements** of the network.
- Take devices that come with only a **generic factory config** and turn them into properly tuned nodes in your topology.

In this module you learn how to:

- **Access Cisco IOS** on network devices.
- Use **basic configuration commands**.
- Configure and verify:
  - a Cisco IOS device (switch), and  
  - an end device (PC) with an **IP address**.

Everything else in network administration (routing, VLANs, security, etc.) depends on first being able to **log in, configure, and verify** your switches and hosts.

---

### 2.0.2 What will I learn to do in this module?

**Module Title:** Basic Switch and End Device Configuration  

**Module Objective:**  
Implement initial settings (passwords, IP addressing, and default gateway parameters) on a network switch and on end devices.

| Topic # | Topic Title               | After this topic you should be able to…                                                 |
|--------:|---------------------------|----------------------------------------------------------------------------------------|
| **2.1** | Cisco IOS Access          | Explain how to access a Cisco IOS device for configuration purposes.                  |
| **2.2** | IOS Navigation            | Explain how to navigate Cisco IOS to configure network devices.                       |
| **2.3** | The Command Structure     | Describe the basic command structure of Cisco IOS software.                           |
| **2.4** | Basic Device Configuration| Configure a Cisco IOS device using the CLI.                                           |
| **2.5** | Save Configurations       | Use IOS commands to save the running configuration.                                   |
| **2.6** | Ports and Addresses       | Explain how devices communicate across network media using ports and addresses.       |
| **2.7** | Configure IP Addressing   | Configure a host device with an IP address and default gateway.                       |
| **2.8** | Verify Connectivity       | Verify connectivity between two end devices using common network tools (e.g. `ping`). |

---


## 2.1 Cisco IOS Access

🧠 **Big idea**  
> _Placeholder – overview of access methods and what “Cisco IOS” actually is._

Sections I’ll add later:

- Difference between **IOS**, **firmware**, and **PC OS**.
- **Access methods:** console, SSH, Telnet, AUX (if used).
- **Terminal emulator examples:** Tera Term, PuTTY, etc.

💻 **Core commands (to add later)**

```text
# examples to add later
line console 0
 password <password>
 login
transport input ssh
