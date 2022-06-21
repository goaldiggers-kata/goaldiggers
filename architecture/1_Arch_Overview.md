# Overview 
To solve the primary business problem our approach was to identify a domain model that reflects the **Spotlight platform vision.** 

We have used **DDD and Bounded Context patterns. Each bounded context will have a fleet of microservice that will have the flexibility of employing different patterns having different responsibilities to solve the Domain problem.**
Proposal is to use **Cell Based Architecture** which gives Spotlight platform to be built as a decentralized cloud native application. **Each Cell represents a Subdomain’s bounded context which can be independently developed, deployed, managed, and will be observable.**

It implies that the Core Subdomains below can have their independent journey. 

- Candidate Onboarding Community.
- Non Profit Community. 
- Candidate and NPC Matching.
- Networking HUB.