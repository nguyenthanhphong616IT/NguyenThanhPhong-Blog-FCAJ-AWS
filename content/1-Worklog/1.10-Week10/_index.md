---
title: "Week 10 Worklog"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

# Week 10: Deploy IaC Infrastructure and Service Integration
**Project:** Smart AI CV Evaluation System
**Deployment Period:** 22/06/2026 – 28/06/2026

### Task Assignment: Phong (AWS Infrastructure)

#### 1. Completed Work
- **AWS CDK & IaC:** Converted the entire infrastructure design into AWS CDK source code, deploying Infrastructure as Code to automate the creation of AWS resources.
- **Amazon DynamoDB:** Deployed the `SmartCVTable`, configuring Point-in-Time Recovery (PITR) to support data recovery in case of incidents. Configured Time To Live (TTL) to automatically delete temporary data and optimize storage space.
- **Authentication (Amazon Cognito):** Deployed an Amazon Cognito User Pool, configured user authentication via Email, and integrated login via Google OAuth. Set up AWS Secrets Manager to store the Client ID and Client Secret for Google OAuth to ensure information security.
- **Amazon API Gateway:** Built the Amazon API Gateway and configured Cognito Authorizers to protect APIs using JWT Tokens.
- **Storage & Content Delivery:** Deployed two buckets, `FrontendBucket` and `ResumeBucket`, on Amazon S3 for storing the UI and candidate profiles. Set up a CloudFront Distribution combined with Origin Access Control (OAC) to restrict direct access to S3, enhancing system security.

#### 2. Difficulties / Pending Issues
- The integration process of Google OAuth with Amazon Cognito encountered errors due to an incorrect Callback URL configuration. It required multiple checks and adjustments to complete the login flow in the Local environment.
- Took significant time to verify IAM Roles and access permissions between AWS services to ensure successful deployment.
