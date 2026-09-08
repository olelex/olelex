# Oleksii Zanko

**SOC Analyst N1 · Blue Team — detection & response**

Montevideo, Uruguay · open to remote · available for rotating shifts, nights, weekends and on-call (7×24)

---

I build a detection stack, attack it, and then try to catch myself doing it. What I learn goes into a lab I run at home, and what I get wrong goes into the write-up.

Before this I spent 7 years in hospitality operations, the last two running a 20-person kitchen on rotating shifts. That is where I learned to work a queue under time pressure, follow written procedure, hand over cleanly at the end of a shift, and escalate before something burns. A SOC runs on the same habits.

## Main project — [soc-home-lab](https://github.com/olelex/soc-home-lab)

Active Directory domain on Windows Server 2022 Core, Windows 11 client, Ubuntu server. Sysmon telemetry shipped into Wazuh, attack simulation with Atomic Red Team, detections mapped to MITRE ATT&CK, cases tracked in GLPI. Seven stages, each one documented with what broke and how it was fixed.

**Featured write-up — [tuning a level 15 false positive](https://github.com/olelex/soc-home-lab/blob/main/docs/06-detection-tuning.md)**

A critical alert mapped to `T1105` was firing on `__PSScriptPolicyTest_*.ps1`, an artefact PowerShell writes into `AppData\Local\Temp` every time it checks the execution policy. Disabling the rule would have removed the coverage entirely, so I narrowed its pattern in `local_rules.xml` instead — then verified in both directions: the benign artefact stopped alerting, and a real `.ps1` dropped into Temp still fired at level 15. My first attempt (`if_sid` + `level 0`) did not work, and that is in the write-up too, with the root cause.

## Skills

- **SIEM & detection** — Wazuh (custom rules, tuning, false-positive analysis), IBM QRadar (SIEM Foundation), Sigma
- **Telemetry** — Sysmon, Windows Event IDs, PowerShell logging, process ancestry, command lines
- **Frameworks & method** — MITRE ATT&CK, Cyber Kill Chain, 5W triage, N1→N2 escalation
- **Attack simulation** — Atomic Red Team
- **Windows** — Server 2022 Core, Active Directory (users, OU, GPO), PowerShell
- **Networking** — TCP/IP, DNS, DHCP, VPN, VLAN; Wireshark, tcpdump, Nmap
- **Linux** — CLI, SSH, permissions, services
- **ITSM** — GLPI: ticket lifecycle, SLA, incident documentation

Also familiar with common offensive tooling from CTF and lab work (Gobuster, Burp Suite, Hydra, John the Ripper). I am not claiming pentest experience — the value for me is recognising what these leave behind in telemetry.

## Certifications & training

- **IBM QRadar SIEM Foundation** — IBM badge (Credly), Sept 2026
- **CompTIA Security+ (SY0-701)** — exam booked for November 2026
- **TryHackMe** — SOC Level 1 path (in progress) · Cyber Security 101 (completed Aug 2026)
- **CTF** — Hacker Holidays 2026 (Byte Lotus)
- **BSc Information Technology** — UTEC, Uruguay (started 2026, in progress)

## Languages

Ukrainian (native) · Russian (native) · Spanish (fluent) · English (technical)

## Contact

- LinkedIn: [oleksii-zanko](https://www.linkedin.com/in/oleksii-zanko)
- TryHackMe: [f8lex](https://tryhackme.com/p/f8lex)
