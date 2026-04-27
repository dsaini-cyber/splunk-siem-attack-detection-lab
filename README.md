# Splunk SIEM Home Lab with Attack Simulation

## Overview
A fully functional home Security Operations Center 
(SOC) lab built using VMware virtualization to simulate 
real-world cyber attacks and detect them using Splunk SIEM.

## Lab Architecture
Kali Linux (192.168.178.158) — Attacker Machine
Windows 11 (192.168.178.160) — Target + Splunk Forwarder
Windows 10 (192.168.178.159) — Splunk Enterprise SIEM

## Attacks Simulated
| Attack | Tool | Event Code Generated |
|--------|------|---------------------|
| Network Reconnaissance | Nmap | Firewall Logs |
| SYN Flood | hping3 | 1025, 4624, 4672 |
| SMB Brute Force | Hydra | 4625, 4624 |
| RDP Brute Force | Hydra | 4625, 4740 |
| Remote Code Execution | Metasploit PSExec | 4624, 4672, 4688 |
| Password Hash Dumping | Mimikatz | 4624, 4672 |

## Detection & Monitoring
| Event Code | Description |
|------------|-------------|
| 4624 | Successful Login |
| 4625 | Failed Login |
| 4672 | Special Privileges Assigned |
| 4688 | New Process Created |
| 4740 | Account Locked Out |
| 1025 | Network Connection Error |

## Tools Used
- Splunk Enterprise
- Splunk Universal Forwarder
- Kali Linux
- Metasploit Framework
- Mimikatz
- Hydra
- Nmap
- hping3
- VMware

## Key Findings
- Collected 1,563+ Windows Security Events
- Successfully established Meterpreter session
- Dumped password hashes using Mimikatz
- Detected all attacks via Splunk SIEM in real time

## Screenshots
See screenshots folder for evidence of attacks
and detection.

## Skills Demonstrated
- SIEM configuration and management
- Log analysis and threat detection
- Network attack simulation
- Incident response
- Windows security monitoring
- Password hash dumping and analysis
