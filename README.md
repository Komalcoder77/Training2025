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

# 📘 Day 6: System Recovery, Backup & Network Tools

---

## 🛠 Safe Mode

Safe Mode boots the system with minimal drivers and services. It's primarily used for fixing critical errors caused by faulty drivers, updates, or malware.

### Types of Safe Mode:

- **Basic Safe Mode:** Starts with essential drivers and services only.
- **Safe Mode with Networking:** Adds network/internet drivers.
- **Safe Mode with Command Prompt:** Launches the system with only Command Prompt for advanced troubleshooting.

---

## 🔧 Recovery Tools in Windows

Recovery tools help you restore your system to a stable state without needing a complete reinstall.

### Key Tools:

- **System Restore:** Reverts system settings to a saved point.
- **Startup Repair:** Scans and fixes boot-related errors.
- **Reset This PC:** Fresh install with an option to keep or remove personal files.
- **Recovery Drive:** USB tool for offline troubleshooting and reinstallation.

---

## 🧩 Operating System Repair

Instead of reinstalling the OS, some tools allow system file repair:

- `sfc /scannow`: Scans and restores corrupt system files.
- `DISM /Online /Cleanup-Image /RestoreHealth`: Repairs Windows system image.
- Bootable USB: Used to repair or reinstall the OS.

---

## 🦠 Signs of Virus/Malware Infections

- Unusual slowness
- Sudden pop-up ads
- Unknown programs appearing
- Browser redirection
- Apps crashing frequently

---

## 🔐 Virus & Malware Removal Methods

- **Safe Mode Scan:** Run antivirus in a low-risk environment.
- **Antivirus Programs:** Detect and remove malicious files.
- **Malware Removal Tools:** Tools like Malwarebytes or AdwCleaner.
- **Manual Deletion:** Delete suspicious apps/files (advanced).
- **Reset PC:** Use as a last resort for deep infections.

---

## 💾 Methods for Backing Up Windows

1. **File History:** Auto-backup of personal files to external storage.
2. **Backup and Restore (Win7):** Create system image or schedule backups.
3. **System Image Backup:** Full snapshot of your OS and settings.
4. **OneDrive:** Cloud-based backup of common folders.
5. **Manual Backup:** Copy essential data to USB/External HDD.
6. **Third-Party Tools:** Apps like Acronis, EaseUS for scheduled backups.

---

## 🔌 RJ45 Cable

RJ45 connectors are standard for Ethernet-based network connections.

### RJ-45 Cable Making (T568B Standard):

| Pin | Color            | Use        |
|-----|------------------|------------|
| 1   | White-Orange     | Transmit   |
| 2   | Orange           | Transmit   |
| 3   | White-Green      | Receive    |
| 4   | Blue             | Unused     |
| 5   | White-Blue       | Unused     |
| 6   | Green            | Receive    |
| 7   | White-Brown      | Unused     |
| 8   | Brown            | Unused     |

**Steps:**
1. Strip ~1 inch of the outer cover.
2. Untwist and arrange wires.
3. Align as per T568B.
4. Trim wires evenly.
5. Insert into connector.
6. Crimp with tool.
7. Test the cable.

---

# 📘 Day 7: Networking Fundamentals

---

## 💻 Hosts in a Network

A **host** is any device that communicates over a network — like computers, mobile phones, printers, IP cameras, or smart appliances.

---

## 🌐 Network Definition

A **network** is a group of interconnected devices for sharing data and resources (e.g., files, internet, printers).

### Key Features:

- File/data exchange
- Centralized control
- Remote access
- Shared resources

---

## 📍 IP Address Basics

An **IP Address** is a unique identifier for a device on a network.

### Types:

- **Public IP:** Provided by ISP, globally reachable.
- **Private IP:** Used within local networks, not routable online.

### Properties:

- **Unique:** No IP duplication allowed in the same network.
- **Universal:** Same structure used globally.

---

## 📊 IPv4 vs IPv6

| Feature         | IPv4                   | IPv6                           |
|-----------------|------------------------|--------------------------------|
| Length          | 32-bit                 | 128-bit                        |
| Format          | Decimal (e.g., 192.168.0.1) | Hexadecimal (e.g., 2001:0db8::1) |
| Address Space   | ~4.3 billion           | ~340 undecillion               |
| Notation        | 4 Octets               | 8 groups, 4 hex digits each    |

