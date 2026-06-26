# Ethical Hacking Task 02 – Nmap Network Scanning

**Student Name:** Reethu

**Course:** BCA Cybersecurity

**Date:** 26 June 2026

---

# Part A – Introduction

## Objective

The objective of this task is to understand the fundamentals of network scanning using Nmap. The task focuses on identifying open ports, detecting running services and their versions, performing operating system detection, and understanding common network ports. The scan was performed only on the local machine to ensure ethical and authorized testing.

---

# Part B – Local Machine Scan

### Command Used

```bash
nmap localhost
```

### Scan Results

| Port | Service               |
| ---- | --------------------- |
| 135  | Microsoft Windows RPC |
| 445  | Microsoft-DS          |
| 1521 | Oracle TNS Listener   |
| 3306 | MySQL                 |
| 5500 | tcpwrapped            |
| 8090 | tcpwrapped            |

### Observation

The scan identified six open TCP ports on the local machine. These ports indicate that Windows services, database services, and application services are running.

**Screenshot:** Localhost_Scan.png

---

# Part C – Service Version Detection

### Command Used

```bash
nmap -sV localhost
```

| Port | Service               | Version                        |
| ---- | --------------------- | ------------------------------ |
| 135  | Microsoft Windows RPC | Microsoft Windows RPC          |
| 445  | Microsoft-DS          | Version not identified         |
| 1521 | Oracle TNS Listener   | Oracle TNS Listener 21.0.0.0.0 |
| 3306 | MySQL                 | MySQL 8.0.45                   |
| 5500 | tcpwrapped            | Protected Service              |
| 8090 | tcpwrapped            | Protected Service              |

### Observation

The service version scan successfully identified software versions for Oracle TNS Listener and MySQL while confirming the presence of Microsoft Windows RPC.

**Screenshot:** Service_Version.png

---

# Part D – Operating System Detection

### Command Used

```bash
nmap -O localhost
```

### Result

Operating System Detected:

**Microsoft Windows 11 (23H2)**

### Why OS Detection is Useful

Operating system detection helps security professionals understand the target platform, identify operating system–specific vulnerabilities, and perform accurate security assessments.

**Screenshot:** OS_Detection.png

---

# Part E – Common Port Research

| Port  | Protocol | Purpose             | Security Risk             |
| ----- | -------- | ------------------- | ------------------------- |
| 20/21 | FTP      | File Transfer       | Weak authentication       |
| 22    | SSH      | Secure Remote Login | Brute-force attacks       |
| 23    | Telnet   | Remote Login        | Unencrypted communication |
| 25    | SMTP     | Email Transfer      | Spam relay                |
| 53    | DNS      | Domain Resolution   | DNS poisoning             |
| 80    | HTTP     | Web Traffic         | Unencrypted traffic       |
| 110   | POP3     | Receive Email       | Credential theft          |
| 143   | IMAP     | Email Access        | Unauthorized access       |
| 443   | HTTPS    | Secure Web Traffic  | TLS misconfiguration      |
| 445   | SMB      | File Sharing        | Ransomware attacks        |
| 3389  | RDP      | Remote Desktop      | Brute-force attacks       |

---

# Part F – Scan Analysis

### Running Services

* Microsoft Windows RPC
* Microsoft-DS
* Oracle TNS Listener
* MySQL
* tcpwrapped

### Are all ports necessary?

Not necessarily. Some ports are required by Windows and installed applications, while unused services should be disabled to reduce security risks.

### Potential Security Risks

Database services such as MySQL and Oracle TNS Listener should be properly secured because weak passwords or outdated versions can expose the system to attacks.

### Port to Disable

If MySQL is not being used, port 3306 should be disabled to reduce the attack surface.

---

# Part G – Scan Summary

## Commands Used

* nmap --version
* nmap localhost
* nmap -sV localhost
* nmap -O localhost

## Open Ports

135, 445, 1521, 3306, 5500, 8090

## Operating System

Microsoft Windows 11 (23H2)

## Recommendations

* Close unused ports.
* Keep software updated.
* Use strong passwords.
* Disable unnecessary services.
* Perform regular security scans.

---

# Conclusion

This task provided practical experience in network scanning using Nmap. By scanning the local machine, I identified open ports, running services, service versions, and the operating system. The activity demonstrated the importance of network reconnaissance during security assessments and showed how unauthorized exposure of services may increase security risks. The task also improved my understanding of ethical hacking practices by emphasizing authorized scanning and responsible security testing.
