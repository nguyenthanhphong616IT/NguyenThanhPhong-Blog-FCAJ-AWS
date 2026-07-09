---
title: "Week 12 Worklog"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

# Week 12: Infrastructure Review, Cost Evaluation, and Handover
**Project:** Smart AI CV Evaluation System
**Deployment Period:** 06/07/2026 – 12/07/2026

### Task Assignment: Phong (AWS Infrastructure)

#### 1. Completed Work
- **Overall Inspection:** Conducted a comprehensive inspection of the AWS infrastructure before handing over the product.
- **Security & Access Permissions:**
  - Reviewed all IAM Policies of Lambda Functions according to the Least Privilege principle, removing unnecessary access permissions.
  - Checked the configuration of Amazon S3 Block Public Access, CloudFront Origin Access Control, and Bucket Policies to ensure data cannot be accessed unauthorizedly.
- **Cost Evaluation:** Evaluated and analyzed deployment costs based on the Serverless Pay-per-request architecture, comparing it with traditional server models to demonstrate cost efficiency.
- **Documentation & Handover Report:**
  - Completed the AWS infrastructure design documentation using AWS CDK, added deployment diagrams, and finalized documents describing the Infrastructure as Code architecture.
  - Wrote the AWS Infrastructure section of the report, explaining in detail how the infrastructure was deployed using AWS CDK, the Serverless architecture, and the DynamoDB Single-Table Design model, serving the project handover and defense process.

#### 2. Difficulties / Pending Issues
- Need to carefully review all IAM permissions and security policies before deploying to Production to avoid any security vulnerabilities.
- Synthesizing technical documentation and architectural descriptions requires cross-referencing multiple components in the system to ensure accuracy and completeness.
