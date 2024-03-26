This project is about:
## Postmortem : Outage on Dec 1, 2022
##
> On Dec 1, 2023, users experienced slow response times while accessing our application platform. Approximately 30% of our users were affected.

- Timeline:
> 12:00 PM: The issue was detected by our monitoring system, which alerted the engineering team.

>12:10 PM: The team investigated the issue and found that the database was experiencing high CPU usage.

>12:30 PM: The team assumed that a recent code deployment was the root cause and rolled back the deployment.

>1:00 PM: The team discovered that the rollback did not fix the issue and continued investigating.

>2:00 PM: The team realized that the high CPU usage was caused by a spike in traffic from a third-party service that was integrated into our platform.

>2:30 PM: The team contacted the third-party service and requested they limit their traffic to our platform.

>3:00 PM: The third-party service limited their traffic and the issue was resolved.

>4:00 PM: The team confirmed that the issue was resolved and closed the incident.


- Root Cause and Resolution:
> The root cause of the issue was a spike in traffic from a third-party service that was integrated into our platform. This caused the database to experience high CPU usage, resulting in slow response times for our users. The issue was resolved by contacting the third-party service and requesting they limit their traffic to our platform.

- Corrective and Preventative Measures:
>To prevent similar incidents in the future, we will implement the following measures:
1. Improve our monitoring system to provide more granular insights into system performance.
2. Implement automatic scaling for our database to handle spikes in traffic.
3. Review and update our third-party service integration policies to ensure they are compliant with our system requirements.
4. Establish better communication channels with third-party services to quickly address any issues that may arise.
5. Train engineering teams to investigate and identify issues more efficiently.

- Tasks:

1. Implement automatic scaling for our database.
2. Review and update our third-party service integration policies.
3. Schedule regular meetings with third-party services to discuss integration performance.
4. Improve documentation on our incident response process and train engineering teams on how to follow it.
5. Improve monitoring systems to provide more granular insights into system performance.