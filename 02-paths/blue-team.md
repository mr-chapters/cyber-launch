# Blue Team (Defense) - Deep Dive

Blue Team is the defensive side of cybersecurity. You protect the organization, monitor for threats, and respond when something goes wrong. This is the most common entry point into cybersecurity.

---

## What you will learn

1. What is Blue Team?
2. Every tier explained in detail
3. Daily work at each tier
4. Skills you need at each tier
5. Tools you will use at each tier
6. Salary and career growth
7. How to get started
8. Common challenges
9. Real-world scenarios

---

## 1. What is Blue Team?

Blue Team = defenders.

You are the security team inside an organization. Your job is to:

- Prevent attacks
- Detect attacks
- Respond to attacks
- Recover from attacks

### Blue Team vs Red Team

| Aspect | Blue Team | Red Team |
|--------|-----------|----------|
| Role | Defend | Attack |
| Goal | Protect | Find weaknesses |
| Mindset | Detective | Adversary |
| Daily | Monitor, respond | Scan, exploit |
| Tools | SIEM, EDR | Nmap, Metasploit |

### Why Blue Team matters

- Most security jobs are defensive
- Easier to enter than Red Team
- Steady demand, always hiring
- Clear career path

### The reality

- You will not stop every attack
- You will work shifts (SOC)
- You will see boring days and chaotic days
- You will learn something new constantly

---

## 2. Every Tier Explained in Detail

### SOC Tier 1 - Triage Analyst

**What you do:**

You are the first line of defense. Alerts come in, you decide if they are real or noise.

**Daily tasks:**

- Watch the SIEM dashboard all day
- Pick up alerts from the queue
- Read the alert details
- Gather basic context (user, host, IP, time)
- Check if similar alerts happened before
- Decide: false positive or escalate
- Document everything in the ticket
- Handover to next shift

**Example day:**

```text
09:00 - Handover from night shift
09:15 - 47 alerts in queue
09:20 - Alert 1: Failed logins (user locked out) -> False positive
09:35 - Alert 2: Malware detected (blocked by AV) -> False positive
09:50 - Alert 3: Login from Russia -> Escalate to Tier 2
10:10 - Alert 4: Suspicious PowerShell -> Escalate
...
17:00 - Handover to night shift
```

**Skills you need:**

- Basic networking (IP, ports, protocols)
- Basic Linux and Windows
- SIEM basics (how to search)
- Log reading
- Ticket writing
- Attention to detail

**Tools you use:**

- SIEM (Splunk, ELK, Sentinel)
- Ticketing (Jira, ServiceNow)
- VirusTotal (check files/URLs)
- Email gateway console

**Challenges:**

- Alert fatigue (too many false positives)
- Repetitive work
- Shift work (nights, weekends)
- Pressure to close tickets fast

**How to succeed:**

- Learn the environment (what is normal)
- Take notes on common alerts
- Ask Tier 2 for feedback
- Study on your own time

**Time to next tier:** 1-2 years

---

### SOC Tier 2 - Incident Analyst

**What you do:**

You take escalated alerts and investigate deeply. You decide if it is a real incident.

**Daily tasks:**

- Pick up escalated alerts from Tier 1
- Do deep investigation (logs, endpoints, network)
- Correlate events across systems
- Use threat intel to check IOCs
- Determine scope of incident
- Contain if needed (isolate host, disable account)
- Write detailed reports
- Mentor Tier 1 analysts

**Example investigation:**

```text
Alert: Login from Russia for user john.doe

Step 1: Check user's normal behavior
- Usually logs in from New York, 9 AM - 5 PM
- This login: Russia, 3 AM

Step 2: Check authentication
- Was MFA used? No
- Was password correct? Yes

Step 3: Check for other activity
- Any file downloads? No
- Any email changes? Yes, forwarding rule added

Step 4: Check threat intel
- Source IP: Known malicious

Conclusion: Account compromised
Action: Disable account, reset password, remove forwarding rule, notify user
```

