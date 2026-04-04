# Cybersecurity Basics

##  CIA Triad

The CIA Triad is the foundation of cybersecurity and ensures the protection of data and systems.

### 1. Confidentiality

* Ensures that sensitive information is accessed only by authorized users.
* Prevents unauthorized access to data.

**Examples:**

* Password protection
* Data encryption

---

### 2. Integrity

* Ensures that data is accurate and not modified by unauthorized users.
* Protects data from tampering.

**Examples:**

* Hashing (MD5, SHA256)
* Digital signatures

---

### 3. Availability

* Ensures that systems and data are accessible when needed.
* Prevents downtime and service disruption.

**Examples:**

* Backup systems
* Load balancing

---

##  Types of Cyber Attacks

Cyber attacks are malicious attempts to damage, disrupt, or gain unauthorized access to systems.

---

###  1. Phishing

**How it works:**

* Attacker sends fake emails or messages pretending to be a trusted source.
* User clicks a malicious link and enters sensitive data.
* Attacker collects login credentials.

**Real-world Example:**

* Fake bank email asking to “verify your account.”

**Prevention:**

* Avoid clicking unknown links
* Check email authenticity
* Use two-factor authentication (2FA)

---

###  2. Malware

**How it works:**

* Malicious software is installed on a system through downloads or attachments.
* It can steal data, monitor activity, or damage the system.

**Types:**

* Virus
* Trojan
* Spyware
* Worm

**Real-world Example:**

* Downloading cracked software infected with a virus.

**Prevention:**

* Install trusted software only
* Use antivirus tools
* Keep system updated

---

###  3. DDoS (Distributed Denial of Service)

**How it works:**

* Attacker uses multiple systems (botnet) to flood a server with traffic.
* Server becomes overloaded and unavailable.

**Real-world Example:**

* Websites going down due to heavy traffic attacks.

**Prevention:**

* Use firewalls
* Rate limiting
* Cloud-based protection

---

###  4. SQL Injection

**How it works:**

* Attacker injects malicious SQL queries into input fields.
* Database executes the query and exposes data.

**Example Input:**
' OR '1'='1

**Impact:**

* Bypass login
* Access sensitive data

**Prevention:**

* Use prepared statements
* Validate user input

---

###  5. Brute Force Attack

**How it works:**

* Attacker tries multiple passwords using automated tools.
* Eventually finds the correct password.

**Real-world Example:**

* Attempting thousands of password combinations on login pages.

**Prevention:**

* Strong passwords
* Account lockout policies
* CAPTCHA

---

###  6. Ransomware

**How it works:**

* Malware encrypts files on a system.
* Attacker demands payment to restore access.

**Real-world Example:**

* Hospitals and companies losing access to critical data.

**Prevention:**

* Regular backups
* Avoid suspicious downloads
* Update software

---

##  Attack Vectors

Attack vectors are the paths or methods attackers use to gain access to a system.

---

###  1. Social Engineering

**Description:**

* Manipulating people to reveal confidential information.

**Examples:**

* Phishing emails
* Fake support calls

---

###  2. Insider Threat

**Description:**

* Threats from employees or internal users.

**Examples:**

* Data theft by employees
* Misuse of access privileges

---

###  3. Wireless Attacks

**Description:**

* Attacks targeting Wi-Fi networks.

**Examples:**

* Unauthorized access to Wi-Fi
* Man-in-the-middle attacks

---

## Conclusion

Cybersecurity focuses on protecting systems, networks, and data from cyber threats. Understanding the CIA Triad, types of attacks, and attack vectors is essential for identifying and preventing security risks.

---

##  Learning Outcome

* Learned the importance of CIA Triad
* Understood different types of cyber attacks
* Identified common attack vectors and prevention techniques
