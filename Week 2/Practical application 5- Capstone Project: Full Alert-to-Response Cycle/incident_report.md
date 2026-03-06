## Incident Report 

A simulated cyberattack was conducted to test the organization’s detection and response capabilities. The attack targeted a vulnerable FTP service running VSFTPD 2.3.4 on a Metasploitable2 system. Using the Metasploit framework, the attacker successfully exploited the backdoor vulnerability to gain unauthorized shell access. The attack was detected by the Wazuh SIEM platform, which generated alerts indicating suspicious FTP activity.

## Timeline

Attack initiated using Metasploit exploit module.

Wazuh generated an alert indicating suspicious FTP activity.

Security analyst reviewed the alert and confirmed exploitation.

The affected system was isolated from the network.

CrowdSec was used to block the attacker’s IP address.

Connectivity tests confirmed the attack was successfully mitigated.

## Recommendations

Update vulnerable services such as VSFTPD to secure versions.

Implement regular vulnerability scanning.

Enable strict firewall policies for external connections.

Continuously monitor logs using SIEM tools.
