# ADR 003: Microservices architecture with containerization 
Microservice architecture is an excellent approach in building decentralized Spotlight platform for both Candidate onboarding, NPC Service offerings and NPC Networking HUB. As it is a greenfield implementation it brings greater level of decision making. It also solves the people aspect for the engineering teams involved in building the platform. As containerization is the approach it gives greater flexibility in deciding the IT assets to run the platform. Decision making will be quick and allows to gather ideas and react on the constructive feedback very quickly.

## Decision 
We will use the Microservices Architecture in implementing the complete platform and they will be containerized using Kubernetes.

## Rationale 
We will be implementing the Spotlight platform using Microservices architecture as the cell based architecture approach will help us in identifying the boundaries. Each cell which has been identified holds a subdomain will fleet of microservices which are containerized. It holds it owns persistent volume, health monitors, observability etc., Based on the subdomain requirement each microservice will adopt it’s own design. Each microservice will be coarse-grained domain unit.
Industry have evolved so much that we will be getting many open source tools which help to design microservices it’s own design style based on the business domain need.

## Status
Proposed. 

## Consequences
- Microservices will give greater flexibility and it is a distributed architecture. It gives eventual consistency, and all the distributed pieces must be stitched together. Thus fault tolerance, domino effect might be seen during synchronous communication.
- Maintenance: As we have pool of services a standard governance have to imposed for implementation
- Performance is often overhead as the services will do many network calls. To increase performance we have many techniques like caching, replication, graph
