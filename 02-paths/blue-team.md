
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
| SIEM | ✅ | ✅ | ✅ | ✅ |
| EDR | ✅ | ✅ | ✅ | ✅ |
| VirusTotal | ✅ | ✅ | ✅ | ✅ |
| Ticketing | ✅ | ✅ | ✅ | ✅ |
| Threat intel | ❌ | ✅ | ✅ | ✅ |
| Forensics | ❌ | Basic | ✅ | ✅ |
| Sandbox | ❌ | ✅ | ✅ | ✅ |
| Custom scripts | ❌ | Basic | ✅ | ✅ |
| Memory forensics | ❌ | ❌ | ✅ | ✅ |

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
- Blue Team → Red Team (common)
- Blue Team → Cloud Security
- Blue Team → Forensics
- Blue Team → Management
- Blue Team → Threat Intel

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

> ⚠️ Ethical Use Only
> Only hack systems you own or have written permission to test.
> Never use these skills to break the law.
