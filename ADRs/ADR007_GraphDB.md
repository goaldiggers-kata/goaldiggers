< [Home](../README.md) | [Previous](./ADR006_Sharding.md) | [Next](./ADR008_GeoServicesIntegration.md) >
# ADR 007: GraphDB
- The architecture behind is designed for optimal management, storage, traversal of nodes and relationships as NPC Service Offerings have to be reached to the maximum onboarded candidates. 
- Graph DB gives the relationships and the primary problem statement how to bridge both the NPC and the candidates.
- Neo4J will be used as the Graph database.

## Decision 

- GraphDB is beyond DB and more of an approach to structure the information between NPCs, Candidates, Program Offerings, Service Offerings. 
- All these are expected to change based on the NPC Roadmap planning and Candidate Aspirations. 
- As the datasets are continously evolving and it requires efficient processing of many to many relationships, hence Graph DB is considered to be the preferred option.
- It brings in greater flexibily and quick decision making

NPC and Candidate Matching

- On the Network HUB Core subdomain as it's all networking and build relationships across NPCs Graph DB gives greater flexibility and it can give the best recommendation engine. 

## Rationale 

The Graph DB is built to handle the highly connected data. The intent is to have value objects created based on the relationships derived during the runtime.

## Status
Proposed. 

## Consequences
- **Advantages**
  -  Improved Object oriented thinking: Explicit semantics for each query that has been written. There will not be any hidden assumptions that might exist in in relational SQL
  -  Performance: Graph DB provides superior performance for querying related data either big or small. The performance is consistent since the traversing a given vertex neighbor nodes via edges are independent of the graph size.
  -  Flexible Online Schema Environment: Graph databases offer a flexible online schema evolvement while serving the query. New vertex can be added or dropped while the existing queries are still working.
- **Disadvantages**
  - It's niche skill and needs training.

< [Home](../README.md) | [Previous](./ADR006_Sharding.md) | [Next](./ADR008_GeoServicesIntegration.md) >