**Skills you need:**

- Advanced SIEM queries
- Log analysis (Windows, Linux, network)
- Threat intelligence
- Basic forensics
- Malware analysis basics
- Incident response process
- Report writing

**Tools you use:**

- SIEM (advanced queries)
- EDR (CrowdStrike, SentinelOne)
- VirusTotal, Any.run
- MITRE ATT&CK
- Forensic tools (Volatility basics)

**Challenges:**

- Complex investigations
- Time pressure
- Unknown threats
- Blame when things go wrong

**How to succeed:**

- Learn MITRE ATT&CK deeply
- Practice investigations in labs
- Build a personal knowledge base
- Learn to write clearly

**Time to next tier:** 2-3 years

---

### SOC Tier 3 - Threat Hunter / Senior Analyst

**What you do:**

You do not wait for alerts. You proactively hunt for hidden threats. You also lead major investigations.

**Daily tasks:**

- Form hypotheses ("Attackers might be using X technique")
- Search logs for evidence
- Identify anomalies that tools missed
- Build new detection rules
- Lead incident response for major events
- Mentor Tier 1 and Tier 2
- Improve SOC processes
- Work with Red Team on purple team exercises

**Example hunt:**

```text
Hypothesis: Attackers might be using scheduled tasks for persistence

Step 1: Query all scheduled tasks across endpoints
Step 2: Filter for unusual ones (odd names, strange paths)
Step 3: Check each against threat intel
Step 4: Found one - "WindowsUpdateCheck" running from Temp folder
Step 5: Investigate - it is Cobalt Strike beacon
Step 6: Scope - how many machines?
Step 7: Contain and eradicate
Step 8: Build detection rule for future
```

**Skills you need:**

- Deep MITRE ATT&CK knowledge
- Advanced forensics
- Malware analysis
- Detection engineering
- Scripting (Python, PowerShell)
- Threat intelligence
- Leadership

**Tools you use:**

- Everything Tier 2 uses, plus:
- Detection engineering platforms
- Custom scripts
- Threat hunting platforms
- Memory forensics (Volatility)
- Sandboxes

**Challenges:**

- Finding what tools miss
- Balancing hunting with response
- Proving value (no alerts = no visible work)
- Keeping skills sharp

**How to succeed:**

- Study advanced attacker techniques
- Read threat reports daily
- Build your own tools
- Share findings with team

**Time to next role:** 2-4 years

---

### Incident Responder

**What you do:**

You jump in during active breaches. You contain, eradicate, and recover.

**Daily tasks:**

- Respond to major incidents
- Contain active threats
- Eradicate malware
- Recover systems
- Document full timeline
- Brief leadership
- Coordinate with legal, HR, PR
- Write post-incident reports

**Example response:**

```text
Incident: Ransomware spreading across network

Hour 1: Confirm incident, activate IR plan
Hour 2: Isolate affected machines
Hour 3: Identify ransomware family
Hour 4: Check backups
Hour 5: Begin restoration
Hour 6: Notify leadership
Hour 8: Eradicate malware
Hour 12: Verify clean systems
Hour 24: Begin restoration
Day 2-7: Full recovery
Week 2: Post-incident report
```

**Skills you need:**

- Deep forensics
- Malware analysis
- System administration
- Network analysis
- Crisis communication
- Legal awareness
- Project management

**Tools you use:**

- Forensic suites (FTK, EnCase)
- Memory analysis (Volatility)
- Malware sandboxes
- Network forensics
- Backup systems

**Challenges:**

- High pressure
- Long hours
- Unknown threats
- Blame from leadership
- Emotional toll

**How to succeed:**

- Practice in labs constantly
- Build checklists and playbooks
- Learn from every incident
- Take care of your mental health

**Time to next role:** 3-5 years

---

### Threat Hunter (Specialist)

