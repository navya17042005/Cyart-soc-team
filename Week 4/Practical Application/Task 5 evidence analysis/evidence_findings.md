# Evidence Analysis Findings

## Tool Used:
Velociraptor

## Query Executed:
SELECT * FROM netstat();

## Observations:
- Multiple active connections detected
- Suspicious external IP: 185.234.x.x
- Port: 4444 (commonly used for reverse shells)
- Connection State: ESTABLISHED

## Analysis:
The connection appears abnormal as it connects to an external unknown IP over a non-standard port. This behavior is consistent with command-and-control (C2) communication.

## Conclusion:
Potential compromise detected. Further investigation required
