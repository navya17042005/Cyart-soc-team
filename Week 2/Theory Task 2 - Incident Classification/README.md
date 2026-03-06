## Task 2 – Incident Classification

## 1. Introduction

Incident classification is the process of categorizing security incidents based on their type, severity, and characteristics. Proper classification helps SOC analysts quickly understand the nature of the threat and apply appropriate response procedures.By classifying incidents correctly, security teams can streamline investigations, identify patterns of attacks, and improve incident response efficiency.

## 2. Common Incident Categories
Security incidents can be categorized into several types based on the attack method or threat actor behavior.
Malware- Malware incidents involve malicious software such as viruses, worms, ransomware, or trojans that compromise system integrity.
Example: Ransomware encrypting user files.
Phishing -Phishing attacks attempt to trick users into revealing sensitive information such as passwords or credit card details through deceptive emails or websites.

Example: Fake login page sent through email.
## Distributed Denial of Service (DDoS)- A DDoS attack floods a server or network with excessive traffic, making services unavailable to legitimate users.
Example: Web server becoming unreachable due to massive traffic.
## Insider Threat- An insider threat occurs when an employee or authorized user intentionally or accidentally causes a security breach.
Example: Employee exporting confidential company data.
## Data Exfiltration- Data exfiltration refers to unauthorized transfer of sensitive data from a system.
Example: Large amount of confidential files being uploaded to external servers.

## 3. Incident Classification Frameworks
To standardize incident classification, several frameworks are used in cybersecurity.
## MITRE ATT&CK- The MITRE Corporation developed the MITRE ATT&CK framework to document attacker tactics and techniques used in real-world cyber attacks.
SOC analysts use this framework to map incidents to attacker behaviors.
Example:
## Phishing attacks are mapped to technique T1566 – Phishing.

## 4. Contextual Metadata in Incident Classification
In addition to identifying the type of incident, SOC analysts enrich incidents with additional information called metadata.
Common metadata includes:
Timestamp of the event
Source IP address
Destination system
Indicators of Compromise (IOCs) such as malicious hashes or domains
Affected user accounts
This information helps investigators understand how the attack occurred and assists in further analysis.

## 5. Example Incident Classification
Below is an example of how incidents can be classified:
| Incident ID | Incident Type  | MITRE Technique | Source IP     | Description                                |
| ----------- | -------------- | --------------- | ------------- | ------------------------------------------ |
| 001         | Phishing       | T1566           | 185.23.45.10  | Suspicious email containing malicious link |
| 002         | Malware        | T1059           | 192.168.1.20  | Malicious PowerShell execution detected    |
| 003         | DDoS           | T1498           | Multiple      | High traffic flood targeting web server    |
| 004         | Insider Threat | T1041           | Internal User | Employee exporting confidential files      |
This classification helps SOC teams quickly understand the attack type and initiate proper response actions.

## 6. Importance of Incident Classification
Incident classification helps SOC teams prioritize incidents, improve investigation workflows, and enhance overall security monitoring. It ensures that security events are consistently labeled and documented, making it easier to analyze attack trends and respond effectively.
