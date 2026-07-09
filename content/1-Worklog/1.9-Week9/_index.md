---
title: "Week 9 Worklog"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

# Week 9: Initialize AWS Infrastructure and Database Design
**Project:** Smart AI CV Evaluation System
**Deployment Period:** 15/06/2026 – 21/06/2026

### Task Assignment: Phong (AWS Infrastructure)

In Week 9, taking on the role of AWS Infrastructure for the Smart AI CV evaluation system, I focused on designing the overall architecture, organizing the IaC project, and optimizing the database. Below are the detailed tasks completed:

#### 1. Infrastructure Architecture Design
- **AWS Network Topology Diagram:** Researched the requirements for the CV evaluation system and designed the infrastructure architecture diagram using a Serverless model.
- **Data Flow Description:** Established the integrated data processing flow among core AWS services, including CloudFront, S3, API Gateway, Lambda, Cognito, DynamoDB, and Amazon Bedrock (for the AI CV analysis component).

#### 2. DynamoDB Database Design
- **Single-Table Design Application:** Designed the Amazon DynamoDB database following the Single-Table Design pattern, thoroughly analyzing business requirements and system query patterns.
- **SmartCVTable:** Reached an agreement with the Backend team to store the main entities (`Applications`, `Notes`, `Settings`, `StatusEvents`) within a single table named `SmartCVTable`.
- **Optimized Key System:** Implemented a key system utilizing `PK`, `SK`, `GSI1PK`, and `GSI1SK` to consolidate entities, optimize query performance, and minimize operational costs.
- **Data Documentation:** Created comprehensive documentation detailing the data structure, key conventions, and query patterns to support the API development team in upcoming phases.

#### 3. Infrastructure as Code (IaC) Initialization
- **AWS CDK (TypeScript):** Initialized the infrastructure project directory using the AWS Cloud Development Kit (CDK) with TypeScript.
- **Structural Organization:** Built a standard Infrastructure as Code directory structure and prepared the necessary Stacks for automated AWS resource deployment in the following Sprints.
