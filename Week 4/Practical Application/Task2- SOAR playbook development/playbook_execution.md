# Playbook Execution Results

| Playbook Step | Status  | Notes                          |
|---------------|---------|--------------------------------|
| Receive Alert | Success | Alert generated from Wazuh      |
| Extract IP    | Success | IP extracted from logs          |
| Check IP      | Success | IP flagged as malicious         |
| Block IP      | Success | IP blocked via CrowdSec         |
| Create Ticket | Success | Incident logged in TheHive      |
| Notify Analyst| Success | Alert sent to SOC analyst       |
