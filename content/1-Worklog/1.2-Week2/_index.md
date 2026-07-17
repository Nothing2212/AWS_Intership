---
title: "Week 2 Worklog"
date: 2026-04-20
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Create an AWS Free Tier account and get familiar with the AWS Console & CLI.
* Understand and practice basic compute services: EC2 (instance families, purchasing options), EBS, Elastic IP, and VPC networking fundamentals.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                          | Start Date | Completion Date | Reference Material                           |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | --------------------------------------------- |
| Mon | - Create an AWS Free Tier account <br> - Install & configure AWS CLI (Access Key, Secret Key, default Region) <br> - Enable MFA on the root account and set up an IAM user for daily use instead of the root account | 20/04/2026 | 20/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Tue | - Learn EC2 in depth: <br>&emsp; + Instance families (t3 burstable vs m5 general purpose vs c5 compute-optimized) <br>&emsp; + AMI (public, custom, Marketplace) <br>&emsp; + EBS volume types (gp3 vs gp2 vs io2) and IOPS/throughput <br>&emsp; + Elastic IP and why it avoids re-associating a new public IP on stop/start | 21/04/2026 | 21/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Wed | - **Practice:** <br>&emsp; + Launch an EC2 instance with a custom Security Group <br>&emsp; + Connect via SSH using a key pair <br>&emsp; + Attach and mount an additional EBS volume, then resize it without downtime | 22/04/2026 | 22/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Thu | - Learn VPC networking fundamentals: <br>&emsp; + CIDR block planning for public/private subnets <br>&emsp; + Route table associations and the default local route <br>&emsp; + Internet Gateway vs NAT Gateway <br>&emsp; + Security Group (stateful, instance-level) vs Network ACL (stateless, subnet-level) | 23/04/2026 | 23/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Fri | - **Practice:** <br>&emsp; + Build a custom VPC from scratch with public/private subnets across two Availability Zones <br>&emsp; + Configure route tables so only the public subnet can reach the Internet Gateway <br>&emsp; + Configure a least-privilege Security Group for EC2 (only required ports open) | 24/04/2026 | 24/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Sat | - Reviewed EC2 instance families and VPC routing logic, redid this week's hands-on labs end-to-end without following the guide to confirm the concepts had actually stuck | 25/04/2026 | 25/04/2026      |                                               |
| Sun | - Read documentation on Amazon S3 (storage classes, durability guarantees, bucket policies) to prepare for Week 3                            | 26/04/2026 | 26/04/2026      |                                               |

### Week 2 Achievements:

* Successfully created and configured an AWS Free Tier account, enabled MFA on root, and set up a least-privilege IAM user for daily work instead of using root.
* Understood EC2 instance families and when to pick each (t3 for bursty/light workloads, m5 for balanced workloads, c5 for compute-heavy workloads), along with AMI, EBS volume types, and why an Elastic IP is needed for a stable public address.
* Practiced launching an EC2 instance, connecting via SSH with a key pair, and attaching/resizing an EBS volume without downtime.
* Built a custom VPC with public/private subnets across two AZs, correctly scoped route tables, and understood the practical difference between Security Groups (stateful) and Network ACLs (stateless).
* ...
