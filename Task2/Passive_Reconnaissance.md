

# ============================================
# PASSIVE RECONNAISSANCE 
# ============================================

# --------------------------------------------
# 🧩 1. WHOIS
# --------------------------------------------

# WHAT IS WHOIS?
 WHOIS is used to get domain registration details
# مثل: owner, registrar, expiry date

# HOW IT WORKS?
 Query → WHOIS Server → Returns domain info

# USAGE:
- Passive recon
- Domain investigation

# ATTACKER USE:
 - Collect emails → phishing
 - Find expiry → domain takeover

# PREVENTION:
 - Enable WHOIS privacy
 - Hide sensitive info

# COMMANDS:

whois example.com
whois vulnweb.com

# Extract specific info
whois example.com | grep "Registrar"
whois example.com | grep "Expiry"


# --------------------------------------------
# 🧩 2. NSLOOKUP
# --------------------------------------------

# WHAT IS NSLOOKUP?
 Used to query DNS and get IP + DNS records

# HOW IT WORKS?
 Query → DNS Resolver → DNS Server → Response

# USAGE:
 - Find IP address
 - Find mail servers
 - DNS troubleshooting

# ATTACKER USE:
 - Identify target IP
 - Find mail servers for phishing
 - Map DNS infra

# PREVENTION:
 - Use DNSSEC
 - Restrict DNS info

# COMMANDS:

# Basic lookup (Domain → IP)
nslookup example.com
nslookup testphp.vulnweb.com

# MX Records (Mail Servers)
nslookup -type=mx example.com

# Name Servers
nslookup -type=ns example.com

# Reverse Lookup (IP → Domain)
nslookup 8.8.8.8

# Use specific DNS server
nslookup google.com 8.8.8.8


# --------------------------------------------
# 3. GOOGLE DORKING
# --------------------------------------------

# NOTE:
# These are NOT bash commands
# Run them in Google search

# SEARCH WITHIN SITE
 site:example.com

# FIND LOGIN PAGES
 site:example.com inurl:login

# FIND ADMIN PANELS
 site:example.com inurl:admin

# FIND FILES
 site:example.com filetype:pdf

# FIND PARAMETERS (IMPORTANT)
 site:example.com inurl:php?id=


# --------------------------------------------
#  COMBINED WORKFLOW
# --------------------------------------------

# STEP 1: WHOIS
whois example.com

# STEP 2: NSLOOKUP
nslookup example.com
nslookup -type=mx example.com
nslookup -type=ns example.com

# STEP 3: GOOGLE DORKING (run in browser)
 site:example.com
 site:example.com inurl:login
 site:example.com filetype:pdf


# --------------------------------------------
#  KEY LEARNINGS
# --------------------------------------------

# - Passive recon = no direct interaction
# - WHOIS → domain info
# - NSLOOKUP → DNS + IP
# - Google Dorks → public sensitive data


# --------------------------------------------
#  SECURITY INSIGHTS
# --------------------------------------------

# - Public info can be exploited
# - Misconfigured DNS = risk
# - Exposure increases attack surface
