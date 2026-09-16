# IAM (Identity & Access Management) - Deep Dive

IAM is the field of controlling who can access what. It is one of the most underrated entry points into cybersecurity. Every company needs it, few people specialize in it, and it pays well.

---

## What you will learn

1. What is IAM?
2. Every role explained in detail
3. Daily work in each role
4. Skills you need
5. Tools you will use
6. Core IAM concepts
7. Authentication and authorization
8. Salary and career growth
9. How to get started
10. Common challenges

---

## 1. What is IAM?

IAM stands for Identity and Access Management.

**Simple definition:** IAM is how a company controls who can access what.

**The core questions IAM answers:**

- Who are you? (Authentication)
- What can you do? (Authorization)
- How do we prove it? (Auditing)

**Why IAM matters:**

- Every breach involves compromised identity
- Most attacks start with stolen credentials
- Companies have thousands of users
- Access must be managed carefully
- Compliance requires it

**The reality:**

- Deeply technical but not hacking
- Lots of directory work
- Automating access is key
- Underrated career path
- High demand, low supply

**IAM vs other paths:**

| Aspect | IAM | Blue Team | Red Team |
|--------|-----|-----------|----------|
| Focus | Access control | Detection | Attack |
| Daily | Directories, policies | Alerts, logs | Scans, exploits |
| Coding | Some | Some | Lots |
| Entry | Medium | Easy | Hard |
| Demand | High | High | Medium |

---

## 2. Every Role Explained in Detail

### IAM Engineer

**What you do:**

You build and maintain the systems that manage identities and access.

**Daily tasks:**

- Configure identity providers
- Set up SSO integrations
- Build user provisioning
- Automate access requests
- Troubleshoot login issues
- Document systems

**Example day:**

```
09:00 - Check overnight alerts
09:30 - Fix SSO issue for new app
10:30 - Build automation for user onboarding
12:00 - Lunch
13:00 - Meeting with HR on joiner/mover/leaver
14:30 - Configure MFA for new team
16:00 - Document new process
17:00 - Handover
```

**Example task — SSO integration:**

```
Task: Add new app to SSO

Step 1: Get app requirements
Step 2: Configure SAML/OIDC
Step 3: Map user attributes
Step 4: Test with pilot users
Step 5: Document
Step 6: Roll out to all users
```

**Skills you need:**

- Active Directory
- LDAP, SAML, OAuth, OIDC
- SSO and MFA
- Scripting (PowerShell, Python)
- Cloud IAM (AWS, Azure)
- Networking basics

**Tools you use:**

- Active Directory
- Azure AD / Entra ID
- Okta
- Ping Identity
- Keycloak
- SailPoint

**Challenges:**

- Legacy systems
- Complex integrations
- User frustration
- Security vs usability
- Constant changes

**How to succeed:**

- Learn AD deeply
- Master one SSO protocol
- Automate everything
- Document clearly
- Communicate well

---

### Identity Analyst

**What you do:**

You monitor and analyze access patterns to detect issues.

**Daily tasks:**

- Review access reports
- Investigate anomalies
- Check for excessive access
- Support audits
- Document findings
- Report to team

**Example investigation:**

```
Alert: User has admin access to 15 systems

Step 1: Check user role (should have 3)
Step 2: Review access history
Step 3: Check who approved access
Step 4: Determine if legitimate
Step 5: Remove excess access
Step 6: Document
```

**Skills you need:**

- Access analysis
- Attention to detail
- Excel
- Communication
- Understanding of roles
- Risk awareness

**Tools you use:**

- Identity governance tools
- Excel
- SIEM
- Access review platforms

**Challenges:**

- Too much data
- Access creep
- Political pushback
- Manual reviews
- Complexity

**How to succeed:**

- Automate reporting
- Build relationships
- Focus on high-risk access
- Document everything
- Stay organized

---

### PAM Specialist (Privileged Access Management)

**What you do:**

You secure the most powerful accounts in the company.

**Daily tasks:**

- Manage privileged accounts
- Set up session recording
- Rotate passwords
- Approve access requests
- Investigate privileged activity
- Document everything

**Example task — vault a server password:**

```
Task: Move admin password into vault

Step 1: Identify all admins
Step 2: Document current process
Step 3: Set up vault entry
Step 4: Configure check-in/check-out
Step 5: Train admins
Step 6: Rotate password
Step 7: Verify
```

**Skills you need:**

