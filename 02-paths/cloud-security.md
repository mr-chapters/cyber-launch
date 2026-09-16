# Cloud Security - Deep Dive

Cloud Security is one of the fastest-growing fields in cybersecurity. Companies are moving everything to the cloud, and they need people who can secure it. This path pays well and has high demand.

---

## What you will learn

1. What is Cloud Security?
2. Every role explained in detail
3. Daily work in each role
4. Skills you need
5. Tools you will use
6. Cloud providers (AWS, Azure, GCP)
7. Cloud attack techniques
8. Salary and career growth
9. How to get started
10. Common challenges

---

## 1. What is Cloud Security?

Cloud Security is protecting data, applications, and infrastructure that run in the cloud.

**What is the cloud?**

The cloud is someone else's computers that you rent. Instead of buying servers, you rent them from Amazon (AWS), Microsoft (Azure), or Google (GCP).

**Why companies use cloud:**

- Cheaper than buying hardware
- Scale up or down instantly
- Global reach
- No maintenance
- Pay only for what you use

**The shared responsibility model:**

This is the most important concept in cloud security.

| Layer | Cloud Provider | You (Customer) |
|-------|----------------|----------------|
| Physical security | ✅ | ❌ |
| Hardware | ✅ | ❌ |
| Network | ✅ | ❌ |
| Hypervisor | ✅ | ❌ |
| Operating system | Depends | Depends |
| Applications | ❌ | ✅ |
| Data | ❌ | ✅ |
| Identity | ❌ | ✅ |

**Simple rule:** The cloud provider secures the cloud. You secure what you put IN the cloud.

**Why Cloud Security matters:**

- Most companies now use cloud
- Misconfigurations are the #1 cause of cloud breaches
- Cloud skills pay 20-30% more
- High demand, low supply of skilled people

**The reality:**

- You must learn one cloud provider deeply
- Misconfigurations are common and dangerous
- Automation is essential
- Identity is the new perimeter

---

## 2. Every Role Explained in Detail

### Cloud Security Engineer

**What you do:**

You build and maintain security controls in cloud environments.

**Daily tasks:**

- Review cloud configurations
- Manage IAM policies
- Set up logging and monitoring
- Automate security checks
- Respond to cloud alerts
- Work with developers
- Document everything

**Example day:**

```
09:00 - Review overnight alerts
09:30 - Fix a misconfigured S3 bucket
10:30 - Update IAM policies
12:00 - Meeting with DevOps team
13:00 - Write Terraform security module
15:00 - Investigate unusual API calls
16:30 - Document findings
17:00 - Handover
```

**Skills you need:**

- One cloud provider (AWS, Azure, or GCP)
- IAM (Identity and Access Management)
- Networking in cloud
- Infrastructure as Code (Terraform)
- Scripting (Python, Bash)
- Containers (Docker, Kubernetes)
- Linux

**Tools you use:**

- AWS Security Hub / Azure Defender / GCP Security Command Center
- Terraform
- Checkov, Trivy
- CloudTrail, CloudWatch
- Prowler, ScoutSuite

**Challenges:**

- Fast-changing cloud services
- Complex IAM policies
- Developer pushback
- Shadow IT
- Cost vs security

**How to succeed:**

- Learn one cloud deeply
- Automate everything
- Understand developer workflows
- Stay current with new services

---

### Cloud Security Architect

**What you do:**

You design the security architecture for cloud environments.

**Daily tasks:**

- Design secure cloud architectures
- Review designs from teams
- Set security standards
- Advise leadership
- Evaluate new services
- Document architecture

**Example task:**

```
Task: Design secure architecture for new app

Step 1: Understand app requirements
Step 2: Choose cloud services
Step 3: Design network segmentation
Step 4: Design IAM model
Step 5: Design encryption strategy
Step 6: Design logging and monitoring
Step 7: Document architecture
Step 8: Present to stakeholders
```

**Skills you need:**

- Deep cloud knowledge (multi-cloud)
- Security architecture
- Networking
- Compliance frameworks
- Communication
- Business acumen

**Tools you use:**

- Architecture diagram tools (draw.io, Lucidchart)
- Cloud provider tools
- IaC tools
- Security frameworks

**Challenges:**

- Balancing security and usability
- Multi-cloud complexity
- Legacy systems
- Stakeholder alignment

**How to succeed:**

- Learn multiple clouds
- Study compliance frameworks
- Build communication skills
- Stay strategic

---

### DevSecOps Engineer

**What you do:**

You embed security into the software development pipeline.

**Daily tasks:**

- Integrate security tools into CI/CD
- Automate security testing
- Review code for security
- Train developers
- Respond to pipeline alerts
- Improve processes

**Example pipeline:**

