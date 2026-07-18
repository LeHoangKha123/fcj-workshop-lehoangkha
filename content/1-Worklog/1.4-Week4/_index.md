---
title: "Week 4 Worklog"
date: 2026-05-11
weight: 4
chapter: false
pre: "  1.4.  "
---

### Week 4 Objectives:

- Build the core Compute Layer with AWS Lambda and Express.js (serverless-http).
- Complete the overall view of LingoRise's Serverless architecture, from frontend to backend resources.

### Tasks to be implemented this week:

| Day | Task | Start Date | End Date | References |
| --- | --- | --- | --- | --- |
| Mon | Wrap Express backend with serverless-http wrapper.<br>Integrate middleware to validate Cognito JWT tokens inside Express routes. | 11/05/2026 | 11/05/2026 | serverless-http Docs |
| Tue - Thu | Research AWS SAM (Serverless Application Model) and CloudFormation.<br>Write the unified <code>template.yaml</code> file, define Lambda resources, and troubleshoot CloudFormation stack creation errors. | 12/05/2026 | 14/05/2026 | AWS SAM / CloudFormation Docs |
| Fri | Configure secure SSM Parameter Store environment variables (SecureString) for Lambda.<br>Deploy the backend stack to AWS Lambda using AWS SAM CLI and verify logs. | 15/05/2026 | 15/05/2026 | AWS SAM CLI Docs |

### LingoRise Architecture Investigated This Week

- **Presentation Layer**: Users access the domain via Route 53, CloudFront distributes assets, and AWS Amplify Hosting serves the Next.js frontend.
- **API Layer**: The frontend calls API Gateway using the REST proxy model to forward requests to Lambda.
- **Compute Layer**: AWS Lambda runs Express.js via `serverless-http`, processing registration and authentication logic.
- **Identity Layer**: Lambda validates JWTs from Amazon Cognito before allowing admin/user operations.
- **Data Layer**: Lambda reads/writes S3 to store assets/draft files and uses RDS PostgreSQL for primary business data.
- **Monitoring Layer**: CloudWatch is used to log and track system activities.
- **External Services**: RDS PostgreSQL, S3, VNPay Gateway, and LLM Provider are integrated as external services to complete the end-to-end flow.

### Achievements in Week 4:

- Core Lambda functions deployed successfully using AWS SAM.
- Spent significant time researching the structure of `template.yaml` and resolving CloudFormation deployment/permission errors.
- Express API is now capable of parsing requests and validating Cognito JWTs on AWS.
- Gained a solid understanding of the end-to-end request flow across API Gateway, Lambda, Cognito, S3, and database services.
