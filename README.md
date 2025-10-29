# ApexPlanet-Cybersecurity-Task2
Network Security &amp; Scanning 

## Overview
Built a virtual cybersecurity lab using *Kali Linux (attacker)* and *Metasploitable2 / DVWA (target)* in VirtualBox (Host-Only network).  
Practiced Linux fundamentals, basic networking (OSI/TCP-IP), cryptography using OpenSSL, and familiarized with core tools: *Nmap, Wireshark, Burp Suite, Netcat*.  
All work performed in an isolated local lab for learning and safe testing only.

---
## Deliverables Summary
1. *Lab Setup Report (PDF)*  
   - docs/lab_report_task1.pdf — includes topology, steps, screenshots, commands, and conclusions.


2. *Scans & Artifacts*
   - scans/full_combo.nmap / scans/svc_detect.txt — Nmap saved outputs
   - pcaps/task1_capture.pcap — Wireshark capture (use Git LFS or external link)
   - vuln_reports/ — any vulnerability scanner HTML/PDF exports (if used)

3. *Notes & Cheat Sheets*
   - notes/linux_cheatsheet.md
   - notes/task1_commands.md (commands used to reproduce)
   - notes/task1_analysis.md (short analysis + mitigation suggestions)

4. *Short Demo Video (5 min)*  
(https://www.linkedin.com/posts/palak-baranwal-a98145337_cybersecurity-ethicalhacking-infosec-activity-7389166344681734144-m7vT?utm_source=social_share_send&utm_medium=android_app&rcm=ACoAAFSPZ9QBM7MH4wKOnhLjjQttu_AWlDqDMA0&utm_campaign=copy_link)

---

## How to reproduce:
1. Import/Install VMs:
   - Import Metasploitable2.ova (or deploy DVWA) and install Kali from ISO in VirtualBox.  
2. Configure network:
   - Kali: Adapter1 = NAT, Adapter2 = Host-Only (vboxnet0).  
   - Target: Adapter1 = Host-Only (vboxnet0).  
3. Verify IPs:
   - On Kali: ip a → note 192.168.56.xxx.  
   - On Target: ifconfig / ip a → note 192.168.56.yyy.  
4. Basic tests:
   - ping -c 4 <target-ip>  
   - sudo nmap -sS -sV -O -p- <target-ip> -oA scans/full_combo  
   - Run Wireshark on host-only interface and curl http://<target-ip> to capture HTTP traffic.  
   - openssl demos from notes/task1_commands.md.


## Contact
- *Name:* Palak Baranwal 
- *LinkedIn / Video:* Paste LinkedIn video link here after upload
