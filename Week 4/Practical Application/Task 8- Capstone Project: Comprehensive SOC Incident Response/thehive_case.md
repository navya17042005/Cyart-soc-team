## Incident Case - Unauthorized Samba Exploitation

### Title:
Samba Exploit Attempt Detected

### Severity:
High

### Description:
A suspicious SMB-based exploitation attempt was detected from attacker machine (Kali Linux). The attack targeted a vulnerable Samba service on the Metasploitable system.

### Observables:
- Source IP: 192.168.56.101
- Target IP: 192.168.56.102
- Technique: T1210 (Exploitation of Remote Services)

### Actions Taken:
- Alert generated in Wazuh
- Incident logged in TheHive
- Attacker IP marked for blocking

### Status:
In Progress
