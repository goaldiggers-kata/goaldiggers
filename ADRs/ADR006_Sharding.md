# ADR 006: Sharding

Data sharding is dividing data into horizontal partitions that are organized into various Graph instances or servers. This gives us to spread the load across multiple access points based on the Non Profit community activities on the HUB.

These shards can be accessed individually or aggregated to see all of the data based on need. This gives the ability to access in distributed sources in the form of a common graph partitioned on multiple databases.

## Decision 

This domain holds Shard DB Architecture which is very critical to handle the traffic. The proposed architecture is to divide data into horizontal partitions that are organized into various servers. Primarily this decision is amde ba

Data will be siloed into separate instances based on different NPC activities

By Region

By Action

By Service Offerings

By Likes, Events

To minimize the latency

## Rationale 

The rationale behind is seperation based on the NPC activities, as well and placing them is different graph nodes. The fabric database will solely handle all of the load and it has 2 instances active/active it gives greater flexibility is processing.

## Status
Proposed. 

## Consequences

Cost of the infrastructure. Primarily in the initial phases the recommendation will be use on DBMS node hosting all the activities but later based on the spike of user concurrency the investment on the infrastructure can be increased. The initial gives flexibility to expand later based on demand.

