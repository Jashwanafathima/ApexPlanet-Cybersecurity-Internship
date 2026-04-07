# 📌 Day 1 – Passive Reconnaissance

## 🔍 Introduction
Passive Reconnaissance is the process of collecting information about a target **without directly interacting with it**. It is the first phase of ethical hacking and penetration testing.

---

## 🎯 Objectives
- Gather domain information
- Identify DNS records
- Discover publicly available data
- Find potential attack surfaces

---

# 🧩 1. WHOIS

## 🔹 What is WHOIS?
WHOIS is a protocol used to retrieve domain registration details such as owner, registrar, and expiry date.

## 🔹 How it Works
- A query is sent to a WHOIS server
- The server responds with domain details

## 🔹 Usage
- Passive reconnaissance
- Domain ownership verification
- Cybersecurity investigations

## 🔹 Attacker Perspective
- Collect email IDs for phishing
- Identify domain expiry for takeover
- Map organization infrastructure

## 🔹 Prevention
- Enable WHOIS privacy protection
- Avoid exposing sensitive data
- Use domain locking

## 🔹 Commands
```bash
whois example.com
whois vulnweb.com
