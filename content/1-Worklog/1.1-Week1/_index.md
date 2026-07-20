---
title: "Week 1 Worklog"
date: 2026-04-17
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Week 1 Objectives:

* Connect and get acquainted with members of First Cloud Journey (FCJ) and the mentor.
* Understand the internship schedule (17/04/2026 - 30/07/2026), rules, and weekly worklog process.
* Get an overview of AWS's global infrastructure and core service groups, and understand the Shared Responsibility Model.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                          | Start Date | Completion Date | Reference Material                           |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | --------------------------------------------- |
| Fri | - Meet and get acquainted with FCJ members and mentor <br> - Read and take note of internship unit rules and regulations <br> - Get an overview of AWS's global infrastructure (Regions, Availability Zones, Edge Locations) and the Shared Responsibility Model <br> - Study the main AWS service groups and how they relate to each other <br>&emsp; + Compute (EC2, Lambda) <br>&emsp; + Storage (S3, EBS) <br>&emsp; + Networking (VPC, Route 53) <br>&emsp; + Database (RDS, DynamoDB) | 17/04/2026 | 17/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Sat | - Reviewed notes from the onboarding session in detail, mapped out how the Shared Responsibility Model splits duties between AWS and the customer for each service group (still mixed up some of the boundaries for the Networking group and had to re-read the material a few times to get it straight), and prepared to create an AWS Free Tier account for next week | 18/04/2026 | 18/04/2026      |                                               |
| Sun | - Read additional overview material on EC2 (instance types, purchasing options) and VPC (CIDR blocks, subnets) to prepare for Week 2's hands-on labs                        | 19/04/2026 | 19/04/2026      |                                               |

### Week 1 Achievements:

* Got acquainted with FCJ members, the mentor, and the internship schedule.
* Understood the rules, regulations, and the weekly worklog reporting process.
* Started building a mental model of AWS's global infrastructure (Regions/AZs for high availability, Edge Locations for CDN) and the Shared Responsibility Model (AWS secures "of the cloud", the customer secures "in the cloud"), though some of the finer boundaries — especially around Networking — still need more reading to fully click.
* Gained a basic overview of AWS's main service groups and how a typical workload combines them:
  * Compute (EC2 for VMs, Lambda for serverless)
  * Storage (S3 for objects, EBS for block storage)
  * Networking (VPC as the isolated network boundary, Route 53 for DNS)
  * Database (RDS for relational, DynamoDB for NoSQL)
* Overall grasped the foundational material at a fairly good (not yet deep) level; plan to reinforce this through hands-on practice in the coming weeks.
