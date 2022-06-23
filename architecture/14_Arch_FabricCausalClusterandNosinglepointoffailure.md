< [Home](../README.md) | [Previous](./13_Arch_NPCRecommendationEngine.md) >

# Multi Cluster Deployment

**Neo4J Fabric** is the solution for graph sharding which allows the NPCs to break the graphs based on the relationships. It allows to store smaller graphs and store them in separate databases. The proposed architecture is multi cluster deployment with no single point of failure. 

<p align="center">
  <img src="..//Images/FabricCausalClusterandNosinglepointoffailure.png" />
</p>

- Architecture proposed is separating the data stores into shards and placing them based on the activity into separate graph DBs. 
- This gives flexibility any combination of inhouse or cloud to fit the business needs and requirements. 
- The above architecture representation has 2 coordinated shards which will give us always high availability and We have separated the fabric database to solely handle all of the load and processing of requests.

## Data Division
- As part of the analysis the context and the data definitions will be clearly defined and how the data has to be modeled so that we can have subgraphs.
- All the shards will be divided based on the NPC activities.

< [Home](../README.md) | [Previous](./13_Arch_NPCRecommendationEngine.md) >
