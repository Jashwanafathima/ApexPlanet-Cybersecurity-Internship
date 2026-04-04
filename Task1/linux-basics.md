# 🐧 Linux Basics

Linux is an open-source operating system widely used in cybersecurity for its flexibility, security, and powerful command-line tools.

---

## 📁 File System Navigation

* `pwd` → Displays current directory
* `ls` → Lists files and directories
* `cd <directory>` → Changes directory
* `cd ..` → Moves to parent directory

---

## 📂 File & Directory Operations

* `touch file.txt` → Create a new file
* `mkdir folder` → Create a new directory
* `cp file.txt folder/` → Copy file
* `mv file.txt new.txt` → Rename or move file
* `rm file.txt` → Delete file
* `rm -r folder` → Delete directory

---

## 🔐 File Permissions

Linux uses permissions to control access to files.

Command:

```bash id="l1"
chmod 777 file.txt
chmod 644 file.txt
ls -l
```

### Permission Meaning:

* `r` → Read
* `w` → Write
* `x` → Execute

### Numeric Values:

* 7 → Read + Write + Execute
* 6 → Read + Write
* 4 → Read

---

## 👤 Ownership

* `chown user file.txt` → Change file owner
* `chgrp group file.txt` → Change group

---

## 📦 Package Management

Used to install and manage software.

```bash id="l2"
sudo apt update
sudo apt upgrade
sudo apt install <package>
```

Example:

```bash id="l3"
sudo apt install nmap
```

---

## 🌐 Networking Commands

* `ifconfig` → Display IP address
* `ping <IP>` → Test connectivity
* `netstat -tuln` → Show open ports
* `traceroute <IP>` → Show route of packets

---

## 🎯 Importance in Cybersecurity

* Used for penetration testing
* Helps manage systems and tools
* Essential for running security tools like Nmap, Wireshark, etc.

---

## 📌 Learning Outcome

* Learned basic Linux commands
* Understood file permissions and ownership
* Practiced networking commands in Linux
