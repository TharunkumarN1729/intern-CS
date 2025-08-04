# 🔍 Task 1 - Scan Your Local Network for Open Ports

## 🎯 Objective

The goal of this task is to scan a device in the local network using Nmap to identify open ports and understand network exposure. Even when no open ports are found, it is essential to document and analyze the outcome.

---

## 🛠 Tools Used

- Kali Linux
- Nmap (`nmap -sS` for TCP SYN scan)

---

## 📍 Steps Performed

### 1. Identified Local IP

Command used:
```bash
ip a
```
Subnet identified: `192.168.28.0/24`

---

### 2. Ran a TCP SYN Scan

Command used:
```bash
nmap -sS 192.168.28.130 -oN local_network_scan.txt
```

This scanned all 1000 common TCP ports on the host.

---

### 3. Scan Result

```
All 1000 scanned ports on 192.168.28.130 are in ignored states.
Not shown: 1000 closed tcp ports (reset)
```

✅ This means:
- The host is online (`Host is up`)
- All ports are **closed**
- No services are exposed to the network

---

## 🔐 Security Risk Analysis

### ✅ Findings:
- **No open ports** were found on the scanned system.
- This is a **secure configuration** — it minimizes the attack surface.

### 🔒 Interpretation:
- Either the system has no active services
- Or it’s protected by a **host-based firewall**

### 🧠 What This Means:
- The system is **not vulnerable** to service-based attacks like SSH brute-force, HTTP exploits, etc.
- This is **good network hygiene**.

---

## 📁 Files Included

| File Name             | Description                                |
|-----------------------|--------------------------------------------|
| `local_network_scan.txt` | Nmap output file from the scan             |
| `screenshot1.png`     | Output of `ip a` command showing local IP   |
| `screenshot2.png`     | Nmap scan terminal output                   |
| `README.md`           | This documentation file                    |

---

## 🧠 Learning Outcome

- Learned how to scan a local device using Nmap
- Understood what closed ports indicate
- Understood the importance of reducing exposed services
- Practiced documenting and pushing results to GitHub

---

## 🔗 Submission

**GitHub Repository Link:** [https://github.com/TharunkumarN1729/intern-CS]
