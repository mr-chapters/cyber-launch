# 03 - Networking (Detailed)

Attacks travel through networks. If you do not understand networking, you cannot defend or attack anything. This file goes deep.

---

## What you will learn
1. What is a network?
2. IP addresses and subnetting (detailed)
3. DNS (detailed)
4. DHCP (detailed)
5. TCP/IP and ports (detailed)
6. OSI model (detailed)
7. HTTP vs HTTPS (detailed)
8. Routers, switches, firewalls (detailed)
9. Basic networking tools (detailed)

---

## 1. What is a Network?

A network is two or more devices connected so they can share data.

**Types of networks:**
| Type | Full Name | Range | Example |
|------|-----------|-------|---------|
| PAN | Personal Area Network | ~10 meters | Bluetooth, phone to earbuds |
| LAN | Local Area Network | Building | Home Wi-Fi, school lab |
| MAN | Metropolitan Area Network | City | City-wide ISP network |
| WAN | Wide Area Network | Country/Global | The internet |

**Network topologies:**
| Topology | Shape | Pros | Cons |
|----------|-------|------|------|
| Star | All connect to center | Easy to manage | Center fails = all fail |
| Bus | One main cable | Cheap | One break = all fail |
| Ring | Loop | Predictable | One break = all fail |
| Mesh | All connect to all | Very reliable | Expensive, complex |

**Why this matters:** Every attack moves across a network. Knowing the type and shape tells you where to look and where to defend.

---

## 2. IP Addresses and Subnetting (Detailed)

An IP address is a unique number for every device on a network.

### IPv4
- 32-bit address
- Written as 4 numbers (octets) separated by dots
- Example: `192.168.1.1`
- Range: `0.0.0.0` to `255.255.255.255`
- Total: ~4.3 billion addresses (running out)

