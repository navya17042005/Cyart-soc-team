## Incident Response

## Once the malicious activity was confirmed, the following response actions were performed:

## The compromised virtual machine was isolated from the network to prevent further compromise.

## The attacker’s IP address (192.168.1.100) was blocked using CrowdSec firewall rules.

System logs were reviewed to ensure no additional backdoors were installed.

Network connectivity tests were performed to verify that the attacker could no longer communicate with the target machine.

## Verification

A ping test from the attacker system confirmed that the target system was no longer reachable, indicating successful containment.
