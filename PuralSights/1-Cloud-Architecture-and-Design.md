# CompTIA Cloud +

# Domain 1: Cloud Architecture and Design

## Cloud Characteristics

A cloud solution typically uses virtualization solutions but virtualization solution is not automatically a cloud solution.

Cloud defined by NIST (National Institute of Standards and Technology) in Pub. 800-145 
(The NIST Definition of Cloud Computing)[https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-145.pdf]
This definition includes:
- On-demand self-service
- Broad network access
- Resource Pooling
- Rapid elasticity
- Measured service

**On-demand Self-service** -  

    Must be provisionable without human interaction

**Broad network access** - 

    Reachability using standard mechanism (Internet)

    Accessibility depends on deployment model

    Ubiquitous  

**Resource pooling** -

    Hardware resources pooled

    Customers don't know specific location

    Do know general location

**Rapid Elasticity** - 

    Ability to scale up and down
    
    Automatic scaling supported
    
    Cloud resources should appear unlimited

**Measured Service** -

    Offered pay-per-use/charge-per-use:

        - Processor use

        - Memory amount

        - Network speed


## Cloud Deployment Models

Defined by NIST:

- Private cloud
- Community Cloud
- Public Cloud
- Hybrid Cloud

**Private Cloud**

    Developed for single organization

    Often an evolution of data center

    Doesn't need to be hosted by organization

**Community Cloud**

    Used by a community to meet industry regulations in cloud

    i.e. Scientific organizations and educational institutions

    Considered multitentent

**Public Cloud**

    Solutions offered to the public

    i.e. Microsoft Azure, Amazon Web Services (AWS), and Google Cloud
    
    Considered to be multitentent

**Hybrid Cloud**

    Includes multiple deployment models

    Most common inclue public-private cloud
    
    Common example is cloud bursting

Other terms used in reference to cloud:

**Multi-Cloud**

    Often linked with hybrid cloud offerings; Similar but different

    Uses two or more cloud offerings and use the same deployment model

    Pros:

    Multi-cloud is helpful as multiple providers don't often fail together

    Take advantage of best solution from each provider i.e. Azure for authentication with Entra ID and AWS for storage within S3

**Virtual Private Cloud (VPC)**

    Provides private network inside the cloud

    May give reason to not use multi-cloud but also may be able to 
    
    peer VPCs to bridge provider's solutions

## Cloud Service Models

Defined by NIST
- Infrastructure as a Service (IaaS)
- Platform as a Service (PaaS)
- Software as a Service (SaaS)

The network layers of cloud in the shared responsibility model:

- People
- Data
- Applications
- Runtime
- Middleware
- OS
- Virtual Network
- Virtualization
- Servers
- Storage
- Networking

**Infrastructure-as-a-Service (IaaS)**

    Cloud provider manages virtualization, servers, storage, and networking

    User manages virtual network, OS, Middleware, Runtime, Applications, Data, and People

    i.e. Amazon EC2, Azure Virtual Machines, and Google Computer Engine

**Platform-as-a-Service (PaaS)**

    Cloud provider manages everything up to Runtime

    User manages applications, data, and people

    i.e. Amazon Elastic Beanstalk, Azure Web Apps, and Google App Engine

**Software-as-a-Service (SaaS)**

    Cloud manages most of it

    Users manage data and people
    
    i.e. Dropbox, Microsoft Office 365

Service Types Change

- Main three have been around since cloud birth
- Nothing stops evolving in tech
- Time has given us four other models

**Kubernetes-as-a-Service (K8SaaS)**

    Cloud provider manages up to OS (control plane)

    Users manage middleware and up (data plane)

    i.e. Amazon Elastic Kubernetes Service (EKS), Amazon Kubernetes Service (AKS), and Google Kubernetes Engine (GKE)

**Container-as-a-Service (CaaS)**

    More controlled by provider than K8SaaS with provider managing up to middleware (control and data planes)

    Users bring the containers only

    i.e. AWS Fargate, Azure Container Instances (ACI), and Google CloudRun

**Function-as-a-Service (FaaS)**

    User brings logic (code) and functional layers and cloud provider does the rest

    i.e. AWS Lambda, Azure Functions, and Google Cloud Functions

**NoCode as a Service (NoCodeaaS)**

    Customer does no coding but set specifications for a solution to configure it
    
    Cloud Provider does the rest

    i.e. AWS Honeycode, Azure Power Apps, and Google AppSheet

Next Generation PaaS

- Some overlap with traditional models
- FaaS/NoCodeaaS = PaaS
- Other options fill out model definitions

More targeted cloud offerings:

**Communications-as-a-Service (CaaS)**

    Allows outsourcing of communication systems

    Includes:
        
        - VOIP
        - Instant messaging
        - Collaboration
        - Voice mail
        - Video conferencing
        - Presence


**Desktop-as-a-Service (DaaS)**

    Cloud virtual desktop

    Extends globally

**Database-as-a-Service (DBaaS)**

    Database management is outsourced to cloud provider
    
    User handles structure and data


## Cloud Actors

Cloud actors are entities involved with the solution and is defined by NIST 100-292

Cloud Actors:
- Cloud consumer
- Cloud provider
- Cloud auditor
- Cloud broker
- Cloud carrier

**Cloud consumer**

    Person or organization who consumes service
    
    Business has relationship with provider

**Cloud provider**

    Provides cloud service and its availability


**Cloud auditor**

    Person or organization assesssing services

    Can include: 

        - System operations
        - Cloud performance
        - Cloud security

**Cloud broker**

    Manages use, performancy, delivery of service

    Sits between consumer and provider

**Cloud carrier**

    Typically, an ISP (Internet Service Provider)
    
    Provides intermediary connectivity

## Cloud Components

Cloud is often a combination of virtualization/cloud technologies and mirror virtualization components

Cloud is flexibile so interactions with these solutions in the categories are dependent on provider

Categories of Cloud Components:

- Compute
- Storage
- Network
- Security
- Application

### Compute Components

Core server components:
- Processor
- Memory

### Storage Components

Relate to data storage

i.e. Data on Local, SAN (Storage Area Network), or NAS (Network Attached Storage)

### Network Components

Connect cloud instances

i.e. vNIC (Virtual Network Interface Card), vSwitch (Virtual Switch), and vRouters (Virtual Routers)

### Security Components

Wide component group, including:

- Firewalls
- IPS (Intrusion Protection System)
- Identity management
- Encryprion
- Tunneling

### Application Components

Open ended application type

Must be build for the cloud

Many exisiting applications can be modified for the cloud

Provider solutions tightly intergrated with their offerings


## Advanced Cloud Services

Advanced cloud services CompTIA will test on:

- Internet of Things (IoT)
- Serverless
- Machine Learning/Artificial Intelligence (AI)

### Internet of Things
**Internet of Things (IoT)**

    References physical devices that link together using a connection like the internet

    i.e. Smart home, mobile phones, and appliances

Devices usually have a processor (not the main processor) that sends data to be anaylzed in the cloud

Connections from IoT to cloud has security risks and should be tested and monitored

### Serverless

**Serverless**

    User doesn't interact with server and goes along with the cloud service models as server is maintained by cloud provider

    i.e. AWS Lambda, Azure Functions, and Google Cloud Functions

Server is still there just abstracted from the view of the customer

CaaS to SaaS solutions are serverless

Billing for serverless solutions are billed by resource use and not time

If you don't use it, you are not billed as it is sort of for small solutions to be easy to implement fast and not used often enough for it's own infrastructure

### Machine Learning and Artificial Intelligence

**Machine Learning/Artificial Intelligence (AI)**