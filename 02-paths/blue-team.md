# Blue Team (Defense) - Deep Dive

Blue Team is the defensive side of cybersecurity. You protect the organization, monitor for threats, and respond when something goes wrong. This is the most common entry point into cybersecurity.

---

## What you will learn
1. What is Blue Team?
2. Roles in Blue Team
3. Daily work
4. Skills you need
5. Tools you will use
6. Certifications and learning path
7. Salary and career growth
8. How to get started
9. Common challenges
10. Real-world scenarios

---

## 1. What is Blue Team?

Blue Team = defenders.

You are the security team inside an organization. Your job is to:
- Prevent attacks
- Detect attacks
- Respond to attacks
- Recover from attacks

**Blue Team vs Red Team:**
| Aspect | Blue Team | Red Team |
|--------|-----------|----------|
| Role | Defend | Attack |
| Goal | Protect | Find weaknesses |
| Mindset | Detective | Adversary |
| Daily | Monitor, respond | Scan, exploit |
| Tools | SIEM, EDR | Nmap, Metasploit |

**Why Blue Team matters:**
- Most security jobs are defensive
- Easier to enter than Red Team
- Steady demand, always hiring
- Clear career path

**The reality:**
- You will not stop every attack
- You will work shifts (SOC)
- You will see boring days and chaotic days
- You will learn something new constantly

---

## 2. Roles in Blue Team

### SOC Analyst (Tier 1)
**What you do:** Monitor alerts, triage, escalate.

**Daily tasks:**
- Watch SIEM dashboard
- Investigate alerts
- Close false positives
- Escalate real threats
- Document everything

**Skills:**
- SIEM basics
- Log reading
- Network basics
- Ticketing systems

**Entry:** Easiest entry point.

---

### SOC Analyst (Tier 2)
**What you do:** Deep investigation of escalated alerts.

**Daily tasks:**
- Investigate complex alerts
- Correlate events
- Use threat intel
- Write reports
- Mentor Tier 1

**Skills:**
- Advanced SIEM
- Threat hunting
- Malware analysis basics
- Forensics basics

**Entry:** 1-2 years as Tier 1.

---

### SOC Analyst (Tier 3)
**What you do:** Lead investigations, improve detection.

**Daily tasks:**
- Lead incident response
- Build detection rules
- Threat hunt
- Mentor team
- Improve processes

**Skills:**
- Deep forensics
- Malware analysis
- Detection engineering
- Automation

**Entry:** 3-5 years experience.

---

### Incident Responder
**What you do:** Respond to active breaches.

**Daily tasks:**
- Contain active threats
- Eradicate malware
- Recover systems
- Document timeline
- Brief leadership

**Skills:**
- Forensics
- Malware analysis
- System administration
- Crisis communication

**Entry:** 2-4 years in SOC.

---

### Threat Hunter
**What you do:** Proactively search for hidden threats.

**Daily tasks:**
- Form hypotheses
- Search logs
- Identify anomalies
- Build detection rules
- Document findings

**Skills:**
- MITRE ATT&CK
- SIEM query languages
- Forensics
- Threat intel

**Entry:** 3-5 years in SOC.

---

### Digital Forensics Analyst
**What you do:** Analyze evidence from devices.

**Daily tasks:**
- Image drives
- Recover deleted files
- Analyze artifacts
- Write reports
- Testify in court

**Skills:**
- Forensics tools
- File systems
- Legal procedures
- Chain of custody

**Entry:** 2-4 years experience.

---

### Malware Analyst
**What you do:** Study malicious software.

**Daily tasks:**
- Reverse engineer malware
- Identify capabilities
- Write signatures
- Report findings
- Track malware families

**Skills:**
- Assembly
- Debuggers
- Sandboxes
- Programming

**Entry:** 3-5 years experience.

---

### Security Operations Manager
**What you do:** Lead the SOC team.

**Daily tasks:**
- Manage staff
- Set strategy
- Report to leadership
- Handle budget
- Improve processes

**Skills:**
- Leadership
- Communication
- Business acumen
- Technical depth

**Entry:** 5+ years experience.

---

## 3. Daily Work (Detailed)

### A typical SOC day
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

### Alert triage process
1. **Alert fires** - SIEM detects something
2. **Read alert** - What triggered it?
3. **Gather context** - User, host, time, IP
4. **Check history** - Has this happened before?
5. **Decide** - False positive or real?
6. **Act** - Close or escalate
7. **Document** - Write notes

### Example: Suspicious login alert
1. SIEM alerts: "Login from unusual location"
2. Check user: `john.doe@company.com`
3. Check history: John usually logs in from New York
4. Check current: Login from Russia, 3 AM
5. Check MFA: Was MFA used? No
6. Decide: Likely compromised
7. Action: Disable account, contact John, escalate

---

## 4. Skills You Need

### Technical skills
| Skill | Why |
|-------|-----|
| Networking | Understand traffic |
| Linux | Most servers |
| Windows | Most endpoints |
| SIEM | Core tool |
| Log analysis | Core skill |
| Scripting | Automation |
| Forensics | Investigations |
| Malware analysis | Threat understanding |

