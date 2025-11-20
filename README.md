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
  - [2.1.1 Operating Systems](#211-operating-systems)
  - [2.1.2 GUI](#212-gui)
  - [2.1.3 Purpose of an OS](#213-purpose-of-an-os)
  - [2.1.4 Access Methods](#214-access-methods)
  - [2.1.5 Terminal Emulation Programs](#215-terminal-emulation-programs)
  - [2.1.6 Check Your Understanding – Cisco IOS Access](#216-check-your-understanding--cisco-ios-access)
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

> **Topic objective:** Explain how to access a Cisco IOS device for configuration purposes.

At this point the goal is **not** to memorize every IOS feature.  
You just need to know:

- what OS network devices run  
- how we talk to that OS (**CLI vs GUI**)  
- which access methods are safe to use in real life  

---

### 2.1.1 Operating Systems  

**Key ideas**

- Every **end device** (PC, phone, server) and every **network device** (switch, router) needs an **operating system (OS)**.
- The OS is usually shown in layers:
  - **Hardware** – the physical components.  
  - **Kernel** – talks directly to the hardware, manages resources.  
  - **Shell** – where the user interacts (CLI or GUI).  
  - **User interface** – what you actually see/use.
- With a **CLI**, you interact with the shell using text commands.  
- With a **GUI**, you use windows, icons, and menus.

**Remember**

- On PCs you might see **Windows / macOS / Linux**.  
- On Cisco network devices you’ll see **Cisco IOS families** (IOS, IOS XE, IOS XR, NX-OS, etc.).

---

### 2.1.2 GUI  

**What a GUI is**

- A **GUI (Graphical User Interface)** lets users interact using icons, menus, and windows.
- Examples: **Windows desktop, macOS, Linux KDE/GNOME, iOS, Android**.

**Pros**

- More **user-friendly**.  
- Requires **less knowledge** of the underlying command structure.  
- Great for **everyday users**.

**Cons (for networking)**

- May not expose **all features**.  
- Can **crash** or behave unpredictably.  
- Needs more **resources** than a CLI.

**Network world twist**

- Most **home routers**: OS is called *firmware* and you configure it with a **web GUI**.  
- Professional **Cisco routers/switches**: usually configured mainly through the **CLI**, even if a GUI exists.

---

### 2.1.3 Purpose of an OS  

On a **PC OS**, the OS allows you to:

- Use a mouse to **select/run programs**.  
- **Type commands** and interact with the system.  
- See **output on the screen**.

On a **network OS (Cisco IOS)** the same idea applies, but focused on networking:

- Run **CLI-based network programs**.  
- Enter **text commands** to configure and monitor the device.  
- View **text output** (e.g. `show` commands, logs, errors).

**IOS versions**

Different models (switches, routers) run different IOS versions depending on:

- **Hardware**  
- **Memory**  
- **Feature set** (e.g. Layer 3 routing, advanced security)

IOS can usually be **upgraded** to newer releases or feature sets.

---

### 2.1.4 Access Methods  

> How do we actually reach the IOS CLI?

There are three main methods you need to know here:

#### Console (local, out-of-band)

- Physical **console port** on the device.  
- Uses a **console cable** + **terminal emulator** on a PC.  
- Works even if **no IP address** or network services are configured.  
- Used for **initial setup**, **password recovery**, and when the **network is down**.

#### SSH – Secure Shell (remote, in-band, secure)

- Recommended method for **remote access**.  
- Uses the **network** (IP connectivity) and **encrypts** the session.  
- Requires:
  - an **active interface** with an IP address  
  - **SSH configured and enabled** on the device  
  - **vty lines** set to use SSH  
- Runs typically on **TCP port 22**.

#### Telnet (remote, in-band, insecure)

- Same idea as SSH but **no encryption**.  
- Usernames, passwords, and commands go across the network in **plaintext**.  
- Should only be used in **lab environments** or very controlled situations.  
- Exists in IOS for compatibility, but best practice: **use SSH instead**.

> 📝 Some devices also have an **AUX port** (legacy modem dial-in). Like console, it’s out-of-band but much less common nowadays.

---

### 2.1.5 Terminal Emulation Programs  

To talk to the device over **console / SSH / Telnet**, you use a **terminal emulator** on your PC.

**Common examples**

- **PuTTY**  
- **Tera Term**  
- **SecureCRT**  
- (In Packet Tracer: the built-in **Terminal** at `Desktop → Terminal`)

**What they let you do**

- Open sessions via:
  - **Serial/COM** (for console cables)  
  - **SSH**  
  - **Telnet**
- Adjust:
  - **window size and fonts**  
  - **color schemes**  
  - **logging** of output to text files  

**Typical quick-use pattern**

- **Console**: choose **Serial / COM port → 9600 baud** (lab default).  
- **SSH/Telnet**: choose **SSH** or **Telnet**, enter device **IP** and **port** → connect.

---

### 2.1.6 Check Your Understanding – Cisco IOS Access  

This quiz usually checks that you can:

- Recognize that **all devices need an OS** and what the OS does.  
- Distinguish **GUI vs CLI** (pros/cons, when each is used).  
- Choose the right **access method** for a scenario:
  - initial setup / recovery → **Console**  
  - secure remote management → **SSH**  
  - lab-only legacy remote access → **Telnet**
- Identify the role of **terminal emulation programs** (PuTTY, Tera Term, etc.).

Use this section as a reminder before taking the NetAcad mini-quiz — if you can explain those bullets in your own words, you’re good.  

---
