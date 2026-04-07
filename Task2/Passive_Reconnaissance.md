📌 Day 1 – Passive Reconnaissance
🔍 Introduction

Passive Reconnaissance is the process of collecting information about a target without directly interacting with it.
It is the first phase of ethical hacking / penetration testing.

🎯 Objectives
Gather domain information
Identify DNS records
Discover publicly available data
Find potential attack surfaces
🧩 1. WHOIS
🔹 What is WHOIS?

WHOIS is a protocol used to retrieve domain registration details such as owner, registrar, and expiry date.

🔹 How it Works
User sends a query to a WHOIS server
Server responds with domain details
🔹 Usage
Passive reconnaissance
Domain ownership verification
Cybersecurity investigations
🔹 Attacker Perspective
Collect email IDs → phishing
Identify domain expiry → takeover
Map organization infrastructure
🔹 Prevention
Enable WHOIS privacy protection
Avoid exposing sensitive data
Use domain locking
🔹 Commands
whois example.com
whois vulnweb.com
🔹 Key Information Extracted
Registrar
Creation Date
Expiry Date
Name Servers
Registrant Info
🧩 2. NSLOOKUP
🔹 What is nslookup?

nslookup is a tool used to query DNS and retrieve IP addresses and DNS records.

🔹 How it Works
Sends query to DNS resolver
Resolver fetches data from DNS servers
Returns IP or DNS records
🔹 Usage
DNS troubleshooting
Passive recon
Finding mail servers and subdomains
🔹 Attacker Perspective
Identify target IP for scanning
Discover mail servers for phishing
Map DNS infrastructure
🔹 Prevention
Use DNSSEC
Restrict DNS information exposure
Disable unnecessary records
🔹 Commands
nslookup example.com
nslookup testphp.vulnweb.com

# MX Records
nslookup -type=mx example.com

# Name Servers
nslookup -type=ns example.com

# Reverse Lookup
nslookup 8.8.8.8
🔹 Key Information Extracted
IP Address
Mail Servers (MX)
Name Servers (NS)
🧩 3. Google Dorking
🔹 What is Google Dorking?

Google Dorking is the use of advanced search operators to find sensitive or hidden information indexed by Google.

🔹 How it Works
Uses special operators to filter search results
Helps locate specific data
🔹 Usage
Bug bounty
Information gathering
Finding exposed data
🔹 Attacker Perspective
Find login/admin pages
Discover sensitive files
Identify vulnerable parameters
🔹 Prevention
Use robots.txt
Disable directory listing
Protect sensitive files
Implement authentication
🔹 Common Dorks
# Search within a site
site:example.com

# Find login pages
site:example.com inurl:login

# Find admin panels
site:example.com inurl:admin

# Find files
site:example.com filetype:pdf

# Find parameters
site:example.com inurl:php?id=
🔗 Combined Workflow
🧪 Step 1: WHOIS
whois example.com
🧪 Step 2: NSLOOKUP
nslookup example.com
nslookup -type=mx example.com
nslookup -type=ns example.com
🧪 Step 3: Google Dorking
site:example.com
site:example.com inurl:login
site:example.com filetype:pdf
🧠 Key Learnings
Passive recon does not interact with target systems
WHOIS reveals domain ownership details
nslookup provides DNS and IP information
Google Dorking exposes publicly available sensitive data
⚠️ Security Insights
Public information can be used for attacks
Misconfigured DNS and exposed data increase risk
Proper security measures are required to prevent misuse
🚀 Conclusion

Passive reconnaissance is a critical first step in cybersecurity.
It helps in understanding the target and identifying potential vulnerabilities without alerting the system.
