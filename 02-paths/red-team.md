# Red Team (Offense) - Deep Dive

Red Team is the offensive side of cybersecurity. You are paid to think like an attacker, find weaknesses, and exploit them before real criminals do. This is the most exciting path, but also the hardest to enter.

---

## What you will learn

1. What is Red Team?
2. Every role explained in detail
3. Daily work in each role
4. Skills you need
5. Tools you will use
6. Methodology (how attacks work)
7. Salary and career growth
8. How to get started
9. Common challenges
10. Real-world scenarios

---

## 1. What is Red Team?

Red Team = attackers (with permission).

You simulate real attacks to test an organization's defenses. You find weaknesses, exploit them, and report how to fix them.

### Blue Team vs Red Team

| Aspect | Blue Team | Red Team |
|--------|-----------|----------|
| Role | Defend | Attack |
| Goal | Protect | Find weaknesses |
| Mindset | Detective | Adversary |
| Daily | Monitor, respond | Scan, exploit |
| Tools | SIEM, EDR | Nmap, Metasploit |
| Legal | Always authorized | Always authorized |

### Why Red Team matters

- You find weaknesses before criminals do
- You prove if defenses actually work
- You help organizations fix real problems
- You develop deep technical skills

### The reality

- Hard to enter (needs strong fundamentals)
- Constant learning required
- You will fail often
- Report writing is 50% of the job
- You must be ethical always

### Types of Red Team work

| Type | What it is |
|------|------------|
| Penetration Test | Time-boxed, specific scope |
| Red Team Exercise | Full adversary simulation |
| Bug Bounty | Independent, public targets |
| Vulnerability Research | Finding new bugs |
| Exploit Development | Writing exploit code |

---

## 2. Every Role Explained in Detail

### Penetration Tester

**What you do:**

You are hired to test a specific system, network, or application. You find vulnerabilities and report them.

**Types of pen tests:**

| Type | What it is |
|------|------------|
| Black box | No information given |
| White box | Full information given |
| Grey box | Some information given |
| Network | Test network infrastructure |
| Web app | Test websites |
| Mobile | Test mobile apps |
| Physical | Test physical security |
| Social engineering | Test people |

**Daily tasks:**

- Scope the engagement
- Reconnaissance (gather info)
- Scan for vulnerabilities
- Exploit findings
- Escalate privileges
- Move laterally
- Document everything
- Write report
- Debrief with client

**Example engagement:**

```
Day 1: Kickoff call, scope review
Day 2-3: Reconnaissance (OSINT, scanning)
Day 4-5: Vulnerability discovery
Day 6-7: Exploitation
Day 8: Post-exploitation
Day 9-10: Report writing
Day 11: Client debrief
```

**Skills you need:**

- Networking (deep)
- Linux (deep)
- Windows (deep)
- Web technologies
- Scripting (Python, Bash)
- Active Directory
- Report writing
- Communication

**Tools you use:**

- Kali Linux
- Nmap
- Burp Suite
- Metasploit
- SQLmap
- Hashcat
- Impacket
- BloodHound
- Cobalt Strike (paid)

**Challenges:**

- Time pressure
- Scope limitations
- Client pushback
- Report writing (boring but essential)
- Constant learning

**How to succeed:**

- Practice daily (Hack The Box, TryHackMe)
- Learn one thing deeply at a time
- Write clear reports
- Build a personal methodology

---

### Ethical Hacker

**What you do:**

Same as penetration tester. "Ethical hacker" is the older term. Used more in marketing and training.

**Daily tasks:**

- Same as pen tester
- Often more focused on training/awareness

**Skills you need:**

- Same as pen tester

**Tools you use:**

- Same as pen tester

**Challenges:**

- Term is sometimes seen as outdated
- Some roles are less technical

**How to succeed:**

- Focus on technical skills
- Build a portfolio

---

### Red Team Operator

**What you do:**

You simulate a full adversary campaign. You test people, processes, and technology together.

**Difference from pen test:**

| Pen Test | Red Team |
|----------|----------|
| Find all bugs | Test detection |
| Time-boxed | Weeks to months |
| Specific scope | Full organization |
| Report bugs | Report detection gaps |
| Technical | Technical + social |

