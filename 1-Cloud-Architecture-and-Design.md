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

## Cloud Serice Models

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
