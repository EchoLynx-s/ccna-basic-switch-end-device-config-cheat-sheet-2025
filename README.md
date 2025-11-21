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
  - [2.2.1 Primary Command Modes](#221-primary-command-modes)
  - [2.2.2 Configuration Mode and Subconfiguration Modes](#222-configuration-mode-and-subconfiguration-modes)
  - [2.2.3 Video – IOS CLI Primary Command Modes](#223-video--ios-cli-primary-command-modes)
  - [2.2.4 Navigate Between IOS Modes](#224-navigate-between-ios-modes)
  - [2.2.5 Video – Navigate Between IOS Modes](#225-video--navigate-between-ios-modes)
  - [2.2.6 A Note About Syntax Checker Activities](#226-a-note-about-syntax-checker-activities)
  - [2.2.7 Syntax Checker – Navigate Between IOS Modes](#227-syntax-checker--navigate-between-ios-modes)
  - [2.2.8 Check Your Understanding – IOS Navigation](#228-check-your-understanding--ios-navigation)
- [2.3 The Command Structure](#23-the-command-structure)
  - [2.3.1 Basic IOS Command Structure](#231-basic-ios-command-structure)
  - [2.3.2 IOS Command Syntax Check](#232-ios-command-syntax-check)
  - [2.3.3 IOS Help Features](#233-ios-help-features)
  - [2.3.4 Video – Context Sensitive Help and Command Syntax Check](#234-video--context-sensitive-help-and-command-syntax-check)
  - [2.3.5 Hot Keys and Shortcuts](#235-hot-keys-and-shortcuts)
  - [2.3.6 Video – Hot Keys and Shortcuts](#236-video--hot-keys-and-shortcuts)
  - [2.3.7 Packet Tracer – Navigate the IOS](#237-packet-tracer--navigate-the-ios)
  - [2.3.8 Lab – Navigate the IOS by Using Tera Term for Console Connectivity](#238-lab--navigate-the-ios-by-using-tera-term-for-console-connectivity)
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

Welcome to **Basic Switch and End Device Configuration**!

As part of your career in networking, you might have to set up a new network or maintain and upgrade an existing one. In either case, you’ll configure switches and end devices so that they are secure and perform effectively based on your requirements.

Out of the box, switches and end devices come with some general configuration. But for your particular network, switches and end devices require your specific information and instructions. In this module, you will learn how to access Cisco IOS network devices. You will learn basic configuration commands and use them to configure and verify a Cisco IOS device and an end device with an IP address.

Of course, there is much more to network administration, but none of that can happen without first configuring switches and end devices.


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

## 2.2 IOS Navigation  

**Topic objective:** Understand the main IOS command modes and how to move between them efficiently.

At this point you’re not expected to know every command, just:

- which **mode** you’re in,  
- what you’re allowed to do there,  
- and which command gets you to the mode you actually need.  

---

### 2.2.1 Primary Command Modes

IOS uses different modes to separate privileges.

**User EXEC mode (`>` prompt)**  

- “View-only” / basic monitoring.  
- Limited commands: e.g. `ping`, some `show` commands, `exit`.  
- Prompt examples:

```text
Switch>
Router>
```

**Privileged EXEC mode (`#` prompt)**  

- Full monitoring and management commands.  
- Required before you can enter configuration modes.  
- Prompt examples:

```text
Switch#
Router#
```

**How to move between them**

```text
Switch> enable        ← user EXEC → privileged EXEC
Switch# disable       ← privileged EXEC → user EXEC
```

If a command isn’t working even though the syntax looks right, **check the prompt first** – you’re probably in the wrong mode.

---

### 2.2.2 Configuration Mode and Subconfiguration Modes

To actually **change** the device config, you go into **global configuration mode**:

```text
Switch# configure terminal
Switch(config)#
```

From global config you can reach many **subconfiguration** modes.

Common ones in this module:

**Line configuration mode – console, vty, aux**

```text
Switch(config)# line console 0
Switch(config-line)#
```

**Interface configuration mode – switchport or routed interface**

```text
Switch(config)# interface FastEthernet0/1
Switch(config-if)#
```

**Prompts to remember**

- `Switch(config)#` → global configuration  
- `Switch(config-line)#` → line configuration  
- `Switch(config-if)#` → interface configuration  

You normally move **down** the tree with specific commands (`line …`, `interface …`) and **up** with `exit` or `end`.

---

### 2.2.3 Video – IOS CLI Primary Command Modes

The video basically walks through:

- Opening a **console** session in a terminal emulator.  
- Landing in **User EXEC** (`Switch>`).  
- Typing `enable` to reach **Privileged EXEC** (`Switch#`).  
- Typing `configure terminal` to reach **Global Config** (`Switch(config)#`).  
- Entering interface config:

```text
Switch(config)# interface vlan 1
Switch(config-if)#
```

**Key message**

> Many commands only work in certain modes.  
> If the syntax is correct but IOS complains, check the **mode** shown by your prompt.

---

### 2.2.4 Navigate Between IOS Modes

This section is the **movement toolkit** between modes.

**Core navigation commands**

```text
enable                → user EXEC → privileged EXEC
disable               → privileged EXEC → user EXEC

configure terminal    → privileged EXEC → global config
(conf t)

exit                  → up one level (e.g. config-if → config, config → #)
end                   → jump straight back to privileged EXEC (#)
Ctrl+Z                → same as end from config modes
```

**Examples from the module**

User → Privileged → Global config:

```text
Switch> enable
Switch# configure terminal
Switch(config)#
```

Global config → line config → back:

```text
Switch(config)# line console 0
Switch(config-line)# exit
Switch(config)#
```

Move between sub-modes directly:

```text
Switch(config-line)# interface vlan 1
Switch(config-if)#
Switch(config-if)# interface FastEthernet0/1
Switch(config-if)#
```

Escape back to Privileged EXEC from anywhere:

```text
Switch(config-if)# end
Switch#
```

(or press **Ctrl+Z**)

Being quick with these transitions saves a ton of time during labs and exams.

---

### 2.2.5 Video – Navigate Between IOS Modes

The second video reinforces the same ideas with a live demo:

- `enable` / `disable` – toggle between user and privileged EXEC.  
- `configure terminal` / `config t` – enter global config.  
- `exit` – step up one level (sub-mode → global config, or `#` → close console).  
- `line console 0`, `line vty 0 15`, `interface vlan 1`, `interface fastethernet 0/1` – examples of sub-modes.  
- `end` or **Ctrl+Z** – exit all config modes straight back to `Switch#`.

**Takeaway**

Learn the **pattern**, not just the commands:  

`> → # → (config)# → (config-XYZ)# → #`

---

### 2.2.6 A Note About Syntax Checker Activities

NetAcad’s **Syntax Checker** is a lightweight simulator focused on **exact command syntax**:

- You’re given a list of required commands.  
- You must type them **exactly** as instructed to move on.  
- It doesn’t support abbreviations or shortcuts the way real IOS / Packet Tracer does.

Use it to:

- Build **muscle memory** for core commands and modes.  
- Practice without worrying about “breaking” a real device.

Later, **Packet Tracer** lets you be more flexible (`conf t`, `int fa0/1`, etc.), closer to real gear.

---

### 2.2.7 Syntax Checker – Navigate Between IOS Modes

This specific activity makes you practice the whole path:

- `enable` / `disable`  
- `configure terminal`  
- `exit`  
- `line console 0`  
- `line vty 0 15`  
- `interface vlan 1`  
- and usually `end` / **Ctrl+Z**

Use this mini-checklist while doing it:

- Do I know **which mode** I’m in from the prompt?  
- Do I know **which command** moves me to the mode I want?  
- Can I get back to `Switch#` quickly with `end` / **Ctrl+Z`?  

If you can move around confidently without thinking about it, you’re ready for the later config sections.

---

### 2.2.8 Check Your Understanding – IOS Navigation

This mini-quiz is just making sure you really **own the prompts and mode changes**:

- **Q1 – “Which IOS mode allows access to all commands and features?”**  
  That’s the mode with full monitoring + management power.  
  👉 Think: the prompt that ends with `#` **before** any `(config)` text.

- **Q2 – “Which IOS mode are you in if `Switch(config)#` is displayed?”**  
  When you see `(config)#` after the hostname, you’re in **global configuration mode**, where you change device-wide settings.

- **Q3 – “Which IOS mode are you in if `Switch>` is displayed?”**  
  Prompt ending with `>` means **user EXEC mode** – basic, mostly “view-only” monitoring.

- **Q4 – “Which two commands would return you to the privileged EXEC prompt regardless of the configuration mode?”**  
  From *any* config/sub-config mode you can:
  - Use `end` to jump straight back to **privileged EXEC (`Switch#`)**.  
  - Press **`Ctrl+Z`** (same effect as `end`).  

  Notes for contrast:
  - `exit` only moves you **up one level** (e.g. `config-if` → `config` → `#`).  
  - `disable` drops you from **privileged EXEC → user EXEC (`Switch>`)**.  
  - `enable` goes **user EXEC → privileged EXEC**, not from config modes.

If you can look at a prompt and instantly say **which mode you’re in** and **which command gets you back to `Switch#`**, you’re solid for this quiz.

---
