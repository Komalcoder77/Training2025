# Training2025
# Day 1 – Environment Setup

**Date:** 25th June 2025  
**Objective:** Setting up the environment for Linux and Virtualization-based training.

### ✅ Tasks Completed:
1. Installed **Oracle VirtualBox** – a free and open-source hosted hypervisor for x86 virtualization.
2. Installed **Microsoft Visual C++ Redistributable** – required for running certain Windows applications.
3. Downloaded and installed **Ubuntu (ISO)** – to use as the guest OS in VirtualBox.

### 🔗 Resources:
- [VirtualBox Download](https://www.virtualbox.org/)
- [Visual C++ Redistributables](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist)
- [Ubuntu ISO](https://ubuntu.com/download/desktop)
---
## 🔁 Booting and Its Types
**Booting** is the process of starting or restarting a computer system.  
There are two main types:

1. **Cold Booting** – When the system is powered on from an off state.
2. **Warm Booting** – When the system restarts without being turned off (e.g., using `Ctrl + Alt + Del`).
---

# Day 2 - Linux Basics: Kernel, Shell, Root, and Command

## Kernel
The **Kernel** is the core of an operating system.  
It manages system resources, memory, processes, and hardware communication.
---
![image](https://github.com/user-attachments/assets/339b746b-82f4-498d-aa6c-6fb7cdd6f1b7)

## Shell and Its Categories
The **Shell** is an interface between the user and the kernel.
---
### Types of Shells:
bash (most Common, Friendlist)
sh (Original Shell, basic)
zsh (fancy waiter, more features)
fish ( user-friendliness, interactive features)
---

## Root User
**Root** is the superuser in Linux systems.  
The root has full administrative privileges and access to all files and commands.
---

## 💻 Basic Linux Commands

| Command         | Description                                 |
|------------------|---------------------------------------------|
| `ls`            | Lists files and directories                 |
| `whoami`        | Displays the current logged-in user         |
| `date`          | Shows current date and time                 |
| `cd`            | Changes directory (`cd ..` to go up)        |
| `mkdir name`    | Creates a new directory                     |
| `cat file.txt`  | Displays contents of a file                 |
| `touch file.txt`| Creates an empty file                       |
| `cp src dest`   | Copies a file or folder                     |
| `pwd`           | Prints current working directory            |
| `whereis cmd`   | Locates the binary/source/man page of cmd  |
| `whatis cmd`    | Gives a one-line description of a command   |
| `mv src dest`   | Moves or renames a file or directory        |

![image](https://github.com/user-attachments/assets/3bca2ac1-b138-4f0d-9a87-be9547ca0f8c)
![image](https://github.com/user-attachments/assets/a0856ad2-5a84-4c10-bd5f-91fd95484e97)

## Day 3 – Linux File Permissions, Redirection & Pipes

### Topics Covered:

1. **File Permissions using `chmod`**
   - Modified file permissions to control access:
     - `chmod 444 file` → read-only for all users
     - `chmod 644 file` → read/write for owner, read-only for others
     - `chmod +x script.sh` → make a shell script executable

![image](https://github.com/user-attachments/assets/12fb724e-b6ac-41c3-9be9-33b9f4d3b1fa)

![image](https://github.com/user-attachments/assets/c1671d97-228f-4a92-9bdb-5c7406282a9c)
![image](https://github.com/user-attachments/assets/08f1da85-b34d-43e4-9a4e-929c5a4c2fc8)

2. **Shell Script Creation (`.sh` files)**
   - Created basic shell scripts using `nano`
   - Saved with `.sh` extension
   - Made executable using `chmod +x`
   - Ran scripts using: `./filename.sh`

3. **Input/Output Redirection**
   - Used redirection operators:
     - `>` → overwrite file
     - `>>` → append to file
     - `<` → read input from file
   - Example: 
    ![image](https://github.com/user-attachments/assets/ec2493be-4219-4c17-b206-0a8bc527b475)


4. **Pipes (`|`)**
   - Connected commands to filter/process output:
![image](https://github.com/user-attachments/assets/2e40ac72-9e72-4eea-b88f-b41968854132)
![image](https://github.com/user-attachments/assets/a32d62f7-2823-4db1-8455-3c4ce6e6532d)


# Example of using variable:
![image](https://github.com/user-attachments/assets/77d39b1f-ac93-4999-b6f2-7c92b60041d0)
![image](https://github.com/user-attachments/assets/60a7d512-4c33-48e2-abc3-457ea029a3df)

# Example of making table of a number:
![image](https://github.com/user-attachments/assets/f8dbd94e-0678-4c15-bfa5-c936928ddeae)

![image](https://github.com/user-attachments/assets/31c2524c-0979-42b4-b36c-260a95123fee)

# Example of comparing two numbers:
![image](https://github.com/user-attachments/assets/ff4dc72b-2fcf-46b7-8e83-c36111e9a466)
![image](https://github.com/user-attachments/assets/f8b2805c-57e6-495b-af55-2cbef454f565)


# 📘 Day 4 Training – Tech Basics

---

## 🔐 File Compression

File compression in Linux is the process of reducing the size of files or folders to save disk space or make them easier to transfer.

### 📌 Syntax

```bash
gzip file.txt
# creates file.txt.gz and deletes file.txt

gunzip file.txt.gz
# unzips the file file.txt.gz

gzip -k file.txt
# keeps both file.txt and file.txt.gz
```

## 🃏 Wildcards

Wildcards match files without typing their full names.

| Wildcard | Description                                 | Example             | Matches                               |
|----------|---------------------------------------------|---------------------|----------------------------------------|
| `*`      | Matches zero or more characters              | `ls *.txt`          | All `.txt` files                       |
| `?`      | Matches exactly one character                | `ls file?.txt`      | file1.txt, fileA.txt, etc.             |
| `[1-3]`  | Matches any one character in the brackets    | `ls file[1-3].txt`  | file1.txt, file2.txt, file3.txt        |
| `[^1]`   | Matches any one character NOT in the brackets| `ls file[^1].txt`   | All files except file1.txt             |
| `{a,b}`  | Matches either a or b (brace expansion)      | `echo {Jan,Feb}`    | Prints: `Jan Feb`                      |
| `\`      | Escapes a wildcard character                 | `ls \*.txt`         | Matches a file literally named `*.txt` |

---

## ✳️ Escaping Characters

Escaping characters are used in the Linux command line (like Bash) to prevent special characters from being interpreted by the shell.

> Escaping characters = telling the shell:  
> “Treat this symbol as a normal character, not something special.”

| Character | Purpose                                      | Example                      | Result                       |
|-----------|----------------------------------------------|------------------------------|------------------------------|
| `\`       | Escape special characters                    | `echo \*`                    | `*`                          |
| `\"`      | Escape double quote inside double quotes     | `echo "She said \"Hi\""`     | She said "Hi"                |
| `\'`      | Escape single quote (rare in single quotes)  | `echo 'It\'s OK'`            | May not work properly        |
| `\\`      | Escape backslash                             | `echo \\`                    | `\`                          |
| ``\` ``   | Escape backtick / command substitution       | `` `echo Hello` ``           | Hello                        |
| `\$`      | Escape dollar sign (prevent expansion)       | `echo \$HOME`                | `$HOME`                      |
| `\` inside `''` | No effect (literal backslash)         | `echo '\$HOME'`              | `\$HOME`                     |

---

## 🖥️ Hardware

Hardware refers to the **physical components** of a computer that you can touch and see.

| Category         | Examples                                 | Purpose                                      |
|------------------|------------------------------------------|----------------------------------------------|
| Input Devices     | Keyboard, Mouse, Microphone, Scanner     | Send data into the computer                  |
| Output Devices    | Monitor, Printer, Speakers               | Display or deliver results                   |
| Processing Unit   | CPU, GPU                                 | The "brain" – executes instructions          |
| Storage Devices   | HDD, SSD, USB Drive, CD/DVD              | Store data permanently or temporarily        |
| Memory            | RAM, Cache                               | Hold data temporarily for fast access        |
| Motherboard       | —                                        | Connects all components                      |
| Power Supply      | PSU                                      | Converts AC power into usable DC power       |
| Cooling System    | Fans, Heat Sinks                         | Prevents components from overheating         |
| Ports & Expansion | USB Ports, HDMI, PCIe                    | Connect external devices or add components   |

---

## 🧰 Key Components of CPU Cabinet

| Component              | Description                                                          |
|------------------------|----------------------------------------------------------------------|
| Motherboard            | Main board that connects all hardware components                    |
| CPU (Processor)        | Performs calculations and tasks                                      |
| RAM (Memory)           | Temporary fast memory for active tasks                              |
| Hard Drive / SSD       | Long-term storage for files and the OS                              |
| Power Supply (PSU)     | Converts power from wall to usable DC power                         |
| Cooling System         | Fans or liquid cooling to reduce heat                               |
| Optical Drive (optional)| Reads CDs/DVDs (becoming obsolete)                                 |
| Expansion Cards        | GPU, sound card, network card, etc.                                 |
| Ports & Connectors     | USB, HDMI, Ethernet for device connection                           |
| Cables & Wires         | Connect power and data between all components                       |

---

## 🧠 Difference Between RAM and Hard Disk

| Feature         | RAM (Random Access Memory)              | Hard Disk (HDD/SSD)                 |
|-----------------|------------------------------------------|--------------------------------------|
| Function        | Temporary memory used while running apps | Permanent storage for files and OS   |
| Data Storage    | Volatile (erased on shutdown)            | Non-volatile (data remains)          |
| Speed           | Very fast                                | Slower                              |
| Capacity        | 4GB to 32GB                              | 256GB to several TBs                |
| Use             | Active programs and processes            | Documents, software, system files    |
| Upgrade Benefit | Improves multitasking                    | Increases storage capacity           |

---

## ⚡ Difference Between RAM and Cache Memory

| Feature        | RAM                             | Cache Memory                          |
|----------------|----------------------------------|----------------------------------------|
| Function       | Holds OS and program data        | Stores frequently used CPU data        |
| Location       | On motherboard                   | Inside or close to CPU                 |
| Speed          | Fast                             | Faster than RAM                        |
| Size           | Larger (4–32GB)                  | Very small (KBs to a few MBs)          |
| Access Time    | Slower than cache                | Extremely fast                         |
| Volatility     | Volatile                         | Volatile                               |
| Purpose        | Supports system & application use| Minimizes CPU wait time                |
| Cost           | Cheaper per GB                   | More expensive per KB                  |

---

## 💾 ROM (Read-Only Memory)

ROM stands for **Read-Only Memory** — a **non-volatile** type of memory used in computers.

| Feature       | Description                                                    |
|----------------|----------------------------------------------------------------|
| Full Form      | Read-Only Memory                                               |
| Volatility     | Non-volatile (retains data after shutdown)                    |
| Function       | Stores firmware / startup instructions                        |
| Write Access   | Usually read-only; rarely updated                             |
| Speed          | Slower than RAM                                               |
| Examples       | BIOS, UEFI, Embedded firmware                                 |

---

## ⚙️ Process of Booting

The **booting process** is the sequence of steps a computer follows from power-on to running the OS.

| Step | Component              | Description                                                  |
|------|------------------------|--------------------------------------------------------------|
| 1    | Power Supply (PSU)     | Activates system power when turned on                       |
| 2    | Motherboard            | Supplies and distributes power to all components            |
| 3    | CPU                    | Begins fetching instructions                                |
| 4    | ROM (BIOS/UEFI)        | Runs POST (Power-On Self-Test)                              |
| 5    | RAM                    | Checked and then used to load system files                  |
| 6    | Storage Drive          | BIOS/UEFI locates bootloader in HDD/SSD                     |
| 7    | Bootloader             | Loads OS from disk into RAM                                 |
| 8    | Operating System       | Takes over and presents login or desktop screen             |

# day - 5

# 💽 Computer Hardware & Troubleshooting – Extended Notes

---

## 🗃️ What is HDD?

HDD (Hard Disk Drive) is a non-volatile storage device that stores and retrieves digital data using magnetic storage. It contains spinning disks (platters) and read/write heads.

### 🔑 Key Features
- Long-term data storage
- Uses magnetic platters and mechanical arms
- Slower than SSDs
- Large storage capacity at low cost

### 🧩 Types of HDD

| Type            | Description                                                      |
|------------------|------------------------------------------------------------------|
| PATA (IDE)       | Older standard, slow, now obsolete                               |
| SATA             | Common in modern desktops/laptops                                |
| SCSI             | Used in servers, supports multiple devices, high performance     |
| SSHD             | Hybrid: SSD speed + HDD capacity                                 |
| External HDD     | Portable, connects via USB                                       |
| Enterprise HDD   | For servers/data centers, 24/7 operation                         |

### 📏 HDD Form Factors

| Form Factor | Usage             |
|-------------|-------------------|
| 3.5 inch    | Desktop computers |
| 2.5 inch    | Laptops, compact PCs |

> 💡 **Note:** SSD (Solid-State Drive) is not a type of HDD but serves the same purpose — storage. SSDs have no moving parts and are much faster.

---

## 🎮 GPU (Graphics Processing Unit)

A specialized processor for rendering images, videos, animations, and visual content.

### ⚠️ What Causes GPU Failure?

| Cause            | Description                                          |
|------------------|------------------------------------------------------|
| Overheating      | Dust, fan failure, poor airflow                      |
| Power Surges     | Electric surges or unstable PSU                      |
| Driver Conflicts | Corrupt or outdated drivers                          |
| Physical Damage  | Dropping or improper handling                        |
| Age/Wear         | Heavy use over time causes degradation               |

### 🛠️ What to Do When GPU Fails

| Step                         | Action                                                              |
|------------------------------|---------------------------------------------------------------------|
| Check Connections            | Reseat GPU, check cables                                            |
| Clean the Card               | Remove dust, clean fans                                             |
| Switch to Integrated Graphics| Remove GPU, use onboard graphics                                    |
| Try GPU on Another PC        | Test card on a different system                                     |
| Stress Test                  | Use FurMark / GPU-Z to monitor temp & performance                   |
| Reinstall Drivers            | Use DDU to clean old drivers, install fresh ones                    |
| Check Temperature            | Use MSI Afterburner or similar tools                                |

> 🔧 **If GPU is dead:**  
- If under warranty: Contact manufacturer  
- If not: Replacement is recommended unless minor (e.g., fan) issue

---

## 🔌 PSU (Power Supply Unit)

### ⚠️ Symptoms of PSU Issues
- PC won’t power on
- Random shutdowns or reboots
- Burning smell or electrical noise
- Flickering lights or fans

### 🔎 Diagnosis Steps

| Method                    | How To Do It                                                  |
|---------------------------|---------------------------------------------------------------|
| Check Power Cable/Outlet  | Test with a known working cable/outlet                        |
| Paperclip Test (ATX PSU)  | Short green & black wires on 24-pin connector                 |
| Multimeter Test           | Check 12V, 5V, 3.3V rails                                      |
| Try Another PSU           | Swap with working PSU to confirm                              |

> ⚠️ **Safety Tips:**
- Always unplug the PC before opening
- Ground yourself
- Don’t repair PSU unless professionally trained

---

## 🐌 PC Running Slow – Causes & Fixes

| Issue                    | Explanation                                      | Fix/Solution                                                   |
|--------------------------|--------------------------------------------------|----------------------------------------------------------------|
| Too Many Startup Apps    | Slows boot time                                  | `Ctrl + Shift + Esc → Startup → Disable unnecessary apps`      |
| Low RAM                  | Can’t multitask well                             | Upgrade RAM to 8GB+                                            |
| Fragmented HDD           | File access delays (HDD only)                    | Run Disk Defragmenter                                          |
| Old/Faulty HDD           | Degrading speed                                  | Replace with SSD                                               |
| Background Processes     | Resource hogging apps                            | End unnecessary processes from Task Manager                    |
| Virus/Malware            | System lag & damage                              | Scan with antivirus                                            |
| Outdated Drivers         | Causes lag or crashes                            | Update from Device Manager or manufacturer site                |
| Overheating              | Thermal throttling slows system                  | Clean fans, apply thermal paste                                |
| Too Many Browser Tabs    | High RAM usage                                   | Close tabs, use light browsers                                 |
| Background Updates       | Slows performance                                | Let updates finish or pause                                    |
| Weak CPU                 | Can’t handle new apps                            | Upgrade processor (if possible)                                |

---

## 🖨️ Common Printer Problems & Solutions

| Issue                | Cause                              | Solution                                      |
|----------------------|------------------------------------|-----------------------------------------------|
| Not Printing         | Loose cable / offline / driver     | Check connections; update driver              |
| Printer Offline      | Manual setting or network issue    | Set printer online in settings                |
| Paper Jam            | Misaligned or stuck paper          | Carefully remove paper & debris               |
| Low Ink              | Empty or clogged cartridge         | Replace/refill cartridge; clean printhead     |
| Poor Print Quality   | Dirty nozzle / wrong settings      | Run nozzle cleaning tool                      |

---

## 🧨 BSOD (Blue Screen of Death)

BSOD is a critical Windows error screen caused by system crashes.

### 💥 What Causes BSOD?

| Cause                  | Explanation                                             |
|------------------------|---------------------------------------------------------|
| Faulty Drivers         | Incompatible or corrupt                                 |
| Hardware Failure       | RAM, GPU, HDD issues                                    |
| Corrupt System Files   | Damaged Windows components                              |
| Malware                | Can corrupt system processes                            |
| Update Issues          | Failed or incomplete Windows updates                    |
| Overclocking/BIOS      | Unstable configuration                                  |

### 🛠️ Crash Analysis Tools
- **Event Viewer** – View system logs
- **WinDbg** – Analyze crash dump files

---

## 🧬 BIOS/UEFI & POST

| Term     | Description                                                                 |
|----------|-----------------------------------------------------------------------------|
| BIOS     | Traditional firmware for booting                                            |
| UEFI     | Modern firmware with faster boot, graphical UI, mouse support               |

### 🔧 Common BIOS Settings

| Setting         | Description                                             |
|------------------|--------------------------------------------------------|
| Boot Order       | Choose drive to boot from                              |
| Secure Boot      | Protects against unauthorized OS                       |
| XMP Profile      | Enables RAM to run at full speed                       |
| Fan Control      | Adjust fan speed                                       |
| Virtualization   | Enables VM support                                     |
| SATA Mode        | Switch between AHCI/IDE for SSDs/HDDs                  |

---

## 🧪 What is POST?

POST = Power-On Self-Test  
It checks hardware before booting OS.

### 🚨 Common POST Errors

| Error               | Cause                        | Fix                                   |
|---------------------|------------------------------|----------------------------------------|
| No Display / Beeps  | RAM not detected             | Reseat or change RAM                  |
| Continuous Beeps    | GPU or CPU issue             | Recheck installation or replace       |
| No Beep / No Boot   | PSU or motherboard failure   | Test with another PSU                 |
| CMOS Error          | Dead CMOS battery            | Replace battery (CR2032)              |
| Boot Device Missing | Drive not found              | Reconnect drive, check boot order     |
| Overclock Failed    | Unsafe BIOS settings         | Reset BIOS to default                 |

---

### ⚙️ Accessing and Resetting BIOS

| Action             | Steps                                      |
|--------------------|---------------------------------------------|
| Access BIOS        | Press `Del`, `F2`, or `Esc` during startup |
| Reset BIOS         | Select “Load Setup Defaults” or remove CMOS battery |
| Update BIOS        | Download from motherboard website          |

# Day - 6
# Safe Mode
Safe Mode is a diagnostic mode in an operating system that starts the system with only essential files and drivers. It helps in fixing problems like software errors, driver conflicts, or malware.

### Types :

**1. Safe Mode –** Starts with basic drivers only.

**2. Safe Mode with Networking –** Includes internet/network drivers.

**3. Safe Mode with Command Prompt –** Opens Command Prompt instead of the normal desktop.

# Recovery Tools
Recovery tools are built-in or external tools used to troubleshoot, fix, or restore the system to a previous or working state.

### Types:

**System Restore –** Rolls back the system to a previous restore point.

**Startup Repair –** Fixes boot-related issues.

**Reset This PC –** Reinstalls Windows (with or without keeping files).

**Recovery Drive or Disk –** External drive used to access recovery options.

# OS Repair (Operating System Repair)
OS Repair refers to methods used to fix corrupted or missing system files without completely reinstalling the operating system.

Use repair commands:

sfc /scannow – Scans and restores system files.
DISM /Online /Cleanup-Image /RestoreHealth – Repairs corrupted Windows images.
Bootable USB for repair and system reinstall.

# Virus and Malware Symptoms

* Slow performance
* Frequent pop-ups
* Programs crashing
* Unknown apps installed
* Browser redirecting to strange websites

# Basic Virus/Malware Removal

**Using Safe Mode –** Run antivirus in safe environment.

**Using Antivirus Software –** Scan and delete threats.

**Using Malware Removal Tools –** Like Malwarebytes, AdwCleaner.

**Manual Removal –** Deleting infected files and apps.

**Resetting System –** Reinstall OS if damage is severe.

# Ways to back up Windows:

**1. File History -** Backs up personal files (Documents, Pictures, etc.) to an external drive automatically.

**2. Backup and Restore (Windows 7) -** Creates regular backups or a full system image. Still available in newer Windows versions.

**3. System Image Backup -** Makes a complete copy of your system, including OS and settings. Useful for full recovery.

**4. OneDrive (Cloud Backup) -** Backs up important folders (Desktop, Documents, Pictures) to the cloud.

**5. Manual Backup -** Copy important files manually to an external hard drive or USB.

**6. Third-Party Backup Tools -** Use software like Acronis, Macrium Reflect, or EaseUS for full or scheduled backups.

# RJ45 (Registered Jack 45) :
RJ45 is a standard connector used to connect computers and networking devices like routers and switches using Ethernet cables.

### Key Points about RJ45:

# How to Make a RJ‐45 Cable:
1. Strip the cable to remove 1 inch of the outer sheath.
2. Untwist and straighten the wires inside of the cable
3. Arrange the wires into the right order as following.

|Pin| Number	Wire Color (T568B)	|
|---|---------------------------|
|1|	White Orange	|
|2|	Orange	Transmit| 
|3|	White Green	Receive| 
|4|	Blue	Unused |
|5|	White Blue	Unused |
|6|	Green	Receive |
|7|	White Brown	Unused |
|8|	Brown|

![image](https://github.com/user-attachments/assets/08b500e9-2e5c-4696-9c11-00a7df39b5d0)

4. Trim the wires into an even line 1⁄2 inch (13 mm) from sheathing
5. Insert the wires into the RJ-45 connector.
6. Stick the connector into the crimping part of the tool and squeeze twice.
7. Remove the cable from the tool and check that all of the pins are down & test the cable.

# Day -7
# Networking  Basics
### Hosts :
A host refers to any device that connects to a network and is capable of sending or receiving data. This includes:

* Computers (Desktops, Laptops)

* Servers

* Smartphones

* Printers

* IP cameras

* IoT devices (like smart TVs, smart bulbs, etc.)

![host](https://github.com/user-attachments/assets/1beb5235-156d-475e-ac26-dc22f161f254)

# Network :
A network is a group of two or more connected devices (like computers, servers, or mobile phones) that are linked together to share resources, exchange data, and communicate with each other. These devices are connected using wired (like Ethernet cables) or wireless (like Wi-Fi) communication methods.

**Key Features:**
Data sharing (files, messages)

Resource sharing (printers, internet)

Communication (email, video calls)

Centralized or distributed control

# IP Address:
An IP address (Internet Protocol address) is a unique number assigned to each device connected to a network. It helps in identifying and locating devices so they can communicate with each other over the internet or a local network.

### Types of IP Addresses
**1. Public IP Address :** Assigned to your network by your Internet Service Provider (ISP), allowing devices within your network to communicate with the internet.

**2.Private IP Address :** Used within a private network (e.g., home or office) and not routable over the internet. Devices within the same local network communicate using private IPs.

### Properties of an IP Address:
**1. Unique**
* Every IP address must be unique within a network.

* This means no two devices on the same network can have the same IP address.

* If two devices have the same IP, it leads to IP address conflicts, and communication may fail.

* Example: If your laptop has the IP 192.168.1.10, no other device in that network can use the same address at the same time.

**2. Universal**
* IP addresses follow a universal standard that is understood worldwide.

* No matter where you are, IP addresses follow the same format (IPv4 or IPv6).

* This allows devices from different parts of the world to communicate with each other over the internet.

* It ensures global connectivity and compatibility between networks and devices.

### IPv4 (Internet Protocol Version 4):
**Address Length:**

* IPv4 uses a 32-bit address format.

* This means the IP address is made up of 32 binary digits (0s and 1s).

**Notation:**

* IPv4 addresses are written in decimal format.

* The 32 bits are divided into 4 groups, called octets.

* Each octet is separated by a dot (.).

* Each octet can range from 0 to 255.

* Example: 192.168.1.1.

**Address Space:**

* Since IPv4 uses 32 bits, it can have 2³² = 4,294,967,296 unique addresses.

* This gives approximately 4.3 billion possible IP addresses.

* Due to the large number of internet-connected devices, this space is becoming exhausted.

### IPv6 Explanation in Points
**Address Length:**

* IPv6 uses a 128-bit address format.

* This means each IP address is made up of 128 binary digits (0s and 1s).

* It provides a much larger range than IPv4.

**Notation:**

* IPv6 addresses are written in hexadecimal format.

* The 128 bits are divided into 8 groups, each containing 4 hexadecimal digits.

* Groups are separated by colons (:).

* Example: 2001:0db8:85a3:0000:0000:8a2e:0370:7334

**Address Space:**

* IPv6 provides 2¹²⁸ = 340 undecillion unique addresses.

* This is enough to assign trillions of addresses to every person or device on Earth.

* The huge space ensures scalability for the future internet.

### IPv4 vs IPv6:

|Feature|	IPv4|	IPv6|
|-------|-----|-----|
|Address Length|	32 bits (4 octets)|	128 bits (16 octets)|
|Address Format|	Decimal (e.g., 192.168.1.1)|	Hexadecimal (e.g., 2001:0db8::1)|
|Address Space|	~4.3 billion addresses|	~340 undecillion addresses|
|Configuration|	Manual or DHCP|	Auto-configuration (SLAAC) or DHCPv6|

![IP](https://github.com/user-attachments/assets/693b218c-c492-4a09-9aef-d6f8d4343d47)

# Notation:
### Binary Notation (used internally in networking)
* In binary notation, an IP address is written in binary (base-2) numbers — using only 0s and 1s.

* IPv4 addresses are made up of 32 bits, which are grouped into 4 sets of 8 bits (called octets).

* Computers use this format to understand and process IP addresses.

* Example:
Binary: 11000000.10101000.00000001.00000001
This represents the IP address in binary form.

### 2. Dotted Decimal Notation (used by humans)
* In dotted decimal notation, the 32-bit binary address is converted into 4 decimal numbers.

* Each 8-bit binary group (octet) is converted to a number between 0 and 255.

* The four decimal numbers are separated by dots (.).

* This is the standard readable format for IPv4 addresses.

* Example:
Binary:      11000000.10101000.00000001.00000001  
Decimal:     192      .168      .1        .1  
IPv4 Address: 192.168.1.1

# Classful Addressing in IP (IPv4)
Classful addressing is a system used in IPv4 to divide the IP address space into five classes (A to E) based on the first few bits of the IP address. Each class has a different range, size of network and host portions, and specific use.

This method helps in identifying how much of the IP address is used for the network part and how much is used for the host part.

### Structure of IPv4 Address:
* IPv4 address = 32 bits

* Divided into network part and host part (depending on the class)

**IP Address Classes:**  
|Class|	Starting Bits|	Range of First Octet|	Network/Host Bits	|No. of Hosts	Use|
|-----|--------------|---------------------|-------------------|----------------|
|A|	0xxxxxxx|	1 – 126|	8 bits (N) / 24 bits (H)|	~16 million per network	Large networks|
|B|	10xxxxxx|	128 – 191|	16 bits (N) / 16 bits (H)|	~65,000 per network	Medium-sized networks|
|C|	110xxxxx|	192 – 223|	24 bits (N) / 8 bits (H)|	254 hosts per network	Small networks|
|D|	1110xxxx|	224 – 239|	Not divided (multicast)|	Not for host addressing	Multicast communication|
|E|	1111xxxx|	240 – 255|	Reserved	Not used for devices|	Research & Experimental use|

 **Key Points of Classful Addressing:**
* Divides IP addresses into fixed classes (A–E).

* Helps in identifying the size of the network.

* Simple but wastes IP addresses (not efficient).

* Replaced by Classless Addressing (CIDR) for better IP utilization.

![462012671-628b0cc6-8c90-454d-bccd-ac12a5129733](https://github.com/user-attachments/assets/b3f6a8cc-aad9-4817-8579-827996df669d)

# Broadcast vs. Multicast vs. Unicast :

|Parameters|	Unicast|	Broadcast|	Multicast|
|----------|--------|----------|----------|
|Basics|	There is only one receiver and one sender.|	There are multiple receivers and one sender.|	There are multiple receivers and multiple senders.|
|Meaning and Definition|	Unicast is used to transfer data from a single sender to a single recipient.|	Broadcast sends data from one sender to all devices on a network.|	Multicast sends data from one or more senders to a selected group of receivers.|
|Mapping|	One-to-one type of communication.|	One-to-many type of communication.|	Many-to-many type of communication.|
|Uses|	Used for direct communication like web browsing, emails, etc.|	Used in TV/radio networks, ARP, DHCP discovery, etc.|	Used in stock exchanges, live video streaming, multimedia delivery.|

# Subnetting:
Subnetting is the process of dividing a large IP network into smaller, manageable sub-networks called subnets. It helps in efficient use of IP addresses, reduces network traffic, and improves security by isolating different parts of a network.
or 
Dividing a large network into smaller, more manageable sub-networks. It helps to utilize the network bandwidth in more intelligent way.

* Bandwidth: Capacity of network; data transmission rate (e.g., Mbps). Should be maximum.

* Latency: Delay in data transmission. Should be minimum.

* Host Bits: Denoted by '0's in subnet mask.

* Network IP: First IP of a subnet (cannot be assigned to host).

* Broadcast IP: Last IP of a subnet (cannot be assigned to host).

![image](https://github.com/user-attachments/assets/3dae5fc9-981f-4c78-b36a-b41a616dffcb)

### Subnet Mask :
A subnet mask is a 32-bit number used to separate the network part and the host part of an IP address. It helps identify which portion of the IP address refers to the network and which part refers to the host within that network.

* Example:
For IP 192.168.1.10 and subnet mask 255.255.255.0,

255.255.255.0 means the first 3 octets are the network part,

The last octet is for hosts.
### MAC (Media Access Control Address):

**Nature:** A unique, 12-character hexadecimal (alphanumeric) attribute used to identify individual electronic devices on a network.
Distinction from IP Address:
**MAC Address:** Identifies the physical location of a device within a local network. It's like your permanent home address. The manufacturer provides it.
**IP Address:** Signifies the device's global or internet-accessible identity. It's more like a temporary vacation rental address, changing depending on your network connection.

### DNS (Domain Name System):
It is a naming system for computers, service etc connected to the Internet or a private network. It translates domain names (www.google.com) into machine-readable IP addresses (172.217.160.142).

**Default Gateway:**
Its a device (typically a router) that acts as a pathway for data to leave a local network and reach other networks, including the internet.

### CIDR (Classless Inter-Domain Routing):
Modern method for IP allocation and routing, replacing classful addressing with more flexible network sizing (e.g., /24).
**Types of Cables**
**Twisted Pair:**
Types: Shielded (STP) and Unshielded (UTP).
Use: LANs (Ethernet).
**Coaxial:**
Use: TV networks, older computer networks.
**Fiber-Optic:**
Use: High-speed networks, long distances (most commonly used today).

# Numerical:

For 205.150.65.0/26. Find:
Subset mask
Number of subsets
Number of hosts
Network IP
Broadcast IP.

**Solution:**
1. Subnet Mask
/26 means 26 bits are used for the network portion.

So, the subnet mask in decimal is:

Copy
Edit
11111111.11111111.11111111.11000000 → 255.255.255.192
Subnet Mask = 255.255.255.192

2. Number of Subnets
Given: It's from Class C (default /24), and we're using /26

Subnet bits = 26 - 24 = 2 bits

Number of subnets = 2² = 4

Number of Subnets = 4

3. Number of Hosts per Subnet
Host bits = 32 - 26 = 6 bits

Number of hosts = 2⁶ - 2 = 64 - 2 = 62
(Subtract 2 for Network & Broadcast addresses)

Number of Hosts = 62 per subnet

4. Network IP (of first subnet)
Subnet range = 2⁶ = 64 IPs per subnet

First subnet starts at:

Network IP = 205.150.65.0

5. Broadcast IP (of first subnet)
Broadcast = Last IP of the subnet

First subnet = 205.150.65.0 – 205.150.65.63

Broadcast IP = 205.150.65.63