- Privileged access concepts
- PAM tools
- Windows and Linux admin
- Scripting
- Security best practices
- Compliance knowledge

**Tools you use:**

- CyberArk
- BeyondTrust
- Thycotic (Delinea)
- HashiCorp Vault
- AWS Secrets Manager

**Challenges:**

- Resistance from admins
- Legacy systems
- Complex integrations
- Break-glass scenarios
- Business continuity

**How to succeed:**

- Learn PAM tools deeply
- Understand admin workflows
- Automate rotation
- Document exceptions
- Build trust

---

### Authentication Engineer

**What you do:**

You build and maintain login and authentication systems.

**Daily tasks:**

- Configure MFA
- Set up passwordless auth
- Integrate biometrics
- Improve login UX
- Fix authentication issues
- Document systems

**Example task — roll out MFA:**

```
Task: Roll out MFA to 5000 users

Step 1: Pick MFA method
Step 2: Pilot with 100 users
Step 3: Gather feedback
Step 4: Train help desk
Step 5: Roll out by department
Step 6: Handle exceptions
Step 7: Monitor
```

**Skills you need:**

- Authentication protocols
- MFA methods
- Passwordless tech
- User experience
- Scripting
- Security best practices

**Tools you use:**

- Okta
- Azure AD
- Duo
- Auth0
- YubiKey
- Windows Hello

**Challenges:**

- User resistance
- Legacy apps
- Help desk load
- Security vs usability
- Exceptions

**How to succeed:**

- Focus on UX
- Plan rollouts carefully
- Train users well
- Handle exceptions
- Monitor adoption

---

### Identity Governance Analyst

**What you do:**

You ensure access is appropriate and approved.

**Daily tasks:**

- Run access reviews
- Track certifications
- Identify orphaned accounts
- Support audits
- Document processes
- Report findings

**Example task — quarterly access review:**

```
Task: Review access for finance team

Step 1: Generate access report
Step 2: Send to managers
Step 3: Collect approvals
Step 4: Remove denied access
Step 5: Document
Step 6: Report
```

**Skills you need:**

- Governance concepts
- Attention to detail
- Excel
- Communication
- Compliance knowledge
- Risk awareness

**Tools you use:**

- SailPoint
- Saviynt
- Identity governance platforms
- Excel
- ServiceNow

**Challenges:**

- Manual reviews
- Manager pushback
- Missing data
- Complexity
- Audit pressure

**How to succeed:**

- Automate reporting
- Simplify reviews
- Build relationships
- Document everything
- Focus on risk

---

### IAM Architect

**What you do:**

You design the overall IAM strategy and architecture.

**Daily tasks:**

- Design IAM architecture
- Set standards
- Evaluate new tools
- Advise leadership
- Document strategy
- Support major projects

**Example task — design IAM for merger:**

```
Task: Merge IAM for acquired company

Step 1: Assess current IAM at both
Step 2: Identify gaps
Step 3: Design target state
Step 4: Plan migration
Step 5: Coordinate with teams
Step 6: Execute
Step 7: Document
```

**Skills you need:**

- Deep IAM knowledge
- Architecture design
- Business understanding
- Communication
- Project management
- Strategic thinking

**Tools you use:**

- Architecture tools
- IAM platforms
- Documentation tools
- Diagram tools

**Challenges:**

- Complex environments
- Legacy systems
- Merger/acquisition issues
- Stakeholder alignment
- Budget

**How to succeed:**

- Learn multiple IAM tools
- Understand business
- Communicate clearly
- Stay strategic
- Document well

---

## 3. Daily Work in Each Role

### A typical IAM Engineer day

**Morning:**

- Check login issues
- Review access requests
- Troubleshoot SSO

**Midday:**

- Build automations
- Configure new apps
- Test integrations

**Afternoon:**

- Document changes
- Meet with teams
- Plan improvements

### A typical PAM Specialist day

**Morning:**

- Review privileged activity
- Check vault health
- Handle requests

**Midday:**

- Rotate passwords
- Investigate incidents
- Update policies

**Afternoon:**

- Document work
- Train admins
- Plan improvements

---

## 4. Skills You Need

### Technical skills

| Skill | Why |
|-------|-----|
| Active Directory | Core directory |
| LDAP | Directory protocol |
| SAML | SSO protocol |
| OAuth / OIDC | Modern auth |
| SSO | Single sign-on |
| MFA | Multi-factor |
| PowerShell | Windows automation |
| Python | General automation |
| Cloud IAM | AWS, Azure, GCP |
| Linux | Servers |

