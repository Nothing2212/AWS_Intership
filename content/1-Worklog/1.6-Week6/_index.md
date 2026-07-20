---
title: "Week 6 Worklog"
date: 2026-05-18
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Understand DNS (Route 53) routing policies and CDN (CloudFront) caching behavior in depth.
* Learn advanced networking concepts: VPC Peering (and its non-transitive nature) and NAT Gateway.

### Tasks to be carried out this week:
| Day | Task                                                                                    | Start Date | Completion Date | Reference Material                           |
| --- | ---------------------------------------------------------------------------------------- | ---------- | --------------- | --------------------------------------------- |
| Mon | - Learn Route 53 in depth: hosted zones, record types (A, CNAME, Alias), and routing policies (simple, weighted, latency-based, failover)                          | 18/05/2026 | 18/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Tue | - **Practice:** point a domain to an EC2/ALB via Route 53 using an Alias record, and compare it against a plain CNAME                                     | 19/05/2026 | 19/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Wed | - Learn Amazon CloudFront in depth: CDN edge caching, origin types (S3, ALB), cache behaviors, TTL settings, and Origin Access Control (OAC) for private S3 origins                                     | 20/05/2026 | 20/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Thu | - **Practice:** create a CloudFront distribution for the S3 static website using OAC (instead of a public bucket); first attempt forgot to update the bucket policy for the OAC's principal, so the bucket was still directly publicly accessible — had to review and fix the policy before it actually blocked direct access                  | 21/05/2026 | 21/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Fri | - Learn VPC Peering (point-to-point, non-transitive routing between VPCs) and NAT Gateway (managed, highly available, vs a self-managed NAT instance)                                                         | 22/05/2026 | 22/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| Sat | - Reviewed the Route 53/CloudFront setup and why OAC is safer than a public bucket policy, cleaned up test resources to avoid extra cost | 23/05/2026 | 23/05/2026      |                                               |
| Sun | - Read overview material on the LunaGenZ project to prepare for joining the project next week | 24/05/2026 | 24/05/2026      |                                               |

### Week 6 Achievements:

* Successfully configured a domain pointing to AWS infrastructure via Route 53 using an Alias record, and understood how routing policies (weighted, latency-based, failover) apply to real traffic-distribution scenarios.
* Deployed a CloudFront distribution in front of the S3 static website using Origin Access Control; after catching and fixing a bucket-policy gap that left direct public access open, locked it down properly so only CloudFront could read the objects, while still serving content quickly over HTTPS via edge caching.
* Understood how VPCs connect via Peering (and why peered connections are not transitive), and how a NAT Gateway lets private subnets reach the internet outbound-only, without exposing them to inbound traffic.
* ...