**What you do:**

You focus only on hunting. No alerts, no tickets. Just proactive search.

**Daily tasks:**

- Research new attacker techniques
- Form hypotheses
- Hunt across all data
- Build detection rules
- Document findings
- Train others
- Work with threat intel team

**Example hunt:**

```text
Hypothesis: APT might be using DNS tunneling

Step 1: Analyze DNS traffic patterns
Step 2: Look for unusual domain lengths
Step 3: Check for high query volume to single domain
Step 4: Found suspicious domain: "a1b2c3d4.evil.com"
Step 5: Analyze - data exfiltration via DNS
Step 6: Scope - which machines?
Step 7: Block domain, contain hosts
Step 8: Build DNS monitoring rule
```

**Skills you need:**

- Expert MITRE ATT&CK
- Expert forensics
- Expert malware analysis
- Data analysis
- Scripting
- Threat intel
- Creativity

**Tools you use:**

- SIEM (expert level)
- EDR (expert level)
- Custom hunting tools
- Data analytics platforms
- Threat intel platforms

**Challenges:**

- Proving value (no alerts)
- Finding new techniques
- Keeping up with attackers
- Isolation from team

**How to succeed:**

- Read everything
- Build a hunting methodology
- Share findings
- Collaborate with Red Team

---

### Digital Forensics Analyst

**What you do:**

You analyze evidence from devices. You support investigations and legal cases.

**Daily tasks:**

- Image hard drives
- Recover deleted files
- Analyze artifacts (registry, logs, browser)
- Build timelines
- Write forensic reports
- Testify in court if needed
- Maintain chain of custody

**Example investigation:**

```text
Case: Suspected insider data theft

Step 1: Image suspect's laptop
Step 2: Recover deleted files
Step 3: Analyze USB history
Step 4: Check browser history
Step 5: Analyze email
Step 6: Build timeline of activity
Step 7: Write report
Step 8: Present findings to legal
```

**Skills you need:**

- File systems (NTFS, ext4, APFS)
- Forensic tools
- Legal procedures
- Chain of custody
- Report writing
- Testimony skills

**Tools you use:**

- Autopsy
- FTK
- EnCase
- Volatility
- Eric Zimmerman tools
- Cellebrite (mobile)

**Challenges:**

- Legal pressure
- Complex cases
- Time-consuming
- Court testimony stress

**How to succeed:**

- Learn forensics deeply
- Practice on test images
- Understand legal process
- Stay neutral

---

### Malware Analyst

**What you do:**

You study malicious software to understand how it works.

**Daily tasks:**

- Receive malware samples
- Analyze in sandbox
- Reverse engineer code
- Identify capabilities
- Write signatures
- Report findings
- Track malware families

**Example analysis:**

```text
Sample: suspicious.exe

Step 1: Static analysis (strings, PE headers)
Step 2: Dynamic analysis (run in sandbox)
Step 3: Observe network traffic
Step 4: Identify C2 server
Step 5: Reverse engineer code
Step 6: Document capabilities
Step 7: Write detection signature
Step 8: Share with team
```

**Skills you need:**

- Assembly language
- Debuggers
- Reverse engineering
- Programming
- Network analysis
- Patience

**Tools you use:**

- IDA Pro / Ghidra
- x64dbg
- OllyDbg
- Cuckoo Sandbox
- Any.run
- PEStudio

**Challenges:**

- Obfuscated malware
- Anti-analysis techniques
- Time-consuming
- Constant learning

**How to succeed:**

- Learn assembly
- Practice on safe samples
- Read malware reports
- Build a lab

---

### Security Operations Manager

**What you do:**

You lead the SOC team. You handle strategy, people, and reporting.

**Daily tasks:**

- Manage staff and schedules
- Set SOC strategy
- Report to leadership
- Handle budget
- Improve processes
- Hire and train
- Handle escalations

**Skills you need:**

