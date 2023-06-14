# Postmortem: Web Stack Debugging Issue

## Issue Summary:
Duration: 2 hours (May 15, 2023, 9:00 AM - 11:00 AM GMT +1)
Impact: The API service experienced intermittent slowdowns, resulting in a delay in response times for approximately 20% of users. Users reported sluggish performance and occasional timeouts during this period.

## Timeline:
- 9:00 AM: The issue was detected when an engineer noticed an increase in error rates and response time deviations.
- Actions taken: The monitoring system alerted the team about the anomaly. Investigations focused on the database layer and network infrastructure.
- Misleading investigation/debugging paths: Initial suspicion fell on a database query optimization issue, leading to unnecessary indexing adjustments and query rewriting.
- Escalation: The incident was escalated to the DevOps team for further analysis and to the Product Manager for user impact assessment.
- Incident resolution: After thorough investigation, it was identified that a recent network configuration change caused intermittent packet loss and increased latency.
- The issue was resolved by rolling back the network configuration change and ensuring the proper functioning of network devices.

## Root Cause and Resolution:
- Root cause: A misconfiguration in the network equipment caused intermittent packet loss and increased latency, affecting API service performance.
- Resolution: The issue was fixed by rolling back the recent network configuration change and restoring the network to its previous stable state. Additionally, network monitoring was enhanced to detect and alert on similar anomalies in the future.

## Corrective and Preventative Measures:
- Improve network change management processes to ensure thorough testing and validation before implementing any configuration changes.
- Enhance network monitoring capabilities to promptly detect network performance deviations.
- Implement redundancy and failover mechanisms to minimize the impact of network-related issues.
- Conduct regular audits and reviews of network configurations to identify and rectify potential misconfigurations.


During the investigation, our suspicion initially fell on a rat chewing on network cables at the hosting company. However, after a thorough examination, we discovered it was just a case of network misconfiguration. The rat has been forgiven and is no longer considered a prime suspect.

Nevertheless, the intermittent slowdown issue in the API service was successfully resolved by addressing the misconfiguration in the network equipment. We have implemented corrective measures to prevent such issues in the future and ensure a smoother user experience. Stay tuned for more updates, and rest assured, our network is now rat-proof!

Checkout my blog post : 