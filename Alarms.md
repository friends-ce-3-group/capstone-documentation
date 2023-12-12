## Summary Of Alarms
| Resource | Count of Alarms | Summary of Alarm Type |
| ---------- | ---------- | ---------- | 
| AWS Lambda | 4 | Monitor Lambda function duration, invocation patterns, and memory usage for anomalies. Identify unusual invocation patterns, detect function throttling, and set up alerts for errors. Keep an eye on memory utilization patterns and identify any unusual trends in Lambda function memory usage. | 
| Elastic Container Service | 1 | Monitor ECS CPU utilization. | 
| S3 | 6 | Monitor latency of S3 requests | 
| Application Load Balancer | 6 | Monitor ALB logs for 4xx errors and set up alerts for 5xx errors. Detect elevated 5xx error counts and unhealthy hosts in the ALB. Identify instances of unhealthy hosts and monitor rejected connections. Set up alerts for elevated 5xx counts in ALB targets and detect elevated 4xx counts in ALB logs. | 
| RDS | 6 | Monitor RDS CPU utilization. | 
| WAF | 1 | Alert on elevated blocked requests in WAF. | 
| NAT Gateway | 4 | Set up alerts for NAT Gateway port allocation errors, monitor the successful connection percentage, and detect any packet drops in the NAT Gateway. | 


## Detailed Alarms

| Alarm Type                                         | Description                                                                          | Use Case                                                   |
| -------------------------------------------------- | ------------------------------------------------------------------------------------ | ---------------------------------------------------------- |
| Lambda Anomalous Duration Count Alarm              | Duration is outside the band (width: 5) for 3 datapoints within 15 minutes           | Monitor Lambda function duration anomalies                 |
| Lambda Anomalous Invocation Count Alarm            | Invocations is outside the band (width: 2) for 3 datapoints within 15 minutes        | Detect unusual Lambda function invocation patterns         |
| Lambda Errors Alarm                                | Errors > 0 for 3 datapoints within 3 minutes                                         | Alert on Lambda function errors                            |
| Lambda Throttles Alarm                             | Throttles > 0 for 3 datapoints within 3 minutes                                      | Identify Lambda function throttling                        |
| Lambda Anomalous Memory Soft Limit Alarm           | used_memory_max > 2000 for 1 datapoint within 3 minutes                              | Monitor Lambda function memory usage                       |
| Lambda Anomalous Memory Deviations Alarm           | memory_utilization is outside the band (width: 5) for 3 datapoints within 15 minutes | Detect unusual Lambda function memory utilization patterns |
| ALB 5xx Count Alarm                                | HTTPCode_ELB_5XX_Count >= 100 for 3 datapoints within 5 minutes                      | Detect elevated 5xx counts in ALB                          |
| ALB Healthy Host Count Alarm                       | HealthyHostCount <= 0 for 3 datapoints within 5 minutes                              | Alert on unhealthy hosts in ALB                            |
| ALB Unhealthy Host Count Alarm                     | UnHealthyHostCount >= 1 for 1 datapoint within 1 minute                              | Identify instances of unhealthy hosts in ALB               |
| ALB Rejected Connections Count Alarm               | RejectedConnectionCount >= 100 for 3 datapoints within 5 minutes                     | Monitor rejected connections in ALB                        |
| ALB Target 5xx Count Alarm                         | HTTPCode_Target_5XX_Count >= 100 for 3 datapoints within 5 minutes                   | Alert on elevated 5xx counts in ALB targets                |
| ALB 4xx Count Alarm (ELB)                          | HTTPCode_ELB_4XX_Count >= 100 for 3 datapoints within 5 minutes                      | Detect elevated 4xx counts in ALB                          |
| 4xx Errors Alarm (ALB Log)                         | 4xxErrors > 0 for 3 datapoints within 5 minutes                                      | Monitor 4xx errors in ALB logs                             |
| 5xx Errors Alarm (ALB Log)                         | 5xxErrors > 0 for 1 datapoint within 1 minute                                        | Alert on 5xx errors in ALB logs                            |
| NAT Gateway Port Allocation Errors Alarm           | ErrorPortAllocation > 0 for 3 datapoints within 5 minutes                            | Alert on NAT Gateway port allocation errors                |
| NAT Gateway Successful Connection Percentage Alarm | Successful Connection Percentage < 50 for 3 datapoints within 5 minutes              | Monitor NAT Gateway successful connection percentage       |
| NAT Gateway Packets Drops Alarm                    | Packets Drop Count > 0 for 3 datapoints within 5 minutes                             | Detect NAT Gateway packet drops                            |
| ECS CPU Utilization Alarm                          | CPUUtilization > 90 for 5 datapoints within 25 minutes                               | Monitor ECS CPU utilization                                |
| S3 Total Request Latency Alarm                     | TotalRequestLatency > 2000 for 1 datapoint within 1 minute                           | Monitor latency of S3 requests                             |
| RDS CPU Utilization Alarm                          | CPUUtilization > 90 for 5 datapoints within 25 minutes                               | Monitor RDS CPU utilization                                |
| WAF Blocked Requests Alarm                         | BlockedRequests > 10 for 1 datapoint within 5 minutes                                | Alert on elevated blocked requests in WAF                  |
| ECS Memory Utilization Alarm                       | MemoryUtilization < 10 for 1 datapoint within 6 hours                                | Monitor ECS memory utilization                             |
| ECS CPU Utilization Alarm                          | CPUUtilization > 90 for 5 datapoints within 25 minutes                               | Monitor ECS CPU utilization                                |