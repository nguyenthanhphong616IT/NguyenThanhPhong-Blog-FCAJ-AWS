---
title: "Week 11 Worklog"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

# Week 11: Frontend, Backend Integration and System Optimization
**Project:** Smart AI CV Evaluation System
**Deployment Period:** 29/06/2026 – 05/07/2026

### Task Assignment: Phong (AWS Infrastructure)

#### 1. Completed Work
- **API Gateway & Lambda Integration:** Collaborated with the Backend team to connect all AWS Lambda Functions with methods on Amazon API Gateway. Tested the data processing flow from `Frontend` → `API Gateway` → `Lambda` → `DynamoDB` to ensure the entire system functions seamlessly.
- **Automated Scheduling (EventBridge):** Developed AWS CDK code to deploy Amazon EventBridge Rules for automatically scheduling recurring tasks according to the UTC timezone.
- **CORS Policy Optimization:** Configured and optimized the CORS Policy on Amazon S3 and API Gateway, allowing only valid domains to access system resources.
- **Frontend CI/CD Deployment:** Completed the automated Frontend deployment process via CI/CD, including:
  - Building the Frontend source code.
  - Uploading to Amazon S3.
  - Performing CloudFront Cache Invalidation to update to the new version immediately after deployment.
- **Environment Variables:** Checked and optimized environment variables for the deployment process across different environments.

#### 2. Difficulties / Pending Issues
- Encountered CORS errors when configuring via AWS CDK due to inconsistent settings between API Gateway and S3.
- Had to redeploy multiple times to check Mock Integration, Header configurations, and the OPTIONS method before the entire API operated stably.
