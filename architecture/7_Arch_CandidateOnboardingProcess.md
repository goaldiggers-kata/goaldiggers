< [Home](../README.md) | [Previous](./6_Arch_CandidateRegistration.md) | [Next](./8_Arch_CandidateRoadmapTracker.md) >

# Candidate Onboarding Process:

- Candidate and Mentor both are primary actors for the candidate onboarding process.
- Candidate has an intake and waiting for the Mentor to onboard him/her onto the platform.
- As part of the registration the candidate has just raised the request for Non Profit Community offerings and got the Intake ID assigned.
- Once the candidate gets onboarded completely, mentor will assign him the NPC based on the assessment results.
- The below representation shows the high level steps which both the candidate and mentor have to undergo in order to complete the onboarding process. 
- **Every milestone of the Candidate Onboarding process has been captured in the Status Management tile**.

## Prerequisite: 
  - Candidate Intake ID Assigned.

## Process Discovery:

- The onboarding process gets initiated once the candidate completes the registration process.
  <p align="center">
  <img src="..//Images/CandidateOnboardingProcess.png" />
</p>
  
<br />

## Output:
- Mentor Assigned.
- Non Profit Community Assigned and Program assigned.
- Candidate and Mentor initial Meeting is complete
- Roadmap Created

## Subdomain and Bounded Context:

Below are the **Core, Generic and Supporting Subdomains** which get involved for the candidate onboarding process.

- **Core Subdomain:** Candidate NPC Matching
- **Supporting Subdomain:** Candidate Roadmap Tracker
- **Generic Subdomains:** Platform Services, Status Manager, Notification Services

## Candidate Registration Context view and bounded context 

<p align="center">
  <img src="..//Images/CandidateRegistrationContextviewandboundedcontext.png" />
</p>
<br />

## Candidate Registration Sequence Diagram

<p align="center">
  <img src="..//Images/CandidateRegistrationSequenceDiagram.png" />
</p>
 
## Key Patterns and ADRs identified for the Candidate Onboarding process
- [BFF](../ADRs/ADR012_BFF.md)
- [CQRS](../ADRs/ADR013_CQRS.md)

< [Home](../README.md) | [Previous](./6_Arch_CandidateRegistration.md) | [Next](./8_Arch_CandidateRoadmapTracker.md) >
