---
title: "Week 8 Worklog"
date: 2026-06-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Design prompts for LunaGenZ's AI content generation feature.
* Integrate AWS Lambda (Core Logic) with Amazon Bedrock to generate results (the Gen Prompt AI step).

### Tasks to be carried out this week:
| Day | Task                                                                                                                                | Start Date | Completion Date | Reference Material |
| --- | --------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------- |
| Mon | - Analyze the incoming request data (from API Gateway after passing the Cognito Authorizer) <br> - Build request validation logic  | 01/06/2026 | 01/06/2026      |                     |
| Tue | - Design the prompt template for Claude 3 Haiku tailored to LunaGenZ's business logic                                               | 02/06/2026 | 02/06/2026      |                     |
| Wed | - Code the AWS Lambda (Core Logic): build the request payload, call Bedrock InvokeModel, parse the response                         | 03/06/2026 | 03/06/2026      |                     |
| Thu | - Handle errors & retries when calling Bedrock (timeout, throttling) <br> - Securely store API keys/secrets via AWS Secrets Manager | 04/06/2026 | 04/06/2026      |                     |
| Fri | - Test the prompt with various sample inputs, tune it to improve the quality of generated results                                   | 05/06/2026 | 05/06/2026      |                     |
| Sat | - Attended the **Meeting 06/6** event with FCJ members (see the "Events Participated" &rarr; Event 2 section for details)           | 06/06/2026 | 06/06/2026      |                     |
| Sun | - (Self-study at home) Reviewed this week's prompt-tuning results, researched Bedrock throttling limits further                     | 07/06/2026 | 07/06/2026      |                     |

### Week 8 Achievements:

* Completed the Lambda (Core Logic) that calls Amazon Bedrock/Claude 3 Haiku to generate content from the designed prompt template.
* Securely managed API keys/secrets via AWS Secrets Manager instead of hardcoding them.
* Made error handling, timeout, and retry logic for Bedrock calls more stable.
* Tuned the prompt over multiple iterations to improve the quality and consistency of the AI output.
* ...
