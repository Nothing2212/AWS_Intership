---
title: "Week 3 Worklog"
date: 2026-04-27
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:

* Understand and practice the Amazon S3 storage service in depth.
* Learn storage classes and their durability/cost/retrieval-time trade-offs, lifecycle policies, versioning, access control layers, and static website hosting on S3.

{{% notice note %}}
30/04 and 01/05/2026 are public holidays in Vietnam, so this week only has 3 working days.
{{% /notice %}}

### Tasks to be carried out this week:
| Day | Task                                                                                                                              | Start Date | Completion Date | Reference Material                           |
| --- | -------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | --------------------------------------------- |
| Mon | - Learn Amazon S3 in depth: buckets, objects, storage classes (Standard, Standard-IA, One Zone-IA, Glacier, Glacier Deep Archive) and their durability (11 nines), availability, and retrieval-time trade-offs | 27/04/2026 | 27/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Tue | - **Practice:** create a bucket, upload/download objects via console and CLI <br> - Configure versioning (forgot to enable it before testing an object overwrite the first time, had to recreate the bucket and redo the test to actually see the benefit) & permissions (bucket policy vs IAM policy vs ACL, and the precedence between them) | 28/04/2026 | 28/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Wed | - Learn S3 lifecycle policies: transition rules between storage classes and expiration rules, and how they reduce long-term storage cost <br> - **Practice:** host a static website on S3, understand its HTTP-only limitation and why CloudFront + OAC is needed for HTTPS | 29/04/2026 | 29/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Thu | - Public holiday (Reunification Day)                                                                                               | 30/04/2026 | 30/04/2026      |                                                |
| Fri | - Public holiday (International Labor Day)                                                                                         | 01/05/2026 | 01/05/2026      |                                                |
| Sat | - Made up practice on S3 lifecycle policies and static website hosting missed due to the mid-week holidays, and tested how an object actually behaves once transitioned to Glacier (retrieval delay, restore request) | 02/05/2026 | 02/05/2026      |                                                |
| Sun | - Reviewed this week's S3 material end-to-end, read ahead on RDS/DynamoDB for Week 4                                              | 03/05/2026 | 03/05/2026      |                                                |

### Week 3 Achievements:

* Understood S3 storage classes (Standard, Standard-IA, One Zone-IA, Glacier tiers) and the concrete trade-offs (cost vs retrieval latency vs durability) that decide when to use each.
* Practiced creating a bucket, uploading/downloading objects via both console and CLI, and configuring versioning together with the layered access-control model (bucket policy, IAM policy, ACL) and how they combine.
* Configured a lifecycle policy to automatically transition objects across storage classes and expire old ones, reducing long-term storage cost.
* Successfully deployed static website hosting on S3 and understood why it's HTTP-only, which sets up the motivation for adding CloudFront later.
* Learned to enable important settings (like versioning) before testing rather than after, to avoid having to redo a lab from scratch.
* ...