```
Developer commits code
    ↓
Static analysis (SAST)
    ↓
Dependency scan (SCA)
    ↓
Container scan
    ↓
IaC scan
    ↓
Deploy to staging
    ↓
Dynamic analysis (DAST)
    ↓
Deploy to production
```

**Skills you need:**

- CI/CD (Jenkins, GitLab, GitHub Actions)
- Containers (Docker, Kubernetes)
- IaC (Terraform, CloudFormation)
- Scripting (Python, Bash)
- Security tools (SAST, DAST, SCA)
- Cloud platforms

**Tools you use:**

- GitHub Actions, GitLab CI
- Jenkins
- Snyk, Trivy, Checkov
- SonarQube
- OWASP ZAP
- Vault

**Challenges:**

- Developer resistance
- Speed vs security
- Tool sprawl
- False positives
- Pipeline complexity

**How to succeed:**

- Learn developer workflows
- Automate everything
- Reduce friction
- Build trust with developers

---

### Application Security (AppSec) Engineer

**What you do:**

You secure applications before they ship.

**Daily tasks:**

- Review code for vulnerabilities
- Run security tests
- Threat model new features
- Train developers
- Respond to findings
- Improve secure coding practices

**Example review:**

```
Code review: User login function

Check 1: Input validation? ✅
Check 2: SQL injection? ❌ Found
Check 3: Password hashing? ✅
Check 4: Rate limiting? ❌ Missing
Check 5: Logging? ✅

Report: 2 issues found
Recommendation: Fix SQLi, add rate limiting
```

**Skills you need:**

- Programming (multiple languages)
- Web security (OWASP Top 10)
- API security
- Threat modeling
- Code review
- Communication

**Tools you use:**

- SAST (SonarQube, Checkmarx)
- DAST (OWASP ZAP, Burp)
- SCA (Snyk, Dependabot)
- IAST tools
- Threat modeling tools

**Challenges:**

- Developer pushback
- Legacy code
- Speed vs security
- Complex apps
- False positives

**How to succeed:**

- Learn to code well
- Understand business context
- Build developer relationships
- Automate where possible

---

### Cloud Security Analyst

**What you do:**

You monitor cloud environments for threats and respond to incidents.

**Daily tasks:**

- Monitor cloud logs
- Investigate alerts
- Respond to incidents
- Tune detection rules
- Document findings
- Report to team

**Example investigation:**

```
Alert: Unusual API calls from new IP

Step 1: Check user account
Step 2: Check source IP reputation
Step 3: Review API call history
Step 4: Check for data access
Step 5: Determine if compromised
Step 6: Contain if needed
Step 7: Document
```

**Skills you need:**

- Cloud platforms
- SIEM (Splunk, Sentinel)
- Log analysis
- Incident response
- Scripting
- Networking

**Tools you use:**

- AWS GuardDuty / Azure Sentinel / GCP Chronicle
- Splunk, ELK
- CloudTrail, CloudWatch
- Prowler, ScoutSuite

**Challenges:**

- Alert volume
- Cloud complexity
- Limited visibility
- Fast-changing environment

**How to succeed:**

- Learn cloud deeply
- Build detection rules
- Automate triage
- Stay curious

---

### Cloud Penetration Tester

**What you do:**

You test cloud environments for weaknesses.

**Daily tasks:**

- Test IAM configurations
- Test network exposure
- Test storage permissions
- Test serverless functions
- Test containers
- Document findings

**Example test:**

```
Target: AWS environment

Test 1: S3 bucket permissions
Result: Public bucket found ❌

Test 2: IAM role trust policies
Result: Overly permissive role ❌

Test 3: Security group rules
Result: SSH open to internet ❌

Test 4: Lambda function permissions
Result: Excessive permissions ❌

Report: 4 findings
Severity: 2 Critical, 2 High
```

**Skills you need:**

- Cloud platforms (deep)
- Penetration testing
- Scripting
- IAM
- Networking
- Report writing

**Tools you use:**

- Pacu (AWS)
- MicroBurst (Azure)
- ScoutSuite
- Prowler
- CloudGoat (labs)
- Custom scripts

**Challenges:**

- Cloud complexity
- Shared responsibility confusion
- Limited tooling
- Fast-changing services

**How to succeed:**

- Learn cloud deeply
- Practice in cloud labs
- Study cloud attacks
- Build custom tools

---

## 3. Daily Work in Each Role

### A typical Cloud Security Engineer day

**Morning:**

- Review overnight alerts
- Check cloud security posture
- Respond to urgent issues

**Midday:**

- Work on security automation
- Review configurations
- Meet with teams

**Afternoon:**

- Fix misconfigurations
- Document findings
- Plan improvements

### A typical DevSecOps day

**Morning:**

- Check pipeline security alerts
- Review failed builds
- Respond to developer questions

**Midday:**

- Improve security tooling
- Write automation scripts
- Review code

**Afternoon:**

