# 1-Cloud-Architecture-and-Design

## Cloud Deployment Models

Cloud Deployment Models:
- Public Cloud
- Private Cloud
- Hybrid Cloud
- Community Cloud

### Public Cloud

Refered to as multitenancy.
Public cloud is what we think of a lot when thinking of cloud as it is open to the general public
You share resources with other people or organizations.
The cloud provider takes care of the datacenter your resources are hosted on.
You own, manage, and operate resource utilization.
Could have issues if there is compliance as you don't know who is on the datacenter rack.

### Private Cloud

Refered to as "Cloud within a Cloud".
Private cloud is used by companies to isolate their resources. 
You can set how much of memory and CPUs are alloted to the whole cloud.
You and the company own, managem and operate resource utilization.
This is important for compliance such as PCI, HIPPA, and others.

### Hybrid Cloud

Refered to as Centrally Managed.
The most common cloud deployment as it encompasses on-premise and cloud resources for an organization.
It is compromised of on-premises and another cloud model such as private cloud.
For instance, you have your datacenter on-premise but your backups are being stored on cloud storage.
Requires a connection between on-premise and cloud like a VPN or IPsec tunnel.

### Community Cloud

Refered to as multicloud.
Community Cloud is where similar organizations such as healthcare or transportation use the same resources.
This allows for compliance and things to be baselined.

## Cloud Service Models

Also called "shared responsibility models".
Service models dictate the service aggreement between the customer and cloud provider. 
You take care of certain measures and the cloud provider takes care of others depending on the model you have.

### Shared Responsibility Model
The Shared Responsibility Model comprises of:
- Applications
- Data
- Runtime
- Middleware
- OS
- Virtualization
- Servers
- Storage
- Networking

Applications are the services that do what you want it to do. Such as a mail application deals with retrieving mail to customers.

Data is what the application uses or makes. This could be cache, databases, and other information.

Runtime is the environment structure in which the application is run on such .NET framework.

Middleware is the layer that is an intermediary between software application or components. It allows communication, integration, and data exchange between systems.

OS is operating system such as Windows 11 and has different features that allows you to interact with applications and their dependencies. This is the part you will not be able to control in the cloud.

Virtualization is basically done on the device that is hosting your OS and above. The datacenter rack could have many different OS and it isolates them from the actual physical hardware. This is the part you will not be able to control in the cloud.

Servers are the hardware that houses virtualizaiton of OS. These have compute (CPU), Storage, memory (RAM) to allow the OS to use based on partition of how much you set it or if you need more. This is the part you will not be able to control in the cloud.

Networking is the physical connections between servers and storage. This is fabric that allows data to be passed through them by use of networking devices such as switch and router.
This is the part you will not be able to control in the cloud.

Shared responsibility model changes with different cloud providers. It is also subject to change.

### Service Models

The service models will show what you have responsibility over and what the cloud has responsibilty over.

Service Models:
- On-premise
- IaaS - Infrastructure as a Service
- PaaS - Platform as a Service
- SaaS - Software as a Service
- FaaS - Function as a Service

### On-premise

This is the old way of doing things. There is no cloud involved and you take care of all the resposibilities.
This requires a lot of planning and forcasting of what you need in the future.
This uses capital expenture as you need the money up front to buy all the hardware, licenses, and networking equipment.

### IaaS

This is where you use just the datacenter's racks and you provision the memory, compute, and storage you are going to use.
This is what AWS EC2 and Azure Virtual Machines are.
You have to patch everything and be able to scale as you need to keep up with demand.
Requires less know how and planning as on-premise because if you don't need it anymore, you can deprovision it by shutting it off or deleting it.
This uses flexible expentures as you do not pay unless you use it and is based of metering. 
For instance, you get billed from how much data your service is using and how much compute you need to add.

### PaaS

In this instance, everything that isn't application or data is taken care by the cloud.
The infrastructure is scaled by the cloud.
This allows developers and companies to focus on their product or application as it does not require a lot of knowledge.
A great example is Azure App Service as you specify you code out the application using a framework that is supported.
Azure will choose the best size of instance or Virtual machine for you.
This is where the share responsibility model is gray depending on the shared responsibility model for each offering and cloud provider.
You might have to take care of the data backups and application patching.
The cloud provider might do data backups but not at an interval that is acceptable for your organization.

### SaaS

This is what people use when using everyday applications such as gmail or outlook. The cloud provides the application and you just use it. 
Applications are hosted by the cloud provider and you subscribe to the service and pay for usage, user count, and other metrics. 
SaaS are often multi-tenancy with customer's data and configurtions being separate from other customers.
The majority of the leg work is done but customers will still need to create, update, and delete their data on it. 
The customer determines usage with user accounts, defines workflows, and configures the settings within the application.

### FaaS

Function as a service is also called serverless. You don't manage any servers but bring the code that will be used and what framework (i.e. Python) the code is.
You maintain the code and update packages as needed. 
This allows you to not have permanent infrastructure as the code is only "turned on" when triggered.
You set up the triggers based on what events happen or using CRON jobs (time-based equation). 
Every time the function runs, you are charged and often have limits to API (application Protocol Interface; how apps talk to each other to do actions or retrive data).
Examples of this is AWS Lamdda and Azure functions.

## Cloud Service Model Table