### IPv6
- 128-bit address
- Written in hex, separated by colons
- Example: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`
- Total: 340 undecillion (basically unlimited)

### Private vs Public IPs
| Type | Range | Use |
|------|-------|-----|
| Private | 10.0.0.0 – 10.255.255.255 | Home/office |
| Private | 172.16.0.0 – 172.31.255.255 | Home/office |
| Private | 192.168.0.0 – 192.168.255.255 | Home/office |
| Public | Everything else | Internet |

Private IPs cannot be reached from the internet directly. A router uses **NAT** (Network Address Translation) to translate them.

### Subnet Mask
Tells which part of the IP is network and which is host.

| CIDR | Subnet Mask | Hosts |
|------|-------------|-------|
| /24 | 255.255.255.0 | 254 |
| /25 | 255.255.255.128 | 126 |
| /26 | 255.255.255.192 | 62 |
| /27 | 255.255.255.224 | 30 |
| /28 | 255.255.255.240 | 14 |
| /29 | 255.255.255.248 | 6 |
| /30 | 255.255.255.252 | 2 |

### Example: 192.168.1.0/24
- Network: `192.168.1.0`
- First host: `192.168.1.1`
- Last host: `192.168.1.254`
- Broadcast: `192.168.1.255`
- Total hosts: 254

**Why this matters:** You must know which devices are on which network before you can scan or attack them. Subnetting is asked in every security interview.

---

## 3. DNS (Detailed)

DNS turns names into IP addresses. It is the phonebook of the internet.

### How DNS works (step by step)
1. You type `google.com` in your browser
2. Your computer checks its local cache
3. If not found, it asks your **DNS resolver** (usually your ISP)
4. Resolver asks the **root server** (`.`)
5. Root says "ask the `.com` server"
6. `.com` server says "ask Google's nameserver"
7. Google's nameserver returns the IP
8. Your browser connects to that IP

### Common DNS records
| Record | Meaning | Example |
|--------|---------|---------|
| A | Name to IPv4 | google.com → 142.250.190.46 |
| AAAA | Name to IPv6 | google.com → 2607:f8b0::... |
| MX | Mail server | mail.google.com |
| CNAME | Alias | www → google.com |
| TXT | Text info | SPF, verification |
| NS | Nameserver | ns1.google.com |
| PTR | Reverse lookup | IP → name |

### DNS attacks
| Attack | What it does |
|--------|--------------|
| DNS Spoofing | Fake DNS response |
| DNS Poisoning | Corrupt DNS cache |
| DNS Tunneling | Hide data in DNS queries |
| DDoS on DNS | Take down DNS server |

**Why this matters:** DNS is a huge target. If you control DNS, you control where users go.

---

## 4. DHCP (Detailed)

DHCP gives devices IP addresses automatically.

### How DHCP works (DORA)
1. **Discover** - Device broadcasts "I need an IP"
2. **Offer** - DHCP server offers an IP
3. **Request** - Device requests that IP
4. **Acknowledge** - Server confirms

### What DHCP gives
- IP address
- Subnet mask
- Default gateway
- DNS servers
- Lease time

### DHCP attacks
| Attack | What it does |
|--------|--------------|
| Rogue DHCP | Fake server gives wrong IPs |
| DHCP Starvation | Exhaust all IPs |
| DHCP Spoofing | Redirect traffic |

**Why this matters:** A rogue DHCP server can redirect all traffic through an attacker.

---

## 5. TCP/IP and Ports (Detailed)

### TCP vs UDP
| Feature | TCP | UDP |
|---------|-----|-----|
| Connection | Yes (3-way handshake) | No |
| Reliable | Yes | No |
| Order | Guaranteed | Not guaranteed |
| Speed | Slower | Faster |
| Use | Web, email, file transfer | Streaming, games, DNS |

### TCP 3-Way Handshake
1. **SYN** - Client says "hello"
2. **SYN-ACK** - Server says "hi, ready"
3. **ACK** - Client says "connected"

### Common ports
| Port | Service | Protocol |
|------|---------|----------|
| 20/21 | FTP | TCP |
| 22 | SSH | TCP |
| 23 | Telnet | TCP |
| 25 | SMTP | TCP |
| 53 | DNS | TCP/UDP |
| 67/68 | DHCP | UDP |
| 80 | HTTP | TCP |
| 110 | POP3 | TCP |
| 143 | IMAP | TCP |
| 443 | HTTPS | TCP |
| 445 | SMB | TCP |
| 3306 | MySQL | TCP |
| 3389 | RDP | TCP |
| 8080 | HTTP alt | TCP |

### Port states
| State | Meaning |
|-------|---------|
| Open | Service is running |
| Closed | No service |
| Filtered | Firewall blocks it |

**Why this matters:** Open ports are doors. Attackers scan for them. You must know what each port means.

---

## 6. OSI Model (Detailed)

| Layer | Name | What it does | Examples | Attacks |
|-------|------|--------------|----------|---------|
| 7 | Application | User services | HTTP, DNS, FTP | Phishing, SQL injection |
| 6 | Presentation | Encryption, format | SSL/TLS, JPEG | SSL stripping |
| 5 | Session | Manage connections | NetBIOS, RPC | Session hijacking |
| 4 | Transport | TCP/UDP, ports | TCP, UDP | SYN flood, port scan |
| 3 | Network | IP, routing | IP, ICMP | IP spoofing, DDoS |
| 2 | Data Link | MAC, switches | Ethernet, ARP | ARP spoofing, MAC flood |
| 1 | Physical | Cables, signals | Cables, Wi-Fi | Cable cut, jamming |

**Memory trick:** Please Do Not Throw Sausage Pizza Away
(Physical, Data Link, Network, Transport, Session, Presentation, Application)

**Why this matters:** Every attack happens at a layer. Knowing the layers helps you diagnose and defend.

---

## 7. HTTP vs HTTPS (Detailed)

### HTTP
- Unencrypted
- Anyone on the network can read it
- Port 80

### HTTPS
- Encrypted with TLS
- Safe from eavesdropping
- Port 443

### HTTP methods
| Method | Meaning | Safe? |
|--------|---------|-------|
| GET | Request data | Yes |
| POST | Send data | No |
| PUT | Update data | No |
| DELETE | Remove data | No |
| PATCH | Partial update | No |
| HEAD | Get headers only | Yes |
| OPTIONS | Get allowed methods | Yes |

### Status codes
| Code | Meaning |
|------|---------|
| 200 | OK |
| 201 | Created |
| 301 | Moved permanently |
| 302 | Found (redirect) |
| 400 | Bad request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Server error |
| 503 | Service unavailable |

### HTTP headers (important for security)
| Header | Meaning |
|--------|---------|
| Host | Target domain |
| User-Agent | Browser info |
| Cookie | Session data |
| Authorization | Credentials |
| Content-Type | Data type |
| Referer | Where you came from |

**Why this matters:** Most web attacks target HTTP. You must understand it deeply. Burp Suite intercepts and modifies HTTP requests.

---

## 8. Routers, Switches, Firewalls (Detailed)

| Device | Layer | What it does |
|--------|-------|--------------|
| Hub | 1 | Broadcasts to all (obsolete) |
| Switch | 2 | Sends to correct device (MAC) |
| Router | 3 | Connects networks (IP) |
| Firewall | 3-7 | Filters traffic by rules |
| Load Balancer | 4-7 | Distributes traffic |
| Proxy | 7 | Middleman for requests |
| IDS | 2-7 | Detects intrusions |
| IPS | 2-7 | Detects and blocks |

### Firewall types
| Type | What it does |
|------|--------------|
| Packet filter | Checks headers |
| Stateful | Tracks connections |
| Application | Inspects content |
| Next-gen (NGFW) | All of the above + more |

**Why this matters:** These are the walls and doors of a network. You attack or defend them.

---

## 9. Basic Networking Tools (Detailed)

| Command | What it does | Example |
|---------|--------------|---------|
| `ping host` | Check reachability | `ping google.com` |
| `traceroute host` | Show path | `traceroute google.com` |
| `nslookup domain` | DNS lookup | `nslookup google.com` |
| `dig domain` | Detailed DNS | `dig google.com` |
| `netstat -tuln` | Open ports | `netstat -tuln` |
| `ss -tuln` | Modern netstat | `ss -tuln` |
| `ifconfig` | Network info | `ifconfig` |
| `ip a` | Modern ifconfig | `ip a` |
| `curl url` | Fetch URL | `curl google.com` |
| `wget url` | Download file | `wget file.zip` |
| `nmap host` | Scan ports | `nmap 192.168.1.1` |
| `arp -a` | Show ARP table | `arp -a` |
| `route -n` | Show routes | `route -n` |

### Nmap basics
| Command | What it does |
|---------|--------------|
| `nmap host` | Basic scan |
| `nmap -sV host` | Version detection |
| `nmap -O host` | OS detection |
| `nmap -p 1-1000 host` | Scan port range |
| `nmap -A host` | Aggressive scan |

**Why this matters:** These are your daily tools. Learn them well. Nmap is the #1 tool for scanning.

---

## Practice Tasks
- [ ] Find your own IP address
- [ ] Ping google.com
- [ ] Run traceroute to a website
- [ ] Look up DNS for a domain
- [ ] List open ports on your machine
- [ ] Install and run Nmap on your VM
- [ ] Open a website and view it in Wireshark
- [ ] Capture a TCP handshake in Wireshark
- [ ] Identify 5 open ports on your home network
- [ ] Look up the OSI layer for 5 common attacks

---

## Free Practice
- Cisco Networking Basics (free)
- Professor Messer Network+ videos
- Wireshark official tutorials
- OverTheWire Bandit

---

## Key Terms
| Term | Meaning |
|------|---------|
| IP | Internet Protocol address |
| DNS | Domain Name System |
| DHCP | Gives out IPs |
| TCP | Reliable protocol |
| UDP | Fast protocol |
| Port | Door for services |
| OSI | 7-layer model |
| Firewall | Traffic filter |
| NAT | Network Address Translation |
| Subnet | Smaller network |
| CIDR | Subnet notation |
| ARP | IP to MAC mapping |

---

## What now?
Next file: **04-windows-basics.md**

> ⚠️ Ethical Use Only
> Only hack systems you own or have written permission to test.
> Never use these skills to break the law.
