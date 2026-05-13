# Implementing Snort as IDS/IPS for Compliance Rules

## Overview
This project implements Snort as both an Intrusion Detection System (IDS) and 
Intrusion Prevention System (IPS) in a virtualized lab environment. Custom Snort 
rules were written and mapped to real-world compliance frameworks to detect and 
block unauthorized network activity.

## Objectives
- Deploy Snort in IDS and IPS mode on Ubuntu (VMware)
- Write custom rules aligned with compliance standards
- Simulate real attacks and validate detection/prevention
- Generate compliance alert logs as evidence

## Tools & Technologies
| Tool | Purpose |
|------|---------|
| Snort | IDS/IPS engine |
| Nmap | Network reconnaissance |
| Hydra | Brute-force attack simulation |
| Wireshark | Packet analysis |
| OpenSSH | SSH service on victim machine |
| Kali Linux | Attacker machine |
| VMware | Virtualized lab (Kali + Ubuntu) |

## Compliance Frameworks Implemented
| Framework | Rule Applied |
|-----------|-------------|
| PCI-DSS (Req. 2.2.3) | Block Telnet (Port 23) cleartext protocol |
| ISO/IEC 27001 (Control A.9) | Detect SSH brute-force attempts (Port 22) |
| HIPAA Transmission Security | Flag unauthorized outbound connections / data exfiltration |
| NIST CSF Detect & Protect | Block port scanning reconnaissance (Nmap SYN scan) |

## Attack Simulation & Results
- **Nmap scan** → Snort detected and blocked reconnaissance activity
- **Hydra SSH brute-force** → All login attempts dropped by Snort IPS
- **Telnet connection attempt** → PCI-DSS violation alert triggered
- **Unauthorized outbound connection** → HIPAA rule flagged data exfiltration attempt

## Key Outcomes
- 100% detection rate on all simulated attack vectors
- Real-time alerts generated in Snort console and log files
- Compliance violation evidence documented for audit purposes

## Team
5-member project | BS Cybersecurity | Air University, Multan
