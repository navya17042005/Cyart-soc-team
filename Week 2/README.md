Task 1: Alert Priority Levels

1. Introduction
A Security Operations Center (SOC) processes numerous security alerts daily. Effective alert prioritization ensures that critical threats are handled immediately while lower-risk events are monitored appropriately. The purpose of this task is to understand how alerts are categorized based on severity, business impact, and exploit likelihood. Alert prioritization helps reduce response time, prevent security breaches, and maintain operational continuity.

2. Priority Definitions
Security alerts are categorized into four primary severity levels:
Critical- Represents immediate threats causing active damage such as ransomware encryption or data exfiltration.
High- Indicates serious threats like unauthorized administrative access or exploitation attempts.
Medium- Represents suspicious activity requiring investigation but not causing immediate harm.
Low- Informational or minor events such as port scans or policy violations.

3. CVSS (Common Vulnerability Scoring System)
The Common Vulnerability Scoring System (CVSS) is a standardized framework used to measure the severity of software vulnerabilities. It helps SOC analysts quantify risk and determine appropriate priority levels.
CVSS scores range from 0.0 to 10.0 and are categorized as follows:
0.0 – 3.9 : Low
4.0 – 6.9 : Medium
7.0 – 8.9 : High
9.0 – 10.0 : Critical
The score is calculated using three metric groups:
Base Metrics – Represents the intrinsic severity of a vulnerability.
Temporal Metrics – Accounts for exploit availability and current threat activity.
Environmental Metrics – Considers business impact and asset importance.
For example, Log4Shell (CVE-2021-44228) had a CVSS score of 9.8, making it Critical due to remote code execution and active exploitation.

4. Alert Priority Assignment Criteria
Alert priority is not determined only by CVSS score. SOC analysts consider multiple factors before assigning severity levels. The key criteria used for prioritization include:
4.1 Asset Criticality
The importance of the affected asset within the organization.
Production Server → High criticality
Domain Controller → High criticality
Test VM → Low criticality
If a vulnerability affects a critical production server, its priority increases.
4.2 Exploit Likelihood
The probability that a vulnerability can be exploited.
Public exploit available → High likelihood
Actively exploited in the wild → Very High
No known exploit → Medium or Low
Higher exploit likelihood increases alert severity.
4.3 Business Impact
The potential impact on the organization if the threat succeeds.
Data breach → Critical
Financial loss → High
Minor service delay → Medium
No significant impact → Low
Alert priority is assigned by combining CVSS score, asset value, exploit likelihood, and business impact.

5. Real-World Case Study: Log4Shell Vulnerability
One of the most critical vulnerabilities in recent cybersecurity history was CVE-2021-44228, commonly known as Log4Shell.
Log4Shell affected the Apache Log4j logging library and allowed attackers to perform remote code execution (RCE) on vulnerable systems. The vulnerability received a CVSS score of 9.8 (Critical).
Why It Was Critical:
Remote code execution without authentication,Public exploit code available,Mass exploitation globally,Impact on production servers and cloud infrastructure
Due to its high severity and active exploitation, organizations were required to patch systems immediately. SOC teams worldwide classified Log4Shell alerts as Critical priority because of its potential to cause full system compromise and data breaches.
This case demonstrates how CVSS score, exploit availability, and business impact collectively determine alert priority levels.

6. Mock Alert Prioritization
To understand alert prioritization practically, the following simulated alerts were analyzed and assigned severity levels based on CVSS score, asset criticality,
exploit likelihood, and business impact.
| Alert ID | Alert Type                      | CVSS Score | Asset Affected    | Business Impact            | Assigned Priority |
| -------- | ------------------------------- | ---------- | ----------------- | -------------------------- | ----------------- |
| 001      | Phishing Email                  | 7.5        | Employee Laptop   | Credential Theft Risk      | High              |
| 002      | Log4Shell Exploit Attempt       | 9.8        | Production Server | Remote Code Execution      | Critical          |
| 003      | Port Scan                       | 3.2        | Test VM           | Minimal Impact             | Low               |
| 004      | Multiple Failed Admin Logins    | 8.2        | Domain Controller | Privilege Compromise       | High              |
| 005      | Suspicious PowerShell Execution | 6.8        | HR Workstation    | Possible Malware Execution | Medium            |

7. Escalation Procedure Example
When a critical alert is detected, it must be escalated immediately to Tier 2 analysts or the incident response team.
Example escalation email:
Subject: [Critical] Log4Shell Exploit Attempt Detected
Dear Tier 2 Team,
A critical severity alert has been generated indicating a Log4Shell exploitation attempt on the production application server (192.168.1.15). The vulnerability carries a CVSS score of 9.8 and allows remote code execution without authentication.
Initial logs show suspicious outbound connections suggesting possible payload execution. The affected server hosts sensitive customer transaction data, increasing business risk.
Immediate investigation and containment actions are recommended.
Regards
SOC Analyst
