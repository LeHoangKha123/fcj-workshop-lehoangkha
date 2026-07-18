---
title: "Week 2 Worklog"
date: 2026-04-27
weight: 2
chapter: false
pre: "  1.2.  "
---

### Week 2 Objectives:

- Initialize foundational security resources (Identity Layer) and storage (Data Layer).
- Configure IAM Role permissions adhering to the Principle of Least Privilege.

### Tasks to be implemented this week:

| Day | Task | Start Date | End Date | References |
| --- | --- | --- | --- | --- |
| Mon - Wed | Research documentation and initialize Amazon Cognito User Pool for Learners and Admins.<br>Configure App Client, customize JWT tokens, and set up User Groups. | 27/04/2026 | 29/04/2026 | AWS Documentation (Cognito) |
| Thu | Create Amazon S3 buckets to store question assets and import drafts.<br>Set up CORS and block public access for S3 Buckets. | 30/04/2026 | 30/04/2026 | AWS Documentation (S3) |
| Fri | Write policies and initialize a specific IAM Role (Scoped Role) for AWS Lambda.<br>Attach S3 access and Cognito Admin operations permissions to the IAM Role. | 01/05/2026 | 01/05/2026 | AWS Documentation (IAM) |

### Achievements in Week 2:

- Cognito User Pool is ready for user management and JWT issuance (spent the most time researching secure configuration).
- S3 buckets are properly secured for hosting question assets.
- Lambda Execution Role was created with strictly limited permissions (Least Privilege) ensuring system safety.
