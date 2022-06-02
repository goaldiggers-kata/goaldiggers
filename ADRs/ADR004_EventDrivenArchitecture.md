# ADR 004: Event Driven Architecture 
An event is something that has happened in the past. A domain event is, something that happened in the domain that we want other parts of the same subdomain (in-process) or other subdomains to be aware of. The notified subdomain has to react somehow to the events. 

Using domain events, the platform explicitly implements the microservices to consume the side effects of changes within the subdomain or the other subdomain. As DDD is adopted, using Event driven Architecture will give the aggregation of all the facts per business process. 


## Decision
Use Event Driven Architecture for the backend of the system 

## Rationale 
The rationale of the domain events help you to express, explicitly, the domain rules, based in the ubiquitous language provided by the domain experts. Domain events also enable a better separation of concerns among classes within the same domain. As the Spotlight Platform is a distributed application all the domain events will be eventually consistent. Event driven architecture will help in integrating multiple Bounded Contexts, microservices, or even different applications.

## Status
Proposed. 

## Consequences
- The domain events and their side effects (the actions triggered afterwards that are managed by event handlers) should occur almost immediately, usually in-process, and within the same domain. Thus, domain events could be synchronous or asynchronous. Integration events, however, should always be asynchronous. 

- If executing a command related to one aggregate instance requires additional domain rules to be run on one or more additional aggregates, you should design and implement those side effects to be triggered by domain events. The Status Management subdomain will complement.