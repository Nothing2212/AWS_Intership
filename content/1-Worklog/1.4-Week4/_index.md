---
title: "Week 4 Worklog"
date: 2026-05-04
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* Understand Amazon RDS in depth: database engines, Multi-AZ (synchronous, for high availability) vs Read Replica (asynchronous, for read scaling), backup/restore strategy.
* Get familiar with Amazon DynamoDB fundamentals: partition/sort key design and its impact on performance.

### Tasks to be carried out this week:
| Day | Task                                                                                                    | Start Date | Completion Date | Reference Material                           |
| --- | --------------------------------------------------------------------------------------------------------- | ---------- | --------------- | --------------------------------------------- |
| Mon | - Learn Amazon RDS in depth: database engines (MySQL, PostgreSQL,...), Multi-AZ (synchronous standby replica for failover) vs Read Replica (asynchronous, offloads read traffic) and when to combine both | 04/05/2026 | 04/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Tue | - **Practice:** create an RDS instance, connect from EC2/local, and verify the security group only allows access from the app tier, not the public internet                                              | 05/05/2026 | 05/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Wed | - Learn RDS backup, snapshot, and restore: automated backups + retention window vs manual snapshots, and point-in-time recovery                                                                   | 06/05/2026 | 06/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Thu | - Learn Amazon DynamoDB in depth: partition key vs sort key, how the partition key determines data distribution, and why a poorly chosen key causes "hot partitions"                                                      | 07/05/2026 | 07/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Fri | - **Practice:** create a DynamoDB table with a composite key, perform CRUD operations, and compare on-demand vs provisioned capacity mode (first attempt picked a partition key based on a fixed category field, which piled data onto just a few partitions under load testing, so the key had to be redesigned)                                               | 08/05/2026 | 08/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Sat | - Reviewed RDS Multi-AZ/Read Replica and DynamoDB partition key design, practiced a few more CRUD operations and a simple query using a sort key range              | 09/05/2026 | 09/05/2026      |                                               |
| Sun | - Read documentation on Elastic Load Balancer and Auto Scaling to prepare for Week 5     | 10/05/2026 | 10/05/2026      |                                               |

### Week 4 Achievements:

* Understood RDS database engines and, concretely, how Multi-AZ (synchronous replication for failover) differs from a Read Replica (asynchronous, used to scale reads) — and when a production setup needs both.
* Successfully created and connected to an RDS instance from EC2 with network access scoped only to the application tier.
* Learned how automated backups (with a retention window) differ from manual snapshots, and how point-in-time recovery works.
* Got familiar with DynamoDB and practiced designing a composite key (partition + sort key); the first key choice actually caused a hot partition under load testing, so it had to be redesigned for better distribution, and compared on-demand vs provisioned capacity.
* Thanks to that hot-partition incident, understood — from hands-on experience rather than just theory — why picking a good partition key really matters.
* ...
