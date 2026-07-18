---
title: "Event 3"
date: 2026-06-20
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Reflection Report: “Event: Cloud Architect - Game Show”

### Event Objectives

- Consolidate foundational knowledge of cloud services (AWS) and system architecture design patterns.
- Practice situational analysis thinking, breaking down business requirements to choose optimal technology solutions under time pressure.
- Enhance teamwork, strategic communication, and risk management skills in a competitive head-to-head environment.

### Organizers & Participants

- **Organizer** - AWS Study Group
- **Players** - 8 competing teams (each team consists of 5 members randomly selected after the registration round)
- **Role** - Contestant

### Key Highlights

#### Head-to-Head Competition Format
- 8 teams were divided into pairs for a knockout tournament. Teams took turns answering case study questions of increasing difficulty.
- The team that accumulated more points advanced to the next round. 
- **Tie-breaker Rule**: If the question set ended in a tie, "Question 11" (Sudden Death) was deployed. The team that rang the bell and provided the correct answer faster instantly won.

#### Professional Focus: AWS Service Selection
- The questions were not heavy on pure theory but placed players in real-world contexts. For example: "The system is bottlenecking while processing Black Friday orders, requiring decoupled microservices without losing data. Should we use AWS SQS or Amazon Kinesis?".
- It required contestants to thoroughly understand the limits, characteristics, and pricing models of each AWS service to make the most accurate architectural decisions.

#### Risk Management Strategy via Skill Cards
- **Minimum Risk (1 use/match)**: A defensive skill. Used for questions where the team was unsure or had many uncertain assumptions. If the answer was wrong, the score was protected (no deduction). If correct, the team received 1/2 the points for that question.
- **Star of Hope (1 use/match)**: An offensive skill (High risk, High reward). Activated when the team had thoroughly analyzed the problem and was 100% confident in the answer. A correct answer doubled the points (x2), while a wrong answer deducted the corresponding points (x2).

### What I Learned

#### System Design Thinking
- **No guessing, no hiding ambiguity**: The game show context proved that rushing to choose an AWS service just because it "sounds familiar" often leads to lost points. Architectural thinking requires exposing all trade-offs and closely following the original requirements of the prompt.
- **Simplicity and Goal-Oriented**: Designing architecture is like writing code: the best solution is the simplest one that correctly meets the need. Do not over-engineer with complex services if the problem only requires static storage (S3) instead of an expensive file system (EFS).

#### Technical Architecture
- Strongly reinforced the ability to differentiate the use-cases of similar AWS services (e.g., when to use DynamoDB vs. RDS, ALB vs. NLB, CloudFront vs. Global Accelerator).
- Clear awareness of "anti-patterns" in Cloud design, especially design flaws that cause budget deficits or create a "single point of failure".

#### Strategy & Teamwork
- **Surgical communication**: Short discussion times required members to communicate directly, bypassing general opinions and getting straight to verifying the feasibility of each AWS service.
- **Risk management**: Learned how to assess the reliability of the reasoning flow before deciding to "cash in" with the *Star of Hope* card or step back safely with the *Minimum Risk* card.

### Application to Work
- **Building test-cases for architecture**: Applying the competitive mindset to actual work: before deciding to integrate any AWS service into a project, clearly list the verification criteria (load requirements, cost, latency) just like solving case studies in the game.
- **Problem-solving planning**: When facing complex tasks or system bugs, always adhere to the principle of situational breakdown. Divide the problem into short, clear verification steps rather than offering intuitive or emotional solutions.

### Event Experience

Participating in the **Cloud Architect Game Show** provided a completely different perspective compared to one-way seminars. This is where architectural design thinking is put to a practical test under time pressure. 

#### Alignment with Programming Philosophy
The most interesting aspect of the event was that it accurately reflected the working philosophy I always pursue: "Caution is always more important than Speed." Faced with a tough architectural question, the urge to ring the bell quickly was immense. However, our team agreed on a strict principle: absolutely no answers based on vague guesses. Every selection decision (e.g., choosing Lambda over EC2) had to be based on clear assumptions extracted from the prompt's own verbal "traps". 

#### Team Coordination and Decision Making
Working with 5 other team members was a fantastic communication experience. Arguing to eliminate wrong answers was intense but extremely logical. The most memorable moment was when the team decided to activate *Minimum Risk* for a complex network load distribution question, and used the *Star of Hope* at the exact right time for a familiar decoupling design scenario, thereby turning the tables.

#### Key Takeaways
- Understanding a service inside out (its nature, strengths, weaknesses) is far more important than knowing the names of dozens of different services. 
- In system architecture as well as in programming, every decision to change or integrate technology must be clearly verifiable. Do not arbitrarily apply complex architectural patterns if a minimal solution can fully solve the problem.

#### Event Photos
![Event Photo](/images/Event3/1.JPG)

![Event Photo](/images/Event3/2.JPG)

![Event Photo](/images/Event3/3.JPG)

> Overall, the event was not just an entertaining game but a sharp practical test. It reinforced my belief in goal-oriented working principles, prioritizing accuracy and cautious analytical thinking when dealing with any cloud system.