### Soft skills

| Skill | Why |
|-------|-----|
| Attention to detail | Access matters |
| Communication | Work with users |
| Patience | Complex issues |
| Documentation | Everything |
| Problem-solving | Troubleshooting |
| User empathy | Login issues are painful |
| Business understanding | Understand roles |
| Security mindset | Balance access |

### Frameworks to know

| Framework | Use |
|-----------|-----|
| NIST 800-63 | Digital identity |
| ISO 27001 | Access controls |
| SOX | Financial access |
| HIPAA | Health access |
| GDPR | Privacy access |
| Zero Trust | Modern approach |

---

## 5. Tools You Will Use

### Directory services

| Tool | Use |
|------|-----|
| Active Directory | Windows directories |
| Azure AD / Entra ID | Cloud directory |
| OpenLDAP | Linux directory |
| Okta | Cloud IdP |
| JumpCloud | Cloud directory |

### SSO and federation

| Tool | Use |
|------|-----|
| Okta | SSO platform |
| Ping Identity | SSO platform |
| Azure AD | SSO |
| Auth0 | Developer SSO |
| Keycloak | Open source SSO |

### MFA

| Tool | Use |
|------|-----|
| Duo | MFA platform |
| Okta Verify | MFA |
| Microsoft Authenticator | MFA |
| YubiKey | Hardware MFA |
| RSA SecurID | Enterprise MFA |

### PAM

| Tool | Use |
|------|-----|
| CyberArk | Enterprise PAM |
| BeyondTrust | Enterprise PAM |
| Delinea (Thycotic) | PAM |
| HashiCorp Vault | Secrets |
| AWS Secrets Manager | Cloud secrets |

### Identity governance

| Tool | Use |
|------|-----|
| SailPoint | Governance |
| Saviynt | Governance |
| One Identity | Governance |
| Omada | Governance |

---

## 6. Core IAM Concepts

### Authentication vs Authorization

| Concept | Question | Example |
|---------|----------|---------|
| Authentication | Who are you? | Login with password |
| Authorization | What can you do? | Access files |

**Authentication happens first. Then authorization.**

### Identity lifecycle

```
1. Joiner (new employee)
   - Create account
   - Assign roles
   - Provide access

2. Mover (role change)
   - Update roles
   - Remove old access
   - Add new access

3. Leaver (employee leaves)
   - Disable account
   - Remove all access
   - Preserve data
```

### Authentication factors

| Factor | Type | Example |
|--------|------|---------|
| Something you know | Knowledge | Password, PIN |
| Something you have | Possession | Phone, token |
| Something you are | Biometric | Fingerprint, face |
| Somewhere you are | Location | GPS, IP |
| Something you do | Behavior | Typing pattern |

### Single Sign-On (SSO)

**What it is:** Login once, access many apps.

**How it works:**
```
1. User visits app
2. App redirects to IdP
3. User authenticates
4. IdP sends token
5. User accesses app
```

**Benefits:**
- Fewer passwords
- Better security
- Easier management
- Better UX

### Multi-Factor Authentication (MFA)

**What it is:** Using 2+ factors to authenticate.

**Common combinations:**
- Password + SMS
- Password + app
- Password + hardware key
- Biometric + PIN

**Why it matters:** Passwords alone are not enough.

### Federation

**What it is:** Trust between organizations for authentication.

**Example:** Login to a website using your Google account.

**Protocols:**
- SAML
- OAuth
- OIDC

### Privileged Access Management (PAM)

**What it is:** Securing admin accounts.

**Why it matters:** Admin accounts are the biggest target.

**Key features:**
- Password vaulting
- Session recording
- Just-in-time access
- Approval workflows

### Zero Trust

**What it is:** Never trust, always verify.

**Principles:**
- Verify explicitly
- Least privilege
- Assume breach

**Why it matters:** Traditional perimeter security is dead.

---

## 7. Authentication and Authorization

### Authentication methods

| Method | Security | Usability |
|--------|----------|-----------|
| Password | Low | High |
| Password + MFA | Medium | Medium |
| Passwordless | High | High |
| Biometric | High | High |
| Certificate | Very High | Low |
| Hardware key | Very High | Medium |

### Authorization models

| Model | How it works |
|-------|--------------|
| RBAC | Role-based access control |
| ABAC | Attribute-based access control |
| PBAC | Policy-based access control |
| ReBAC | Relationship-based access control |

