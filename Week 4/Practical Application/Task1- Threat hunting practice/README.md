## Threat Intelligence Hunt

Threat intelligence was used to validate potential indicators related to MITRE ATT&CK technique T1078 (Valid Accounts).

### OTX Analysis

AlienVault OTX was used to search for known indicators such as suspicious IP addresses and attacker techniques. This provided context on how attackers misuse valid credentials.

### Endpoint Analysis (Velociraptor)

The following query was executed:

SELECT * FROM processes()

This query retrieves active processes from the endpoint to identify suspicious or unauthorized activity.

The analysis helps detect abnormal process execution that may indicate credential misuse or attacker persistence.
