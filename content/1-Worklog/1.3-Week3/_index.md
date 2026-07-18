---
title: "Week 3 Worklog"
date: 2026-05-04
weight: 3
chapter: false
pre: "  1.3.  "
---

### Week 3 Objectives:

- Set up and connect to services outside of AWS (External Services).
- Ensure Lambda can interact with the database and cache.

### Tasks to be implemented this week:

| Day | Task | Start Date | End Date | References |
| --- | --- | --- | --- | --- |
| Mon | Initialize Amazon RDS for PostgreSQL 16 project as the primary datastore.<br>Configure pg pool for connection. | 04/05/2026 | 04/05/2026 | RDS PostgreSQL Docs |
| Tue | Design basic tables for LingoRise (Users, Courses, MockTests). | 05/05/2026 | 05/05/2026 | LingoRise Docs |
| Wed | Integrate AWS SDK and configure local environment / dotenv for Node.js backend. | 06/05/2026 | 06/05/2026 | AWS SDK / dotenv Docs |
| Thu | Install Database (pg, pg-pool) connection libraries into the local Node.js 20 project. | 07/05/2026 | 07/05/2026 | npm Docs |
| Fri | Write and successfully test connection scripts from local to RDS PostgreSQL. | 08/05/2026 | 08/05/2026 | Node.js Docs |

### Achievements in Week 3:

- Completed the Data Layer environment outside of AWS.
- Local code can successfully query SQL and query from RDS PostgreSQL database.