---

## 🧮 IP Address Representation

- **Binary Notation:** Used internally by computers.
- **Dotted Decimal:** Used by humans. e.g., `192.168.0.1`

---

## 🏷 Classful Addressing (IPv4)

| Class | Range       | Network/Host Bits | Hosts per Network | Usage                 |
|-------|-------------|-------------------|-------------------|------------------------|
| A     | 1–126       | 8N / 24H           | ~16 million       | Huge networks          |
| B     | 128–191     | 16N / 16H          | ~65K              | Medium-sized networks  |
| C     | 192–223     | 24N / 8H           | 254               | Small networks         |
| D     | 224–239     | N/A                | Multicast only    | Multicast communication|
| E     | 240–255     | Reserved           | N/A               | Research               |

---

## 🔁 Communication Types

| Type     | Sender | Receiver(s)     | Use Case                          |
|----------|--------|-----------------|-----------------------------------|
| Unicast  | 1      | 1               | Web browsing, email               |
| Broadcast| 1      | All on network  | DHCP, ARP                         |
| Multicast| 1+     | Selected Group  | Video streaming, stock updates    |

---

## 🔢 Subnetting Essentials

**Subnetting** breaks a large network into smaller, efficient sub-networks to reduce congestion and boost performance.

- **Bandwidth:** Data transfer rate (↑ better)
- **Latency:** Delay in communication (↓ better)
- **Network IP:** First address in a subnet
- **Broadcast IP:** Last address (reserved)

---

## 🧮 Subnet Mask

Used to distinguish between network and host portions of an IP.

**Example:**
IP: 192.168.1.10  
Mask: 255.255.255.0 → First 3 octets for network

---

## 🆔 MAC Address

A **MAC Address** is a permanent, physical ID assigned to a device by its manufacturer. It's used locally, unlike IP addresses which are logical and changeable.

---

## 🌍 DNS - Domain Name System

DNS converts human-readable web addresses like `www.google.com` into machine-readable IPs like `142.250.77.238`.

---

## 🛤 Default Gateway

The **default gateway** is your device’s door to the external network (usually your router).

---

## 🔢 CIDR - Classless Inter-Domain Routing

CIDR allows flexible subnetting using notation like `/24`, replacing rigid classes.

---

## 📡 Types of Network Cables

- **Twisted Pair (UTP/STP):** Common in LANs
- **Coaxial:** Used in older networks, TV
- **Fiber Optic:** Fastest; used for long-distance data

---

## 🧠 Numerical Example:

**Given:** `205.150.65.0/26`

1. **Subnet Mask:**  
   26 bits → 255.255.255.192

2. **Subnets Possible:**  
   /26 from Class C (/24) → 2 bits → `2² = 4`

3. **Hosts per Subnet:**  
   32 - 26 = 6 bits → `2⁶ - 2 = 62`

4. **Network IP:**  
   First Subnet starts at → `205.150.65.0`

5. **Broadcast IP:**  
   First Subnet ends at → `205.150.65.63`

# 🛠️ Training Day: 08

## 🧠 What is DHCP?
**DHCP – Dynamic Host Configuration Protocol**

### 📌 Definition:
DHCP is a network protocol that automatically gives IP addresses to devices (like your phone, computer, etc.) when they connect to a network.

### 🔧 Why is DHCP used?
- To avoid manual IP configuration.
- To save time and reduce mistakes.
- Makes it easy to manage IPs in big networks.

### 🧠 How it Works (Simple Steps):
1. You connect your device to Wi-Fi.
2. Your device asks for an IP address.
3. The DHCP server picks a free IP and gives it to your device.
4. You are now connected to the network and internet!

### 📎 Example:
You connect your laptop to Wi-Fi.  
DHCP gives it IP: `192.168.1.5`  
Next time, it may give a different IP like `192.168.1.8`.

### 🧾 Key Terms:

| Term         | Meaning                                      |
|--------------|----------------------------------------------|
| DHCP Server  | The device (router or server) that gives IP addresses |
| DHCP Client  | The device (your phone, PC, etc.) that gets an IP    |

### 🔄 Without DHCP vs With DHCP

