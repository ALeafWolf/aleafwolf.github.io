---
title: "AWS CCP Study Note"
layout: single
categories: 
    - Study
tags:
    - AWS
    - CCP
---
www.exampro.co/clf-c01
# Cloud Concepts
## Cloud Service Provider (CSP)
* the company which provides multiple cloud services
* cloud services can be **chained together** to create cloud architecture
* cloud services are accessible via **Single Unified API**
* cloud services are **metered billing** based on usage
* rich monitoring built in
* have an infrastructure as a Service (IaaS) offering
### Landscape
* T1: AWS, Azure, Google Cloud Platform (GCP), Alibaba Cloud
* T2: IBM Cloud, Oracle Cloud, Rackspace (OpenStack)
* T3: Vultr, Digital Ocean, Linode
### Common Cloud Service
* AWS has over **200+** cloud services
* The term "cloud computing" refer to all categories of cloud services
#### Four Core
* Compute: virtual computer for running application, programs and code
* Networking: virtual network that define internet connections or network isolation between services or outbound to the internet
  * ex. VPC Private Cloud Network
* Storage: virtual hard-drive that store files
* Databases: virtual database that storing reporting data or a database for general purpose web-application
 
## Evolution of Computing
### Dedicated
* a physical server wholly utilized by a single customer
* will overpay for an underutilized server
* cannot vertical scale, need a manual migration
* replacing server is very difficult
* limited by the host OS
* multiple apps might conflict in resource sharing
* it's **guarantee of security, privacy, and full utility of underlying resources**
### VMs
* can run **multiple Virtual Machines on one machine**
* **Hypervisor** is the software layer for running VMs
* pay for a fraction of the server
* will overpay for an underutilized Virtual Machine
* limited by the guest OS
* multiple apps on a single VM can result in conflicts in resource sharing
* easy to export or import images for migration
* easy to vertical of horizontally scale
### Containers
* VM running multiple containers
* **Docker Deamon** is the layer allow to run multiple containers
* containers share the same underlaying OS so they are more efficient than multiple VMs
* multiple apps can run side by side without being limited to the same OS requirements and will not cause conflicts during resource sharing
### Functions
* are managed VMs running managed containers
* known as **Serverless Compute**
* user upload the code, choose the amount of memory and duration
* very cost-effective, only pay for the time code is running, VMs only run when there is code to be executed
* **cold starts** is a side-effect of this startup

## Types of Cloud computing
### Software as a Service (SaaS)
* for customers
* a product is run and managed by the service provider
* ex. salesforce, office365, gmail
### Platform as a Service (PaaS)
* for developers
* Focus on the deployment and management of the apps
* ex. Heroku, Google App Engine
### Infrastructure as a Service (IaaS)
* for admins
* the basic building blocks for cloud IT. 
* provide access to networking features, computers, and data storage space
* ex. aws, Azure
  
## Cloud Computing Deployment Models
### Public Cloud
* **everything** is built on the CSP
* is known as Cloud-Native or Cloud First
* used by start up company, or small enough to make the leap from VPS to CSP
  * ex. Dropbox, Workspace
### Private Cloud
* everything built on company's datacenters
* also known as **On-Premise**
* the cloud could be OpenStack
* organization that cannot run on cloud due to strict regulatory compliance or the sheer size of their organizaiton
  * ex. public sector like government, super sensitive data like hospitals, large enterprice with heavy regulation like Insurance Companies
### Hybrid
* use both **On-Premise** and CSP
* used by the company started with their own datacenter, cannot fully move to cloud due to effort of migration or security compliance
  * ex. banks, FinTech, large prefessional service providers, lagacy on-premise
### Cross-Cloud
* using multiple CSP
* not same as hybrid


# The Benefits of Cloud
* 