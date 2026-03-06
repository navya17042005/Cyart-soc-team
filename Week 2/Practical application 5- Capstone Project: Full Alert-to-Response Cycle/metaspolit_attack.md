## Capstone Project: Full Alert-to-Response Cycle (SOC Simulation)
# 1. Objective

The objective of this capstone project was to simulate a real-world cyberattack and perform the complete SOC workflow, including attack simulation, detection, triage, response, and incident reporting. The project demonstrates how security monitoring tools such as Metasploit, Wazuh, and CrowdSec work together to detect and mitigate malicious activities.

# 2. Attack Simulation

In this phase, a vulnerability in the Metasploitable2 virtual machine was exploited using Metasploit from the attacker machine (Kali Linux).

The vulnerability targeted was the VSFTPD 2.3.4 backdoor vulnerability, which allows attackers to gain unauthorized shell access.

## Metasploit Module Used
exploit/unix/ftp/vsftpd_234_backdoor
# Attack Steps

The attacker scanned the target machine to identify open services.

The FTP service running VSFTPD version 2.3.4 was detected.

The Metasploit exploit module for the vulnerability was launched.

A malicious username triggered the backdoor.

The attacker obtained shell access to the target system.

This demonstrated how attackers exploit outdated services to gain unauthorized access.

## 3. Detection and Triage

The Wazuh SIEM platform was configured to monitor logs and detect suspicious activities.

During the simulated attack, Wazuh generated alerts related to the FTP exploitation attempt.

# Alert Details
Timestamp	Source IP	Alert Description	MITRE Technique
2025-08-18 11:00:00	192.168.1.100	VSFTPD Exploit Attempt Detected	T1190
MITRE ATT&CK Mapping

## The activity was mapped to:

T1190 – Exploit Public-Facing Application

This technique is commonly used by attackers to exploit vulnerabilities in internet-facing services.
