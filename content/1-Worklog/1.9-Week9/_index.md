---
title: "Week 9 Worklog"
date: 2026-06-08
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Store the generated AI result in Amazon DynamoDB.
* Handle the asynchronous handoff of the job to the Report Processor via Amazon SQS.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                  | Start Date | Completion Date | Reference Material |
| --- | -------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------- |
| Mon | - Learn Amazon SQS: queues, messages, visibility timeout                                                                                 | 08/06/2026 | 08/06/2026      |                     |
| Tue | - Design the flow: the Lambda (Core Logic) stores the generated AI result in DynamoDB, then pushes the job to SQS for the Report Processor | 09/06/2026 | 09/06/2026      |                     |
| Wed | - Code the logic to write the result to the DynamoDB table (partition key designed around user/request id)                              | 10/06/2026 | 10/06/2026      |                     |
| Thu | - Code the Lambda (Core Logic) to send a job message to SQS after the DynamoDB write succeeds (the first test run had the Lambda retried on a timeout and it accidentally sent a duplicate message, so an idempotency check based on request id had to be added before writing/sending)                                          | 11/06/2026 | 11/06/2026      |                     |
| Fri | - Test the end-to-end flow: request &rarr; validate &rarr; generate AI result (Gemini) &rarr; store in DynamoDB &rarr; push job via SQS | 12/06/2026 | 12/06/2026      |                     |
| Sat | - Reviewed this week's SQS/DynamoDB flow, wrote up personal technical notes                                          | 13/06/2026 | 13/06/2026      |                     |
| Sun | - Read documentation on PDF-generation libraries to prepare for Week 10                                              | 14/06/2026 | 14/06/2026      |                     |

### Week 9 Achievements:

* Successfully built the logic to store the generated AI result in Amazon DynamoDB with a sensible partition key.
* Built an asynchronous processing flow using Amazon SQS to hand the job off to the Report Processor; after catching a duplicate-message bug caused by a Lambda retry, added an idempotency check keyed on request id.
* Tested the end-to-end request &rarr; generate AI result &rarr; store in DynamoDB &rarr; push to SQS flow, running stably.
* ...
