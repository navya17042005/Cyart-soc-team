## Executive Summary

A simulated cyber attack was conducted to evaluate SOC detection and response capabilities. The attack involved exploitation of a vulnerable Samba service using Metasploit. The activity was successfully detected through monitoring tools, and response actions were initiated.

## Incident Timeline

- Attack initiated from Kali Linux
- Exploit executed targeting Samba service
- Reverse shell obtained
- Detection triggered in Wazuh
- Incident recorded and analyzed

## Impact

The attacker gained unauthorized shell access to the target system, demonstrating critical security gaps.

## Recommendations

- Implement regular patch management
- Strengthen intrusion detection rules
- Automate response using SOAR tools
- Improve network segmentation
