🛡️ Cyber Security Internship – Task 1: Local Network Port Scan
This document outlines the process and findings of a local network port scan conducted as part of a cybersecurity internship. The goal was to discover open ports on active devices and understand potential network exposure in a controlled, isolated test environment.
🎯 Objective
To perform a local network scan to discover open ports on active devices and understand potential network exposure.
💻 Environment & Tools
 * 🖥️ Operating System: Kali Linux (Live Boot)
 * 🛠️ Core Tool: Nmap (Network Mapper) <img src="https://www.google.com/search?q=https://upload.wikimedia.org/wikipedia/commons/thumb/a/a6/Nmap_logo.svg/32px-Nmap_logo.svg.png" alt="Nmap logo" height="20" style="vertical-align:middle;">
 * 🔬 Optional Tool: Wireshark (for packet-level insight) <img src="https://www.google.com/search?q=https://upload.wikimedia.org/wikipedia/commons/thumb/8/82/Wireshark_Icon.svg/32px-Wireshark_Icon.svg.png" alt="Wireshark logo" height="20" style="vertical-align:middle;">
 * 🌐 Network: Personal mobile-hotspot test network (10.x.x.x/24)
⚙️ Steps Executed
 * Determined the private IP range (10.x.x.x/24) of the test network using ifconfig.
 * Ran a stealthy SYN scan (-sS) across the entire subnet to identify active hosts and open ports.
   sudo nmap -sS 10.x.x.x/24

 * Saved the complete scan results to scan_results.txt for analysis.
 * (Optional) Captured scan traffic using Wireshark to observe the SYN packet exchange at a granular level.
 * Analyzed the output to identify services associated with the detected open ports.
📊 Key Findings
 * 📡 Total Scanned Hosts: 256
 * 🖥️ Active Hosts Detected: 2
 * 🚪 Example Open Port: 53/tcp was found open on one test device (10.x.x.x), corresponding to the DNS (Domain Name System) service.
 * 🔒 Other Host: All scanned ports were in a closed or filtered state.
 * 📄 Detailed Logs: Refer to scan_results.txt and nmap_output.png (if included in this repository).
🧐 Security Observations
 * 🔵 The discovered 53/tcp (DNS) port is a common and often necessary service for network functionality.
 * 🟡 This exercise demonstrates that even simple networks can have open ports. Continuous monitoring is essential to minimize the attack surface and reduce unnecessary exposure.
 * 🟢 Ethical Scoping: All scans were conducted strictly on a controlled, self-owned test network. No external or institutional systems were probed, adhering to ethical hacking principles.
🧠 Learnings & Key Takeaways
 * ✅ Gained practical experience using Nmap for network reconnaissance and port scanning.
 * ✅ Developed the ability to interpret Nmap scan outputs and correlate open ports with their corresponding network services.
 * ✅ Reinforced the importance of responsible disclosure, privacy, and ethical boundaries when handling network scan data.
EXAMPLE:
Aashish Bishokarma
Cyber Security Student | Ethical Hacking Enthusiast
📧 Email: aashishgorkhali0@gmail.com
🌐 GitHub: DarkCipherAashish