**Daily tasks:**

- Plan campaign
- Reconnaissance (deep)
- Initial access
- Establish persistence
- Move laterally
- Escalate privileges
- Exfiltrate data (simulated)
- Evade detection
- Document everything
- Debrief with Blue Team

**Example campaign:**

```
Week 1: Reconnaissance, target selection
Week 2: Initial access (phishing)
Week 3: Establish persistence
Week 4: Lateral movement
Week 5: Privilege escalation
Week 6: Data exfiltration
Week 7: Report writing
Week 8: Debrief
```

**Skills you need:**

- Everything a pen tester knows
- Social engineering
- Advanced evasion
- C2 frameworks
- Operational security
- Patience
- Creativity

**Tools you use:**

- Cobalt Strike
- Sliver
- Mythic
- Empire
- BloodHound
- Custom implants
- Phishing platforms

**Challenges:**

- Long engagements
- Detection by Blue Team
- Ethical boundaries
- Complex planning
- High pressure

**How to succeed:**

- Learn Blue Team (to evade them)
- Study real APT groups
- Practice in labs
- Stay patient

---

### Bug Bounty Hunter

**What you do:**

You find vulnerabilities in public programs and get paid per bug.

**Platforms:**

| Platform | Notes |
|----------|-------|
| HackerOne | Largest |
| Bugcrowd | Large |
| Intigriti | Europe |
| YesWeHack | Europe |
| Synack | Invite only |

**Daily tasks:**

- Pick a target program
- Reconnaissance (deep)
- Test for vulnerabilities
- Write clear report
- Submit to platform
- Wait for triage
- Get paid if valid

**Example workflow:**

```
Day 1: Pick program (e.g., company.com)
Day 2-3: Recon (subdomains, endpoints, tech)
Day 4-5: Test common bugs (XSS, IDOR, SSRF)
Day 6: Found IDOR in API
Day 7: Write report with PoC
Day 8: Submit
Week 2: Triaged as valid
Week 3: Paid $500
```

**Skills you need:**

- Web security (deep)
- API security
- Mobile security (optional)
- Scripting
- Patience
- Writing

**Tools you use:**

- Burp Suite
- FFUF
- Amass
- Subfinder
- Nuclei
- Custom scripts

**Challenges:**

- No steady income
- Duplicate reports
- Rejected as "not a bug"
- Competitive
- Time-consuming

**How to succeed:**

- Pick programs you understand
- Learn from public reports
- Build recon automation
- Be patient

---

### Exploit Developer

**What you do:**

You write code that takes advantage of vulnerabilities. Deep technical work.

**Types:**

| Type | What it is |
|------|------------|
| Memory corruption | Buffer overflows |
| Web exploits | XSS, SQLi, etc. |
| Kernel exploits | OS-level |
| Browser exploits | Chrome, Firefox |
| Mobile exploits | Android, iOS |

**Daily tasks:**

- Analyze vulnerability
- Develop proof of concept
- Refine exploit
- Test reliability
- Document
- Share responsibly

**Example workflow:**

```
Step 1: Get vulnerability details
Step 2: Analyze binary/source
Step 3: Find offset
Step 4: Control EIP/RIP
Step 5: Build ROP chain
Step 6: Test shellcode
Step 7: Refine reliability
Step 8: Write report
```

**Skills you need:**

- Assembly (x86, x64, ARM)
- C/C++
- Python
- Debuggers
- Reverse engineering
- Operating systems (deep)
- Patience

**Tools you use:**

- IDA Pro / Ghidra
- x64dbg
- GDB + pwndbg
- Pwntools
- Mona
- ROPgadget

**Challenges:**

- Very hard
- Years to master
- Modern mitigations
- Constantly changing

**How to succeed:**

- Learn assembly deeply
- Practice on CTFs (pwn category)
- Read exploit writeups
- Be patient

---

### Vulnerability Researcher

**What you do:**

You find new vulnerabilities in software. You discover zero-days.

**Daily tasks:**