- Train developers
- Document processes
- Plan next improvements

---

## 4. Skills You Need

### Technical skills

| Skill | Why |
|-------|-----|
| Cloud platform | Core skill |
| IAM | Most important |
| Networking | Cloud networks |
| Linux | Most cloud runs Linux |
| Scripting | Automation |
| IaC | Infrastructure as code |
| Containers | Modern apps |
| Kubernetes | Orchestration |
| CI/CD | DevSecOps |
| Cryptography | Encryption |

### Soft skills

| Skill | Why |
|-------|-----|
| Communication | Work with teams |
| Automation mindset | Cloud is automated |
| Business understanding | Balance security and speed |
| Continuous learning | Cloud changes fast |
| Documentation | Share knowledge |
| Problem-solving | Complex environments |

### Frameworks to know

| Framework | Use |
|-----------|-----|
| CIS Benchmarks | Cloud hardening |
| NIST CSF | Security framework |
| CSA CCM | Cloud controls |
| MITRE ATT&CK | Cloud techniques |
| OWASP Top 10 | Web security |

---

## 5. Tools You Will Use

### Cloud provider tools

| Provider | Security Tools |
|----------|----------------|
| AWS | Security Hub, GuardDuty, CloudTrail, Config |
| Azure | Defender for Cloud, Sentinel, Monitor |
| GCP | Security Command Center, Chronicle, Cloud Armor |

### Cloud Security Posture Management (CSPM)

| Tool | Use |
|------|-----|
| Prowler | AWS, Azure, GCP |
| ScoutSuite | Multi-cloud |
| Checkov | IaC scanning |
| Wiz | Commercial |
| Orca | Commercial |

### IaC security

| Tool | Use |
|------|-----|
| Checkov | Terraform, CloudFormation |
| tfsec | Terraform |
| Terrascan | IaC |
| KICS | IaC |

### Container security

| Tool | Use |
|------|-----|
| Trivy | Container scanning |
| Clair | Container scanning |
| Falco | Runtime security |
| Aqua | Commercial |

### Kubernetes security

| Tool | Use |
|------|-----|
| kube-bench | CIS benchmarks |
| kubesec | Manifest scanning |
| Polaris | Best practices |
| OPA/Gatekeeper | Policy enforcement |

### Secrets management

| Tool | Use |
|------|-----|
| HashiCorp Vault | Secrets |
| AWS Secrets Manager | AWS secrets |
| Azure Key Vault | Azure secrets |
| GCP Secret Manager | GCP secrets |

---

## 6. Cloud Providers (AWS, Azure, GCP)

### AWS (Amazon Web Services)

**Market share:** ~32% (largest)

**Key services:**
| Service | What it does |
|---------|--------------|
| EC2 | Virtual machines |
| S3 | Storage |
| IAM | Identity |
| VPC | Networking |
| Lambda | Serverless |
| RDS | Databases |
| CloudTrail | Logging |

**Security tools:** GuardDuty, Security Hub, Inspector, Macie

### Azure (Microsoft)

**Market share:** ~23%

**Key services:**
| Service | What it does |
|---------|--------------|
| Virtual Machines | Compute |
| Blob Storage | Storage |
| Entra ID | Identity |
| Virtual Network | Networking |
| Functions | Serverless |
| SQL Database | Databases |
| Monitor | Logging |

**Security tools:** Defender for Cloud, Sentinel, Key Vault

### GCP (Google Cloud Platform)

**Market share:** ~11%

**Key services:**
| Service | What it does |
|---------|--------------|
| Compute Engine | Virtual machines |
| Cloud Storage | Storage |
| IAM | Identity |
| VPC | Networking |
| Cloud Functions | Serverless |
| Cloud SQL | Databases |
| Cloud Logging | Logging |

**Security tools:** Security Command Center, Chronicle, Cloud Armor

### Which one to learn?

| If you... | Learn... |
|-----------|----------|
| Want most jobs | AWS |
| Work in enterprise | Azure |
| Like data/ML | GCP |
| Want to start | AWS |

**My advice:** Start with AWS. It has the most jobs and best learning resources.

---

## 7. Cloud Attack Techniques

### Common cloud attacks

| Attack | What it does |
|--------|--------------|
| Misconfigured S3 | Public storage bucket |
| Overly permissive IAM | Too much access |
| Exposed credentials | Keys in code |
| SSRF | Server-side request forgery |
| Container escape | Break out of container |
| Metadata service abuse | Steal credentials |
| Subdomain takeover | Hijack subdomains |
| Supply chain | Compromise dependencies |

### Real-world examples

**Capital One (2019):**
- Misconfigured WAF
- SSRF attack
- 100 million records stolen
- $80 million fine

**SolarWinds (2020):**
- Supply chain attack
- Malicious update
- 18,000+ customers affected
- Nation-state attack

