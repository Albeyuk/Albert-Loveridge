# Home Lab – Virtual Network Cyber Security Project

## 📌 Overview
This home lab provides a controlled environment for practising penetration testing, network enumeration, vulnerability assessment, and system hardening. It is designed to simulate real-world scenarios in a safe virtual network.

## 🖥️ Lab Environment
- **Platform:** VirtualBox  
- **Virtual Machines:**  
  - Kali Linux (Attacker)  
  - Metasploitable 2 (Vulnerable Target)  
  - Optional: Windows VM for additional testing

## 🌐 Network Configuration
- Host-only networking to isolate the lab  
- Example IP addressing:  
  - Kali: 192.168.56.101  
  - Metasploitable: 192.168.56.102

## 🛠️ Tools Used
- **Kali Linux:** Nmap, Netcat, Metasploit Framework, Wireshark  
- **Other:** VirtualBox snapshots, logging, and monitoring tools

## 📋 Activities Performed
- Network scanning and enumeration  
- Vulnerability identification  
- Exploitation of services (planned / simulated)  
- Traffic capture and analysis  
- System hardening practices  

## 🔐 Proof of Access

### 💻 Attacker Machine Session
The following output demonstrates the active user on the Kali Linux attacker machine used in this lab:

```bash
albey@kali:~$ whoami
albey
