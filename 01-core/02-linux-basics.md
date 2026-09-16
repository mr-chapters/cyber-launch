# 02 - Linux Basics

Linux runs most of the internet, most servers, and most security tools. If you want to work in cybersecurity, you must know Linux.

---

## What you will learn

- What is Linux?
- Installing Ubuntu in a virtual machine
- The terminal
- Basic commands
- File permissions
- Users and groups
- Processes
- Package management
- Text editors

---

## 1. What is Linux?

Linux is a free, open-source operating system. It powers:

- Most web servers
- Android phones
- Supercomputers
- Security tools like Kali Linux

**Why Linux for cybersecurity:**

- Most hacking tools run on Linux
- It is free and open source
- You can see and change everything
- Servers you will attack run Linux

**Popular Linux versions (called "distros"):**

| Distro | Use |
|--------|-----|
| Ubuntu | Beginner-friendly |
| Kali Linux | Hacking and pentesting |
| Debian | Stable, servers |
| Fedora | Developer-focused |
| Arch | Advanced users |

Start with **Ubuntu**. Move to **Kali** when ready.

---

## 2. Installing Ubuntu in a Virtual Machine

**Steps:**

1. Download VirtualBox (free)
2. Download Ubuntu ISO from ubuntu.com
3. Open VirtualBox, click "New"
4. Name it "Ubuntu", choose Linux, Ubuntu 64-bit
5. Give it at least 2GB RAM and 20GB storage
6. Attach the Ubuntu ISO
7. Start the VM and follow the install steps

**Why a VM:** Safe place to practice. If you break it, delete and start over.

---

## 3. The Terminal

The terminal is where you type commands instead of clicking.

**Why use it:**

- Faster than clicking
- Most security tools are command-line only
- You can automate tasks
- Required skill for every security job

**How to open it:**

- Ubuntu: Ctrl + Alt + T
- Or search "Terminal" in apps

---

## 4. Basic Commands

| Command | What it does |
|---------|--------------|
| pwd | Show current folder |
| ls | List files |
| ls -la | List all files with details |
| cd foldername | Go into a folder |
| cd .. | Go back one folder |
| mkdir name | Create a folder |
| touch file.txt | Create an empty file |
| rm file.txt | Delete a file |
| rm -r folder | Delete a folder |
| cp file1 file2 | Copy a file |
| mv file1 file2 | Move or rename |
| cat file.txt | Show file contents |
| nano file.txt | Edit a file |
| clear | Clear the screen |
| man command | Show manual for a command |
| history | Show past commands |

**Practice every day.** These must become muscle memory.

---

## 5. File Permissions

Every file has permissions for three groups:

- **Owner** — the person who made it
- **Group** — a set of users
- **Others** — everyone else

Three permission types:

- **r** = read
- **w** = write
- **x** = execute

**Viewing permissions:**

    ls -l

Output example:

    -rwxr-xr-- 1 user group 1234 Jan 1 file.sh

- First dash = file type
- Next 3 = owner (rwx)
- Next 3 = group (r-x)
- Last 3 = others (r--)

**Changing permissions:**

| Command | Meaning |
|---------|---------|
| chmod +x file | Make executable |
| chmod 755 file | rwxr-xr-x |
| chmod 644 file | rw-r--r-- |
| chown user file | Change owner |

**Why this matters:** Weak permissions are a common vulnerability.

---

## 6. Users and Groups

| Command | What it does |
|---------|--------------|
| whoami | Show current user |
| id | Show user ID and groups |
| sudo command | Run as admin |
| su user | Switch user |
| useradd name | Add user (admin) |
| passwd | Change password |
| groups | Show your groups |

**Why this matters:** Attackers try to become root (admin). Understanding users is key.

---

## 7. Processes

A process is a running program.

| Command | What it does |
|---------|--------------|
| ps aux | Show all processes |
| top | Live process view |
| htop | Better version of top |
| kill PID | Stop a process |
| kill -9 PID | Force stop |
| systemctl status | Check service status |

**Why this matters:** Malware runs as a process. You must spot unusual ones.

---

## 8. Package Management

Installing software on Linux uses a package manager.

**Ubuntu/Debian:**

| Command | What it does |
|---------|--------------|
| sudo apt update | Refresh package list |
| sudo apt upgrade | Update installed packages |
| sudo apt install name | Install software |
| sudo apt remove name | Uninstall |

**Why this matters:** You will install tools like Nmap, Wireshark, and Burp Suite this way.

---

## 9. Text Editors

**nano (easy):**

    nano file.txt

- Ctrl + O = save
- Ctrl + X = exit

**vim (advanced):**

    vim file.txt

- i = insert mode
- Esc = exit insert
- :w = save
- :q = quit
- :wq = save and quit

Start with nano. Learn vim later.

---

## Practice Tasks

- [ ] Install Ubuntu in VirtualBox
- [ ] Open the terminal
- [ ] Practice 10 basic commands
- [ ] Create, move, and delete files
- [ ] Change file permissions
- [ ] Install a package with apt
- [ ] Complete OverTheWire Bandit Levels 0 to 15

---

## Free Practice

- OverTheWire Bandit: overthewire.org/wargames/bandit
- Linux Journey: linuxjourney.com

---

## Key Terms

| Term | Meaning |
|------|---------|
| Terminal | Command-line interface |
| Distro | Linux version |
| Root | Admin user |
| sudo | Run as admin |
| chmod | Change permissions |
| apt | Ubuntu package manager |
| Process | Running program |

---

## What now?

Next file: **03-networking.md**

> Ethical Use Only
> Only hack systems you own or have written permission to test.
> Never use these skills to break the law.
