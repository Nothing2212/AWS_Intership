---
title: "Week 9 Worklog"
date: 2026-06-08
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Handle asynchronous processing of AI results via Amazon SQS.
* Tie the payment verification flow (Verify Payment) to DynamoDB before returning the AI result to the user.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                  | Start Date | Completion Date | Reference Material |
| --- | -------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------- |
| Mon | - Learn Amazon SQS: queues, messages, visibility timeout                                                                                 | 08/06/2026 | 08/06/2026      |                     |
| Tue | - Design the flow: the Lambda (Core Logic) pushes the generated AI result to SQS (the "Out result" step)                                 | 09/06/2026 | 09/06/2026      |                     |
| Wed | - Code the SQS message consumer <br> - Query DynamoDB to check the payment status (Verify Payment) before returning the result           | 10/06/2026 | 10/06/2026      |                     |
| Thu | - Integrate with the Lambda (Payment Webhook Handler): receive the payment callback, update the status in DynamoDB                       | 11/06/2026 | 11/06/2026      |                     |
| Fri | - Test the end-to-end flow: request &rarr; validate &rarr; verify payment &rarr; generate AI result &rarr; push result via SQS           | 12/06/2026 | 12/06/2026      |                     |
| Sat | - Reviewed this week's SQS/DynamoDB flow, wrote up personal technical notes                                          | 13/06/2026 | 13/06/2026      |                     |
| Sun | - Read documentation on PDF-generation libraries to prepare for Week 10                                              | 14/06/2026 | 14/06/2026      |                     |

### Week 9 Achievements:

* Successfully built an asynchronous processing flow using Amazon SQS for the generated AI results.
* Ensured the system only returns the AI result to the user once the payment status is confirmed in DynamoDB.
* Successfully integrated with the Lambda Payment Webhook Handler to update payment status automatically.
* ...
