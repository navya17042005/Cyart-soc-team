# Capstone Project: Comprehensive SOC Incident Response

## Tools Used
- Metasploit 
- Wazuh
- CrowdSec 
- TheHive 
- MITRE Caldera 
- Elastic Security 

---

## Attack Simulation

A simulated attack was performed using a Samba usermap script exploit targeting a vulnerable Linux system. The attack originated from IP address 192.168.1.102 and aimed to gain remote access.

---

## Adversary Emulation

| Timestamp            | Source IP      | Alert Description | MITRE Technique |
|----------------------|----------------|-------------------|-----------------|
| 2025-03-26 16:00:00 | 192.168.1.102  | Samba exploit detected | T1210 |

---

## Detection and Triage

Wazuh generated an alert for suspicious activity involving unauthorized access attempts. The alert was analyzed and categorized as a high-severity incident. A case was created in TheHive for tracking and investigation.

---

## Response and Containment

The compromised system was isolated from the network. The attacker’s IP (192.168.1.102) was blocked using CrowdSec. A ping test confirmed that the attacker could no longer reach the target system.

---

## SOAR Automation

A playbook was simulated where:
- IP reputation was checked
- Malicious IP was blocked automatically
- Incident ticket was created in TheHive

---

## Post-Incident Analysis (5 Whys)

1. Why did the attack succeed? → Vulnerable Samba service
2. Why was it vulnerable? → Outdated software
3. Why not updated? → Lack of patch management
4. Why no patching? → Poor asset monitoring
5. Root Cause → Weak vulnerability management

---

## Metrics Reporting

- MTTD: 2 hours
- MTTR: 4 hours
- Dwell Time: 6 hours

---

## Executive Summary 

A simulated cyberattack targeting a vulnerable Samba service was successfully detected and mitigated. The attack originated from an internal IP address and attempted remote exploitation. Wazuh effectively detected the suspicious activity and generated alerts, enabling timely response. The SOC team performed triage and identified the attack as a high-severity incident. Immediate containment actions were taken by isolating the affected system and blocking the malicious IP using CrowdSec. The incident response process demonstrated moderate efficiency, with a Mean Time to Detect (MTTD) of 2 hours and Mean Time to Respond (MTTR) of 4 hours. However, the dwell time of 6 hours highlights a delay in early detection. Root cause analysis revealed that the vulnerability existed due to outdated software and lack of proper patch management practices. This incident emphasizes the importance of continuous monitoring, timely patching, and proactive threat hunting. To improve SOC performance, it is recommended to enhance vulnerability management processes, automate incident response workflows, and reduce false positives through better rule tuning. Overall, the SOC demonstrated effective detection and response capabilities but requires improvement in preventive security measures.

## Stakeholder Briefing 

A cybersecurity incident involving unauthorized access attempts was detected and contained successfully. The attack targeted a system vulnerability and originated from an internal IP address. Security monitoring tools identified the threat within 2 hours, and the response team mitigated it within 4 hours by isolating the affected system and blocking the attacker. While no major damage occurred, the analysis revealed that outdated software allowed the attack to happen. Improvements are needed in patch management and proactive monitoring to prevent similar incidents. Overall, the organization’s security team responded effectively, but enhancements in early detection and system updates are recommended to strengthen defenses.
