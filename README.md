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

