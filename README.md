# AzureFundamentals
Readme with Important notes about azure
---

- [AzureFundamentals](#azurefundamentals)
  - [Readme with Important notes about azure](#readme-with-important-notes-about-azure)
- [What is Azure?](#what-is-azure)
    - [How does it work?](#how-does-it-work)
  - [What is the Azure portal?](#what-is-the-azure-portal)
  - [Azure services](#azure-services)
  - [Azure accounts:](#azure-accounts)
- [Azure fundamental concepts](#azure-fundamental-concepts)
  - [What are public, private, and hybrid clouds?](#what-are-public-private-and-hybrid-clouds)
  - [Cloud model comparison](#cloud-model-comparison)
  - [What are Cloud Service models?](#what-are-cloud-service-models)
  - [Azure Resources and Manager](#azure-resources-and-manager)
    - [Azure resource groups](#azure-resource-groups)
    - [Logical grouping](#logical-grouping)
  - [Billing and subscriptions](#billing-and-subscriptions)
- [Azure Compute Services](#azure-compute-services)
    - [VMs](#vms)
      - [Examples of when to use VMs](#examples-of-when-to-use-vms)
      - [Move to the cloud with VMs](#move-to-the-cloud-with-vms)
      - [Scale VMs in Azure](#scale-vms-in-azure)
      - [What are virtual machine scale sets?](#what-are-virtual-machine-scale-sets)
      - [What is Azure Batch?](#what-is-azure-batch)
  - [Decide when to use azure app service](#decide-when-to-use-azure-app-service)
    - [Costs](#costs)
    - [Types of app services](#types-of-app-services)
  - [Decide when to use Azure Container instances or Azure Kubernetes service](#decide-when-to-use-azure-container-instances-or-azure-kubernetes-service)
    - [Manage containers](#manage-containers)
  - [When to use Azure Functions](#when-to-use-azure-functions)
    - [What is serverless computing?](#what-is-serverless-computing)
    - [Azure functions:](#azure-functions)
    - [Azure logic apps](#azure-logic-apps)
  - [When to use Azure Virtual Desktop](#when-to-use-azure-virtual-desktop)
    - [What is it?](#what-is-it)
    - [Why?](#why)
  - [Summary:](#summary)
  - [Networking Services](#networking-services)
  - [Azure VPN fundamentals](#azure-vpn-fundamentals)
    - [Vpn gateways](#vpn-gateways)
  - [VPN gateway sizes:](#vpn-gateway-sizes)
  - [Deploying the VPN:](#deploying-the-vpn)
  - [Azure Express Fundamentals:](#azure-express-fundamentals)
    - [Features and benefits of ExpressRoute](#features-and-benefits-of-expressroute)
- [Cloud Storage](#cloud-storage)
- [Azure DB and Analytics Service](#azure-db-and-analytics-service)
  - [Azure Cosmos DB:](#azure-cosmos-db)
  - [Azure SQL DB](#azure-sql-db)
  - [Azure Managed SQL db:](#azure-managed-sql-db)
  - [Migration](#migration)
  - [About Big Data:](#about-big-data)
- [Azure Functions](#azure-functions-1)
- [Azure Logic Apps](#azure-logic-apps-1)
- [What are the differences between these services?](#what-are-the-differences-between-these-services)
  - [Use Azure Functions:](#use-azure-functions)
- [Best tools for the best solutions:](#best-tools-for-the-best-solutions)
- [Best Tools for configuring and managing Azure Environment:](#best-tools-for-configuring-and-managing-azure-environment)
  - [Decision Criteria:](#decision-criteria)
- [Monitoring Services, outage mitigation:](#monitoring-services-outage-mitigation)
  - [Decision Criteria:](#decision-criteria-1)
- [Cloud Security](#cloud-security)
- [Network Conectivity:](#network-conectivity)

# What is Azure?

Azure is microsoft Cloud computing platform.

Azure supports platform softare and infrastructure as service.

- Azure container and Kubernetes is a thing.

- Be ready for the future: Continuous innovation from Microsoft supports your development today and your product visions for tomorrow.

- Build on your terms: You have choices. With a commitment to open source, and support for all languages and frameworks, you can build how you want and deploy where you want to.

- Operate hybrid seamlessly: On-premises, in the cloud, and at the edge--we'll meet you where you are. Integrate and manage your environments with tools and services designed for a hybrid cloud solution.

- Trust your cloud: Get security from the ground up, backed by a team of experts, and proactive compliance trusted by enterprises, governments, and startups.

### How does it work?

It uses virtualization to decouple OS from hardware, through a Hypervisor.

- it emulates an os inside the VM and tightens the components toghether. can run multiple VMs in it. each server in a data center has a hypervisor.

## What is the Azure portal?
The Azure portal is a web-based, unified console that provides an alternative to command-line tools. With the Azure portal, you can manage your Azure subscription by using a graphical user interface. You can:

Build, manage, and monitor everything from simple web apps to complex cloud deployments.
Create custom dashboards for an organized view of resources.
Configure accessibility options for an optimal experience.

---

## Azure services

most commonly used services:

Let's take a closer look at the most commonly used categories:

- Compute
- Networking
- Storage
- Mobile
- Databases
- Web
- Internet of Things (IoT)
- Big data
- AI
- DevOps

further info: https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-fundamentals/tour-of-azure-services

## Azure accounts: 

![scope-levels-12669ee1](https://user-images.githubusercontent.com/34945430/162189279-3713484c-7c16-4a66-aae3-4defff7c6132.png)


---

# Azure fundamental concepts

## What are public, private, and hybrid clouds?

There are three deployment models for cloud computing: public cloud, private cloud, and hybrid cloud. Each deployment model has different aspects that you should consider as you migrate to the cloud.

| Deployment model  |         Description |
|-------------------|---------------|
|Public cloud       |Services are offered over the public internet and available to anyone who wants to purchase them. Cloud resources, such as servers and storage, are owned and operated by a third-party cloud service provider, and delivered over the internet.|
|Private cloud       | A private cloud consists of computing resources used exclusively by users from one business or organization. A private cloud can be physically located at your organization's on-site (on-premises) datacenter, or it can be hosted by a third-party service provider. |
|Hybrid cloud|A hybrid cloud is a computing environment that combines a public cloud and a private cloud by allowing data and applications to be shared between them. |

## Cloud model comparison

- Public cloud:
  
  - No capital expenditures to scale up.
  - Applications can be quickly provisioned and deprovisioned.
  - Organizations pay only for what they use.

- Private cloud:
  
  - Hardware must be purchased for start-up and maintenance.
  - Organizations have complete control over resources and security.
  - Organizations are responsible for hardware maintenance and updates.
- Hybrid cloud:
  
  - Provides the most flexibility.
  - Organizations determine where to run their applications.
  - Organizations control security, compliance, or legal      requirements.

## What are Cloud Service models?

see here: https://docs.microsoft.com/en-gb/learn/modules/fundamental-azure-concepts/categories-of-cloud-services


## Azure Resources and Manager

### Azure resource groups

Resource groups are a fundamental element of the Azure platform. A resource group is a logical container for resources deployed on Azure. These resources are anything you create in an Azure subscription like VMs, Azure Application Gateway instances, and Azure Cosmos DB instances. All resources must be in a resource group, and a resource can only be a member of a single resource group. Many resources can be moved between resource groups with some services having specific limitations or requirements to move. Resource groups can't be nested. Before any resource can be provisioned, you need a resource group for it to be placed in.

### Logical grouping

Resource groups exist to help manage and organize your Azure resources. By placing resources of similar usage, type, or location in a resource group, you can provide order and organization to resources you create in Azure. Logical grouping is the aspect that you're most interested in here, because there's a lot of disorder among our resources.

https://docs.microsoft.com/en-gb/learn/modules/azure-architecture-fundamentals/resources-resource-manager


## Billing and subscriptions

https://docs.microsoft.com/en-gb/learn/modules/azure-architecture-fundamentals/management-groups-subscriptions

I think on subs the documentation explains it very well and cannot be summarized, so refer to the original docmentation.

---

# Azure Compute Services

- Azure Virtual Machines
- Azure Container Instances
- Azure App Service
- Azure Functions (or serverless computing)

You have:

- Virtual machine scale sets
- Containers and kubernetes
- app services
- functions

### VMs

#### Examples of when to use VMs
- During testing and development. VMs provide a quick and easy way to create different OS and application configurations. Test and development personnel can then easily delete the VMs when they no longer need them.

- When running applications in the cloud. The ability to run certain applications in the public cloud as opposed to creating a traditional infrastructure to run them can provide substantial economic benefits. For example, an application might need to handle fluctuations in demand. Shutting down VMs when you don't need them or quickly starting them up to meet a sudden increase in demand means you pay only for the resources you use.
- When extending your datacenter to the cloud. An organization can extend the capabilities of its own on-premises network by creating a virtual network in Azure and adding VMs to that virtual network. Applications like SharePoint can then run on an Azure VM instead of running locally. This arrangement makes it easier or less expensive to deploy than in an on-premises environment.
- During disaster recovery. As with running certain types of applications in the cloud and extending an on-premises network to the cloud, you can get significant cost savings by using an IaaS-based approach to disaster recovery. If a primary datacenter fails, you can create VMs running on Azure to run your critical applications and then shut them down when the primary datacenter becomes operational again.

#### Move to the cloud with VMs

VMs are also an excellent choice when you move from a physical server to the cloud (also known as lift and shift). You can create an image of the physical server and host it within a VM with little or no changes. Just like a physical on-premises server, you must maintain the VM. You update the installed OS and the software it runs.

#### Scale VMs in Azure

You can run single VMs for testing, development, or minor tasks. Or you can group VMs together to provide high availability, scalability, and redundancy. No matter what your uptime requirements are, Azure has several features that can meet them. These features include:

- Virtual machine scale sets
- Azure Batch

#### What are virtual machine scale sets?

Virtual machine scale sets let you create and manage a group of identical, load-balanced VMs.

#### What is Azure Batch?

Azure Batch enables large-scale parallel and high-performance computing (HPC) batch jobs with the ability to scale to tens, hundreds, or thousands of VMs.

When you're ready to run a job, Batch does the following:

- Starts a pool of compute VMs for you.
- Installs applications and staging data.
- Runs jobs with as many tasks as you have.
- Identifies failures.
- Requeues work.
- Scales down the pool as work completes.

## Decide when to use azure app service

App Service enables you to build and host web apps, background jobs, mobile back-ends, and RESTful APIs in the programming language of your choice without managing infrastructure. It offers automatic scaling and high availability.

App Service supports Windows and Linux and enables automated deployments from GitHub, Azure DevOps, or any Git repo to support a continuous deployment model.

### Costs

The App Service plan determines how much hardware is devoted to your host. For example, the plan determines whether it's dedicated or shared hardware and how much memory is reserved for it. 

### Types of app services

With App Service, you can host most common app service styles like:

- Web apps
- API apps
- WebJobs
- Mobile apps

App Service handles most of the infrastructure decisions you deal with in hosting web-accessible apps:

- Deployment and management are integrated into the platform.
- Endpoints can be secured.
- Sites can be scaled quickly to handle high traffic loads.
- The built-in load balancing and traffic manager provide high availability.

See more: https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/azure-app-services

## Decide when to use Azure Container instances or Azure Kubernetes service

### Manage containers

Containers are managed through a container orchestrator, which can start, stop, and scale out application instances as needed. There are two ways to manage both Docker and Microsoft-based containers in Azure: Azure Container Instances and Azure Kubernetes Service (AKS).

- Azure container instances
- Azure Kubernetes Service

Use contanerisation to split your app in multiple containers that can be accessed and managed separately, for example front end back end and data (3 containers).

See further: https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/azure-container-services

MICROSERVICES!!!

## When to use Azure Functions

Serverless computing includes the abstraction of servers, an event-driven scale, and micro-billing:

- Abstraction of servers: Serverless computing abstracts the servers you run on. You never explicitly reserve server instances. The platform manages that for you. Each function execution can run on a different compute instance. This execution context is transparent to the code. With serverless architecture, you deploy your code, which then runs with high availability.

- Event-driven scale: Serverless computing is an excellent fit for workloads that respond to incoming events. Events include triggers by:

  - Timers, for example, if a function needs to run every day at 10:00 AM UTC.
  - HTTP, for example, API and webhook scenarios.
  -  Queues, for example, with order processing.
  - And much more.

Instead of writing an entire application, the developer authors a function, which contains both code and metadata about its triggers and bindings. The platform automatically schedules the function to run and scales the number of compute instances based on the rate of incoming events. Triggers define how a function is invoked. Bindings provide a declarative way to connect to services from within the code.

- Micro-billing: Traditional computing bills for a block of time like paying a monthly or annual rate for website hosting. This method of billing is convenient but isn't always cost effective. Even if a customer's website gets only one hit a day, they still pay for a full day's worth of availability. With serverless computing, they pay only for the time their code runs. If no active function executions occur, they're not charged. For example, if the code runs once a day for two minutes, they're charged for one execution and two minutes of computing time.

### What is serverless computing?

The goal is to take care of management tasks and automate them.

Azure has two implementations of serverless compute:

- Azure Functions: Functions can execute code in almost any modern language.
- Azure Logic Apps: Logic apps are designed in a web-based designer and can execute logic triggered by Azure services without writing any code.

Benefits:

- No infrastructure management
- Scalability
- Pay as you use

### Azure functions:

When you're concerned only about the code running your service, and not the underlying platform or infrastructure, using Azure Functions is ideal. Functions are commonly used when you need to perform work in response to an event (often via a REST request), timer, or message from another Azure service, and when that work can be completed quickly, within seconds or less

### Azure logic apps

Logic apps are similar to functions. Both enable you to trigger logic based on an event. Where functions execute code, logic apps execute workflows that are designed to automate business scenarios and are built from predefined logic blocks.

Every Azure logic app workflow starts with a trigger, which fires when a specific event happens or when newly available data meets specific criteria. Many triggers include basic scheduling capabilities, so developers can specify how regularly their workloads will run. Each time the trigger fires, the Logic Apps engine creates a logic app instance that runs the actions in the workflow. These actions can also include data conversions and flow controls, such as conditional statements, switch statements, loops, and branching.

You create logic app workflows by using a visual designer on the Azure portal or in Visual Studio. The workflows are persisted as a JSON file with a known workflow schema.

see more: 
https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/azure-functions

## When to use Azure Virtual Desktop

### What is it?

Azure Virtual Desktop is a desktop and application virtualization service that runs on the cloud. It enables your users to use a cloud-hosted version of Windows from any location. Azure Virtual Desktop works across devices like Windows, Mac, iOS, Android, and Linux. It works with apps that you can use to access remote desktops and apps. You can also use most modern browsers to access Azure Virtual Desktop-hosted experiences.

### Why? 

- Provide the best user experience
- Enhance security
- Simplified management
- Performance management
- Multi session W10 deployment

## Summary: 

In this module, you learned how you can help Tailwind Traders resolve its application demand challenges through the use of Azure virtualization services like Azure Virtual Machines, Azure Container Instances, and Azure Kubernetes Service. You also learned how you can use:

- Azure App Service to create your website front-ends.

- Azure Functions to create event-driven application logic that only runs when you need it.

- Azure Virtual Desktop to quickly provide a customized operating system and software environment for your remote workers.

Further reading: 
https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/summary

---

## Networking Services

- Virtual networks
- Service endpoints

On prem: 

- Points to site vrtual private networks
- Site to site VPN
- Azure ExpressRoute

Route network traffic:

- Route table
- Border Gateway Protocol

Filter traffic: 

- Network Security Groupd
- Network virtual appliance

Connect virtual networks:

You can link virtual networks together by using virtual network peering. Peering enables resources in each virtual network to communicate with each other. These virtual networks can be in separate regions, which allows you to create a global interconnected network through Azure.

User-defined routes (UDR) are a significant update to Azure’s Virtual Networks that allows for greater control over network traffic flow. This method allows network administrators to control the routing tables between subnets within a VNet, as well as between VNets.

![image](https://user-images.githubusercontent.com/34945430/162455203-035f1973-f0ee-4612-bc22-21fcea3a4708.png)


## Azure VPN fundamentals

VPNs use an encrypted tunnel within another network. They're typically deployed to connect two or more trusted private networks to one another over an untrusted network (typically the public internet). Traffic is encrypted while traveling over the untrusted network to prevent eavesdropping or other attacks.

### Vpn gateways
A VPN gateway is a type of virtual network gateway. Azure VPN Gateway instances are deployed in a dedicated subnet of the virtual network and enable the following connectivity:

- Connect on-premises datacenters to virtual networks through a site-to-site connection.
- Connect individual devices to virtual networks through a point-to-site connection.
- Connect virtual networks to other virtual networks through a network-to-network connection.

Types: 

- Policy based VPN
- Route-Based VPN

![image](https://user-images.githubusercontent.com/34945430/162458555-728cc79f-823e-497c-8910-1c39d8c7cd39.png)

## VPN gateway sizes:

![image](https://user-images.githubusercontent.com/34945430/162458680-e0844098-f867-409b-831e-21ed19894087.png)

## Deploying the VPN:

![image](https://user-images.githubusercontent.com/34945430/162458809-5a0fd227-7e16-435b-b8b9-e174fc92af01.png)

See more about VPNS here:

https://docs.microsoft.com/en-us/learn/modules/azure-networking-fundamentals/azure-vpn-gateway-fundamentals

## Azure Express Fundamentals:

![image](https://user-images.githubusercontent.com/34945430/162459508-54cc2fdb-2e91-4e86-bd14-344b24a74441.png)

### Features and benefits of ExpressRoute
There are several benefits to using ExpressRoute as the connection service between Azure and on-premises networks.

- Layer 3 connectivity between your on-premises network and the Microsoft Cloud through a connectivity provider. Connectivity can be from an any-to-any (IPVPN) network, a point-to-point Ethernet connection, or through a virtual cross-connection via an Ethernet exchange.
- Connectivity to Microsoft cloud services across all regions in the geopolitical region.
- Global connectivity to Microsoft services across all regions with the ExpressRoute premium add-on.
- Dynamic routing between your network and Microsoft via BGP.
- Built-in redundancy in every peering location for higher reliability.
- Connection uptime SLA.
- QoS support for Skype for Business.

https://docs.microsoft.com/en-us/learn/modules/azure-networking-fundamentals/express-route-fundamentals

# Cloud Storage

https://docs.microsoft.com/en-us/learn/modules/azure-storage-fundamentals/azure-storage-accounts

Blobs aren't limited to common file formats. A blob could contain gigabytes of binary data streamed from a scientific instrument, an encrypted message for another application, or data in a custom format for an app you're developing. One advantage of blob storage over disk storage is that it does not require developers to think about or manage disks; data is uploaded as blobs, and Azure takes care of the physical storage needs.

Blob Storage is ideal for:

- Serving images or documents directly to a browser.
- Storing files for distributed access.
- Streaming video and audio.
- Storing data for backup and restore, disaster recovery, and archiving.
- Storing data for analysis by an on-premises or Azure-hosted service.
- Storing up to 8 TB of data for virtual machines.

![image](https://user-images.githubusercontent.com/34945430/162463966-2f0c0660-5322-4aef-a010-5c78cfa46ea0.png)


Files:

![image](https://user-images.githubusercontent.com/34945430/162464155-4b7a78e4-4868-4e01-91e8-10e2d3b89404.png)

Setting up blob tiers:

Hot, cold , Archive.

![image](https://user-images.githubusercontent.com/34945430/162464440-390a3425-ad54-4cb9-9ffe-422b315cc76d.png)

# Azure DB and Analytics Service

## Azure Cosmos DB:

Azure Cosmos DB is a globally distributed, multi-model database service. You can elastically and independently scale throughput and storage across any number of Azure regions worldwide. You can take advantage of fast, single-digit-millisecond data access by using any one of several popular APIs. Azure Cosmos DB provides comprehensive service level agreements for throughput, latency, availability, and consistency guarantees.

![image](https://user-images.githubusercontent.com/34945430/162468277-6b0d1fd0-5f79-4c06-a6ca-b315288cf4f5.png)


## Azure SQL DB

![image](https://user-images.githubusercontent.com/34945430/162469028-2efc001d-772e-4f08-bc66-8d67fa87f2d4.png)

EXCERSISE:

https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/exercise-create-sql-database

## Azure Managed SQL db:

https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/azure-sql-managed-instance

## Migration
Azure SQL Managed Instance makes it easy to migrate your on-premises data on SQL Server to the cloud using the Azure Database Migration Service (DMS) or native backup and restore. After you have discovered all of the features that your company uses, you need to assess which on-premises SQL Server instances you can migrate to Azure SQL Managed Instance to see if you have any blocking issues. Once you have resolved any issues, you can migrate your data, then cutover from your on-premises SQL Server to your Azure SQL Managed Instance by changing the connection string in your applications.

![image](https://user-images.githubusercontent.com/34945430/162473083-013480e3-a9ea-4d12-98a3-6ea3b114b135.png)

## About Big Data:

https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/azure-big-data-analytics


![image](https://user-images.githubusercontent.com/34945430/162473403-22914330-0736-484e-9db9-5fc38317506e.png)
![image](https://user-images.githubusercontent.com/34945430/162473427-434b28da-8a4d-4e5b-bb57-d2ef1911aa5c.png)

---

# Azure Functions

With the Azure Functions service, you can host a single method or function by using a popular programming language in the cloud that runs in response to an event. An example of an event might be an HTTP request, a new message on a queue, or a message on a timer.

Because of its atomic nature, Azure Functions can serve many purposes in an application's design. Functions can be written in many common programming languages, such as C#, Python, JavaScript, Typescript, Java, and PowerShell.

Azure Functions scales automatically, and charges accrue only when a function is triggered. These qualities make Azure Functions a solid choice when demand is variable. For example, you might be receiving messages from an IoT solution that monitors a fleet of delivery vehicles. You'll likely have more data arriving during business hours. Azure Functions can scale out to accommodate these busier times.

An Azure function is a stateless environment. A function behaves as if it's restarted every time it responds to an event. This feature is ideal for processing incoming data. And if state is required, the function can be connected to an Azure storage account.

Azure Functions can perform orchestration tasks by using an extension called Durable Functions, which allow developers to chain functions together while maintaining state.

The Azure Functions solution is ideal when you're concerned only with the code that's running your service and not the underlying platform or infrastructure. You use Azure Functions most commonly when you need to perform work in response to an event. You do this often via a REST request, timer, or message from another Azure service, and when that work can be completed quickly, within seconds or less.

# Azure Logic Apps

Logic Apps is a low-code/no-code development platform hosted as a cloud service. The service helps you automate and orchestrate tasks, business processes, and workflows when you need to integrate apps, data, systems, and services across enterprises or organizations. Logic Apps simplifies how you design and build scalable solutions, whether in the cloud, on-premises, or both. This solution covers app integration, data integration, system integration, enterprise application integration (EAI), and business-to-business (B2B) integration.

Azure Logic Apps is designed in a web-based designer and can execute logic that's triggered by Azure services without writing any code. You build an app by linking triggers to actions with connectors. A trigger is an event (such as a timer) that causes an app to execute, then a new message to be sent to a queue, or an HTTP request. An action is a task or step that can execute. There are logic actions such as those you would find in most programming languages. Examples of actions include working with variables, decision statements and loops, and tasks that parse and modify data.

To build enterprise integration solutions with Azure Logic Apps, you can choose from a growing gallery of over 200 connectors. The gallery includes services such as Salesforce, SAP, Oracle DB, and file shares.

If you can't find the action or connector you need, you can build your own by using custom code.

# What are the differences between these services?

You can call Azure Functions from Azure Logic Apps, and vice versa. The primary difference between the two services is their intent. Azure Functions is a serverless compute service, and Azure Logic Apps is intended to be a serverless orchestration service. Although you can use Azure Functions to orchestrate a long-running business process that involves various connections, this was not its primary use case when it was designed.

Additionally, the two services are priced differently. Azure Functions pricing is based on the number of executions and the running time of each execution. Logic Apps pricing is based on the number of executions and the type of connectors that it utilizes.

![image](https://user-images.githubusercontent.com/34945430/162738549-4595fd1d-7426-4204-ae72-fa4f0597e56a.png)

## Use Azure Functions:

![image](https://user-images.githubusercontent.com/34945430/162738613-011a94b3-d8bb-4c3c-b326-11fd0651cb88.png)

---

# Best tools for the best solutions:

![image](https://user-images.githubusercontent.com/34945430/162739135-2efaa659-c9e8-4a8c-9e35-151d6ff672ea.png)

GITHUB AND GITHUB ACTIONS:

![image](https://user-images.githubusercontent.com/34945430/162739222-e5253edf-e91e-40fa-a966-4afc6d75a353.png)

Azure Dev Test Labs:

![image](https://user-images.githubusercontent.com/34945430/162739266-488ec7a2-09f6-45c4-8480-25ed65091476.png)



Decision critaria:

https://docs.microsoft.com/en-gb/learn/modules/azure-devops-devtest-labs/3-analyze-decision-criteria

---

# Best Tools for configuring and managing Azure Environment:

- Visual tools and code based tools

![image](https://user-images.githubusercontent.com/34945430/162739906-57d24b52-15ff-4e40-9499-721af9f54365.png)

![image](https://user-images.githubusercontent.com/34945430/162739930-bb6a0a1e-710e-473b-9928-3b51f90e7191.png)

## Decision Criteria:

https://docs.microsoft.com/en-gb/learn/modules/management-fundamentals/3-analyze-decision-criteria

# Monitoring Services, outage mitigation:

![image](https://user-images.githubusercontent.com/34945430/162741549-695eb9f7-0172-417a-9ecd-59887ff3acfd.png)

![image](https://user-images.githubusercontent.com/34945430/162741577-19510470-f96d-4773-a557-d6ec2526cce3.png)

![image](https://user-images.githubusercontent.com/34945430/162741610-17b89201-20cb-44ab-b674-c18e527f38b7.png)

## Decision Criteria:

![image](https://user-images.githubusercontent.com/34945430/162741979-592ecfe1-b505-4df6-b62b-911f9b0203d4.png)


---

# Cloud Security

![image](https://user-images.githubusercontent.com/34945430/162981989-4431f7d2-1490-452c-adce-6cfaea5918dd.png)

![image](https://user-images.githubusercontent.com/34945430/162982314-88f6f0d7-96e8-44e3-a83a-d940e30b8b81.png)
![image](https://user-images.githubusercontent.com/34945430/162982365-484aafab-b61c-43d3-b2f3-0b2c5cc41e39.png)
![image](https://user-images.githubusercontent.com/34945430/162982390-180cd2ea-3fc9-4459-95a7-8329fe9a5b31.png)
![image](https://user-images.githubusercontent.com/34945430/162982443-de8f0344-5535-45b7-a262-899a4c546692.png)
![image](https://user-images.githubusercontent.com/34945430/162982845-b6cd4243-daa6-4d3e-bc6e-40d3d514c28b.png)
![image](https://user-images.githubusercontent.com/34945430/162982900-b69e9d2b-132c-40d1-8d03-b3bf6bcd7be5.png)
![image](https://user-images.githubusercontent.com/34945430/162982934-e33a83b5-8644-4fda-8766-2a04cae3edb6.png)
Excersise: https://docs.microsoft.com/en-us/learn/modules/protect-against-security-threats-azure/5-manage-password-key-vault

![image](https://user-images.githubusercontent.com/34945430/162983097-ddcd1969-5af6-41c5-ae7a-66abf904906b.png)

---

# Network Conectivity:

![image](https://user-images.githubusercontent.com/34945430/162983416-c24323a8-deac-4aa5-87fc-716201c07742.png)
![image](https://user-images.githubusercontent.com/34945430/162983457-7a95694f-fcec-43f8-a8c7-abc4b77384ef.png)
![image](https://user-images.githubusercontent.com/34945430/162983492-8c48614b-7045-4525-ba55-3186c0ac0a23.png)
![image](https://user-images.githubusercontent.com/34945430/162983526-6256ca71-ff06-4958-b607-11237d0a1d93.png)
![image](https://user-images.githubusercontent.com/34945430/162983554-6c5ca5e2-bd90-4b36-ba99-2500530451af.png)
![image](https://user-images.githubusercontent.com/34945430/162983594-7351b6b9-0169-491d-9210-774096ebe0e1.png)
![image](https://user-images.githubusercontent.com/34945430/162983662-bfe6952f-46ee-4e0a-b537-6d9bfe4f0a1c.png)
![image](https://user-images.githubusercontent.com/34945430/162983703-4b5f763d-df80-40b1-b671-ffb9cc8ab09a.png)
![image](https://user-images.githubusercontent.com/34945430/162983732-318df967-6f89-48c5-84c3-2c1ca7fc9c12.png)
![image](https://user-images.githubusercontent.com/34945430/162983753-3b5f4901-c413-4e16-8666-070e0320279e.png)

![image](https://user-images.githubusercontent.com/34945430/162983797-4d5a4c31-da20-4977-8842-737774e96218.png)
Excersise 2: https://docs.microsoft.com/en-us/learn/modules/secure-network-connectivity-azure/6-configure-access-network-security-group

![image](https://user-images.githubusercontent.com/34945430/162983919-b91bc9fd-140d-4f03-a4f5-e11d9508514e.png)
![image](https://user-images.githubusercontent.com/34945430/162983940-093756c1-256c-4dfe-83a7-dc7437b73fd2.png)

# Azure Cost Management and Service level agreements.

## Whats the TCO cost calculator?

- It helps you estimate the cost savings of operating your solution on Azure over time, instead of the on premises datacenter.

the term total cost of ownership is commonly use in finance. It can be hard to see all the hidden costs related to operating a technology capability on prem.

With the TCO Calculator you enter the details of your on-premises workloads. Then you review the suggested industry average costs. These costs include electricity, network maintenance, and IT labor. You're then presented with a side-by-side report. Using the report, you can compare those costs wwith the sample workloads running on Azure.

![image](https://user-images.githubusercontent.com/34945430/163142016-2643f6a8-9e14-4ca2-aeca-522ed11ef754.png)

![image](https://user-images.githubusercontent.com/34945430/163142052-14829e62-1cdf-4dfe-9b2a-eb7fdea33b1d.png)

### Step 1: Define your workloads

First you enter the specifications of your on prem infrastructure into the TCO Calculator based on these 4 categories:

- Servers
  
  This Categor,y includes OS VMs , CPU cores and RAM.

- DBs

  This category includes DB types, Server hardware, and the Azure Service you want to use, which includes the expected maximum concurrent user sign-ins.

- Storage

  This category includes storage type and capacity, which includes any backup or archive storage.

- Networking

This category includes the amount of network bandwidth you currently consume in your on prem environment.

### Step 2: Adjust assumptions

Next, you specify whether your current on-premises licenses are enrolled for Software Assurance, which can save you money by reusing those licenses on Azure. You also specify whether you need to replicate your storage to another Azure region for greater redundancy.

Then, you can see the key operating cost assumptions across several different areas, which vary among teams and organizations. These costs have been certified by Nucleus Research, an independent research company. For example, these costs include:

- Electrivity price per kilowatt hour (KWh).
- Hourly pay rate for it Admin.
- Network maintenance cost as a percentage of network hardware and Software costs.

To improve the accuracy of the TCO Calculator results, you adjust the values so that they match the costs of your current on-premises infrastructure.

### Step 3: View the report

Choose a time frame between one and five years. The TCO calculator generates a report that's based on the information you've entered. here is an example:

![image](https://user-images.githubusercontent.com/34945430/163143095-fcae9dca-3a21-4c13-9a98-6d45b268a93e.png)

![image](https://user-images.githubusercontent.com/34945430/163143159-2c714d2c-14d5-4910-afb4-b9c8b0dff76a.png)

## Compare sample Workload costs by using the TCo Calculator

## Define your workloads: 

Using the TCO we estimated a total cost of: over 3 years.

![image](https://user-images.githubusercontent.com/34945430/163155878-de3ced2d-448b-452e-85ba-383112d1fcac.png)

[Total Cost of Ownership (TCO) Calculator _ Microsoft Azure.pdf](https://github.com/Tabooabr/AzureFundamentals/files/8480479/Total.Cost.of.Ownership.TCO.Calculator._.Microsoft.Azure.pdf)

# Purchase Azure Services

## Types of azure subscriptions:

- Free trial ( self explanatory)
- Pay as you go: 
   A pay-as-you-go subscription enables you to pay for what you use by attaching a credit or debit card to your account. Organizations can apply for volume discounts and prepaid invoicing.
   
 -  Members offers:

    Your existing membership to certain Microsoft products and services might provide you with credits for your Azure account and reduced rates on Azure services. For example, member offers are available to Visual Studio subscribers, Microsoft Partner Network members, Microsoft for Startups members, and Microsoft Imagine members.

## Azure services: 

![image](https://user-images.githubusercontent.com/34945430/163156736-4720a665-cf4b-4421-9e14-8e595070de7e.png)

## Billing Zones:

![image](https://user-images.githubusercontent.com/34945430/163157143-c3a9d151-9ad6-452c-8db7-7e88cc7a47f4.png)

# Workload calculator:

Link: https://azure.microsoft.com/en-gb/pricing/calculator/

![image](https://user-images.githubusercontent.com/34945430/163157572-a860fea5-b0c7-48d2-87f3-504004ff23e7.png)

Excersise:

 ![image](https://user-images.githubusercontent.com/34945430/163158190-f7714e54-7afe-4940-801d-8d912b47caf4.png)

# Azure Advisor: 

![image](https://user-images.githubusercontent.com/34945430/163158325-6ab58d2c-2d57-4848-ae3f-40bee8abf731.png)

![image](https://user-images.githubusercontent.com/34945430/163158424-387f33cb-56c2-4cdf-b20d-b79a1e3ef713.png)

## Further reading: 

https://docs.microsoft.com/en-us/learn/modules/plan-manage-azure-costs/8-summary

# Choose the right azure services by examinign SLAs


## What is an SLA?

A service-level agreement (SLA) is a formal agreement between a service company and the customer. For Azure, this agreement defines the performance standards that Microsoft commits to for you, the customer.

In this part, you'll learn more about Azure SLAs, including why SLAs are important, where you can find the SLA for a specific Azure service, and what you'll find in a typical SLA.


## Why are SLAs Important?

Understanding the SLA for each Azure service you use helps you understand what guarantees you can expect.

When you build applications on Azure, the availability of the services that you use affect your application's performance. Understanding the SLAs involved can help you establish the SLA you set with your customers.

Later in this module, you'll learn about some strategies you can use when an Azure SLA doesn't meet your needs.


### Access SLAs in Azure: 

https://azure.microsoft.com/support/legal/sla/


## Typical SLA:

![image](https://user-images.githubusercontent.com/34945430/163160141-5961be61-eba1-4982-a9f0-fe98a57cafad.png)

## How percentages rerlate to total downtime?

![image](https://user-images.githubusercontent.com/34945430/163160826-f0f4d10f-6d39-45fc-b462-3cfac9861156.png)

## What are service credits?

![image](https://user-images.githubusercontent.com/34945430/163161051-8555fa6b-7c88-4ea8-8158-c72fd76f3fbe.png)


Azure Status to check if service is unavailable: https://status.azure.com/status

# Define your own SLA

### Identify Workloads: 

![image](https://user-images.githubusercontent.com/34945430/163163391-46dc6599-ac98-4715-b5ed-4634767cf060.png)

Calculating the percentages:

![image](https://user-images.githubusercontent.com/34945430/163163600-a75ea8f9-7449-4b3f-b79e-5ea6ac047422.png)

Possible shortcomings:

![image](https://user-images.githubusercontent.com/34945430/163163743-51466914-acc9-4e26-b160-04c1cae66193.png)


![image](https://user-images.githubusercontent.com/34945430/163163779-eed360ea-93a7-4f9a-8d10-e31a56c5e4be.png)

## Access opreview services and preview features

Summary: 

https://docs.microsoft.com/en-us/learn/modules/choose-azure-services-sla-lifecycle/7-summary

---

# Describe Identity, Governace, Privacy and compliance features.

## Authentication and authorization

![image](https://user-images.githubusercontent.com/34945430/163175628-c5902184-e1c0-446a-abaf-7fd986fcac64.png)


![image](https://user-images.githubusercontent.com/34945430/163175649-eec69a4c-eb1e-4913-a81c-a5f3b6f1f2cf.png)

## What is Azure active directory?

In this part, you learn how Azure Active Directory (Azure AD) provides identity services that enable your users to sign in and access both Microsoft cloud applications and cloud applications that you develop. You also learn how Azure AD supports single sign-on (SSO).

![image](https://user-images.githubusercontent.com/34945430/163175941-8a626649-3bea-43cc-ab4b-4acb1f04d865.png)

![image](https://user-images.githubusercontent.com/34945430/163176412-10bb8f03-0e32-4bbd-8099-f357f4be9cb3.png)


![image](https://user-images.githubusercontent.com/34945430/163176538-a670d405-cb06-4ca4-a7fe-b9a0e1dd3499.png)

## SSO:

![image](https://user-images.githubusercontent.com/34945430/163176666-ea7dc80f-6e2b-4bc2-b960-2ac7dc6ac238.png)


![image](https://user-images.githubusercontent.com/34945430/163176834-34aadbd1-f373-4469-a07f-d35b64158bdf.png)

MFA:

![image](https://user-images.githubusercontent.com/34945430/163176906-f593b13f-7d60-432f-854a-6fc6378ca707.png)

Azure MFA: 

![image](https://user-images.githubusercontent.com/34945430/163176999-eaa662b0-647d-4b0a-84ec-932bee65fc49.png)

![image](https://user-images.githubusercontent.com/34945430/163177132-712e5918-7c9c-4bd0-99ef-5772f414a282.png)

---

# Governace Strategies:
![image](https://user-images.githubusercontent.com/34945430/163177957-64e210c5-3fc9-49bd-8fdb-9d6217cd69b3.png)
![image](https://user-images.githubusercontent.com/34945430/163178010-897b181f-08cd-4259-a7ea-2cbf9302b449.png)

![image](https://user-images.githubusercontent.com/34945430/163178203-a6ce98bd-fc76-4127-a4b9-d8ff2e77e956.png)
![image](https://user-images.githubusercontent.com/34945430/163178285-1c13b319-a48f-4268-8c37-1a12bc9060f6.png)
![image](https://user-images.githubusercontent.com/34945430/163178394-369f9da2-3ac2-4cfd-87fa-71e5698ec77e.png)
![image](https://user-images.githubusercontent.com/34945430/163178487-6eef07d2-baf0-48a8-ad28-93e457512da6.png)

Excersise: https://docs.microsoft.com/en-us/learn/modules/build-cloud-governance-strategy-azure/4-protect-storage-account-resource-lock

![image](https://user-images.githubusercontent.com/34945430/163181760-70ba66d0-4814-4955-8bd6-e5c1b2b37f93.png)

![image](https://user-images.githubusercontent.com/34945430/163181783-12f60c51-2ab3-415f-b382-350785a25efb.png)

Tasks (Excersise):

https://docs.microsoft.com/en-us/learn/modules/build-cloud-governance-strategy-azure/6-control-audit-resources-azure-policy
https://docs.microsoft.com/en-us/learn/modules/build-cloud-governance-strategy-azure/7-restrict-location-azure-policy

Ask questions about policing and Auditoring.

https://docs.microsoft.com/en-us/learn/modules/build-cloud-governance-strategy-azure/9-accelerate-cloud-adoption-framework


# Privacy Compliance, And data protection standards

![image](https://user-images.githubusercontent.com/34945430/163184268-1a77f9e9-6c32-402f-bcec-d318cc3777c6.png)

https://docs.microsoft.com/en-gb/learn/modules/examine-privacy-compliance-data-protection-standards/2-explore-compliance-terms-requirements
https://docs.microsoft.com/en-gb/learn/modules/examine-privacy-compliance-data-protection-standards/3-access-microsoft-privacy-statement

