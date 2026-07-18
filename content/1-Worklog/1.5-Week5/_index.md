---
title: "Week 5 Worklog"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

- Complete the Presentation Layer for LingoRise: domain, CDN, and frontend deployment.
- Connect the user interface with the API, Cognito, and the end-to-end authentication flow.
- Validate how AWS services work together with external data services to move closer to the final product.

### Tasks to be implemented this week:

| Day | Task | Start Date | End Date | References |
| --- | --- | --- | --- | --- |
| 2 | Review the `lingorise.xyz` domain, configure Route 53, and verify DNS resolution to the AWS edge. | 18/05/2026 | 18/05/2026 | Route 53 / CloudFront Docs |
| 3 | Check CloudFront and Amplify Hosting to make sure the Next.js frontend is delivered reliably. | 19/05/2026 | 19/05/2026 | AWS Amplify / CloudFront Docs |
| 4 | Integrate the login and registration screens with Amazon Cognito and handle JWT validation on the client side. | 20/05/2026 | 20/05/2026 | Amazon Cognito Docs |
| 5 | Connect the frontend with API Gateway and Lambda, and verify protected requests for Learner/Admin roles. | 21/05/2026 | 21/05/2026 | API Gateway / Lambda Docs |
| 6 | Sync displayed data from S3 and RDS PostgreSQL, and complete the website's end-to-end request flow. | 22/05/2026 | 22/05/2026 | LingoRise Architecture Notes |

### Achievements in Week 5:

- The frontend delivery layer has been confirmed stable through Route 53, CloudFront, and Amplify.
- The web interface can connect to Cognito authentication and call backend APIs successfully.
- I gained a clearer understanding of how the frontend, API, Lambda, S3, and external services work together to form the final LingoRise web product.
