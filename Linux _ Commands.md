# 🐧 Linux Commands for IT Support (L1)

This document contains essential Linux commands for first-line technical support and system diagnostics. It serves as a quick reference and a demonstration of my foundational Linux knowledge.

---

## 📁 Navigation & File System

| Command | Description | Example |
|---------|-------------|---------|
| `pwd` | Print current working directory | `pwd` → `/home/user` |
| `ls -la` | List all files including hidden, with permissions, owner, size | `ls -la /var/log` |
| `cd` | Change directory | `cd /etc` or `cd ..` |
| `mkdir` | Create a new directory | `mkdir backups` |
| `rm` | Remove files or directories | `rm file.txt` or `rm -r folder/` |
| `cp` | Copy files or directories | `cp source.txt dest.txt` |
| `mv` | Move or rename files | `mv oldname newname` |

---

## 🖥️ System Information & Monitoring

| Command | Description | Use Case |
|---------|-------------|----------|
| `top` | Display running processes and resource usage | Identify high CPU/memory processes |
| `htop` | Improved interactive process viewer (may need install) | Easier navigation than `top` |
| `df -h` | Show disk space usage in human-readable format | Check free space on partitions |
| `free -m` | Display memory usage in megabytes | Monitor RAM and swap usage |
| `uname -a` | Print system information (kernel, OS, architecture) | Verify Linux distribution |
| `uptime` | Show how long the system has been running and load average | Quick health check |

---

## 🌐 Network Diagnostics

| Command | Description | Example |
|---------|-------------|---------|
| `ping` | Test connectivity to a host | `ping google.com` or `ping 8.8.8.8` |
| `ip a` | Display network interfaces and IP addresses | `ip a` (modern replacement for `ifconfig`) |
| `ss -tuln` | Show listening ports and established connections | `ss -tuln` |
| `traceroute` | Trace the route packets take to a host | `traceroute google.com` |
| `nslookup` | Query DNS to resolve domain names | `nslookup example.com` |
| `curl` | Transfer data from/to a server; useful for API/HTTP tests | `curl -I https://example.com` |

---

## 🔐 Permissions & Ownership

| Command | Description | Example |
|---------|-------------|---------|
| `chmod` | Change file permissions (read/write/execute) | `chmod 755 script.sh` |
| `chown` | Change file owner and group | `chown user:group file.txt` |
| `ls -l` | View permissions, owner, and group of files | `ls -l /etc/passwd` |

**Permission Numbers Reference:**
- `7` = read (4) + write (2) + execute (1)
- `6` = read (4) + write (2)
- `5` = read (4) + execute (1)

---

## 📦 Package Management (Ubuntu/Debian)

| Command | Description |
|---------|-------------|
| `sudo apt update` | Refresh package list from repositories |
| `sudo apt upgrade` | Upgrade all installed packages |
| `sudo apt install <pkg>` | Install a package |
| `sudo apt remove <pkg>` | Remove a package |
| `dpkg -l` | List all installed packages |

---

## 📝 Text Processing & Log Analysis

| Command | Description | Example |
|---------|-------------|---------|
| `grep` | Search for patterns in text | `grep "error" /var/log/syslog` |
| `tail -f` | Follow a log file in real time | `tail -f /var/log/apache2/access.log` |
| `head` | Show first lines of a file | `head -n 20 file.txt` |
| `less` | View file content page by page | `less /var/log/syslog` |
| `awk` | Pattern scanning and processing | `awk '{print $1}' file.txt` |
| `sed` | Stream editor for text transformation | `sed 's/old/new/g' file.txt` |

---

## ⚙️ Process & Service Management (systemd)

| Command | Description |
|---------|-------------|
| `systemctl status <service>` | Check service status |
| `systemctl start <service>` | Start a service |
| `systemctl stop <service>` | Stop a service |
| `systemctl restart <service>` | Restart a service |
| `journalctl -u <service>` | View logs for a specific service |
| `ps aux` | List all running processes |

---

## 💡 Example Troubleshooting Workflow

1. **User reports "website is down":**  
   `ping webserver-ip` → check connectivity  
   `ss -tuln | grep :80` → verify web server is listening on port 80  
   `tail -f /var/log/nginx/error.log` → inspect error logs  

2. **System is slow:**  
   `top` → identify process consuming CPU  
   `free -m` → check memory exhaustion  
   `df -h` → verify disk is not full  

---

## 📌 About This Document

This file is part of my personal learning repository as I prepare for an **IT Support L1 / Desktop Support** role. It reflects my current working knowledge of Linux command-line tools used in real-world troubleshooting.

**Maintained by:** Ahmad
**Last updated:** April 2026  
---
