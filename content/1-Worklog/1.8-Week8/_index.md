---
title: "Week 8 Worklog"
date: 2026-06-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Design prompts for LunaGenZ's AI content generation feature.
* Integrate AWS Lambda (Core Logic) with the Gemini API to generate results.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                | Start Date | Completion Date | Reference Material |
| --- | --------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------- |
| Mon | - Analyze the incoming request data (from API Gateway) <br> - Build request validation logic                                       | 01/06/2026 | 01/06/2026      |                     |
| Tue | - Design the prompt template for Gemini tailored to LunaGenZ's business logic (the first draft was too generic, so the results often drifted off-topic and didn't stick to the business requirements)                                                       | 02/06/2026 | 02/06/2026      |                     |
| Wed | - Code the AWS Lambda (Core Logic): build the request payload, call the Gemini API, parse the response                             | 03/06/2026 | 03/06/2026      |                     |
| Thu | - Handle errors & retries when calling the Gemini API (timeout, rate limit) <br> - Securely store the API key via AWS Secrets Manager | 04/06/2026 | 04/06/2026      |                     |
| Fri | - Test the prompt with various sample inputs, tune it to improve the quality of generated results (took several rounds of trial and error to narrow the prompt down to the right format and tone)                                   | 05/06/2026 | 05/06/2026      |                     |
| Sat | - Attended the **Meeting 06/6** event with FCJ members (see the "Events Participated" &rarr; Event 2 section for details)           | 06/06/2026 | 06/06/2026      |                     |
| Sun | - Reviewed this week's prompt-tuning results, researched Gemini API rate-limit constraints further                     | 07/06/2026 | 07/06/2026      |                     |

### Week 8 Achievements:

* Completed the Lambda (Core Logic) that calls the Gemini API to generate content from the designed prompt template.
* Securely managed the API key via AWS Secrets Manager instead of hardcoding it.
* Made error handling, timeout, and retry logic for Gemini API calls more stable.
* Tuned the prompt over multiple iterations to improve the quality and consistency of the AI output, after the first draft was too generic and produced off-topic results.
* Some edge-case inputs still make Gemini return content in the wrong format, so further tuning is needed in the coming weeks.
* ...