**RBAC example:**
```
Role: HR Manager
Permissions:
- View employee records
- Edit employee records
- Approve time off
- Cannot access payroll
```

### Access control lists (ACLs)

**What they are:** Lists of who can access what.

**Example:**
```
File: financial_report.pdf
Owner: CFO
Read: Finance team, Auditors
Write: CFO only
Delete: No one
```

### Least privilege

**What it is:** Give users only the access they need.

**Why it matters:** Limits damage from compromised accounts.

**Example:**
```
Bad: Give everyone admin access
Good: Give access based on role
```

---

## 8. Salary and Career Growth

### Salary (2026, Global Average)

| Role | Entry | Mid | Senior |
|------|-------|-----|--------|
| IAM Analyst | $60k | $85k | $115k |
| IAM Engineer | $75k | $105k | $145k |
| Identity Analyst | $65k | $90k | $120k |
| PAM Specialist | $85k | $120k | $160k |
| Authentication Engineer | $80k | $115k | $155k |
| Identity Governance Analyst | $65k | $90k | $120k |
| IAM Architect | $110k | $150k | $200k+ |

**Note:** IAM pays well because few people specialize in it.

### Career growth

| Year | Role |
|------|------|
| 0-2 | IAM Analyst |
| 2-4 | IAM Engineer |
| 4-6 | Senior Engineer |
| 6-8 | Lead / Architect |
| 8-12 | Principal |
| 12+ | Director / CISO |

### Career moves

- IAM → Cloud Security
- IAM → Security Engineering
- IAM → GRC
- IAM → Architecture
- IAM → Management

---

## 9. How to Get Started

### Step 1: Learn the core

Finish `01-core` first. Do not skip.

### Step 2: Learn Active Directory

- Install Windows Server
- Set up a domain
- Create users and groups
- Learn Group Policy
- Practice

### Step 3: Learn authentication

- Study SAML
- Study OAuth / OIDC
- Set up SSO
- Practice with free tools

### Step 4: Learn MFA

- Set up MFA on your accounts
- Learn different methods
- Understand trade-offs

### Step 5: Practice

- Set up Okta developer account
- Set up Azure AD free tier
- Practice SSO integrations
- Build a lab

### Step 6: Build a portfolio

- Document IAM projects
- Write about SSO
- Share on GitHub
- Create diagrams

### Step 7: Apply

- IAM Analyst
- Help Desk (as entry)
- IT Support (as entry)
- Identity Analyst

### Step 8: Keep learning

- Follow IAM communities
- Read IAM blogs
- Attend webinars
- Network

---

## 10. Common Challenges

| Challenge | Reality |
|-----------|---------|
| Legacy systems | Old apps don't support SSO |
| User resistance | People hate change |
| Complex integrations | Every app is different |
| Access creep | People accumulate access |
| Orphaned accounts | Forgotten accounts |
| Help desk load | Password resets |
| Security vs UX | Balance needed |
| Compliance pressure | Audits are stressful |

### How to survive

- Automate everything
- Document clearly
- Train users well
- Build relationships
- Focus on UX
- Stay organized
- Take breaks

---

## Practice Tasks

- [ ] Install Windows Server
- [ ] Set up Active Directory
- [ ] Create users and groups
- [ ] Configure Group Policy
- [ ] Learn SAML basics
- [ ] Learn OAuth basics
- [ ] Set up Okta developer account
- [ ] Set up Azure AD free tier
- [ ] Configure SSO for an app
- [ ] Set up MFA on your accounts
- [ ] Build a PAM lab
- [ ] Document an IAM process

---

## Free Practice

- Okta Developer (free)
- Azure AD Free Tier
- AWS IAM (free)
- Keycloak (open source)
- TryHackMe AD rooms
- Microsoft Learn (free)
- Okta Learning (free)

---

## Key Terms

| Term | Meaning |
|------|---------|
| IAM | Identity and Access Management |
| AD | Active Directory |
| SSO | Single Sign-On |
| MFA | Multi-Factor Authentication |
| SAML | SSO protocol |
| OAuth | Authorization protocol |
| OIDC | Authentication on OAuth |
| PAM | Privileged Access Management |
| RBAC | Role-Based Access Control |
| Least Privilege | Minimum access |
| Joiner/Mover/Leaver | Employee lifecycle |
| Zero Trust | Never trust, always verify |

---

## What now?

Next path: `ai-security.md`

> **Ethical Use Only**
> Only hack systems you own or have written permission to test.
> Never use these skills to break the law.
