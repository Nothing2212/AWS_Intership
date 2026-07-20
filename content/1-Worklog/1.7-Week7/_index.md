---
title: "Week 7 Worklog"
date: 2026-05-25
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Assigned to the **LunaGenZ** project, responsible for the **AI part**.
* Understand the overall AWS architecture of the system (frontend, backend, AI, reporting).
* Learn about the Gemini API and the Gemini models.

{{% notice note %}}
Starting this week, the worklog focuses on the AI workstream of the LunaGenZ project that I am directly responsible for.
{{% /notice %}}

### Tasks to be carried out this week:
| Day | Task                                                                                                                                        | Start Date | Completion Date | Reference Material |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ------------------- |
| Mon | - Attend the LunaGenZ project kickoff meeting, understand the business problem & requirements                                               | 25/05/2026 | 25/05/2026      |                     |
| Tue | - Study the overall architecture: CloudFront, Amplify (Next.js), API Gateway, Lambda, DynamoDB, SQS, S3, SES (being new to the project, was fairly confused at first about how these services connected, needed the mentor to walk through the data flow again)                                  | 26/05/2026 | 26/05/2026      |                     |
| Wed | - Learn about the Gemini API: model tiers (Gemini Flash, Gemini Pro), free-tier limits <br> - Register an API key on Google AI Studio         | 27/05/2026 | 27/05/2026      |                     |
| Thu | - **Practice:** try calling the Gemini API (generateContent) via REST/SDK (hit the free-tier rate limit after several back-to-back test calls, had to read up on quotas/exponential backoff)                                                                     | 28/05/2026 | 28/05/2026      |                     |
| Fri | - Study the AI processing flow: user request &rarr; AWS Lambda (Core Logic) &rarr; Gemini API &rarr; return the generated result              | 29/05/2026 | 29/05/2026      |                     |
| Sat | - Attended the **Meeting 30/5** event with FCJ members (see the "Events Participated" &rarr; Event 1 section for details)                     | 30/05/2026 | 30/05/2026      |                     |
| Sun | - Read further material on the Gemini API and effective prompt writing to prepare for Week 8                              | 31/05/2026 | 31/05/2026      |                     |

### Week 7 Achievements:

* Understood the overall architecture diagram of LunaGenZ and the role of each service: CloudFront, Amplify, API Gateway, Lambda, DynamoDB, Gemini API, SQS, S3, SES, though the first week was fairly confusing and needed the mentor's help to clarify the data flow between services.
* Understood where and how the AI part (content-generation step) fits into the overall processing flow.
* Successfully test-called the Gemini API to generate sample content, and learned about the free-tier rate limit the hard way after hitting it during repeated testing.
* ...
