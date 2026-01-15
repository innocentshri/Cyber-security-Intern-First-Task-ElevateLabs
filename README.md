# Cyber-security-Intern-First-Task-ElevateLabs
Cybersecurity Internship Task 1: Understanding CIA Triad, Attack Surfaces, OWASP Top 10, and Common Attack Vectors. Foundational learning covering confidentiality, integrity, availability, threat actors, and web application vulnerabilities.


# Task Overview
So basically I had to cover:
- The CIA Triad thing (not the spy agency) with examples I could relate to
- Where attackers usually target systems
- Different types of hackers and why they do what they do
- OWASP Top 10 vulnarabilities (this was interesting)
- looking at how data moves and where it can get attacked

# What I actutally learned 
### The CIA Triad
- **Confidentiality**: Basically keeping your stuff private from people who shouldn't see it
- **Intergrity**: Making sure nobody messes with your data
- **Availability**: Keeping everthing up and running when you need it

### How I mapped Attack Surfaces
Phone/Laptop --> Website --> API --> Server --> Database

(Phishing emails)  (XSS)   (Broken APIs)  (Remote Code)  (SQL Injection)

## What I used 
- Browser for looking stuff up
- OWASP website
- Dra.io for diagram

## 1 CIA TRIAD - Cybresecurity Foundation 

### Confindentiality
**Definition**: Only authorized users access sensitive data
**Example**: PhonePe shows UPI transactin only to sender/receiver
**Breach**: Hacker intercepts OTP via SS7 attack --> Sees Rs.5000 Transfer
**Attack**: Phishing, network sninffing, keyloggers

### Integrity 
**Definition**: Data cannot bee modifies unauthorized 
**Example**: Gpay transfer "Rs.1000" cannot be changed to "Rs.10,000"
**Breach**: Man-in-middle modifies transaction amount
**Attack**: MITM, code injection

### Availability
**Definition**: Systems accessible when needed
**Example**: IRCTC available during Tatkal booking 
**Breach**: DDoS crashes site --> No ticket booking
**Attack**: DDoS, ransomare

**Daily Apps CIA Mapping:**
| App | Confidentiality | Integrity | Availability |
|-----|----------------|-----------|--------------|
| Gmail | Email encryption | Email tampering | Server down |
| WhatsApp | E2E encryption | Message editing | App crash |
| SBI YONO | PIN/biometrics | Transaction change | ATM down |

## 2 ATTACK SURFACES
**Definition**: All potential entry points for attackers

### Common Attack Surfaces:
1. **Web Apps**: Login forms, search bars, filee uploads
2. **Mobile Apps**: Local storage, netork calls
3. **APIs**: Unauthenticated endpoints
4. **Networks**: Open WiFi, HTTP protocols
5. **Cloud**: Misconfigured S3 buckets

**Daily Apps Attack Mapping:**
| App | Attack Surface | Example Attack |
|-----|----------------|---------------|
| Gmail | Login form | Phishing page |
| WhatsApp | QR scanning | Account takeover |
| PhonePe | UPI PIN | Keylogger |

---

## 3 TYPES OF ATTACKERS

| Attacker | Skill Level | Motivation | Example Target |
|----------|-------------|------------|---------------|
| **Script Kiddie** | Low | Fame/curiosity | School websites |
| **Insider** | Medium | Revenge/money | Bank employee steals data |
| **Hacktivist** | High | Politics | Government sites |
| **Nation-State** | Expert | Espionage | Power grids, elections [file:1]

---

## 4 OWASP TOP 10 (Most Critical)

| # | Vulnerability | Impact | Prevention |
|---|---------------|--------|------------|
| **A01** | **Injection** | Database dump | Prepared statements |
| **A02** | **Broken Auth** | Account takeover | MFA, strong passwords |
| **A03** | **Data Exposure** | Identity theft | TLS 1.3 encryption |
| **A07** | **XSS** | Session theft | Output encoding |

**SQL Injection Example**
-- Vulnerable Code:
SELECT * FROM users WHERE username='$username';

-- Attack Input:
username = admin' --

-- Executed Query:
SELECT * FROM users WHERE username='admin' --';

-- Impact: 
The '--' comments out the password validation, 
allowing authentication bypass and unauthorized admin access.

## 5 Dataflow and Attack Points
![WhatsApp Image 2026-01-15 at 3 46 54 PM](https://github.com/user-attachments/assets/2e2ccd03-02d6-4460-b8ce-28f52594d9e7)

