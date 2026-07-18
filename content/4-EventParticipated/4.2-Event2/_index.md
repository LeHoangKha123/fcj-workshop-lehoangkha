---
title: "Event 2"
date: 2026-06-13
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Reflection Report: “AWS First Cloud AI Journey — Career & Culture Sharing at MNCs Seminar”

### Event Objectives

- Aim to bridge the gap between academic theory and the practical corporate environment.
- Provide career guidance through sharing practical experiences regarding career paths and working culture at multinational corporations (MNCs) and fast-growing startups.
- Identify the core skill set and career development mindset in the data and cloud industry.

### List of Speakers

- **Mr. Dat Pham** - Data Analytics Engineer
- **Mr. Cuong Nguyen** - Process Engineer
- **Trong H. Truong** - DevOps Engineer @ Endava Vietnam
- **Danh Hoang Hieu Nghi** - AI Engineer, AWS Community Builder, AWS Student Builder Group Leader
- **Đinh Trung Kiên** - Lead Developer at a startup
- **Nguyễn Minh Thọ** - Student

### Key Highlights

#### Actual Work and Skill Sets in Enterprises
- The role of a data engineer varies flexibly depending on the domain: from designing performance tracking dashboards at startups like Kamereo to optimizing costs and IoT devices at manufacturing corporations like Colgate-Palmolive.
- 4 vital skills: Critical thinking, communication skills, Data Storytelling, and data-driven problem solving.
- The career progression path is divided into 3 milestones: Follower (Executor) -> Learner (Active Learner) -> Problem Solver.

#### The Big Picture of DevOps
- Breaking stereotypical views: DevOps is not just about installing tools or fixing bugs at night, but a core strategy to accelerate software delivery and enhance reliability.
- The actual scope of work is shaped by project size, team structure, and the level of cloud infrastructure automation.
- Mapping the 10 stages of the tool ecosystem: from Plan & Code (Git, Jira), Build & Test (Jenkins), Release & Deploy (Terraform), to Operate (Kubernetes, AWS) and Security/Platform Engineering (SonarQube).

#### AWS Ecosystem Development Roadmap
- The 8-step growth loop: Starting from Student Curiosity, moving to hands-on labs, building a real-world project portfolio, and finally becoming an AWS Partner to share knowledge back with the community (Share Back).
- AWS Student Builder community privileges: Providing a practical environment through AWS Credits and international certification vouchers, helping to reduce cost barriers.

#### URL Shortening System Architecture on AWS
- **Infrastructure**: Leveraging Route 53, CloudFront, and WAF for routing and security; Amplify for the static frontend; and Fargate (ECS) running a Spring Boot API behind an Application Load Balancer.
- **Data processing strategy**: Using DynamoDB as the primary storage, combined with Amazon ElastiCache for Redis to optimize read access speed.
- **Key Generation Service (KGS) Model**: Running a background process to pre-generate unique keys, pushing them into a Redis queue (LPUSH), and extracting them (RPOP) immediately upon request. This method helps prevent write bottlenecks when the system is under high load.

### What I Learned

#### Design Thinking
- **Domain-Driven Design**: Technology and source code only truly deliver value when tightly aligned with the specific context and goals of the business.
- **Problem Solver Mindset**: Clearly recognizing the need to shift from executing tasks based on existing scripts to proactively analyzing business problems, finding root causes, and proposing solutions.
- **Data Storytelling**: Building technical infrastructure is not enough; the core competency also lies in the ability to turn data into meaningful messages to communicate with stakeholders.

#### Technical Architecture
- **Write task optimization strategy**: Deeply understanding the pre-computation model (KGS Pattern) to handle scenarios where the system receives a massive number of concurrent requests.
- **Distributed architecture**: How to combine a durable NoSQL database (DynamoDB) and an in-memory cache (Redis) to achieve maximum performance.
- **IaC (Infrastructure as Code) Ecosystem**: The importance of packaging infrastructure into code to ensure consistency and automation in the deployment lifecycle (CI/CD).

### Application to Work
- **System Architecture**: Applying the philosophy of decoupling heavy tasks into background tasks (like the KGS model) combined with an in-memory queue to eliminate bottlenecks.
- **Automated Deployment**: Integrating resource provisioning automation tools (such as AWS SAM or Terraform) into the operational workflow to standardize the product release process.
- **Database Optimization**: Evaluating and deploying Distributed Caching solutions for processing flows with high read ratios to reduce the load on the primary Database.
- **Quality Management**: Building a culture of transparent project documentation (portfolio) to track technical progress and serve as a baseline for measuring performance.

### Event Experience

Attending the "Career & Culture Sharing at MNCs Seminar" provided a professional, practical perspective on the gap between the academic environment and the strict operational standards at multinational enterprises. Some standout experiences:

#### Acquiring Enterprise-Grade System Design Thinking
- Through the URL Shortening system analysis case study, I clearly understood how services like AWS Fargate, DynamoDB, and Redis interact closely to create a fault-tolerant and infinitely scalable architecture.
- Strongly impressed by the technique of solving the "write bottleneck" problem by pre-generating keys through the KGS Pattern. This is a clear testament to the technical mindset of staying one step ahead to protect the system from the risk of crashing.

#### Positioning Myself on the Technology Map
- The seminar helped systematize the entire DevOps lifecycle into 10 clear stages, thereby accurately identifying current capabilities and the toolsets needed to meet industry standards.
- Deeply realized the need to change my working mindset: not just stopping at the position of a "Learner", but striving to advance to the role of a "Problem Solver", taking responsibility for the final output quality.

#### Key Takeaways
- The core of software development does not lie in the number of technologies used, but in how the solution optimizes costs and performance for the business.
- Accumulating certificates through programs like AWS Student Builder is a solid stepping stone, but the ability to clearly present project architecture (Portfolio) and technical storytelling (Data Storytelling) is the true key to creating a core competitive advantage.
- Automating the deployment pipeline (CI/CD) is no longer an optional add-on, but a mandatory requirement to maintain fast and safe release speeds in modern environments.

> Overall, the seminar not only provided a genuine perspective on the career development path and the DevOps ecosystem but also reshaped my professional mindset: shifting strongly from a passive executor (Follower) to the mentality of a proactive engineer (Problem Solver), ready to design high-load architectures that meet the strict standards of enterprises.