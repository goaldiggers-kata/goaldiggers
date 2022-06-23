<- [Home](../README.md) 

# Deployment View

We will be adopting **Scale Cube model**. This model will be adopted from the discovery phase to deployment. **Based on the business expansion the capacity planning of the infrastructure can be planned. It gives a very cost effective approach**.

This model helps to make all the stakeholders to talk **ubiquitous language**, because of which the scale related explicit requirements can be discussed in the initial phase of the architectural discussions. 

In the below representation we have 3 dimensions but we will be adopting **2 Y and Z Axis**. **Y Axis** allows to split dissimilar things and **Z-axis** allows segmentation of “similar” things. 

- **Y-Axis:** Domain Driven Design, Bounded Context and Cell Architecture has already made the Spotlight Platform to get decomposed and segmented. This allowed us to deploy all our Domain Services, Framework, Supporting Services etc., as microservices.

    -  This Axis focuses on separating services and data. All the splits will be dissimilar from each other. In the Spotlight platform, consider the example of Candidate Assessment. There will be 2 Supporting Subdomains 
    -  Candidate Metrics Management : This domain holds all the services which allow the mentor to feed the primary data required to assess the candidate.  
    -  Candidate Roadmap Tracker:  This domain holds all Roadmap which the mentor has created for the candidate to achieve their career goals. In order to assess the   candidate progress this subdomain interacts with Candidate Metrics Management Services and capture the progression for a specific goal. 

    - **This approach allows**
       - Segmentation of Teams
       - Improved Organization scalability 
       - Fault Isolation etc.,

- **Z-Axis:** Networking HUB core subdomain on the spotlight platform which gives capability for NPC to expand their network. The implicit characteristic is needed for HUB to be highly scalable. It also helps us to Shard the data. 
  - Examples are already defined in the Non Profit Community Networking HUB and the Shards will be 
   - By Region
   - Action
   - By Service Offerings
   - By Likes
   - Events
    - To minimize the latency

![Spotlight Context Diagram](..//Images/ScaleCube.PNG)

<- [Home](../README.md) 
