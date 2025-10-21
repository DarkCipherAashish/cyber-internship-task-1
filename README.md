# Cyber Security Internship – Task 1: Local Network Port Scan 

## Objective
Performed a local network scan to discover open ports on active devices and understand potential network exposure.

## Environment
- Operating System: Kali Linux (Live Boot)
- Tools Used: Nmap, Wireshark (optional)
- Network: Personal mobile-hotspot test network (10.x.x.x/24)

## Steps Executed
1. Determined the private IP range (10.x.x.x/24) using ifconfig.
2. Ran a SYN scan with: sudo nmap -sS 10.x.x.x/24
3. Saved results to scan_results.txt.
4. Optionally captured traffic using Wireshark for packet-level insight.
5. Identified services associated with detected open ports.

## Key Findings
- Total scanned hosts: 256
- Active hosts: 2
- Example open port: 53/tcp (open DNS service) on one test device (10.x.x.x).
- Other host: All ports in closed or filtered state.
- Detailed logs: See scan_results.txt and nmap_output.png.

## Security Observations
- The discovered open port (53/tcp) corresponds to the DNS service, which is typical in most networks.
- Continuous monitoring of open ports is essential to reduce unnecessary exposure.
- Scans were conducted only on a controlled, self-owned test network — no external or institutional systems were probed.

## Learnings
- Learned practical usage of Nmap for reconnaissance and port scanning.
- Understood how to interpret scan outputs and correlate them with real network services.
- Gained awareness of responsible disclosure and privacy when handling scan data.
