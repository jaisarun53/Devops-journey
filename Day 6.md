# 🐧 Day 6: Linux Fundamentals & Shell Scripting Basics

## 📖 Overview
Day 6 focuses on why Linux is the preferred operating system for DevOps and introduces the essential commands needed to navigate and manage a Linux server.

---

## 🏗️ 1. Why Linux?
In the software world, 80-90% of production systems run on Linux.
* **Open Source & Free:** No licensing fees like Windows.
* **Security:** Inherently more secure with robust permission systems.
* **Performance:** Extremely fast and lightweight (no heavy GUI required).
* **Stability:** Can run for years without needing a reboot.

---

## 🛠️ 2. Linux Architecture
The Linux OS is built in layers:
1.  **Hardware:** CPU, RAM, Disk.
2.  **Kernel:** The heart of the OS. It manages communication between hardware and software.
    * *Key tasks:* Memory management, Process management, and Device management.
3.  **Shell:** The interface that takes your commands and gives them to the Kernel.
4.  **Applications/Tools:** Compilers, User processes, and system softwares.

---

## 💻 3. Essential Shell Commands
Navigating a server without a mouse requires knowing these commands:

### Navigation & Files
| Command | Description |
| :--- | :--- |
| `pwd` | **P**resent **W**orking **D**irectory (Where am I?) |
| `ls` | **L**i**s**t files and folders. |
| `ls -ltr` | List files with details (permissions, owner, size, time). |
| `cd <dir>` | **C**hange **D**irectory. |
| `mkdir <name>`| **M**a**k**e a new **dir**ectory. |
| `touch <file>`| Create an empty file. |
| `vi <file>` | Open the VI text editor to write inside a file. |
| `cat <file>` | **Cat**enate (Read/display) file content. |

### System Monitoring
| Command | Description |
| :--- | :--- |
| `free -m` | Check available **Memory** (RAM). |
| `nproc` | Check number of **Processors** (CPUs). |
| `df -h` | Check **Disk** space usage (human-readable). |
| `top` | Real-time **Task Manager** (CPU, RAM, Processes). |

---

## ✍️ 4. The VI Editor Basics
Since there is no "Notepad," we use **VI**.
1.  **Open:** `vi filename`
2.  **Insert Mode:** Press `i` to start typing.
3.  **Save & Exit:** Press `Esc`, then type `:wq` and hit `Enter`.
4.  **Exit without Saving:** Press `Esc`, then type `:q!` and hit `Enter`.

---

## 💡 Key Takeaways
* The **Kernel** is the bridge between hardware and software.
* **Shell** is your primary tool as a DevOps engineer to talk to the server.
* Monitoring commands like `top` and `df -h` are vital for troubleshooting production issues.

---

## 🔗 Resources
* **Video Reference:** [Day 6 - Linux & Shell Scripting](https://www.youtube.com/watch?v=9jw9F6mcQDo)
* **Advanced Shell Playlist:** [Complete Shell Scripting Guide](https://www.youtube.com/playlist?list=PLdpzxOOAlwvIKMhk8WhzN1pYoJ1YU8Csa)

---
[⬅️ Back to Main README](./README.md)
