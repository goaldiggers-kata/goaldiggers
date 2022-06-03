# Deployment View

We will be adopting **Scale Cube model**. This model will be adopted from the discovery phase to deployment. **Based on the business expansion the capacity planning of the infrastructure can be planned. It gives a very cost effective approach.**

This model helps to make all the stakeholders to talk **ubiquitous language**, by having this consistentency the scale related explicit requirements can be discussed in the initial phase of the architectural discussions. 

In the below representation we have 3 dimensions but we will be adopting **2 Y and Z Axis.**

- **Y-Axis:** Domain Driven Design, Bounded Context and Cell Architecture has already made the Spotlight Platform to get decomposed and segmented. This allowed us to deploy all our Domain Services, Framework, Supporting Services etc., to get deployed as microservices.

-  This Axis focuses on separating services and data. All the splits will be dissimilar from each other. In the Spotlight platform if we take the example of Candidate Assessment we have 2 Supporting Subdomains Candidate Metrics Management and Candidate Roadmap Tracker.
    - Candidate Metrics Management: This domain holds all the services which allow the mentor to feed the primary data to assessing the candidate.
    -	Candidate Roadmap Tracker: This domain holds all Roadmap which the mentor has created for the candidate to achieve this career goals. In order to assess the  Candidate progress this subdomain interacts with Candidate metrics Management services and capture the milestone goal progress. 

**This approach allows**

- Segmentation of Teams
- Organization scalability will increase
- Fault Isolation and many more

**Z-Axis:** Networking HUB subdomain on the spotlight platfomr gives capability of NPC to network. The implicit characteristic is this HUB to make the scalable. 

- Z Axis helps us to Shard the data. 
- Y axis allows to split dissimilar things and Z-axis allows segmentation of “similar” things. Examples are already defined in the Non Profit Community Networking HUB and the Shards will be 

    - By Region
    - Action
    - By Service Offerings
    - By Likes
    - Events
    - To minimize the latency

![Spotlight Context Diagram](..//Images/ScaleCube.PNG)
