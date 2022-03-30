---
title: "AWS CCP Study - Domain 1: Cloud Concepts"
layout: single
categories: 
    - Study
tags:
    - AWS
    - CCP
---
# Cloud Concepts
## Define AWS Cloud and its value proposition
### Benefits of AWS cloud
* Security
  * cloud provider takes care of physical security
* Reliability
  * data backup
  * disaster recovery (durability)
    * **recover** from a disaster and prevent the **loss** of data
  * data replication
  * fault tolerance
    * the ability for the service to ensure there is no single point of failure, preventing the chance of failure
    * **fail-over**: have a plan to **shift trafic** to a redundant system in case the primary system fails
      * ex. having a secondary copy of the database which sync the ongoing changes, the secondary is not in-use until a fail over occurs to the primary database
* High Availablity
  * the ability for the service to remain available
  * no single point of failure/or ensure a certain level of performance
  * running the workload across **multiple Availability** Zones on AWS to secure its availability
* Elasticity
  * **automatically** increase or decrease the capacity based on current demand of traffic, memory and computing power
  * horizontal scaling:
    * out: add more servers of the same size
    * in: removing underutilized servers of the same size
  * vertical scaling is generally hard for traditional architecture, so only going to see horizontal described with elasticity
* Agility
* Pay-as-you go Pricing
  * no up-front cost
  * thousands of customers sharing the cost of the resources
* Scalability
  * increase or decrease resources and services based on demand
  * vertical scaling (scaling up): upgrade to a bigger server
  * horizontal scaling (scaling out): add more servers of the same size, which also add availability
* Global Reach
  * launch workloads anywhere in the world, just choose a region
* Economy of scale
### AWS allow users to focus on business value
* shifting technical resources to revenue-generating activities as opposed to managing infrastructure