| Service Model  | Application          | Data          | Runtime | Middleware | OS | Virtualization | Servers | Storage | Networking |
|----------------|----------------------|---------------|---------|------------|----|----------------|---------|---------|------------|
| On-premises    | Customer             | Customer      | Customer | Customer   | Customer | Customer | Customer | Customer | Customer    |
| IaaS           | Customer             | Customer      | Customer | Customer   | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider | Customer or Cloud Provider |
| PaaS           | Customer             | Customer      | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider |
| SaaS           | Cloud Provider       | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider |
| FaaS           | Customer (Functions) | Customer      | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider | Cloud Provider |

## Emerging Cloud Technologies

There are cloud technologies that are newer than the old cloud offerings such as storage that has introduced over 12 years ago.
Most cloud providers have services that provide solutions for these but it is being continously improved on and integrated more and more.

- IoT devices
- Severless
- AI/ML

### IoT devices

Internet of things devices are devices like smart watches but are also devices we use everyday that are becoming "smart". 
They require firmware and connections to hubs like internet such as traffic lights, vaccums, and even soda machines.
Data from this devices are often collected and anaylzed to improve these products.
It is so ingrained in modern day that people do not realize we are using them everyday and the number of them is estimated to be 40 billion or more.
There is so many things to manage that they are often managed as a fleet for these millions of devices to make sense of metrics like what soda is being used.

### Severless

Think of what was talked about ealier with FaaS. There is no server you need to manage.
As the server is abstracted by view of the customer, this is being called serverless.
Although there is actually servers in the background, you don't manage the hardware. 
Serverless runs the code on-demand and you pay for only for the use.

### AI/ML

We all have heard of AI (Artifical Intellgence) from things like ChatGPT and bard. 
ML (Machine learning) goes hand-in-hand with AI.
AI will find the patterns in data and produce insights.
Those insights is learned via ML and then makes decisions based on it and forecasts future trends and behavior.
It is based of a language that is consistantly being developed based on data from things like IoT devices. 
For example, you use Apple Maps (a SaaS offering) to get you around.
You start to visit a place like the bar over and over again. 
Based on that data being analyzed, your device or the service knows that you go to the bar every Saturday at night time and learns that behavior by ML.
Now when you are in your car on a Saturday at that time, it will bring up that bar and ask if you want directions to get there.

## Business Planning

There are two types of expenses in network and cloud engineering:
- Capital Expenditure (CapEx)
- Operational Expenditure (OpEx)

Capital expenditure is a set price such as the cost of buying a server rack and all it's components for on-premises.
There is money up front to buy it and as things progress there might be additional costs such as replacing RAM or End-of-life upgrades.

Operational Expenditure is pay as you go. You don't have to front the money but pay as you go at the bill of each month.
This is most previlant in cloud as the more you use the more you pay.

### On-premises Business Capacity Planning

Capacity is costly as you need more, you need to add more equipment.
You pay CapEx and you have to plan in the future and predict things to grow.
It's easy to grow this by connecting more and more to it but it becomes harder to scale back in.
What if you bought another server upfront expecting your new product to bring more customers and it doesn't.
You wasted resources such as time on planning, people setting this up, electricity, and money that will hurt your bottom line.
You are now stuck with this server that you don't use with additional server licenses that is not being put to use but you still will have to pay for it.

### Cloud Business Capacity Planning

Planning for the cloud is easier as you pay as you go which means the price will shift.
It is often OpEx that fluncutates and price will drop as the cloud grows.
You can also do CapEx that in a way is OpEx by putting in however many years of reservations for the server on the cloud.
This CapEx of reservations actually is discounted and way cheaper than on-premises as you don't need to house the infrastructure with electricity and have a professional adding more storage or compute as you go.
You can always scale up, scale down, or deprovision either horizontally (more servers) or vertically (more vCPUs) within secounds.

### Private Cloud Capacity Planning

This requires that you plan ahead with a buiness need analysis.
This business need analysis could be that you plan with a cloud cost caculator to see what you are using and what would be the cost to run it on cloud.
This will have CapEx as you need to set these limits of what you are going to use virutally to build out hardware and software.
In doing this you also have to take into consideration the user density of how much internally and external will people need this.

### Licensing Models

Licensing Models:
- Per-User
- Socket-Based
- Volume-based
- Core-based
- Subscription

Socket-based means that it based on how many sockets you are actively using on your motherboard and will charge you by that number of sockets.

Volume-based can also be site licensing

Core-based is if you have multiple cores on a CPU, it will charge you based on that.

## Performance Capacity Planning

You need to plan ahead of time what performance you are going to require:
- CPU
- Memory
- Network
- Storage
- App Response times

### Performance requirements considerations:
- System load
    - Each resource utilization currently
    - Currently at workload limits
    - Do we need more?
- User Density
    - current users
    - max number ofusers

### Trend Analysis for Planning

You need to have information based on historical data to plan for what might happen
- Baselines- How does it minumumly need to be
- Patterns
    - Future number of users
    - Future use of each resource
    - What can we do in the future with current configuration
    - Do we need more?
- Anomalies- What might we not be able to expect but happens if it does?

### Licenses for VMs

The license of VMs will be important. If you have Gen 1 Ubuntu Server, you might get more preformance with Gen 2.

Size of CPU for instance size will be important as well.

## High Avaliability and Scaling