- Pick target software
- Analyze code/binary
- Fuzz for crashes
- Triage crashes
- Develop PoC
- Report to vendor
- Publish (after patch)

**Example workflow:**

```
Step 1: Pick target (e.g., PDF reader)
Step 2: Set up fuzzing
Step 3: Run fuzzer for days/weeks
Step 4: Analyze crashes
Step 5: Find exploitable one
Step 6: Develop PoC
Step 7: Report to vendor
Step 8: Wait for patch
Step 9: Publish
```

**Skills you need:**

- Programming (C, C++, Python)
- Reverse engineering
- Fuzzing
- Operating systems
- Assembly
- Patience (extreme)

**Tools you use:**

- AFL++
- libFuzzer
- Honggfuzz
- IDA Pro / Ghidra
- AddressSanitizer

**Challenges:**

- Very hard
- Long timelines
- Few jobs
- Vendor relations
- Legal issues

**How to succeed:**

- Learn fuzzing
- Practice on open source
- Read research papers
- Join bug bounty programs

---

### Social Engineer

**What you do:**

You test the human element. You trick people into giving access or info (with permission).

**Types:**

| Type | What it is |
|------|------------|
| Phishing | Email attacks |
| Vishing | Voice calls |
| Smishing | SMS |
| Pretexting | Fake story |
| Tailgating | Physical entry |
| Impersonation | Pretend to be someone |

**Daily tasks:**

- Plan campaign
- Build pretext
- Craft messages
- Execute campaign
- Track success
- Report findings

**Example phishing campaign:**

```
Step 1: Client approves campaign
Step 2: Build fake login page
Step 3: Craft email (looks real)
Step 4: Send to 100 employees
Step 5: 20% click link
Step 6: 5% enter credentials
Step 7: Report to client
Step 8: Recommend training
```

**Skills you need:**

- Psychology
- Communication
- Writing
- Social awareness
- Ethics

**Tools you use:**

- GoPhish
- Evilginx2
- SET (Social Engineering Toolkit)
- Custom phishing pages

**Challenges:**

- Ethical boundaries
- People get upset
- Legal risks
- Requires approval

**How to succeed:**

- Study psychology
- Learn from real cases
- Be ethical always
- Document everything

---

### Physical Pen Tester

**What you do:**

You test physical security. You try to break into buildings.

**Daily tasks:**

- Recon target building
- Plan entry
- Test locks, badges, guards
- Document findings
- Report to client

**Example operation:**

```
Step 1: Recon (photos, schedules)
Step 2: Tailgate through door
Step 3: Find unlocked office
Step 4: Access computer
Step 5: Plant device (if allowed)
Step 6: Exit
Step 7: Report
```

**Skills you need:**

- Social engineering
- Lock picking
- Observation
- Courage
- Ethics

**Tools you use:**

- Lock pick set
- RFID cloner (Proxmark)
- Hidden cameras
- Recording devices

**Challenges:**

- Legal risks
- Physical danger
- Getting caught
- Insurance

**How to succeed:**

- Learn lock picking
- Study physical security
- Practice legally
- Always have written permission

---

## 3. Daily Work in Each Role

### A typical pen test day

**Morning:**

- Review scope
- Plan day's tests
- Check client communication

**Midday:**

- Recon and scanning
- Exploitation attempts
- Document findings

**Afternoon:**

- Continue testing
- Update notes
- Report to team lead

### A typical Red Team day

**Morning:**

- Check C2 infrastructure
- Review Blue Team activity
- Plan next move

**Midday:**

- Execute attack step
- Evade detection
- Document

**Afternoon:**

- Analyze results
- Adjust plan
- Team sync

### A typical bug bounty day

**Morning:**

- Pick target
- Run recon tools
- Review results

**Midday:**

- Test for bugs
- Write PoC
- Submit report

**Afternoon:**

- Check submissions
- Work on next target

---

## 4. Skills You Need

### Technical skills

| Skill | Why |
|-------|-----|
| Networking | Understand traffic |
| Linux | Attack platform |
| Windows | Common target |
| Web technologies | Most attacks |
| Active Directory | Enterprise target |
| Scripting | Automation |
| Programming | Tool building |
| Reverse engineering | Exploit dev |
| Cryptography | Bypass encryption |
| Social engineering | Human attacks |

