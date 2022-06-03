# ADR 0009: Streams

The architecture proposal behind building the Spotlight platform is distributed and decentralized. In order to bridge the communicaton across all the identified subdomains streaming is platform which will be used.

All the subdomains will push or get notified with their domain or integration events. The business processes will be subscribed to these stream and get reacted based on the event it receives. Stream primary provide
 
-- Effectively store streams of records in the order in which records were generated

-- Publish and subscribe to streams of records

-- Real time processing

## Decision 

The proposal is to use Kafka to process the streams and allows us to build the workflow with reliability. It will be used to move the data from one subdomain to another and the microservices within the subdomain will subscribe and start publish the domain facts.

## Rationale 

Stream meets the platform requirements and as it also addresses the problem statments. That's the primary reason behind opting the Stream processing.

All the Domain and Integration Events will be publish a stream of events and the subscribed microservices will react. In addition Streams API will also enable domains to behave as stream processors which take input from topics. This approach will be adopted in Networking HUB. All the Activities which the NPC do on the platform will posted into unique topics and unique activity services react to them to post back the notifications and recommendations.


## Status
Proposed. 

## Consequences

It requires to build a complex pipeline of interactions between producers and consumers and then maintain the entire platform. This requires substantial work and effort and adds complexity. As part of the intial process discovery meetings and domain context map has to defined. 