- Leadership
- Communication
- Business acumen
- Technical depth
- Project management
- Budgeting

**Tools you use:**

- Management platforms
- Reporting tools
- Budget software
- HR systems

**Challenges:**

- Balancing technical and business
- Managing burnout
- Proving SOC value
- Budget constraints
- Staff turnover

**How to succeed:**

- Learn business skills
- Build strong team
- Automate where possible
- Communicate value clearly

---

## 3. Daily Work Across All Tiers

### A typical SOC day (Tier 1)

**Morning:**

- Handover from night shift
- Check email and alerts
- Review overnight incidents
- Prioritize queue

**Midday:**

- Investigate alerts
- Correlate events
- Contact users if needed
- Update tickets

**Afternoon:**

- Continue investigations
- Attend meetings
- Document findings
- Handover to night shift

### Alert triage process (all tiers)

1. **Alert fires** - SIEM detects something
2. **Read alert** - What triggered it?
3. **Gather context** - User, host, time, IP
4. **Check history** - Has this happened before?
5. **Decide** - False positive or real?
6. **Act** - Close or escalate
7. **Document** - Write notes

### Escalation path

```text
Tier 1 -> Tier 2 -> Tier 3 -> Incident Responder
   |          |          |            |
 False    Deeper     Hunt &       Full IR
Positive  Invest.    Lead
```

---

## 4. Skills You Need at Each Tier

| Skill | Tier 1 | Tier 2 | Tier 3 | IR |
|-------|--------|--------|--------|-----|
| Networking | Basic | Good | Strong | Strong |
| Linux | Basic | Good | Strong | Strong |
| Windows | Basic | Good | Strong | Strong |
| SIEM | Basic | Advanced | Expert | Expert |
| Log analysis | Basic | Good | Expert | Expert |
| Forensics | No | Basic | Strong | Expert |
| Malware analysis | No | Basic | Strong | Expert |
| Scripting | No | Basic | Strong | Strong |
| Threat intel | No | Basic | Strong | Strong |
| Leadership | No | No | Basic | Strong |

---

## 5. Tools You Will Use at Each Tier

| Tool | Tier 1 | Tier 2 | Tier 3 | IR |
|------|--------|--------|--------|-----|
| SIEM | Yes | Yes | Yes | Yes |
| EDR | Yes | Yes | Yes | Yes |
| VirusTotal | Yes | Yes | Yes | Yes |
| Ticketing | Yes | Yes | Yes | Yes |
| Threat intel | No | Yes | Yes | Yes |
| Forensics | No | Basic | Yes | Yes |
| Sandbox | No | Yes | Yes | Yes |
| Custom scripts | No | Basic | Yes | Yes |
| Memory forensics | No | No | Yes | Yes |

---

## 6. Salary and Career Growth

### Salary (2026, Global Average)

| Role | Entry | Mid | Senior |
|------|-------|-----|--------|
| SOC Tier 1 | $50k | $65k | $85k |
| SOC Tier 2 | $65k | $85k | $110k |
| SOC Tier 3 | $85k | $110k | $140k |
| Incident Responder | $80k | $110k | $150k |
| Threat Hunter | $90k | $120k | $160k |
| Forensics Analyst | $75k | $105k | $145k |
| Malware Analyst | $85k | $115k | $155k |
| SOC Manager | $110k | $140k | $180k |

**Note:** Salaries vary by country. US pays highest. Remote work common.

### Career growth

| Year | Role |
|------|------|
| 0-1 | SOC Tier 1 |
| 1-2 | SOC Tier 2 |
| 2-4 | SOC Tier 3 |
| 4-6 | Incident Responder / Threat Hunter |
| 6-10 | Senior roles / Manager |
| 10+ | Director / CISO |

### Career moves

- Blue Team -> Red Team (common)
- Blue Team -> Cloud Security
- Blue Team -> Forensics
- Blue Team -> Management
- Blue Team -> Threat Intel