### Soft skills

| Skill | Why |
|-------|-----|
| Creativity | Find new paths |
| Patience | Long engagements |
| Communication | Report writing |
| Ethics | Stay legal |
| Attention to detail | Find subtle bugs |
| Documentation | Client reports |
| Adaptability | Constant change |
| Persistence | Do not give up |

### Frameworks to know

| Framework | Use |
|-----------|-----|
| MITRE ATT&CK | Map techniques |
| Cyber Kill Chain | Attack stages |
| OWASP Top 10 | Web vulnerabilities |
| PTES | Pen test methodology |
| OSSTMM | Security testing |

---

## 5. Tools You Will Use

### Reconnaissance

| Tool | Use |
|------|-----|
| Nmap | Port scanning |
| Amass | Subdomain enum |
| Subfinder | Subdomain enum |
| theHarvester | Email/domain info |
| Shodan | Internet scanning |
| Maltego | Data mapping |
| Recon-ng | Recon framework |

### Scanning

| Tool | Use |
|------|-----|
| Nessus | Vulnerability scanner |
| OpenVAS | Vulnerability scanner |
| Nikto | Web scanner |
| Nuclei | Template scanner |

### Exploitation

| Tool | Use |
|------|-----|
| Metasploit | Exploit framework |
| Burp Suite | Web proxy |
| SQLmap | SQL injection |
| BeEF | Browser exploitation |
| Impacket | Windows protocols |

### Post-exploitation

| Tool | Use |
|------|-----|
| Mimikatz | Credential dumping |
| BloodHound | AD mapping |
| PowerView | AD enumeration |
| Cobalt Strike | C2 framework |
| Sliver | C2 framework |

### Password attacks

| Tool | Use |
|------|-----|
| Hashcat | Hash cracking |
| John the Ripper | Hash cracking |
| Hydra | Online brute force |
| Medusa | Online brute force |

### Evasion

| Tool | Use |
|------|-----|
| Veil | Payload obfuscation |
| Shellter | Shellcode injection |
| Invoke-Obfuscation | PowerShell obfuscation |

---

## 6. Methodology (How Attacks Work)

### Phase 1: Reconnaissance

Gather information about the target.

- Passive: OSINT, social media, websites
- Active: Scanning, DNS queries

### Phase 2: Scanning

Find open ports, services, vulnerabilities.

- Port scanning (Nmap)
- Service detection
- Vulnerability scanning

### Phase 3: Gaining Access

Exploit a vulnerability to get in.

- Web exploits
- Network exploits
- Social engineering

### Phase 4: Maintaining Access

Keep access even after reboot.

- Backdoors
- Persistence mechanisms
- Rootkits

### Phase 5: Privilege Escalation

Go from normal user to admin.

- Windows: token impersonation, unquoted paths
- Linux: SUID, sudo misconfigs

### Phase 6: Lateral Movement

Move to other systems.

- Pass-the-Hash
- Remote desktop
- SSH keys

### Phase 7: Exfiltration

Steal data (simulated).

- DNS tunneling
- HTTPS
- Covert channels

### Phase 8: Reporting

Document everything.

- Findings
- Evidence
- Impact
- Remediation

---

## 7. Salary and Career Growth

### Salary (2026, Global Average)

| Role | Entry | Mid | Senior |
|------|-------|-----|--------|
| Penetration Tester | $65k | $100k | $150k |
| Ethical Hacker | $60k | $90k | $130k |
| Red Team Operator | $85k | $120k | $170k |
| Bug Bounty Hunter | Variable | Variable | Variable |
| Exploit Developer | $100k | $150k | $200k+ |
| Vulnerability Researcher | $90k | $140k | $200k+ |
| Social Engineer | $60k | $85k | $120k |
| Physical Pen Tester | $55k | $80k | $110k |

**Note:** Bug bounty income is unpredictable. Top hunters earn $500k+.

### Career growth

