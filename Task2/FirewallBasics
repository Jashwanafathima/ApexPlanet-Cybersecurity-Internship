🔥 Firewall Basics using iptables
📌 Objective
Create simple firewall rules using iptables
Allow/Deny specific ports
Demonstrate blocking a port scan attempt
⚙️ What is iptables?

iptables is a Linux firewall utility used to control incoming and outgoing network traffic based on rules.

🧱 Basic Concepts
INPUT → Incoming traffic
OUTPUT → Outgoing traffic
FORWARD → Routed traffic
ACCEPT → Allow traffic
DROP → Block silently
REJECT → Block with response

🚀 Step 1: View Existing Rules
sudo iptables -L

🚀 Step 2: Allow Specific Ports
✅ Allow SSH (Port 22)
sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT
✅ Allow HTTP (Port 80)
sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT
✅ Allow HTTPS (Port 443)
sudo iptables -A INPUT -p tcp --dport 443 -j ACCEPT

🚫 Step 3: Deny Specific Ports
❌ Block Telnet (Port 23)
sudo iptables -A INPUT -p tcp --dport 23 -j DROP
❌ Block FTP (Port 21)
sudo iptables -A INPUT -p tcp --dport 21 -j DROP

🔐 Step 4: Set Default Policy (Strict Firewall)
sudo iptables -P INPUT DROP
sudo iptables -P FORWARD DROP
sudo iptables -P OUTPUT ACCEPT
⚠️ This blocks all incoming traffic except allowed rules.

🔄 Step 5: Allow Established Connections
sudo iptables -A INPUT -m conntrack --ctstate ESTABLISHED,RELATED -j ACCEPT

🧪 Step 6: Demonstrate Blocking a Port Scan
🔍 Run Scan from Attacker Machine (Kali)
nmap -sS <target-ip>
🔴 Before Firewall
Ports appear OPEN
🛡️ After Applying Firewall Rules
Ports appear:
Filtered (if DROP used)
Closed (if REJECT used)
🚫 Block Port Scan (Basic Protection)
Drop suspicious scan traffic (SYN flood / scans)
sudo iptables -A INPUT -p tcp --syn -m limit --limit 1/s -j ACCEPT
sudo iptables -A INPUT -p tcp --syn -j DROP

🔍 Verify Rules
sudo iptables -L -v

💾 Save Rules
sudo iptables-save > rules.v4
🧹 Flush Rules (Reset)
sudo iptables -F

📊 Expected Output in Demo
Scenario	Result
Before firewall	Ports OPEN
After firewall	Ports FILTERED
Scan attempt	Blocked / Limited

🧠 Key Learning
Firewall controls network access
iptables works on rule-based filtering
Helps prevent scanning & unauthorized access
Basic defense against reconnaissance attacks