---

## 7. How to Get Started

### Step 1: Learn the core

Finish `01-core` first. Do not skip.

### Step 2: Build a home lab

- Install VirtualBox
- Kali Linux (attacker)
- Windows 10 (target)
- Ubuntu Server (target)
- Metasploitable (target)

### Step 3: Practice

- TryHackMe: SOC Level 1 path
- Blue Team Labs Online
- LetsDefend
- CyberDefenders

### Step 4: Learn SIEM

- Splunk Free (500 MB/day)
- ELK Stack (free)
- Wazuh (free)

### Step 5: Build a portfolio

- Write up labs on GitHub
- Document incidents
- Create detection rules

### Step 6: Apply

- SOC Tier 1
- IT Support (as entry)
- NOC Analyst
- Help Desk

### Step 7: Keep learning

- Read threat reports
- Follow security news
- Join communities
- Attend conferences

---

## 8. Common Challenges

| Challenge | Reality |
|-----------|---------|
| Shift work | Nights, weekends |
| Alert fatigue | Many false positives |
| Burnout | High in SOC |
| Boring days | Then chaos |
| Imposter syndrome | Common |
| Constant learning | Never stops |
| On-call | Emergencies happen |
| Management pressure | Prove value |

### How to survive

- Take breaks
- Automate what you can
- Learn continuously
- Build a support network
- Document everything
- Say no to burnout
- Move up or out if stuck

---

## 9. Real-World Scenarios

### Scenario 1: Ransomware attack

1. **Detection:** Files being encrypted on shared drive
2. **Alert:** EDR flags suspicious process
3. **Response:**
   - Isolate affected machines
   - Disable user accounts
   - Identify ransomware family
   - Restore from backups
   - Report to management
4. **Recovery:** Restore systems, verify integrity
5. **Post-mortem:** How did it happen? How to prevent?

### Scenario 2: Phishing campaign

1. **Detection:** Users report suspicious email
2. **Alert:** Email gateway flags it
3. **Response:**
   - Block sender
   - Remove email from all inboxes
   - Check who clicked
   - Reset credentials if needed
   - Notify users
4. **Recovery:** No damage if caught early
5. **Post-mortem:** Improve email filtering, training

### Scenario 3: Insider threat

1. **Detection:** Unusual file access by employee
2. **Alert:** DLP flags data exfiltration
3. **Response:**
   - Monitor user activity
   - Preserve evidence
   - Involve HR and legal
   - Interview if needed
   - Disable access
4. **Recovery:** Assess damage, notify affected
5. **Post-mortem:** Improve access controls, monitoring

---

## Practice Tasks

- [ ] Install a SIEM (Splunk Free or ELK)
- [ ] Complete TryHackMe SOC Level 1
- [ ] Read a threat report
- [ ] Write 5 detection rules
- [ ] Investigate a phishing email
- [ ] Analyze a PCAP file
- [ ] Set up Wazuh
- [ ] Write an incident report
- [ ] Map a threat to MITRE ATT&CK
- [ ] Build a home SOC lab

---

## Free Practice

- TryHackMe SOC Level 1
- LetsDefend
- CyberDefenders
- Blue Team Labs Online
- Splunk Free
- Wazuh
- Security Blue Team (free courses)

---

## Key Terms

| Term | Meaning |
|------|---------|
| SOC | Security Operations Center |
| SIEM | Log collection and analysis |
| EDR | Endpoint detection |
| MITRE ATT&CK | Adversary tactics |
| IOC | Indicator of Compromise |
| TTP | Tactics, Techniques, Procedures |
| Threat Hunting | Proactive search |
| Triage | Prioritize alerts |
| False Positive | Wrong alert |
| True Positive | Real alert |

---

## What now?

Next path: `red-team.md`

> Ethical Use Only
> Only hack systems you own or have written permission to test.
> Never use these skills to break the law.
