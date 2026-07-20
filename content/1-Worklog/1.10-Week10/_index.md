---
title: "Week 10 Worklog"
date: 2026-06-15
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Build an AWS Lambda (Report Processor) that generates a PDF report from the AI result.
* Store the report on Amazon S3 and configure a lifecycle policy to transition it to S3 Glacier.

### Tasks to be carried out this week:
| Day | Task                                                                                                                    | Start Date | Completion Date | Reference Material |
| --- | ------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ------------------- |
| Mon | - Evaluate PDF-generation libraries usable inside the Lambda runtime used by the project (the first choice exceeded the Lambda deployment package size limit, had to switch to a lighter library / package it via a Lambda Layer)                                  | 15/06/2026 | 15/06/2026      |                     |
| Tue | - Code the Lambda (Report Processor): consume the AI result message from SQS, build the PDF report content                | 16/06/2026 | 16/06/2026      |                     |
| Wed | - Configure storing the PDF file in Amazon S3 (Report Bucket) with a sensible object naming/path convention               | 17/06/2026 | 17/06/2026      |                     |
| Thu | - Configure an S3 lifecycle policy: transition objects to **S3 Glacier** after **30 days** (first setup had the wrong transition filter so the rule didn't apply to the right objects, had to review and fix it)                                 | 18/06/2026 | 18/06/2026      |                     |
| Fri | - Test the full report generation & storage flow, verify the lifecycle rule works correctly                               | 19/06/2026 | 19/06/2026      |                     |
| Sat | - Reviewed the Report Processor Lambda code, refactored parts of it based on the mentor's feedback    | 20/06/2026 | 20/06/2026      |                     |
| Sun | - Read documentation on Amazon SES to prepare for Week 11                                            | 21/06/2026 | 21/06/2026      |                     |

### Week 10 Achievements:

* Completed the Report Processor Lambda: it consumes the AI result from SQS and automatically generates a PDF report, after switching away from the first PDF library that exceeded the Lambda deployment package size limit.
* Stored PDF reports on S3 (Report Bucket) with a clear naming structure.
* Successfully configured a lifecycle rule that automatically moves objects to S3 Glacier after 30 days (after catching and fixing an incorrect filter on the first attempt), reducing long-term storage cost.
* ...