| Action         | Manual IP (No DHCP) | DHCP (Automatic)     |
|----------------|---------------------|-----------------------|
| Set IP Address | You do it manually  | Given automatically   |
| Easy to Use?   | ❌ No               | ✅ Yes               |
| Error chances  | High                | Low                   |

**✅ In Simple Words:** DHCP is like an auto-assign system that gives an IP address to each device, so you don’t have to do it yourself.

---

## 🛠️ Networking Commands: `ping`, `traceroute`, `ifconfig`

# ✅ 1. `ping` Command

**📌 What is it?**  
`ping` checks if another computer or website is reachable and shows how long the data takes to travel there and back.

**🧠 Technical Meaning:**  
It sends small data packets (ICMP echo requests) to a target IP or domain, and waits for a reply.

**🧪 Example Command:**
```bash
ping google.com


# 🌐 Training Day: 09

## ✅ Introduction to HTML

---

### ✅ What is HTML?

- **HTML** stands for **HyperText Markup Language**.
- It is the **standard language** used to create web pages.
- It defines the **structure and layout** of content using **tags**.
- HTML is **not a programming language**, but a **markup language**.
- Files are saved with `.html` extension.

---

### ✅ What Does HTML Do?

- Creates the **structure** of a web page.
- Organizes content using elements like:
  - Headings (`<h1> to <h6>`)
  - Paragraphs (`<p>`)
  - Images (`<img>`)
  - Links (`<a>`)
- Works with:
  - **CSS** – for styling
  - **JavaScript** – for interactivity
- Acts as the **skeleton** of a webpage.

---

### ✅ How Does a Browser Render HTML?

1. The browser loads the `.html` file.
2. It reads the HTML **line-by-line** (top to bottom).
3. It builds the **DOM (Document Object Model)** in memory.
4. Converts tags into **visual elements**.
5. Applies **CSS** for styling.
6. Runs **JavaScript** for functionality.

---

# 💡 Example

```html
<h1>Hello</h1>

# Basic structure of html
<!DOCTYPE html>
<html>
  <head>
    <title>My First Page</title>
  </head>
  <body>
    <h1>Welcome!</h1>
    <p>This is a paragraph.</p>
  </body>
</html>

# 🌐 Training Day: 10

## ✅ Introduction to HTML & Web Basics

---

### ✅ What is HTML?

**HTML (HyperText Markup Language)** is the standard language used to create web pages.  
It structures content using **tags** that the **browser** can interpret and display.

---

## 🔖 Common HTML Tags

### 1. Headings (`<h1>` to `<h6>`)

- Used to define **titles** and **subheadings**.
- `<h1>` is the **largest**, `<h6>` is the **smallest**.

