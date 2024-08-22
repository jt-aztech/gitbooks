# 🤝 Service Level Objectives (SLOs)

* **Availability:** The service aims for 99.9% uptime.&#x20;
* **Performance:** Given the data intensive nature, a response time below 4 seconds for the 90th percentile of users is required.
* **Fault tolerance:** The service must handle faults by retrieving and processing missed data points in the original order in case of a fault, ensuring temporary issues don't lead to permanent data loss or undesired results.
