Postmortem
Issue Summary:
On March 1st, 2023, our web application experienced an outage that lasted for 2 hours and 15 minutes from 10:00 AM to 12:15 PM Eastern Standard Time (EST). During this time, our users were unable to access the login page and were receiving error messages when attempting to do so. Approximately 40% of our users were affected by this outage.
Root Cause:
The root cause of the issue was a misconfiguration in the load balancer that prevented incoming requests from being forwarded to the backend servers. The misconfiguration occurred during a routine update of the load balancer configuration.
Timeline:
10:00 AM EST: The outage was detected when the monitoring system sent an alert to the operations team. 
10:05 AM EST: The operations team attempted to restart the affected servers but found no issues. 
10:10 AM EST: The team investigated the load balancer configuration as a possible root cause. 
10:30 AM EST: The team identified the misconfiguration in the load balancer and attempted to fix it. 
10:40 AM EST: The team discovered that the fix did not resolve the issue and continued their investigation. 
11:00 AM EST: The team escalated the issue to the development team for additional support. 
11:15 AM EST: The development team identified the root cause of the issue and implemented a fix. 
Noon EST: The operations team confirmed that the issue was resolved, and the application was restored to normal functionality. 
12:15 PM EST: The monitoring system sent a confirmation that the application was functioning correctly. 
Misleading Investigation/Debugging Paths: The initial investigation focused on the server-side components, including the backend servers and the database, which were incident Escalation:
The issue was initially escalated to the development team for additional support.
Resolution:
The development team identified the misconfiguration in the load balancer and implemented a fix to correct it. 
The team also verified that the application was functioning correctly after the fix.
Corrective and Preventative Measures:
To prevent similar issues in the future, the following tasks will be completed:
Automated load balancer configuration testing will be implemented to verify configuration changes. 
A second person will review Load balancer configuration changes before being applied to the production environment. 
Improved monitoring of the load balancer and backend servers will be implemented to quickly detect and diagnose similar issues.
e found to be functioning correctly. The team also focused on the network connectivity between the servers, which was also found to be expected. 
This resulted in a delay in identifying the root cause of the issue.
Incident Escalation:
The issue was initially escalated to the development team for additional support.
Resolution:
The development team identified the misconfiguration in the load balancer and implemented a fix to correct it. 
The team also verified that the application was functioning correctly after the fix.
Corrective and Preventative Measures:
To prevent similar issues in the future, the following tasks will be completed:
Automated load balancer configuration testing will be implemented to verify configuration changes. 
A second person will review Load balancer configuration changes before being applied to the production environment. 
Improved monitoring of the load balancer and backend servers will be implemented to quickly detect and diagnose similar issues.
