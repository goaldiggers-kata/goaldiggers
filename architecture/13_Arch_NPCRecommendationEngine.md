< [Home](../README.md) | [Previous](./12_Arch_NPCActivityTrackeronNPCNetworkHUB.md) | [Next](./14_Arch_FabricCausalClusterandNosinglepointoffailure.md) >

# HUB Recommendation Engine: 
It is core service which sends notifications, recommendations, matching requests and customizes the user content on the page. It’s a background thread gets domain events all the services.
- Every Activity which the user does on the Network HUB it forwards the request to the Shard Indexer service.
- Shard Indexer service exposes an API
- Once the API is invoked it determines which shard to be queried based on the activity done by the user.
- Indexer queries all the sharded graphs to fetch the list based on the activity search and return the list to the Recommendation Engine. 
- Engine applies to filter on the list bases on the NPC Preferences and returns final list.
- Recommendation Engine also pulls data from NPC Roadmap Tracker subdomain.


## NPC Recommendation Engine
![NPC Recommendation Engine](..//Images/NPCRecommendationEngine.png) 

## Shard Indexer: This service provides the data from the Shard Graph DB. 

- This process will have two different set of services
- One pool of services which will keep helping the 
  - **NPC Match Notification Service:** For provide the match notifications
  - **Match NPCs:** For providing match recommendations.  
- For reads, the Indexer service implements queries independently
- For each reading activity we will have a separate instance and whereas for the transactional area we will have separate service. This implementation is primarily because the demands for the queries are drastically different. 
- This domain holds **Shard DB Architecture** which is very critical to handle the traffic. The proposed architecture is to divide data into horizontal partitions that are organized into various servers. Primary reasons to shard
- Data will be siloed into separate instances based on different NPC activities
  - By Region
  - Action  	
  - By Service Offerings
  - By Likes
  - Events
  - To minimize the latency
  
**Neo4J Fabric** is the solution for graph sharding which allows the NPCs to break the graphs based on the relationships. It allows to store smaller graphs and store them in separate databases.

< [Home](../README.md) | [Previous](./12_Arch_NPCActivityTrackeronNPCNetworkHUB.md) | [Next](./14_Arch_FabricCausalClusterandNosinglepointoffailure.md) >