| Year | Role |
|------|------|
| 0-2 | Junior Pen Tester |
| 2-4 | Penetration Tester |
| 4-6 | Senior Pen Tester |
| 6-8 | Red Team Operator |
| 8-12 | Lead / Principal |
| 12+ | Manager / Director |

### Career moves

- Red Team → Blue Team (common)
- Red Team → Cloud Security
- Red Team → Exploit Dev
- Red Team → Management
- Red Team → Bug Bounty (full-time)

---

## 8. How to Get Started

### Step 1: Learn the core

Finish `01-core` first. Do not skip.

### Step 2: Build a home lab

- Install VirtualBox
- Kali Linux (attacker)
- Metasploitable (target)
- DVWA (web target)
- Windows 10 (target)

### Step 3: Practice

- TryHackMe: Jr Penetration Tester path
- Hack The Box: Starting Point
- PortSwigger Web Security Academy
- OverTheWire
- VulnHub

### Step 4: Learn tools

- Nmap, Burp Suite, Metasploit
- Wireshark, SQLmap
- BloodHound, Mimikatz
- Scripting in Python

### Step 5: Build a portfolio

- Write up labs on GitHub
- Document CTF challenges
- Build custom tools
- Write blog posts

### Step 6: Apply

- Junior Pen Tester
- SOC Analyst (as entry)
- IT Support (as entry)
- Bug bounty (part-time)

### Step 7: Keep learning

- Read bug bounty writeups
- Follow security researchers
- Attend conferences
- Practice constantly

---

## 9. Common Challenges

| Challenge | Reality |
|-----------|---------|
| Hard to enter | Needs strong fundamentals |
| Constant learning | Never stops |
| Report writing | 50% of job |
| Scope limits | Cannot test everything |
| Legal risks | Must stay authorized |
| Client pushback | Findings disputed |
| Imposter syndrome | Common |
| Burnout | High in Red Team |

### How to survive

- Practice daily
- Build a methodology
- Document everything
- Stay ethical
- Take breaks
- Build a network
- Keep learning

---

## 10. Real-World Scenarios

### Scenario 1: Web app pen test

1. **Recon:** Find subdomains, endpoints
2. **Scan:** Nmap, Burp Suite
3. **Find:** SQL injection in login
4. **Exploit:** Extract database
5. **Escalate:** Find admin credentials
6. **Report:** Document findings

### Scenario 2: Red Team campaign

1. **Recon:** OSINT on employees
2. **Initial:** Phishing email
3. **Foothold:** Malicious macro
4. **Persistence:** Scheduled task
5. **Lateral:** Pass-the-Hash
6. **Escalate:** Domain Admin
7. **Exfil:** Simulated data theft
8. **Report:** Detection gaps

### Scenario 3: Bug bounty

1. **Pick:** Company program
2. **Recon:** Subdomain enumeration
3. **Test:** IDOR in API
4. **PoC:** Video demonstration
5. **Report:** Clear writeup
6. **Triaged:** Valid
7. **Paid:** $500

---

## Practice Tasks

- [ ] Install Kali Linux
- [ ] Complete TryHackMe Jr Pen Tester
- [ ] Solve 10 Hack The Box machines
- [ ] Complete PortSwigger labs
- [ ] Build a port scanner in Python
- [ ] Exploit a vulnerable VM
- [ ] Write a pen test report
- [ ] Practice with Burp Suite
- [ ] Learn BloodHound
- [ ] Participate in a CTF

---

## Free Practice

- TryHackMe
- Hack The Box
- PortSwigger Web Security Academy
- OverTheWire
- VulnHub
- PicoCTF
- PentesterLab

---

## Key Terms

| Term | Meaning |
|------|---------|
| Pen Test | Authorized attack |
| Red Team | Adversary simulation |
| Bug Bounty | Paid bug hunting |
| Exploit | Code that uses a bug |
| Payload | Code after exploit |
| C2 | Command and control |
| Lateral Movement | Move between systems |
| Privilege Escalation | Get admin |
| Persistence | Stay in system |
| Exfiltration | Steal data |

---

## What now?

Next path: `cloud-security.md`

> **Ethical Use Only**
> Only hack systems you own or have written permission to test.
> Never use these skills to break the law.
