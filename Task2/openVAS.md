#  Vulnerability Scanning Notes (OpenVAS)

##  Introduction

Vulnerability Scanning is the process of identifying security weaknesses in a system using automated tools. It helps in detecting outdated software, misconfigurations, and known vulnerabilities (CVEs).

This task is part of **Network Security & Scanning** and focuses on scanning a vulnerable machine in a controlled lab environment.

---

##  Objective

* Learn how vulnerability scanners work
* Perform scanning on a target machine
* Analyze vulnerabilities based on severity
* Understand real-world security risks

---

##  Tools Used

* Kali Linux
* OpenVAS (Greenbone Vulnerability Manager)
* Metasploitable2

---

##  Key Concepts

###  What is a Vulnerability?

A vulnerability is a weakness in a system that can be exploited by an attacker.

###  What is CVE?

CVE (Common Vulnerabilities and Exposures) is a public database of known vulnerabilities.

###  Severity Levels

| Level       | Description                     |
| ----------- | ------------------------------- |
|  Critical | Full system compromise possible |
|  High     | Serious vulnerability           |
|  Medium   | Moderate risk                   |
|  Low      | Minor issue                     |

---

##  Installation & Setup

### Install OpenVAS

```bash
sudo apt update
sudo apt install openvas -y
```

### Setup OpenVAS

```bash
sudo gvm-setup
```

### Start OpenVAS

```bash
sudo gvm-start
```

### Access Web Interface

```
https://127.0.0.1:9392
```

---

##  Lab Setup

* Attacker Machine: Kali Linux
* Target Machine: Metasploitable2
* Network: Host-Only / NAT

---

##  Scanning Workflow

### Step 1: Add Target

* Go to Configuration → Targets
* Add target IP

---

### Step 2: Create Scan Task

* Go to Scans → Tasks
* Select "Full and Fast" scan

---

### Step 3: Start Scan

* Click Start button
* Wait for scan completion

---

### Step 4: Analyze Results

* View vulnerabilities
* Check severity levels
* Identify affected services

---

##  Example Vulnerabilities

###  Critical: VSFTPD Backdoor

* Port: 21 (FTP)
* Issue: Backdoor vulnerability
* Impact: Remote command execution

---

###  High: Samba Vulnerability

* Port: 445 (SMB)
* Issue: Outdated service
* Impact: Remote exploitation

---

###  Medium: Weak SSH Config

* Port: 22
* Issue: Weak encryption
* Impact: Brute-force attacks

---

###  Low: Banner Disclosure

* Issue: Service version visible
* Impact: Information leakage

---

##  Scan Output Analysis

* Total vulnerabilities identified
* Classification based on severity
* Understanding attack surface

---

##  Key Learnings

* Learned how automated scanners detect vulnerabilities
* Understood severity classification
* Gained hands-on experience with real tools
* Improved analysis and reporting skills

---

##  Limitations

* May produce false positives
* Cannot replace manual testing
* Needs expert analysis

---

##  Conclusion

Vulnerability scanning is a critical step in cybersecurity for identifying weaknesses before attackers exploit them. Tools like OpenVAS help automate this process and provide valuable insights into system security.

---

##  Disclaimer

This project was performed in a controlled lab environment for educational purposes only.

---
