---
title: "Week 7 Worklog"
date: 2026-05-25
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Assigned to the **LunaGenZ** project, responsible for the **AI part**.
* Understand the overall AWS architecture of the system (frontend, backend, payment, AI, reporting).
* Learn about Amazon Bedrock and the Claude 3 Haiku model.

{{% notice note %}}
Starting this week, the worklog focuses on the AI workstream of the LunaGenZ project that I am directly responsible for.
{{% /notice %}}

### Tasks to be carried out this week:
| Day | Task                                                                                                                                        | Start Date | Completion Date | Reference Material |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ------------------- |
| Mon | - Attend the LunaGenZ project kickoff meeting, understand the business problem & requirements                                               | 25/05/2026 | 25/05/2026      |                     |
| Tue | - Study the overall architecture: WAF, CloudFront, Amplify (Next.js), API Gateway, Cognito, Lambda, DynamoDB                                  | 26/05/2026 | 26/05/2026      |                     |
| Wed | - Learn about Amazon Bedrock and its foundation models <br> - Enable access to the **Claude 3 Haiku** model                                   | 27/05/2026 | 27/05/2026      |                     |
| Thu | - **Practice:** try calling the Bedrock InvokeModel API with Claude 3 Haiku via console/SDK                                                   | 28/05/2026 | 28/05/2026      |                     |
| Fri | - Study the AI processing flow: user request &rarr; AWS Lambda (Core Logic) &rarr; Amazon Bedrock &rarr; return result (Gen Prompt AI)        | 29/05/2026 | 29/05/2026      |                     |
| Sat | - Attended the **Meeting 30/5** event with FCJ members (see the "Events Participated" &rarr; Event 1 section for details)                     | 30/05/2026 | 30/05/2026      |                     |
| Sun | - (Self-study at home) Read further material on Amazon Bedrock and effective prompt writing to prepare for Week 8                              | 31/05/2026 | 31/05/2026      |                     |

### Week 7 Achievements:

* Understood the overall architecture diagram of LunaGenZ and the role of each service: WAF, CloudFront, Amplify, Cognito, API Gateway, Lambda, DynamoDB, Bedrock, SQS, S3, SES.
* Understood where and how the AI part ("Gen Prompt AI" step) fits into the overall processing flow.
* Successfully test-called the Claude 3 Haiku model via Amazon Bedrock.
* ...
