---
title: "Week 11 Worklog"
date: 2026-06-22
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:

* Send the PDF report to users via email using Amazon SES.
* Run an end-to-end test of the whole AI pipeline and set up monitoring with Amazon CloudWatch.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                              | Start Date | Completion Date | Reference Material |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------- |
| Mon | - Learn & configure Amazon SES: domain/email verification, sandbox vs. production (initially forgot that sandbox mode only sends to verified addresses, so test emails to regular addresses failed, had to request production access)                                                                    | 22/06/2026 | 22/06/2026      |                     |
| Tue | - Integrate the Lambda (Report Processor) to email the PDF report/link to users via SES                                                              | 23/06/2026 | 23/06/2026      |                     |
| Wed | - Configure CloudWatch Logs & Metrics for the Lambdas (Core Logic, Report Processor) and API Gateway                                                  | 24/06/2026 | 24/06/2026      |                     |
| Thu | - Set up a CloudWatch Alarm to alert on errors/latency when calling the Gemini API                                                                    | 25/06/2026 | 25/06/2026      |                     |
| Fri | - Run an end-to-end test of the full flow: User request &rarr; Validate &rarr; Generate AI result (Gemini) &rarr; DynamoDB &rarr; SQS &rarr; Report &rarr; S3 &rarr; SES &rarr; Email | 26/06/2026 | 26/06/2026      |                     |
| Sat | - Reviewed the CloudWatch alarms/dashboards set up so far, double-checked alert thresholds                                          | 27/06/2026 | 27/06/2026      |                     |
| Sun | - Prepared notes/documentation for the coming weeks (cost optimization, security review)                                 | 28/06/2026 | 28/06/2026      |                     |

### Week 11 Achievements:

* Completed automatic report-email delivery via Amazon SES, after hitting and resolving the sandbox-mode limitation (only verified addresses can receive email) by requesting production access.
* Set up logging and alarms via CloudWatch across all Lambdas and API Gateway in the AI flow.
* Successfully tested the full end-to-end AI pipeline, from the user's request through to receiving the report email.
* ...
