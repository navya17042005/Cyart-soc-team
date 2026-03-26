# SOAR Playbook: Phishing Incident Response

## Objective
Automate response to phishing-related alerts by identifying malicious IPs and blocking them to prevent further compromise.

## Playbook Steps
1. Receive phishing alert from SIEM (Wazuh)
2. Extract IP address from alert
3. Check IP reputation using threat intelligence source
4. If malicious:
   - Block IP using firewall (CrowdSec)
   - Generate alert ticket in TheHive
5. Notify SOC analyst

## Outcome
Automated detection and response reduces manual effort and improves response time.
