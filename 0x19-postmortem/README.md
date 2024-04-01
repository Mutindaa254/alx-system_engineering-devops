Postmortem: Service Outage on Nairobi Data Center
Issue Summary
Duration: March 25, 2024, 09:00 AM EAT to March 25, 2024, 11:30 AM EAT
Impact: The web application hosted on the Nairobi data center experienced a complete outage, affecting all users accessing the service. Approximately 95% of users were unable to access the application during the outage.
Root Cause: The outage was caused by a misconfiguration in the load balancer settings, leading to improper routing of incoming traffic to the application servers.
Timeline
09:00 AM EAT: Issue detected when monitoring alerts indicated a sudden drop in server response times.
09:05 AM EAT: Engineering team notified of the outage.
09:10 AM EAT: Initial investigation focused on the application servers, assuming a potential issue with the application code or server infrastructure.
09:30 AM EAT: Network team joined the investigation, suspecting a network-related issue due to the widespread impact.
10:00 AM EAT: Load balancer configuration was identified as a potential cause after reviewing network traffic logs.
10:30 AM EAT: Misleading paths of investigation, including DNS issues and database connectivity, were ruled out.
11:00 AM EAT: Incident escalated to senior network engineers for further analysis and resolution.
11:30 AM EAT: Load balancer misconfiguration rectified, restoring normal traffic flow to application servers.
Root Cause and Resolution
Root Cause: The misconfiguration in the load balancer settings resulted in incorrect routing of incoming requests, preventing users from accessing the application servers.
Resolution: The load balancer configuration was updated to ensure proper routing of traffic to the application servers. Specifically, the misconfigured routing rules were corrected to direct incoming requests to the appropriate backend servers.
Corrective and Preventative Measures
Improvements/Fixes:
Implement regular audits of load balancer configurations to identify and rectify any misconfigurations.
Enhance monitoring and alerting systems to provide early detection of similar issues in the future.
Tasks to Address the Issue:
Conduct a comprehensive review of all load balancer configurations across data centers.
Develop automated tests to validate load balancer configurations and ensure proper routing of traffic.
Implement a change management process to carefully review and approve any modifications to critical network infrastructure.
By implementing these measures, we aim to prevent similar incidents from occurring in the future and ensure the reliability and availability of our services to users.


This postmortem report serves as a learning opportunity for our team to improve our incident response processes and strengthen our infrastructure's resilience to potential issues.
