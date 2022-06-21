# ADR 0008: Geolocation Services Integration

## Decision 

Use a Google Geolocation Services to derive exact location of the NPCs and Candidates. 

## Rationale 

Geolocation Services brings in great flexibility for Mentors and Community Leaders on the Spotlight Platform. It will be used to map the Candidates to the NPOs based on their location. Primarily this ADR will be used by **Candidate and NPC Matching and Networking HUB core domains**.

In addition it brings many advantages in decision making

- Just by persisitng Candidate/NPC city and state doesn't suffice to make decisions. By capturing Geolocation of the both Candidate and NPC the platform will be able to map to the nearest match. Geolocation services will help us  to convert addresses to coordinates to normalize and fill gaps in data for addresses stored in a database table.
- It gives advantage of analyzing from which location most of the NPOs/Candidates are getting mapped.

Networking HUB uses Geolocation Services for all the Activities performed by the NPC on the platform. 

- The HUB recommends nearest NPCs to extend their network
- It will post the event locations offered by the NPC.

## Status
Proposed. 

## Consequences

- Pricing is based on request. As the platform doesn't need all the services we recommend only to use the APIs needed for the platform. 
