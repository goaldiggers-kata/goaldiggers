# ADR 001: Cell Based Architecture
Diversity Cyber council is a non profit organization and doesn’t have a sizeable team. So the overarching Architecture style should be simple, create, evolve and maintain. The development team can start creating the cell as they are confined to subdomain with a bounded context. They can evolve the domain based on the business priorities. Each cell will have all 
the essential components to be built so that it can support the over goal of the Spotlight platform.

## Decision
We will use the Cell Based Architecture for designing the complete platform as it will help us to align to the Subdomains and Bounded contexts identified as part of the process discovery and event storming sessions. 

## Rationale
Cell Based Architectural approach offers forward looking view for the Spotlight platform to address the emerging challenges. The primary goal of this architecture is to bring great agility to respond effectively and address the need of the business needs in a short time. Agile doesn’t just mean one time change, it’s ongoing. As each cell is defined as a Core Subdomain, Generic Subdomain or Supporting Subdomain of the Spotlight Platform the repeatable adaption to meet the challenges of the business needs will be easy as the following properties can easily be embedded into the platform.
The architectural approach helps and brings in great flexibility to design the Microservices architecture and allow us to abide to the decisions based during the process discovery sessions.
Scalability: It gives an ability to deal with changing workloads by utilizing available resources. Modern Cloud infrastructure will allows to design the components, containers to be scales based on the need.
Modularity: Gives us the flexibility for versioning, well defined interfaces. Primary goal is to mirror with Domain Driven Design. Cell based Architecture lays a foundation and each cell represents the subdomain and allows to define the 
 modularity at a macro level.

- Deployment: Siloed Approach
- Evolutionary: to do
- Fault Tolerance: to do
- Testability: Each cell can be tested independently as it as clear Bounded Context defined.


## Status
Proposed. 

## Consequences
- A cell forms a bounded context that encapsulated a set of functionalities, which may be implemented as set of microservices, serverless functions, or some combination of those.
- Cell Architecture gives great flexibility for the teams to work in siloed mode. Each subdomain will may evolve on its own so it is mandate to mandate to design guidelines, well defined - CI/CD pipeline which acts as a stage gate for all the implementation milestones.
It should have clear representation Architectural representation.
