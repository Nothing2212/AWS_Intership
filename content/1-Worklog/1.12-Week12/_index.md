---
title: "Week 12 Worklog"
date: 2026-06-29
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Week 12 Objectives:

* Optimize prompts and the cost/latency of Gemini API calls, and learn CI/CD for automatic Amplify deployment from GitHub.
* Review system security (Secrets Manager, IAM permissions), run regression tests, and finalize documentation and the final internship report.

{{% notice note %}}
This covers the final stretch of the internship (29/06/2026 - 30/07/2026), merged into one final worklog entry.
{{% /notice %}}

### Tasks to be carried out this week:
| Days                    | Task                                                                                                             | Start Date | Completion Date | Reference Material |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------- |
| 29/6 - 5/7               | - Optimize prompts for the Gemini API: reduce token count, measure and compare latency/cost between Gemini models (Flash vs. Pro) | 29/06/2026 | 05/07/2026      |                     |
| 6/7 - 12/7               | - Learn & practice configuring AWS Amplify CI/CD: connect the GitHub repo, auto-deploy on new commits (the first deploy failed due to a misconfigured build command, had to check the build logs and fix it), test rollback on a failed build | 06/07/2026 | 12/07/2026      |                     |
| 13/7 - 19/7              | - Security review: AWS Secrets Manager, IAM permissions for the Lambdas (found one Lambda had broader permissions than it needed, had to scope it down to least-privilege) <br> - Regression-test the whole system, fix any bugs found | 13/07/2026 | 19/07/2026      |                     |
| Mon - Thu (20-23/7)      | - Prepare and demo the AI part of the LunaGenZ project to the mentor, gather feedback and make revisions <br> - Finalize the technical documentation describing the architecture & AI processing flow | 20/07/2026 | 23/07/2026      |                     |
| Fri - Thu (24-30/7)      | - Finalize the internship final report, hand over work, and submit the report on time                             | 24/07/2026 | 30/07/2026      |                     |

### Week 12 Achievements:

* Optimized prompts to reduce token usage and Gemini API call cost, improving response latency; compared the tradeoffs between Gemini models to pick the right model per use case.
* Successfully configured CI/CD on AWS Amplify to automatically deploy the frontend on every new GitHub commit, after fixing a bad build-command config that broke the first deploy.
* Reviewed and hardened security across the system: secrets managed via Secrets Manager, and scoped down one over-permissive Lambda IAM role to least-privilege after finding it during the review.
* Completed regression testing, ensuring the AI pipeline runs stably.
* Finalized technical documentation, demoed the AI part of the LunaGenZ project, and submitted the final internship report on time (30/07/2026).
* Looking back on the whole internship, I'd rate my own grasp of the LunaGenZ architecture and AI processing flow as fairly good (good, not excellent); areas like Gemini API cost/performance optimization, CI/CD, and system security are still ones I'd like to go deeper on given more time.
