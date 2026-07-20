---
title: "Week 5 Worklog"
date: 2026-05-11
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* Understand and deploy an Elastic Load Balancer (ALB/NLB) and Auto Scaling, including scaling policies.
* Get familiar with system monitoring via Amazon CloudWatch: metrics, alarms, and how alarms can trigger scaling actions.

### Tasks to be carried out this week:
| Day | Task                                                                                          | Start Date | Completion Date | Reference Material                           |
| --- | ------------------------------------------------------------------------------------------------- | ---------- | --------------- | --------------------------------------------- |
| Mon | - Learn about Elastic Load Balancer: Application Load Balancer (Layer 7, path/host-based routing) vs Network Load Balancer (Layer 4, ultra-low latency)                                                       | 11/05/2026 | 11/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Tue | - **Practice:** create an Application Load Balancer, target group, and health check; the first attempt set the unhealthy threshold too low, so a target got marked unhealthy and pulled out of the load balancer after just one slow response (a false positive) — had to raise the threshold/interval to more sensible values                     | 12/05/2026 | 12/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Wed | - Learn about Auto Scaling Group, launch templates, and scaling policy types: target tracking vs step scaling vs scheduled scaling                                                  | 13/05/2026 | 13/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Thu | - **Practice:** configure an Auto Scaling Group combined with an ALB, using a target-tracking policy based on average CPU utilization                                | 14/05/2026 | 14/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Fri | - Learn Amazon CloudWatch: metrics (standard vs custom), alarms (thresholds, evaluation periods), dashboards, and how an alarm can directly trigger an Auto Scaling action                                               | 15/05/2026 | 15/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Sat | - Reviewed the ALB/Auto Scaling Group setup, re-tested scale-out/scale-in scenarios by simulating CPU load and observing how quickly the target-tracking policy reacted | 16/05/2026 | 16/05/2026      |                                               |
| Sun | - Read documentation on Route 53 and CloudFront to prepare for Week 6            | 17/05/2026 | 17/05/2026      |                                               |

### Week 5 Achievements:

* Understood the practical difference between an ALB (Layer 7, content-based routing) and an NLB (Layer 4, ultra-low latency), and picked ALB for this use case.
* Successfully deployed an Application Load Balancer with a target group and health check; after hitting a false-positive unhealthy target from a too-sensitive threshold, gained a better practical understanding of how the health-check interval/threshold trades off failover speed against false positives.
* Configured an Auto Scaling Group with a target-tracking scaling policy based on CPU utilization, integrated with the ALB, and validated scale-out/scale-in behavior under simulated load.
* Set up CloudWatch alarms to monitor EC2 CPU/metrics and understood how an alarm state change can directly drive an Auto Scaling action.
* ...
