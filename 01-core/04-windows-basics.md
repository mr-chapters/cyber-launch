# 04 - Windows Basics

Most companies run Windows. Most employees use Windows. Most malware targets Windows. If you want to work in cybersecurity, you must know Windows.

---

## What you will learn
1. Windows OS overview
2. Active Directory basics
3. Command line (cmd) and PowerShell
4. User accounts and permissions
5. Windows security features
6. Event Viewer and logs

---

## 1. Windows OS Overview

Windows is the most used desktop OS in the world. It is made by Microsoft.

**Versions you should know:**
| Version | Year | Notes |
|---------|------|-------|
| Windows 7 | 2009 | Old, still in some companies |
| Windows 8/8.1 | 2012 | Skipped by most |
| Windows 10 | 2015 | Widely used |
| Windows 11 | 2021 | Current |
| Windows Server 2016/2019/2022 | – | Used in companies |

**Why Windows matters in cybersecurity:**
- Most companies run Windows
- Most malware targets Windows
- Active Directory (used by 90%+ of companies) runs on Windows
- Most employees use Windows daily

**Key Windows folders:**
| Folder | Path | What it holds |
|--------|------|---------------|
| System32 | `C:\Windows\System32` | Core system files |
| Program Files | `C:\Program Files` | Installed apps |
| Users | `C:\Users` | User profiles |
| Temp | `C:\Windows\Temp` | Temporary files |
| Logs | `C:\Windows\System32\winevt\Logs` | Event logs |

**Why this matters:** Attackers hide in these folders. You must know where to look.

---

## 2. Active Directory Basics

Active Directory (AD) is a database of users, computers, and permissions. It is used by 90%+ of companies.

**What AD manages:**
- User accounts
- Computers
- Groups
- Permissions
- Policies

**Key AD terms:**
| Term | Meaning |
|------|---------|
| Domain | A network of AD objects |
| Domain Controller (DC) | The server that runs AD |
| OU | Organizational Unit (like a folder) |
| Group | A set of users |
| GPO | Group Policy Object (rules) |
| LDAP | Protocol to query AD |

**Why AD is a huge target:**
- If you control AD, you control the whole company
- Attackers try to become Domain Admin
- Most enterprise attacks target AD

**Common AD attacks:**
| Attack | What it does |
|--------|--------------|
| Kerberoasting | Steal service account passwords |
| Pass-the-Hash | Use stolen password hash |
| Golden Ticket | Forge admin access |
| DCSync | Steal all AD passwords |

**Why this matters:** AD is the crown jewel of a company. Learn it well.

---

## 3. Command Line (cmd) and PowerShell

### CMD (Command Prompt)
The old Windows command line.

| Command | What it does |
|---------|--------------|
| `dir` | List files |
| `cd foldername` | Change folder |
| `cd ..` | Go back |
| `mkdir name` | Create folder |
| `del file` | Delete file |
| `copy file1 file2` | Copy |
| `move file1 file2` | Move |
| `type file.txt` | Show contents |
| `ipconfig` | Show IP info |
| `ping host` | Check reachability |
| `tracert host` | Trace route |
| `netstat -an` | Show connections |
| `tasklist` | Show running processes |
| `taskkill /PID 1234` | Kill process |
| `whoami` | Show current user |
| `systeminfo` | Show system info |

### PowerShell
The modern Windows command line. Much more powerful.

| Command | What it does |
|---------|--------------|
| `Get-ChildItem` | List files (like ls) |
| `Set-Location` | Change folder (like cd) |
| `New-Item` | Create file/folder |
| `Remove-Item` | Delete |
| `Copy-Item` | Copy |
| `Move-Item` | Move |
| `Get-Content` | Read file |
| `Get-Process` | List processes |
| `Stop-Process` | Kill process |
| `Get-Service` | List services |
| `Get-EventLog` | Read event logs |
| `Get-Help` | Show help |

**Why PowerShell matters:**
- Attackers use PowerShell to run malware
- Defenders use PowerShell to investigate
- It is required for modern Windows security

**Why this matters:** Most Windows attacks use cmd or PowerShell. You must know both.

---

## 4. User Accounts and Permissions

**Account types:**
| Type | What it can do |
|------|----------------|
| Standard User | Normal tasks |
| Administrator | Full control |
| Guest | Very limited |
| Service Account | Runs services |
| System | Highest level |

**Commands:**
| Command | What it does |
|---------|--------------|
| `whoami` | Show current user |
| `whoami /groups` | Show groups |
| `net user` | List users |
| `net user name` | Show user info |
| `net localgroup` | List groups |
| `net localgroup Administrators` | List admins |
| `runas /user:name cmd` | Run as another user |

**Why this matters:** Attackers try to become Administrator. Understanding users is key.

---

## 5. Windows Security Features

| Feature | What it does |
|---------|--------------|
| Windows Defender | Antivirus |
| Windows Firewall | Blocks traffic |
| BitLocker | Disk encryption |
| UAC | User Account Control (asks for admin) |
| Secure Boot | Prevents boot malware |
| Credential Guard | Protects credentials |
| AppLocker | Restricts apps |

**UAC (User Account Control):**
- Asks for permission before admin actions
- Prevents silent malware installs
- Attackers try to bypass UAC

**Why this matters:** These are the defenses you must understand to attack or defend Windows.

---

## 6. Event Viewer and Logs

Windows logs everything. Event Viewer is where you read logs.

**How to open:**
- Press `Win + R`, type `eventvwr.msc`, press Enter

**Key log categories:**
| Log | What it holds |
|-----|---------------|
| Application | App events |
| Security | Logins, permissions |
| System | OS events |
| Setup | Install events |

**Important Event IDs:**
| ID | Meaning |
|----|---------|
| 4624 | Successful login |
| 4625 | Failed login |
| 4634 | Logoff |
| 4648 | Login with explicit credentials |
| 4672 | Special privileges assigned |
| 4720 | User account created |
| 4726 | User account deleted |
| 4732 | User added to group |

**Why this matters:** Logs tell the story of an attack. Every SOC analyst reads them daily.

---

## Practice Tasks
- [ ] Open cmd and run `ipconfig`
- [ ] Open PowerShell and run `Get-Process`
- [ ] List all users with `net user`
- [ ] Check who is in Administrators group
- [ ] Open Event Viewer and find Event ID 4624
- [ ] Find 3 failed login attempts (Event ID 4625)
- [ ] Install Windows in a VM (optional)
- [ ] Read about Active Directory
- [ ] Try 5 PowerShell commands
- [ ] Check Windows Defender settings

---

## Free Practice
- Microsoft Learn (free Windows courses)
- TryHackMe Windows rooms
- Hack The Box Academy Windows modules
- Professor Messer videos

---

## Key Terms
| Term | Meaning |
|------|---------|
| AD | Active Directory |
| DC | Domain Controller |
| GPO | Group Policy Object |
| UAC | User Account Control |
| Event ID | Log event number |
| PowerShell | Modern Windows shell |
| CMD | Old Windows shell |
| Service Account | Account for services |

---

## What now?
Next file: **05-programming.md**

> ⚠️ Ethical Use Only
> Only hack systems you own or have written permission to test.
> Never use these skills to break the law.
