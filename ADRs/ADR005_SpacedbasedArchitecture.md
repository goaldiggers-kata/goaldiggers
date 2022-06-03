# ADR 005:Spaced Based Architecture

In any high volume Domains will a large concurrent user loads Space Based Architecture style specifically addresses and gives high scalability, elasticity and solve high concurrency issues. Especially Networking HUB core Subdomain has unpredictable concurrent NPC user volume and the plan is to extend this subdomain for even candidates just to view the activities provided by the NPCs in their geo locations.

## Decision 

We will be using Space based Architecture as this domain demands Elasticity, Performance, Reliability and Scalability. These are the driving attributes and main advantages of this architecture style. This architecture style removes the Database constraint. Additionally to compliment this proposal we will be using Graph DB and it will be sharded.

## Status
Proposed. 

## Consequences

Cost is the primary factor but the cloud platform will be used in such a way that based on the need and demand the services will scale up and down.
Testing strategy will have to be clearly designed as the environment complexity is more. It’s real difficult to create the simulation environment.
