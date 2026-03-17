# 🔐 Home Lab – Virtual Network Cyber Security Project

## 📌 Overview
This project demonstrates the design and implementation of a virtual cyber security lab used to simulate real-world attacks and defensive techniques. The lab environment allows for safe testing of penetration testing tools, network analysis, and system hardening.

The purpose of this project is to develop practical cyber security skills aligned with real-world scenarios, including identifying vulnerabilities, exploiting weaknesses, and applying mitigation strategies.

---

## 🖥️ Lab Environment

### Virtualisation Platform
- VirtualBox

### Virtual Machines
- Kali Linux (Attacker machine)
- Metasploitable 2 (Vulnerable target machine)
- Windows VM (optional for additional testing)

---

## 🌐 Network Configuration

The lab is configured using an isolated internal network to safely simulate attacks without impacting external systems.

Example IP configuration:

Kali Linux:        192.168.56.101  
Metasploitable:    192.168.56.102  

---

## 🛠️ Tools Used

### Nmap
Used for network discovery and port scanning to identify active hosts and open services.

Example command:
nmap -sV 192.168.56.102

---

### Wireshark
Used for packet capture and analysis to monitor network traffic and identify suspicious activity.

---

### Metasploit Framework
Used to exploit known vulnerabilities within the Metasploitable machine and gain access.

---

## ⚔️ Activities Performed

### 1. Network Scanning
- Identified live hosts within the network
- Discovered open ports and running services
- Detected potential vulnerabilities based on service versions

---

### 2. Vulnerability Identification
- Analysed scan results to identify outdated or insecure services
- Mapped findings to known vulnerabilities (CVEs)

---

### 3. Exploitation
- Used Metasploit Framework to exploit vulnerabilities
- Successfully gained access to the target system
- Demonstrated how attackers can move from discovery to compromise

---

### 4. Traffic Analysis
- Captured network traffic using Wireshark
- Analysed packets to observe communication between attacker and target
- Identified patterns that could indicate malicious activity

---

### 5. System Hardening
- Disabled unnecessary services on the target machine
- Applied basic firewall configurations
- Reduced attack surface and improved system security
- Re-scanned system to confirm improvements

---

## 🧠 Key Learning Outcomes

- Gained hands-on experience with network scanning and enumeration
- Developed understanding of common vulnerabilities and exploitation techniques
- Learned how attackers identify and exploit weaknesses in systems
- Improved knowledge of defensive techniques such as system hardening
- Developed ability to analyse network traffic for security purposes

---

## 📁 Project Structure

Home-Lab-Virtual-Network
│
├── README.md
├── reports/
└── notes/

---

## 📊 Conclusion

This project demonstrates practical cyber security skills including network enumeration, vulnerability assessment, exploitation, and defensive strategies. It highlights the importance of proactive security measures and provides a foundation for more advanced cyber security practices.

The lab environment will continue to be expanded with additional tools, attack scenarios, and monitoring solutions.
