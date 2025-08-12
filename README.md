# 🛰️ Basic Nmap Scan on 192.168.1.5 (Windows PowerShell)

## 📌 Objective

Perform a basic network scan using Nmap on a local target (IP: 192.168.1.5) to identify open ports, running services, and potential vulnerabilities. The scan is executed using Windows PowerShell, and results are documented here for learning and reporting purposes.

> ⚠️ This scan was run on a machine I own or have permission to scan.

---

## 🧪 Scan Details

- 📅 Date of scan: August 12, 2025  
- 🖥️ Target IP: 192.168.1.5  
- 🧰 Scan tool: Nmap (via PowerShell)  
- 💻 OS used: Windows 11  
- 📄 Output file: nmap_scan_results.txt  
- 📸 Screenshots: located in the screenshots/ folder

---

## 🛠️ Nmap Commands Used

```powershell
nmap -sS -sV -p- -T4 192.168.1.5 -oN nmap_scan_results.txt
Explanation:

-sS → TCP SYN scan

-sV → Service version detection

-p- → Scan all 65535 ports

-T4 → Faster timing (normal performance)

-oN → Save output to a normal text file

📋 Summary of Findings
PORT      STATE    SERVICE         VERSION
135/tcp   open     msrpc           Microsoft Windows RPC
137/tcp   filtered netbios-ns
139/tcp   open     netbios-ssn     Microsoft Windows netbios-ssn
445/tcp   open     microsoft-ds?
808/tcp   open     mc-nmf          .NET Message Framing
5040/tcp  open     unknown
5357/tcp  open     http            Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
7070/tcp  open     ssl/realserver?
7680/tcp  open     pando-pub?
49664/tcp open     msrpc           Microsoft Windows RPC
49665/tcp open     msrpc           Microsoft Windows RPC
49666/tcp open     msrpc           Microsoft Windows RPC
49667/tcp open     msrpc           Microsoft Windows RPC
49668/tcp open     msrpc           Microsoft Windows RPC
49672/tcp open     msrpc           Microsoft Windows RPC
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

🛡️ Recommendations
Close any ports that are not in use.

Use strong, unique passwords for services like SSH or MySQL.

Ensure all software/services are updated to the latest secure versions.

Use a firewall to limit external access to only necessary services.
