### Nmap Notes

**What is Nmap?**
Nmap (Network Mapper) is a tool used for network discovery and security auditing. It helps identify open ports and services running on a target system.

**Commands Used:**

```bash
nmap 192.168.56.101
nmap -sS 192.168.56.101
nmap -sV 192.168.56.101
```

**Explanation:**

* `nmap` → Basic scan
* `-sS` → Stealth TCP scan
* `-sV` → Detect service versions

**Observations:**

* Open ports like 21 (FTP), 22 (SSH), and 80 (HTTP) were identified.
* Services running on the target system were detected.

**Conclusion:**
Nmap is useful for identifying vulnerabilities by scanning open ports and services in a system.
