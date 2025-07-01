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

