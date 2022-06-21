# ADR 002: DDD and Bounded Context
This ADR plays a key role in the entire implementation of the platform.
- Cell Based Architecture
- Event Driven Architecture
- Microservices 

## Decision 
Design the system by leveraging the Cell Based architecture by overlapping the DDD and Bounded context.
The same is utilized in Event storming sessions and process discovery
There will not be any time limitation for utilizing DDD in the process as it will always play a key role in demarcating of the subdomains.

## Rationale 
This approach is the backbone for the complete platform design.
- A cell forms a bounded context that encapsulates a set of functionality, which may be implemented as a monolith, a set of microservices, serverless functions, or some combination of those.
- Cell-based architecture aims to create business focused architectural constructs that can be reused at a higher level, so naturally organizing the teams and cells around business functions is essential.
- Communication between cells is via well-defined, versioned APIs. For example, using OpenAPI or gRPC/Protobuf. Asynchronous communication between cells is preferred so that cells can continue to work if their dependent cells are unavailable.
- A cell should implement logic and data. At the least, the logic must offer a versioned business API to that data that is independent of the data storage model.
- As it’s a greenfield implementation it will help in defining the clear team boundaries, the organization growth will reflect the actual Architectural representation.
## Status
Proposed. 

## Consequences
- High Cost of Ownership
- DDD projects require domain experts that are often expensive to hire, since they hold valuable knowledge. Moreover DDD requires strong skills on the modeler side. In particular they have to be:
  - Humble, since they have to accept their ignorance and learn from an expert
  - Really skilled in OOP
  - Diligent, since they have to track decisions
  - Communicative, since they have to explain the domain to the other devs (even through documentation)