```html
<h1>Main Title</h1>
<h2>Subheading</h2>
<p>This is a paragraph of text.</p>
<ul>
  <li>Apple</li>
  <li>Banana</li>
</ul>
<ol>
  <li>First Step</li>
  <li>Second Step</li>
</ol>
<a href="https://www.google.com">Visit Google</a>
<img src="image.jpg" alt="Description of image">

# Day-11

# Common Input Types

HTML input fields are created using the <input> tag.

|Input Type	|Purpose|	Example Code|
|-----------|-------|-------------|
|text|	Single-line text input|	<input type="text" name="username">|
|password|	Hides typed characters|	<input type="password" name="pass">|
|email|	Accepts only email format	|<input type="email" name="email">|
|number|	Numeric input only	|<input type="number" name="age">|
|date|	Date picker	|<input type="date" name="dob">|
|radio|	Choose one option from a group|	<input type="radio" name="gender">|
|checkbox|	Multiple selections	|<input type="checkbox" name="hobby">|
|submit|	Button to submit form	|<input type="submit" value="Submit">|
|reset|	Clears all inputs	|<input type="reset">|
|file|	Upload file	|<input type="file" name="upload">|
|tel|	Telephone number input	|<input type="tel" name="phone">|
|url| Website address	|<input type="url" name="website">|
|color|	Pick a color	|<input type="color" name="favcolor">|
|range|	Slider control	|<input type="range" min="1" max="10">|

# Example of HTML Form:

<img width="558" height="361" alt="image" src="https://github.com/user-attachments/assets/a6ce9721-35d6-480a-86ba-b80e6f3c5441" />
<img width="360" height="238" alt="image" src="https://github.com/user-attachments/assets/1d14d364-778c-4a3d-8d4f-0fb460c231be" />

# Semantic HTML
Semantic HTML refers to the use of HTML5 tags that clearly describe the purpose and meaning of the content. It helps in accessibility, SEO, and code readability.
**Common Semantic Tags**
|Tag	|Purpose|
|----|-------|
|header|	Top section of page (logo, nav, title, etc.)|
|footer	Bottom section of page (copyright, links)|
|nav|	Navigation links to other pages|
|section|	A thematic grouping of content|
|article|	Self-contained content (e.g., blog post, news item)|
# Example of Sementic HTML:
<img width="613" height="481" alt="image" src="https://github.com/user-attachments/assets/05bb47dc-0f15-49c5-bcac-2c6fb6970afc" />
<img width="444" height="323" alt="image" src="https://github.com/user-attachments/assets/c0059037-d33d-4613-ae8d-83a14415a66d" />


# Day-12
# CSS Styling: Inline, Internal & External
### What is CSS?
CSS stands for Cascading Style Sheets. It's a language that lets you control the visual appearance of HTML content — things like layout, colors, fonts, spacing, and more.

You can add CSS to your web page in three main ways:

### 1. Inline CSS
This method places the CSS directly inside an HTML tag using the style attribute.

It's best used for quick changes or testing small tweaks.

**Example:**

<p style="color: green; font-size: 18px;">This text is styled using inline CSS.</p>
### 2. Internal CSS
In this approach, the CSS code is written inside a <style> tag, which is placed within the <head> section of your HTML file.

It's useful when you're working on just one page and want all styles to stay within that same file.

**Example:**

<head>
  <style>
    body {
      background-color: #f0fff0;
      font-family: Arial;
    }
    h1 {
      color: darkgreen;
    }
  </style>
</head>

### 3. External CSS
This method keeps your CSS in a separate file (with a .css extension) and links it to your HTML page using the <link> tag.

It's the most organized and reusable method, especially when you're working on a multi-page website.

HTML File:

<head>
  <link rel="stylesheet" href="styles.css">
</head>
styles.css File:

css
Copy
Edit
body {
  background-color: #e6ffe6;
  font-family: Verdana;
}
h1 {
  color: seagreen;
  text-align: center;
}
# Quick Comparison
|Feature|	Inline CSS|	Internal CSS|	External CSS
|-------|-----------|-------------|------------|
|Where it's written|	Inside the HTML tag|	In <style> within <head>|	In a separate .css file|
|Applies to	|Just one element	|One full HTML page	|Multiple pages|
|Can be reused?| Not reusable| Somewhat reusable| Highly reusable|
|Best for|	Quick edits or testing|	Small projects or one-pagers|	Full websites or large projects|

# Day-13

# What is Git and Why Use Version Control?
Git is a distributed version control system used to track changes in source code during software development.It helps manage code across multiple versions, developers, and updates.

### Why Use Version Control?
1. Tracks Your Work
2. Collaboration Made Easy
3. Backup and Safety
4.  Branching and Experimenting
5.  Open Source and Free

### Git Architecture:
 ### 1. Repository (Repo)
A storage location where Git tracks all changes made to your files over time.

Can be:

Local – stored on your own computer

Remote – hosted on platforms like GitHub, GitLab, or Bitbucket

### 2. Working Tree (or Working Directory)
The actual files and folders you're working with on your system right now.

It reflects the current version of your project

You make your changes here before saving them permanently with Git

### 3. Index (Staging Area)
A middle layer where you place files before committing them to the repository.

You use git add to move changes here

It gives you control over what goes into the next commit

Think of it as a review area before saving

<img width="692" height="454" alt="image" src="https://github.com/user-attachments/assets/7ab5537f-2f02-4948-9554-6ec21210f08a" />


# How to Use Git (Using Command Line)
# Step 1: Create or Clone a Repository
First, get the repository link (usually ends with .git) from GitHub

Open Git Bash (or terminal)

Run this command to clone the repository:

Move into the project folder:
<img width="633" height="612" alt="image" src="https://github.com/user-attachments/assets/b9571563-31ad-4d93-a3bd-dafbbbd9350d" />
<img width="735" height="374" alt="image" src="https://github.com/user-attachments/assets/b3d3479d-d39e-4963-836b-482f314d47bc" />

(Optional) Check the files using ls

# Step 2: Check Git Status
Use this to see changes or file status:
<img width="1118" height="280" alt="image" src="https://github.com/user-attachments/assets/f3177e01-249b-4ec5-9e7b-ba9cefc87e52" />

If it says "Up to date", everything is in sync

# Step 3: Create and Edit a New File
Create a new HTML file:

Open and write your code in it:


Save the file after editing (in Nano, press Ctrl + O, then Enter, then Ctrl + X to exit)

# Step 4: Add the File to Staging Area
Stage the file for commit:

**Warning:**
If you see a message like:
**warning:** in the working copy of 'index.html', LF will be replaced by CRLF
→ It means Git will convert line endings to match Windows (CRLF). It's safe to ignore.

### Step 5: Commit Your Changes
Save your changes to the local repo with a message:

Set your name and email using:


Try committing again:

### Step 6: Push to Remote Repository
Send your changes to GitHub:

You may be asked to authorize Git Credential Manager

Click "Authorize git-ecosystem"

Enter your GitHub username and password or token

# Now Check Your Repo!

# 🧠 Training Day: 14  
## 🔹 Module: Branching, Remote Operations & GitHub/GitLab Basics

---

## 📂 Branching and Merging in Git

### 🔹 What is Branching?

**Branching** means creating a separate line of development. It allows you to work on features or fixes independently without affecting the main code.

### ✅ Features of Branching

- Isolates development work (feature, bug fix, etc.)
- Enables simultaneous collaboration
- Prevents code conflicts
- Allows merging into main branch
- Lightweight and fast

---

### 🧠 Simple Analogy

> Think of Git as a tree:  
> - The `main` branch is the trunk.  
> - New branches are limbs growing off the trunk.  
> - You do work on the limb and later merge it back into the trunk.

---

### 🦪 Steps to Perform Branching in Git

**💼 Example Folder:** `Practice`

#### 1. Create a New Branch

```bash
git branch my-feature
```

#### 2. Switch to the New Branch (Checkout)

```bash
git checkout my-feature
```

👉 *Create and switch in one step:*

```bash
git checkout -b my-feature
```

#### 3. Make Changes → Add → Commit

```bash
git add .
git commit -m "Added feature X"
```

#### 4. Switch Back to Main Branch

```bash
git checkout main
```

#### 5. Merge Feature Branch into Main

```bash
git merge my-feature
```

📅 Now your feature is merged into the main branch.

---

## 🦁 Merging in Git

- Combines changes from one branch into another.
- May result in **merge conflicts**, which must be resolved manually.
- Helps integrate completed work into the main project.

**Merge command:**

```bash
git checkout main
git merge feature-branch
```

---

## 🌐 Remote Operations in Git

### 🔹 `git push`

Sends your **local commits** to the **remote** repository.

```bash
git push origin main
```

---

### 🔹 `git pull`

Fetches changes from the **remote** and merges them into your local branch.

```bash
git pull origin main
```

---

### 🔹 `git remote`

Manages remote repository connections.

```bash
git remote -v
```

---

## 🐙 GitHub / GitLab Basics

### ✔️ What are GitHub and GitLab?

They are **online platforms** that host Git repositories and provide features like:

- Pull/Merge Requests  
- Issue Tracking  
- Collaboration Tools  
- CI/CD Integration  

---

### 🔧 Common Uses

- Store and manage code online  
- Collaborate on private/public projects  
- Review code using Pull Requests (PRs)  

---

## ✅ Summary Commands

| Purpose           | Command Example                       |
|-------------------|----------------------------------------|
| Create branch     | `git branch new-feature`              |
| Switch branch     | `git checkout new-feature`            |
| Create & switch   | `git checkout -b new-feature`         |
| Add changes       | `git add .`                           |
| Commit changes    | `git commit -m "Message"`             |
| Merge branches    | `git merge new-feature`               |
| Push to remote    | `git push origin branch-name`         |
| Pull from remote  | `git pull origin branch-name`         |

---

### 📌 Tip

> 💡 Always pull the latest changes before starting new work:

```bash
git pull origin main