### Soft skills
| Skill | Why |
|-------|-----|
| Attention to detail | Spot anomalies |
| Calm under pressure | Active incidents |
| Communication | Brief leadership |
| Curiosity | Hunt threats |
| Patience | Long investigations |
| Documentation | Reports |

### Frameworks to know
| Framework | Use |
|-----------|-----|
| MITRE ATT&CK | Map attacker behavior |
| Cyber Kill Chain | Attack stages |
| NIST CSF | Security framework |
| Diamond Model | Intrusion analysis |
| Pyramid of Pain | Threat intel |

---

## 5. Tools You Will Use

### SIEM (Security Information and Event Management)
| Tool | Type | Notes |
|------|------|-------|
| Splunk | Commercial | Most popular |
| ELK Stack | Open source | Free |
| Wazuh | Open source | Free |
| Microsoft Sentinel | Cloud | Azure |
| IBM QRadar | Commercial | Enterprise |
| ArcSight | Commercial | Enterprise |

**What SIEM does:**
- Collects logs
- Correlates events
- Generates alerts
- Stores data
- Provides dashboards

### EDR (Endpoint Detection and Response)
| Tool | Notes |
|------|-------|
| CrowdStrike | Popular |
| SentinelOne | Popular |
| Microsoft Defender | Built-in |
| Carbon Black | Enterprise |

**What EDR does:**
- Monitors endpoints
- Detects malicious behavior
- Allows remote response
- Records activity

### Network tools
| Tool | Use |
|------|-----|
| Wireshark | Packet analysis |
| Zeek | Network monitoring |
| Suricata | IDS/IPS |
| Snort | IDS/IPS |
| NetFlow | Traffic analysis |

### Forensics tools
| Tool | Use |
|------|-----|
| Volatility | Memory forensics |
| Autopsy | Disk forensics |
| FTK | Disk forensics |
| Eric Zimmerman tools | Windows forensics |

### Threat intel
| Tool | Use |
|------|-----|
| VirusTotal | File/URL analysis |
| MISP | Threat sharing |
| AlienVault OTX | Threat intel |
| Shodan | Internet scanning |

---

## 6. Certifications and Learning Path

### Entry level
| Cert | Cost | Notes |
|------|------|-------|
| CompTIA Security+ | ~$400 | Baseline |
| CompTIA CySA+ | ~$400 | Blue Team focus |
| Blue Team Level 1 (BTL1) | ~$400 | Hands-on |
| GIAC GSEC | ~$2,500 | Expensive |

### Mid level
| Cert | Cost | Notes |
|------|------|-------|
| CompTIA CySA+ | ~$400 | Analyst |
| GIAC GCIH | ~$2,500 | Incident handler |
| GCIA | ~$2,500 | Analyst |
| GCFA | ~$2,500 | Forensics |

### Advanced
| Cert | Cost | Notes |
|------|------|-------|
| CISSP | ~$700 | Management |
| GIAC GCFA | ~$2,500 | Forensics |
| GIAC GNFA | ~$2,500 | Network forensics |

### Learning path
1. Security+ (basics)
2. Home lab (practice)
3. TryHackMe SOC Level 1
4. CySA+ (certification)
5. Job as SOC Analyst
6. Blue Team Level 1 or GCIH
7. Move up to Tier 2, 3, or specialize

---

## 7. Salary and Career Growth

### Salary (2026, Global Average)
| Role | Entry | Mid | Senior |
|------|-------|-----|--------|
| SOC Analyst Tier 1 | $50k | $65k | $85k |
| SOC Analyst Tier 2 | $65k | $85k | $110k |
| SOC Analyst Tier 3 | $85k | $110k | $140k |
| Incident Responder | $80k | $110k | $150k |
| Threat Hunter | $90k | $120k | $160k |
| Forensics Analyst | $75k | $105k | $145k |
| Malware Analyst | $85k | $115k | $155k |
| SOC Manager | $110k | $140k | $180k |

**Note:** Salaries vary by country. US pays highest. Remote work common.

### Career growth
| Year | Role |
|------|------|
| 0-1 | SOC Analyst Tier 1 |
| 1-2 | SOC Analyst Tier 2 |
| 2-4 | SOC Analyst Tier 3 |
| 4-6 | Incident Responder / Threat Hunter |
| 6-10 | Senior roles / Manager |
| 10+ | Director / CISO |

### Career moves
- Blue Team → Red Team (common)
- Blue Team → Cloud Security
- Blue Team → Forensics
- Blue Team → Management
- Blue Team → Threat Intel

---

## 8. How to Get Started

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

### Step 5: Get certified
- Security+ first
- Then CySA+
- Or Blue Team Level 1

### Step 6: Build a portfolio
- Write up labs on GitHub
- Document incidents
- Create detection rules

### Step 7: Apply
- SOC Analyst Tier 1
- IT Support (as entry)
- NOC Analyst
- Help Desk

### Step 8: Keep learning
- Read threat reports
- Follow security news
- Join communities
- Attend conferences

---

## 9. Common Challenges

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

## 10. Real-World Scenarios

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

> ⚠️ Ethical Use Only
> Only hack systems you own or have written permission to test.
> Never use these skills to break the law.
