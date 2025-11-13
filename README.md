# cyber-security-task1
Network port scanning using Nmap (Cyber Security Internship Task 1)

# Task 1 — Local Network Port Scan (Sanitized)

**Author:** Rajendra P M  
**Date:** 2025-11-13

## Summary
Performed network reconnaissance on my local authorized network to discover open ports and services. Sensitive IP addresses and hostnames have been replaced with anonymized tokens (e.g., HOST_1) before publishing.

## Tools used
- Nmap (version X.Y)
- tcpdump (optional)
- Wireshark (optional)

## Steps performed
1. Identified local network: `192.168.1.0/24`
2. Ran TCP SYN scan: `nmap -sS -oN nmap_scan.nmap 192.168.1.0/24`
3. Ran service/version detection: `nmap -sS -sV -oN nmap_with_versions.txt 192.168.1.0/24`
4. Captured packets with tcpdump: `sudo tcpdump -i eth0 -s 0 -w capture.pcap` (if capture included)
5. Sanitized outputs to remove private IPs before committing.

## Findings (anonymized)
- `HOST_1` — Ports: 22/tcp (ssh), 80/tcp (http)
- `HOST_2` — Ports: 137/udp (netbios), 445/tcp (smb)
- (Add your observations and security risks here)

## Recommendations
- Close or firewall unused ports (e.g., restrict access to 3306, 5432).
- Apply least-privilege and network segmentation.
- Keep services and packages up-to-date.
- Use strong authentication and monitor logs.

## Files included
- `nmap_scan_sanitized.txt` — anonymized nmap output
- `nmap_scan.nmap` — local/private raw output **not included** in this public repo
- `notes.md` — detailed notes and remediation steps
