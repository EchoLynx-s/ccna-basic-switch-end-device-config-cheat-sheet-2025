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

🧠 **Big idea**  
> _Placeholder – will add summary once I finish this subsection._  

- Why device configuration skills matter.
- How Module 2 connects to Module 1 (network basics) and later modules.

✅ **Checklist (I should be able to…)**

- Explain in one sentence why knowing IOS is important for a network tech.  
- Describe at a high level what I’ll do in this module (configure switches & end devices).

---

### 2.0.2 What will I learn to do in this module?

🧠 **Big idea**  
> _Placeholder – short description of learning objectives for Module 2._

Planned bullets:

- List the **main tasks** (access device, navigate IOS, configure, save, test).
- Note which **tools** are used (console cable, terminal, Packet Tracer).

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
