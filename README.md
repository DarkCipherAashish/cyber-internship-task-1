🛡️ Cyber Security Internship – Task 1: Local Network Port Scan

📖 Project Overview

This repository contains the deliverables for Task 1 of the Cyber Security Internship. The task focuses on conducting a local network port scan to identify active hosts, open ports, and associated services on a controlled test network.


---

🎯 Objective

Perform a comprehensive scan of the local network.

Discover active hosts and open ports.

Analyze potential network exposure in a safe, ethical, and controlled environment.



---

💻 Environment & Tools

🖥️ Operating System: Kali Linux (Live Boot) 

🛠️ Primary Tool: Nmap (Network Mapper) 

🔍 Optional Tool: Wireshark (packet-level inspection) 

🌐 Network: Personal mobile-hotspot test network (10.x.x.x/24)



---

⚙️ Methodology

1. Identify the subnet of the test network using ifconfig or ip addr.


2. Conduct a stealth SYN scan across the subnet to detect active hosts and open ports:



sudo nmap -sS 10.x.x.x/24 -oN Scan_Result.txt -oX Scan_Result.xml

3. Save and analyze scan results (Scan_Result.txt and Scan_Result.xml) to identify hosts and services.


4. Optionally capture network traffic using Wireshark for granular SYN/SYN-ACK inspection.


5. Document findings and highlight potential security observations.




---

📊 Key Findings

Total Scanned Hosts: 256

Active Hosts Detected: 2

Example Open Port: 53/tcp (DNS) on 10.x.x.x

Other Hosts: All scanned ports were either closed or filtered


> Note: All scanning activities were performed within a controlled and ethical environment.




---

🧐 Security Observations

53/tcp is a common service (DNS); always monitor to prevent potential abuse.

Even small networks may have exposed services; minimizing unnecessary open ports reduces attack surface.

Ethical scanning ensures no legal or privacy violations while practicing cybersecurity skills.



---

🧾 Learnings & Takeaways

Hands-on experience with Nmap for network reconnaissance.

Ability to interpret scan outputs and associate ports with corresponding services.

Reinforced the importance of ethical practices and controlled testing in cybersecurity.



---

📁 Repository Structure

README.md
Nmap_output.png        
Scan_Result.txt        
Scan_Result.xml        
Wireshark_capture.png  


---

🔄 How to Reproduce

1. Boot Kali Linux on a test machine.


2. Connect to a controlled network (e.g., 10.x.x.x/24).


3. Execute the Nmap scan command.


4. Review Scan_Result.txt or visualize Scan_Result.xml in Zenmap.


5. Optionally, inspect packet captures in Wireshark or open Wireshark_capture.png.




---

📝 Suggested Git Commit Messages

Initial Commit: chore: add README and initial Nmap scan results

Add Nmap screenshot: docs: add Nmap_output.png for scan visualization

Add Wireshark capture: feat: add Wireshark_capture.png for packet inspection



---

⚖️ Ethical Considerations

All scanning and packet captures were performed on self-owned networks. Do not attempt unauthorized scanning on external or public networks.


---

👤 Author

Aashish Bishokarma
Cyber Security Student | Ethical Hacking Enthusiast

📧 Email: aashishgorkhali0@gmail.com
🌐 GitHub: DarkCipherAashish
