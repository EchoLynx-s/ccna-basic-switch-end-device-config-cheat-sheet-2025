# CCNA – Basic Switch & End Device Configuration (Module 2)  
> Repo: `ccna-basic-switch-end-device-config-cheat-sheet-2025`

Quick-reference notes for **NetAcad CCNA – Module 2: Basic Switch and End Device Configuration**.  
Focus is on **IOS basics, device setup, IP addressing, and connectivity testing**.

> ⚠️ This is a **study helper**, not an answer key.  
> I use it to revise concepts and remember commands for labs, Packet Tracer, and exams.

---

## Table of Contents

- [Module 2 Overview](#module-2-overview)
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
  - [2.4.1 Device Names](#241-device-names)
  - [2.4.2 Password Guidelines](#242-password-guidelines)
  - [2.4.3 Configure Passwords](#243-configure-passwords)
  - [2.4.4 Encrypt Passwords](#244-encrypt-passwords)
  - [2.4.5 Banner Messages](#245-banner-messages)
  - [2.4.6 Video – Secure Administrative Access to a Switch](#246-video--secure-administrative-access-to-a-switch)
  - [2.4.7 Syntax Checker – Basic Device Configuration](#247-syntax-checker--basic-device-configuration)
  - [2.4.8 Check Your Understanding – Basic Device Configuration](#248-check-your-understanding--basic-device-configuration)
- [2.5 Save Configurations](#25-save-configurations)
  - [2.5.1 Configuration Files](#251-configuration-files)
  - [2.5.2 Alter the Running Configuration](#252-alter-the-running-configuration)
  - [2.5.3 Video – Alter the Running Configuration](#253-video--alter-the-running-configuration)
  - [2.5.4 Capture Configuration to a Text File](#254-capture-configuration-to-a-text-file)
  - [2.5.5 Packet Tracer – Configure Initial Switch Settings](#255-packet-tracer--configure-initial-switch-settings)
- [2.6 Ports and Addresses](#26-ports-and-addresses)
  - [2.6.1 IP Addresses](#261-ip-addresses)
  - [2.6.2 Interfaces and Ports](#262-interfaces-and-ports)
  - [2.6.3 Check Your Understanding – Ports and Addresses](#263-check-your-understanding--ports-and-addresses)
- [2.7 Configure IP Addressing](#27-configure-ip-addressing)
  - [2.7.1 Manual IP Address Configuration for End Devices](#271-manual-ip-address-configuration-for-end-devices)
  - [2.7.2 Automatic IP Address Configuration for End Devices](#272-automatic-ip-address-configuration-for-end-devices)
  - [2.7.3 Syntax Checker – Verify Windows PC IP Configuration](#273-syntax-checker--verify-windows-pc-ip-configuration)
  - [2.7.4 Switch Virtual Interface Configuration](#274-switch-virtual-interface-configuration)
  - [2.7.5 Syntax Checker – Configure a Switch Virtual Interface](#275-syntax-checker--configure-a-switch-virtual-interface)
  - [2.7.6 Packet Tracer – Implement Basic Connectivity](#276-packet-tracer--implement-basic-connectivity)
- [2.8 Verify Connectivity](#28-verify-connectivity)
  - [2.8.1 Video Activity – Test the Interface Assignment](#281-video-activity--test-the-interface-assignment)
  - [2.8.2 Video Activity – Test End-to-End Connectivity](#282-video-activity--test-end-to-end-connectivity)
- [2.9 Practice Ideas](#29-practice-ideas)
  - [2.9.1 Packet Tracer – Basic Switch and End Device Configuration](#291-packet-tracer--basic-switch-and-end-device-configuration)
  - [2.9.2 Lab – Basic Switch and End Device Configuration](#292-lab--basic-switch-and-end-device-configuration)
  - [2.9.3 What did I learn in this module?](#293-what-did-i-learn-in-this-module)
  - [2.9.4 Module Quiz – Basic Switch and End Device Configuration](#294-module-quiz--basic-switch-and-end-device-configuration)

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

## 2.3 The Command Structure

Topic objective: Understand how IOS commands are built, how to read the syntax, and how to use help + shortcuts so you don’t fight the CLI.

Think of this section as:

- how a command is **formatted**  
- how IOS tells you what’s wrong  
- and the little tricks that make typing faster.

---

### 2.3.1 Basic IOS Command Structure

Every IOS command follows the same basic pattern:

[prompt] command keyword(s) argument(s)

Examples:

Switch> show ip protocols
       ↑    ↑  ↑
     cmd  kwd arg

Switch> ping 192.168.10.5
       ↑    ↑
     cmd  argument (IP)

- **Prompt** – shows device + mode (`Switch>`, `Switch#`, `Switch(config)#`, etc.).
- **Command** – the main action (`show`, `ping`, `description`, `interface`, …).
- **Keyword(s)** – predefined words IOS expects after the command (`ip`, `protocols`).
- **Argument(s)** – user-supplied values like IPs, descriptions, VLAN IDs.

After you type the full command (with any required keywords/arguments), press **Enter** to send it to the IOS parser.

---

### 2.3.2 IOS Command Syntax Check

IOS docs use a few conventions to describe command syntax:

- **boldface** – literal commands/keywords you type exactly as shown.  
  - Example: **description** *string*
- *italics* – arguments where you supply the value.  
  - Example: `ping` *ip-address*

Brackets and braces:

- `[x]` – **optional** element (keyword or argument).
- `{x}` – **required** element.
- `[x {y | z}]` – optional block where you **must choose one** of the items in braces.

Examples:

ping ip-address

→ `ping` is the command, *ip-address* is the user-defined IP.

traceroute ip-address

→ same idea, different command.

Complex example from the course:

Switch(config-if)# switchport port-security aging { static | time time } type { absolute | inactivity }

- You must choose **one** of `static` or `time time`.
- You must also choose **one** of `absolute` or `inactivity`.

If a command is long in the docs, don’t panic. Read it like a sentence:

1. Base command.  
2. Required blocks in `{ }`.  
3. Optional bits in `[ ]`.

---

### 2.3.3 IOS Help Features

IOS gives you two big helpers:

1. **Context-sensitive help** (`?`)  
2. **Command syntax check** (error messages with a `^` marker)

Context-sensitive help answers:

- What commands exist **in this mode**?  
- What commands start with these letters?  
- What keyword/argument comes **next**?

Common patterns:

Switch> ?
Switch# ?
Switch(config)# ?

→ list of commands available in that mode.

Switch(config)# in?

→ IOS shows commands starting with `in` (e.g. `interface`, `ip`).

Switch(config)# interface ?

→ IOS shows what arguments `interface` accepts (e.g. `fastethernet`, `gigabitethernet`, `vlan`, `range`).

Command syntax check:

- IOS reads your command left to right.
- If something is wrong, it shows a message and usually a `^` under the problem spot:
  - `% Invalid input detected at '^' marker.`
  - `% Incomplete command.`
  - `% Ambiguous command.`

You use **help (`?`)** to discover valid options,  
and rely on the **syntax checker** to spot typos or missing pieces.

---

### 2.3.4 Video – Context Sensitive Help and Command Syntax Check

The video walks through practical uses of `?` and the syntax checker:

- `?` at different prompts (`>`, `#`, `(config)#`)  
  → each mode shows a **different** command list.
- Typing part of a command + `?`:
  - `in?` → IOS suggests `interface`.
- Typing command + space + `?`:
  - `interface ?` → shows valid next arguments (e.g. `fastethernet`, `gigabitethernet`, `vlan`, …).

Syntax checker behaviors:

- Wrong argument: `interface 33` → caret under `3` with “invalid input”.
- Ambiguous command: `i` alone, when both `interface` and `ip` exist.
- Incomplete command: `interface` with no argument.

**Takeaway:** if you’re stuck, hit `?` instead of guessing. IOS will tell you what it expects.

---

### 2.3.5 Hot Keys and Shortcuts

The IOS CLI has a bunch of editing and navigation shortcuts that save time.

Core ones to remember (and used in the video):

#### Command completion & shortening

- `Tab` – auto-completes a partially typed command *if it’s unique*.
  - `en` + Tab → `enable`
  - `conf` + Tab → `configure`
- **Command shortening** – you can type the minimum unique characters:
  - `conf t` instead of `configure terminal`
  - `int fa0/1` instead of `interface fastethernet 0/1`

#### History navigation

- `↑` / `↓` (Up / Down Arrow) – cycle through previous commands.  
  Great for re-running `show` commands or long interface commands.

#### Cursor movement

- `Ctrl + A` – jump to **start** of line.
- `Ctrl + E` – jump to **end** of line.
- `←` / `→` – move one character left/right.

#### Abort / exit keys

- `Ctrl + C`  
  - From config mode → back to **Privileged EXEC** (`Switch#`).  
  - Also aborts some operations (like a bad DNS lookup).
- `Ctrl + Z`  
  - From any config mode → back to **Privileged EXEC** (`Switch#`).
- `Ctrl + Shift + 6`  
  - “Break” key – interrupts long-running commands (pings, traceroutes, failed lookups, etc.).

#### Paging output (`--More--`)

When IOS pauses with `--More--`:

- `Enter` – next **line**.  
- `Space` – next **page**.  
- Any other key (except `y`) – stops the output and returns to the prompt.

Big picture: using these keys makes IOS feel *fast*, not painful.

---

### 2.3.6 Video – Hot Keys and Shortcuts

The video demo shows all of this in action:

- Using **Tab completion** to finish `enable` and `configure terminal`.
- Using **command shortening** (`int f0/1` instead of full `interface fastethernet 0/1`).
- Cycling through **command history** with Up/Down Arrow.
- Using **Ctrl+Z** and **Ctrl+C** to bounce back to Privileged EXEC and abort commands.
- **Ctrl+A / Ctrl+E** to jump to beginning/end of a long line.
- **Ctrl+Shift+6** to stop IOS trying to resolve mistyped commands as hostnames.
- **Ctrl+R** to redraw the line after log messages interrupt your typing  
  (note: not fully implemented in Packet Tracer, but real devices support it).

If you practice these in Packet Tracer while doing labs, they quickly become muscle memory.

---

### 2.3.7 Packet Tracer – Navigate the IOS

Activity focus:

- Move between **user EXEC, privileged EXEC, global config, and sub-modes**.
- Use **context-sensitive help (`?`)** to explore commands.
- Configure something simple (like the **clock**) using hints from `?`.
- Get comfortable with `enable`, `conf t`, `exit`, `end`, `Ctrl+Z`, and history keys.

Use this section as a checklist while you do the PT file.

---

### 2.3.8 Lab – Navigate the IOS by Using Tera Term for Console Connectivity

Skills you practice (real gear or PT physical mode):

1. **Access a switch via serial console**
   - PC → console cable → switch console port.
   - Configure Tera Term (or other client) for serial access.

2. **Display and configure basic device settings**
   - Use IOS modes + commands from 2.1 and 2.2:
     - `enable`, `configure terminal`
     - `hostname`, passwords, maybe interface basics.
   - Verify with `show` commands.

3. **(Optional) Mini-USB console to a router**
   - Same idea but different physical cable/port.

This lab ties everything together: physical connection, terminal client, IOS modes, basic commands, and your new shortcut skills.

---
## 2.4 Basic Device Configuration

**Topic objective:** Apply a basic and *secure* initial configuration to a Cisco switch:

- Give the device a meaningful hostname.
- Lock down **console**, **VTY**, and **privileged EXEC** access with passwords.
- Encrypt those passwords in the config file.
- Display a legal **banner** before login.
- Practice the full workflow in Syntax Checker / Packet Tracer.

---

### 2.4.1 Device Names

You’ve now seen IOS, modes, and commands. Time to start actually *configuring* the box.

The very first setting on a new device should be a **hostname** so you know what you’re connected to (especially over SSH).

**Hostname guidelines**

Good hostnames should:

- Start with a **letter**.  
- Contain **no spaces**.  
- End with a **letter or digit**.  
- Use only **letters, digits, and dashes** (`-`).  
- Be **less than 64 characters**.

Most orgs use a naming convention that encodes:

- **Location** (e.g. `Sw-Floor-1`, `Rtr-DC1`).  
- **Role** (core, distribution, access, lab, etc.).  

> Example naming convention: `Sw-Floor-1`, `Sw-Floor-2`, `Sw-Floor-3`.

**Set the hostname**

From privileged EXEC:

```text
Switch# configure terminal
Switch(config)# hostname Sw-Floor-1
Sw-Floor-1(config)#
```

To reset to the default name:

```text
Sw-Floor-1(config)# no hostname
Switch(config)#
```

Keep your documentation updated whenever a device is added or renamed.

---

### 2.4.2 Password Guidelines

Weak or reused passwords are still one of the **biggest** security problems.

Every network device (home routers, enterprise switches/routers, firewalls) should:

- Restrict **administrative access** with passwords or other auth (SSH keys, TACACS+, RADIUS).
- Use **different passwords** for console, VTY, and enable (in real networks).
- Prefer **encrypted storage** of passwords.

When choosing passwords in production:

- Use **more than eight characters** (aim for 12–16+).  
- Mix **upper/lowercase, numbers, symbols**.  
- Avoid **reusing** the same password on multiple devices.  
- Avoid **dictionary words** and obvious patterns.

> Note: In NetAcad labs you’ll often use simple passwords like `cisco` and `class`.  
> These are intentionally weak and only acceptable in **lab/demo** environments.

---

### 2.4.3 Configure Passwords

Here you actually configure **mode passwords**:

- Console (local, physical access).
- Privileged EXEC (`enable secret`).
- VTY lines (Telnet/SSH sessions).

You start in **user EXEC** when you first connect via console.

#### Secure console access (user EXEC)

```text
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# line console 0
Sw-Floor-1(config-line)# password cisco
Sw-Floor-1(config-line)# login
Sw-Floor-1(config-line)# end
Sw-Floor-1#
```

Now, to reach the user EXEC prompt you must enter the console password (`cisco` in this lab).

#### Secure privileged EXEC access (enable secret)

Privileged EXEC gives full access, so you **must** protect it.

```text
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# enable secret class
Sw-Floor-1(config)# exit
Sw-Floor-1#
```

- `enable secret` stores the password in **encrypted** form.  
- Prefer `enable secret` over `enable password`.

#### Secure VTY lines (remote access)

VTY (virtual terminal) lines control remote CLI sessions (Telnet/SSH).  
On many switches you have lines **0–15** (16 total).

```text
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# line vty 0 15
Sw-Floor-1(config-line)# password cisco
Sw-Floor-1(config-line)# login
Sw-Floor-1(config-line)# end
Sw-Floor-1#
```

Later, when you enable SSH, you’ll still use these VTY lines but usually with **username + password** or keys.

---

### 2.4.4 Encrypt Passwords

By default, many passwords in `running-config` / `startup-config` appear in **plaintext**, which is bad if someone can see the config.

To obfuscate all simple (type 0) passwords in the config, use:

```text
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# service password-encryption
Sw-Floor-1(config)# end
Sw-Floor-1#
```

Now check the config:

```text
Sw-Floor-1# show running-config
!
line con 0
 password 7 094F471A1A0A
 login
!
line vty 0 4
 password 7 094F471A1A0A
 login
!
line vty 5 15
 password 7 094F471A1A0A
 login
!
end
```

- The `7` indicates a **type 7** (weak) Cisco encryption.  
- This protects against casual shoulder-surfing / screenshots, not serious attackers.  
- The goal here is mainly to prevent anyone reading the config from seeing passwords in clear text.

---

### 2.4.5 Banner Messages

Passwords are not enough; you also want a **legal warning** for anyone accessing the device.

Use a **Message of the Day (MOTD) banner**:

```text
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# banner motd #Authorized Access Only#
```

Notes:

- The `#` is the **delimiter** — you can use any character that **does not** appear inside the message.
- Real banners often contain a full legal statement, for example:

```text
Sw-Floor-1(config)# banner motd #Authorized access only!
Violators will be prosecuted to the full extent of the law!#
```

After configuring the banner, every login attempt (console or VTY) will display it before prompting for a password.

---

### 2.4.6 Video – Secure Administrative Access to a Switch

The video walks through the full secure setup:

1. **Console access without a password** – shows the initial risk.  
2. Set a **console password** and enable `login`.  
3. Set an **enable secret** for privileged EXEC.  
4. Configure **VTY passwords** for remote access (lines `0 15`).  
5. Use `show running-config` to verify where passwords appear.  
6. Apply `service password-encryption` to encrypt console/VTY passwords.  
7. Configure a **MOTD banner** with a full legal warning.  
8. Exit and reconnect to confirm:
   - Banner shows on login.  
   - Console password is required.  
   - `enable` prompts for the secret.

This is your “**secure basics**” recipe for any lab switch.

---

### 2.4.7 Syntax Checker – Basic Device Configuration

The Syntax Checker activity makes you practice the whole sequence in order:

- Enter **global configuration mode**.
- Assign a **device name** (hostname).
- Secure **user EXEC** (console) access with a password + `login`.
- Secure **privileged EXEC** access with `enable secret`.
- Secure **VTY** lines (`line vty 0 15`) with password + `login`.
- Encrypt all plaintext passwords with `service password-encryption`.
- Configure a **login banner** (`banner motd ...`).

Use this mental checklist while working:

1. `enable`  
2. `configure terminal`  
3. `hostname ...`  
4. `line console 0` → `password ...` → `login` → `end`  
5. `configure terminal` → `enable secret ...`  
6. `line vty 0 15` → `password ...` → `login` → `end`  
7. `configure terminal` → `service password-encryption`  
8. `banner motd #...#`  

Once you can do that sequence from memory, you’re in great shape for the later labs and the exam.

---

### 2.4.8 Check Your Understanding – Basic Device Configuration

The quiz for this topic typically checks that you can:

- Recognize **good hostnames** vs bad ones.  
- Recall **strong password practices**.  
- Identify which commands secure:
  - Console (`line console 0`, `password`, `login`)  
  - VTY (`line vty 0 15`, `password`, `login`)  
  - Privileged EXEC (`enable secret`)  
- Know what `service password-encryption` does (and does **not**) protect.  
- Understand the purpose of a **MOTD banner**.

If you can explain, in your own words, how to:

1. Name the device,  
2. Lock down console + VTY + enable,  
3. Encrypt passwords, and  
4. Add a legal warning,

…then you’ve nailed **2.4 Basic Device Configuration**.

## 2.5 Save Configurations

**Topic objective:** Understand the difference between `running-config` and `startup-config`, how to save / roll back changes, and how to archive configs to a text file.

Think of this section as:

- where your config *lives* (RAM vs NVRAM),  
- how to **save** or **undo** changes,  
- and how to **export/import** configs using a terminal client.

---

### 2.5.1 Configuration Files

IOS keeps the device configuration in two main files:

- **running-config**  
  - Stored in **RAM** (volatile).  
  - Represents the *current* configuration in use.  
  - Any change you make in config mode updates `running-config` immediately.

- **startup-config**  
  - Stored in **NVRAM** (non-volatile).  
  - Loaded when the device boots or reloads.  
  - Only changes when you explicitly **save**.

Key commands:

```text
Sw-Floor-1# show running-config
Sw-Floor-1# show startup-config
```

Save the current running configuration to be used at next reload:

```text
Sw-Floor-1# copy running-config startup-config
Destination filename [startup-config]?  <press Enter>
```

> If the device loses power or reloads **before** you do `copy run start`, all unsaved changes are lost.

---

### 2.5.2 Alter the Running Configuration

Sometimes you change something and regret it. How you revert depends on whether you’ve already saved.

#### Case 1 – Bad changes **not saved** yet

Options:

- Manually remove or fix the changed commands in config mode, **or**
- Reload the device to go back to the last saved `startup-config`:

```text
Sw-Floor-1# reload
System configuration has been modified. Save? [yes/no]: no
```

Answer **no** so the current `running-config` is discarded and the device reloads using the existing `startup-config`.

Downside: the device is offline for a short time while it reloads.

#### Case 2 – Bad changes **already saved** to startup-config

You need to wipe the saved config and start fresh:

1. **Erase startup-config** from NVRAM:

   ```text
   Sw-Floor-1# erase startup-config
   Erasing the nvram filesystem will remove all configuration files! Continue? [confirm]
   ```

   Press **Enter** to confirm.

2. **Reload** to clear `running-config` from RAM:

   ```text
   Sw-Floor-1# reload
   ```

After reload, the switch comes up with its **factory default** config (no hostname, no passwords, etc.).

---

### 2.5.3 Video – Alter the Running Configuration

The video shows a full workflow:

- **Secure and name the switch**

  - Set hostname (`hostname S1`).
  - Configure console and enable passwords.
  - Save with:

    ```text
    S1# copy running-config startup-config
    ```

- **Where configs live**

  - `running-config` → RAM (volatile).
  - `startup-config` → NVRAM (non-volatile).
  - Use `dir nvram:` to see `startup-config`.

- **Command shortening**

  - Instead of full command:

    ```text
    copy running-config startup-config
    ```

  - Use:

    ```text
    copy run start
    ```

- **Reload with saved config**

  - `reload` → after reboot, hostname, banner, passwords all remain because `startup-config` was saved.

- **Erase config and reload**

  - From privileged EXEC:

    ```text
    S1# erase startup-config
    S1# reload
    ```

  - After reload, the switch comes up with default hostname `Switch` and no banner or passwords.

- **Revert to last saved config without reload**

  - Scenario:  
    1. Save configuration when hostname = `MySwitch`.  
    2. Make more changes (e.g. console password, change hostname to `S1`) but **don’t** save.  
    3. Decide you want to go back to the previous saved state.

  - Solution: copy **startup-config back into running-config**:

    ```text
    S1# copy startup-config running-config
    Destination filename [running-config]?  <press Enter>
    ```

  - The device immediately switches back to the hostname and settings from `startup-config` (e.g. `MySwitch`).

  - Note: `startup-config` is **merged** into `running-config`, it doesn’t necessarily wipe everything line by line, but for simple examples it effectively restores the previous state.

---

### 2.5.4 Capture Configuration to a Text File

You can archive configurations to a **text file** using your terminal emulator (PuTTY, Tera Term, etc.). This is great for backups, documentation, or cloning configs to another device.

Assume the switch is already configured and `running-config` is correct.

#### Exporting config to a text file

1. **Open** your terminal emulator and connect to the device (console or SSH).

2. **Enable logging** in the terminal app and choose where to save the file.

   Example in PuTTY:

   - Go to **Session → Logging**.
   - Select **“All session output”**.
   - Set **Log file name**, e.g. `MySwitchLogs.txt`.

3. From the switch, display the config you want to capture:

   ```text
   Sw-Floor-1# show running-config
   ```

   or

   ```text
   Sw-Floor-1# show startup-config
   ```

   Everything printed in the terminal window is written to the log file.

4. **Disable logging** after the output finishes.

   - In PuTTY, set **Session logging** back to **“None”**.

Now you have a text file with the full configuration.

#### Restoring a configuration from a text file

1. On the device, enter **global configuration mode**:

   ```text
   Switch# configure terminal
   ```

2. Open the saved text file on your PC, **select all**, and **copy**.

3. **Paste** the contents into the terminal window.

   - IOS will process each line as if you typed it manually.
   - Those commands become the new **running-config**.

You can then save it permanently with:

```text
Switch# copy running-config startup-config
```

---

### 2.5.5 Packet Tracer – Configure Initial Switch Settings

This PT activity puts everything from 2.4 and 2.5 into practice:

- Set basic switch identity:

  - `hostname`
  - passwords (console, VTY, enable secret)
  - banner message (MOTD)

- Secure access to:

  - **Console** (local admin)
  - **VTY lines** (remote admin via Telnet/SSH)
  - **Privileged EXEC** (`enable secret`)

- Use the correct save / verify commands:

  ```text
  Switch# show running-config
  Switch# copy running-config startup-config
  ```

End goal: a switch with secure administrative access whose configuration is **properly saved** and ready for reloads or power loss.

---
## 2.6 Ports and Addresses

Topic objective: Understand how IP addresses, interfaces, and ports fit together so you can see **where** traffic goes and **how** devices connect.

At this point you should be able to look at a PC or switch, check its IP settings, and know:

- what network it lives on  
- which gateway/router it uses to leave that network  
- which physical/logical port traffic is using  

---

### 2.6.1 IP Addresses

IP addresses are how devices find each other end-to-end across a network or the internet.  
Every end device that talks on an IP network needs an address.

Examples of devices that need IPs:

- Computers (workstations, laptops, file/web servers)
- Network printers
- VoIP phones
- Security cameras
- Smartphones and tablets
- Mobile handheld devices (e.g. wireless barcode scanners)

#### IPv4 basics

- IPv4 addresses are written in **dotted decimal**: `a.b.c.d`  
  - Each part (octet) is 0–255.
- IPv4 in this course is always used together with:
  - **Subnet mask** – identifies the *network* vs *host* portion.
  - **Default gateway** – router IP used to reach remote networks.

Example PC IPv4 config:

- IP address: `192.168.1.10`  
- Subnet mask: `255.255.255.0`  
- Default gateway: `192.168.1.1`

Here:

- `192.168.1.0/24` is the network.
- `.10` is the host address on that LAN.
- `192.168.1.1` is usually the router interface on that LAN.

#### IPv6 basics

IPv6 is the newer IP version gradually replacing IPv4.

- 128-bit address written in **hex**, groups separated by colons `:`.  
  Example: `2001:db8:acad:10::10`
- A **prefix length** (like `/64`) plays the role of the subnet mask.
- You still normally configure:
  - IPv6 address
  - Prefix length
  - Default gateway (often a link-local like `fe80::1`)

Example PC IPv6 config:

- IPv6 address: `2001:db8:acad:10::10`  
- Prefix length: `64`  
- Default gateway: `fe80::1`

IPv6 addresses are not case-sensitive – `ABCD` and `abcd` are treated the same.

---

### 2.6.2 Interfaces and Ports

To actually move bits around, you need **interfaces** (ports) and **media** (cables/wireless).

Common network media:

- **Copper** (twisted pair) – e.g. Ethernet cables (UTP)
- **Fiber-optic** – long distance, high bandwidth
- **Coaxial** – less common in modern LANs
- **Wireless** – Wi-Fi, cellular, etc.

Key differences between media types:

- **Maximum distance** the signal can travel
- **Environment** where they can be installed (indoor, outdoor, noisy, etc.)
- **Amount of data / speed** they can carry
- **Cost of cable + installation**

Each link needs:

1. A **specific media type** (copper, fiber, wireless), and  
2. A **matching interface** on the device (RJ-45 port, SFP fiber port, Wi-Fi NIC, etc.)

#### Switch ports and SVIs

Cisco IOS **Layer 2 switches**:

- Have many physical **Ethernet ports** for devices and uplinks.
- Forward frames using **MAC addresses** – they do *not* need an IP address just to switch traffic.

For management, switches use **Switch Virtual Interfaces (SVIs)**:

- An SVI is a **virtual Layer 3 interface** created in software (no physical port).
- It lets you manage the switch over the network using IPv4/IPv6 (SSH, Telnet, web, etc.).
- Default SVI: `VLAN 1` – comes “out of the box” on most switches.

Notes:

- The IP address you configure on the SVI is for **remote management**, not for normal L2 switching.
- A pure Layer 2 switch can forward frames even **without** any IP configured; the IP is just so *you* can reach the CLI remotely.

---

### 2.6.3 Check Your Understanding – Ports and Addresses

NetAcad gives you a short quiz here (3 questions, 70% to pass).  
Use this checklist before/while you answer:

- Can I explain the difference between:
  - IP address
  - Subnet mask / prefix length
  - Default gateway?
- Do I know which devices need IP addresses on a LAN?
- Do I know why a switch might have:
  - Many physical ports **but only one SVI** for management?
- Can I distinguish between:
  - Copper, fiber, and wireless in terms of distance/speed/cost?

If you can answer those confidently, you’re in good shape for this section.

