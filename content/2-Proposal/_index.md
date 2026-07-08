---
title: "Proposal"
date: 2026-04-18
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# LunaGenZ - Serverless Numerology Web Application
## An Automated Numerology Application System on the AWS Serverless Platform

### 1. Project Overview
LunaGenZ is a Numerology application platform built for young users, allowing them to look up personalized indices based on their date of birth and full name. The system automatically generates a detailed report in PDF format and sends it directly to the user via email.

To ensure flexibility, stability, and cost optimization for the MVP (Minimum Viable Product) stage, the platform adopts a **100% AWS Serverless** architecture and uses a robust in-house PDF generation technology instead of relying on third-party Generative AI services.

### 2. Problem Statement & Solution
#### Current Problem
The market today has many fortune-telling and numerology apps, but most require users to pay upfront or have designs that aren't friendly to the young (Gen Z) customer base. Initially, the team planned to use Generative AI (such as Amazon Bedrock) to generate personalized reports. However, integrating an LLM (Large Language Model) carries the risk of uncontrollable costs for an MVP project and increases latency when generating reports.

#### Technical Solution (Fallback Strategy)
LunaGenZ decided to pivot toward building a solid internal PDF generation system. This solution uses a fully serverless, event-driven architecture:
- **Frontend (Next.js)** is fully hosted on AWS Amplify.
- **Amazon API Gateway** and **AWS Lambda (Node.js)** handle the numerology calculation logic and PDF generation.
- **Amazon DynamoDB** stores request information and metadata.
- **Amazon S3** stores the generated PDF report files.
- **Amazon SES** automatically sends emails with the report attached to the user's inbox.

### 3. Benefits and Return on Investment
The strategy of using an internal PDF generator delivers an extremely stable system (zero cost for calling third-party AI APIs), fast response times, and full control over the output report format. The serverless architecture allows the system to handle load well and auto-scale when a large number of users look up their reports at once (for example, during a TikTok trend), while keeping initial infrastructure costs close to $0 by taking full advantage of the Free Tier.

### 4. Solution Architecture

#### AWS Services Used
- **AWS Amplify:** Hosts the Next.js web application with automatic CI/CD, enabling quick deployment of new frontend versions.
- **Amazon API Gateway:** Acts as the entry point for HTTP requests from the frontend.
- **AWS Lambda:** Runs the logic (Node.js) to calculate numerology numbers, render the PDF file, and trigger the email-sending flow.
- **Amazon DynamoDB:** A high-speed NoSQL database that stores customers' lookup history.
- **Amazon S3:** Ideal object storage for securely storing static PDF report files after they are generated.
- **Amazon SES (Simple Email Service):** An automated email service that quickly attaches and sends the PDF report to customers.

#### Workflow
1. The customer enters their **full name** and **date of birth** on the Next.js interface.
2. The frontend calls the API to send data through **Amazon API Gateway**.
3. The **AWS Lambda function** receives the request, calculates the personal indices, and calls the PDF generation library to render the report.
4. The request payload is recorded in **Amazon DynamoDB**.
5. Once generated, the PDF file is uploaded directly to an **Amazon S3 bucket**.
6. Lambda calls **Amazon SES** to schedule and send an email containing the report to the user.

### 5. Budget & Cost Estimation
Since the system is 100% serverless, the monthly maintenance budget during the first year (MVP stage) is extremely low thanks to the AWS Free Tier:
- **AWS Lambda:** Up to 1 million requests/month ($0)
- **Amazon API Gateway:** 1 million REST API calls/month ($0)
- **Amazon DynamoDB:** 25GB storage, 25 WCU/RCU ($0)
- **Amazon S3:** 5GB Standard storage ($0)
- **Amazon SES:** 62,000 emails/month (if requested from EC2/Lambda) ($0)
- **AWS Amplify:** 1,000 build minutes/month, 5GB storage ($0)

**Total estimated cost:** ~$0/month during the initial (MVP validation) stage.

### 6. Risk Assessment
- **Risk 1:** Amazon SES's email-sending reputation is limited while in Sandbox mode.
  - *Solution:* Submit a request to AWS Support to exit Sandbox mode and verify the domain before officially launching the system to the public.
- **Risk 2:** AWS Lambda's "Cold Start" issue when there's no traffic for a long period, slowing down PDF generation speed.
  - *Solution:* Optimize the Node.js code, use lightweight PDF generation libraries, and set up Provisioned Concurrency if needed during the scaling stage.