**CodeSpaces (2022):**
- GitHub Actions misconfiguration
- Environment variables leaked
- AWS credentials exposed

### Cloud attack phases

```
Phase 1: Reconnaissance
- Find cloud assets
- Check public buckets
- Enumerate services

Phase 2: Initial Access
- Stolen credentials
- Misconfigured services
- SSRF

Phase 3: Persistence
- Create new IAM user
- Add access keys
- Modify trust policies

Phase 4: Privilege Escalation
- Exploit IAM misconfigs
- Assume roles
- Access secrets

Phase 5: Lateral Movement
- Move between accounts
- Access other services
- Pivot to on-prem

Phase 6: Exfiltration
- Copy data to attacker bucket
- Use legitimate services
- Cover tracks
```

---

## 8. Salary and Career Growth

### Salary (2026, Global Average)

| Role | Entry | Mid | Senior |
|------|-------|-----|--------|
| Cloud Security Analyst | $70k | $100k | $140k |
| Cloud Security Engineer | $85k | $125k | $170k |
| Cloud Security Architect | $110k | $150k | $200k+ |
| DevSecOps Engineer | $90k | $130k | $175k |
| AppSec Engineer | $85k | $120k | $165k |
| Cloud Pen Tester | $90k | $130k | $180k |

**Note:** Cloud security pays 20-30% more than traditional security roles.

### Career growth

| Year | Role |
|------|------|
| 0-2 | Cloud Security Analyst |
| 2-4 | Cloud Security Engineer |
| 4-6 | Senior Engineer |
| 6-8 | Architect / Lead |
| 8-12 | Principal / Manager |
| 12+ | Director / CISO |

### Career moves

- Cloud Security → DevSecOps
- Cloud Security → AppSec
- Cloud Security → Cloud Pen Testing
- Cloud Security → Architecture
- Cloud Security → Management

---

## 9. How to Get Started

### Step 1: Learn the core

Finish `01-core` first. Do not skip.

### Step 2: Pick one cloud

Start with AWS. It has the most resources.

### Step 3: Learn the basics

- Create free tier account
- Learn core services (EC2, S3, IAM, VPC)
- Understand billing
- Set up MFA

### Step 4: Learn security

- IAM deep dive
- Security groups
- Encryption
- Logging (CloudTrail)
- Monitoring (CloudWatch)

### Step 5: Practice

- AWS Free Tier
- CloudGoat (labs)
- flaws.cloud (labs)
- TryHackMe cloud rooms
- Hack The Box cloud machines

### Step 6: Learn automation

- Terraform
- Python (boto3)
- CI/CD
- Containers

### Step 7: Build a portfolio

- Document cloud projects
- Write about cloud security
- Build security tools
- Share on GitHub

### Step 8: Apply

- Cloud Security Analyst
- DevSecOps Engineer
- Cloud Engineer (with security focus)
- IT with cloud exposure

---

## 10. Common Challenges

| Challenge | Reality |
|-----------|---------|
| Fast-changing services | New services every month |
| Complex IAM | Easy to misconfigure |
| Shared responsibility | Confusing boundaries |
| Developer pushback | Security slows them down |
| Cost vs security | Budget constraints |
| Tool sprawl | Too many tools |
| Limited visibility | Cannot see everything |
| Compliance complexity | Many frameworks |

### How to survive

- Focus on one cloud
- Automate everything
- Learn continuously
- Build relationships
- Document everything
- Take breaks
- Stay curious

---

## Practice Tasks

- [ ] Create AWS free tier account
- [ ] Set up MFA on AWS
- [ ] Learn IAM basics
- [ ] Create an S3 bucket (private)
- [ ] Launch an EC2 instance
- [ ] Set up CloudTrail
- [ ] Complete CloudGoat scenarios
- [ ] Try flaws.cloud
- [ ] Write a Terraform config
- [ ] Complete TryHackMe cloud rooms
- [ ] Read a cloud breach report
- [ ] Build a cloud security checklist

---

## Free Practice

- AWS Free Tier
- Azure Free Account
- GCP Free Tier
- CloudGoat
- flaws.cloud
- TryHackMe
- Hack The Box
- AWS Skill Builder (free courses)
- Microsoft Learn (free)

---

## Key Terms

| Term | Meaning |
|------|---------|
| Cloud | Rented computers |
| IAM | Identity and Access Management |
| S3 | AWS storage |
| EC2 | AWS virtual machines |
| VPC | Virtual Private Cloud |
| CSPM | Cloud Security Posture Management |
| IaC | Infrastructure as Code |
| SSRF | Server-Side Request Forgery |
| Shared Responsibility | Who secures what |
| Least Privilege | Minimum access needed |

---

## What now?

Next path: `grc.md`

> **Ethical Use Only**
> Only hack systems you own or have written permission to test.
> Never use these skills to break the law.
