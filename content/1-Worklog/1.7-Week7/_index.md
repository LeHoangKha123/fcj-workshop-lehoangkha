---
title: "Week 7 Worklog"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 7. </b> "
---

### Week 7 Objectives:

- Integrate text-to-speech (TTS) features for listening exams.
- Optimize database connection performance and system permissions.

### Tasks to be implemented this week:

| Day | Task | Start Date | End Date | References |
| --- | --- | --- | --- | --- |
| Mon | Review Lambda IAM Roles, refine S3 access, Cognito policies, and Edge-TTS permissions adhering to the Least Privilege principle. | 01/06/2026 | 01/06/2026 | AWS IAM Docs |
| Tue - Thu | Research and build the Edge-TTS Python bridge on AWS Lambda.<br>Resolve Lambda package size limits, temporary directory write constraints (/tmp), and optimize processing latency. | 02/06/2026 | 04/06/2026 | Edge-TTS / Python Bridge Docs |
| Fri | Optimize advanced SQL queries on RDS PostgreSQL and configure connection pooling to prevent Lambda container exhaustion. | 05/06/2026 | 05/06/2026 | RDS PostgreSQL Docs |

### Achievements in Week 7:

- Successfully integrated the natural-sounding text-to-speech (Edge-TTS) feature, automating the listening exam content creation.
- Solved the challenge of running Python sub-processes on Lambda (handling read-only filesystem limits and packaging constraints).
- Database connection pools and RDS PostgreSQL queries are now highly stable, preventing connection leaks.
