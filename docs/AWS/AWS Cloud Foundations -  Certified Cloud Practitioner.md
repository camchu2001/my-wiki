**This contains all my notes from the official AWS Academy Cloud Foundations course. Hopefully, this help you prepare for the [AWS Certified Cloud Practitioner](https://aws.amazon.com/certification/certified-cloud-practitioner/) exam.**
# 1. Module 1 - Cloud Concepts Overview
> #### **Topics**
> * Introduction to cloud computing
> * Advantages to cloud computing 
> * Introduction to Amazon Web Services (AWS)

> * AWS Cloud Adoption Framework (AWS CAF)
## 1. Introduction to Cloud Computing
> **Resources**
> - [Types of Cloud Computing](https://aws.amazon.com/types-of-cloud-computing/)
### 1. Definition 
**Cloud computing** is the **on-demand** delivery of computer power, database, storage, applications, and other IT *resources* **via the internet** with **pay-as-you-go** pricing.

These *IT resources* run on server computers located in large data centers in numerous locations of the world. 
→ When we use AWS cloud services, we’re using the computers owned by that service provider. 

* In a ***traditional computing model***, you need to manage and maintain the hardware infrastructure for your software, which require spaces, staff, physical security, lots of planning, and money, etc. 
→ This approach can be labor-intensive, expensive and time-consuming.
* ***Clouding computing model*** enables you to think as your infrastructure as software. 
	* It is *flexible*, allowing you to select cloud services that best match your needs. 
	* You only pay for what you use, when you use it, so you can *scale resources* up and down to match your demand. 
→ These IT resources as treated as temporary and disposable, allowing you to implement solutions quickly with low up-front cost. 
### 2. Cloud Service Models
![cloud-service-models | 600](https://i.imgur.com/LEublfp.png)

There are ***three*** main cloud service models:

1. <u> **IaaS - infrastructure as a service**</u>
* **Basic building blocks** for cloud information technology. 
* Provides users with a resource-based service via **virtualization technology** (*creating multiple virtual servers on a single physical server*), offering computing infrastructure, physical or (more often) virtual machines and other resources.
* **Highest level of flexibility** and control over IT resources. 

> You rent a virtual server from AWS, which is a server that exists entirely in the cloud. You configure the virtual server’s operating system, software application, security aspects, etc. 

2. <u>**PaaS - platform as a service**</u>
* Provides environments for **developing**, **testing**, and **managing applications**, it is utilized for software development and **offers a platform** to developers to build applications and services over the internet.
* Removes the need for managing the underlying infrastructure such as **hardware** and **operating system**.
* Has a **higher level of abstraction**, hiding the complexities of server management, allowing you to focus on deployment and management of the application. 

> AWS manages the virtual server and operating system for you. The environments and tools can be pre-configured for specific programming languages and frameworks. You simply upload the application code and the platform takes care of the rest. 

3. <u>**SaaS - software as a service**</u>
* Provides you with a **complete product** that is run and managed by the service provider. 
* In most cases, this refers to end-user applications (designed to be used directly by users who aren't involved in its development or maintenance).
* No need to think/know about how the service is maintained or how the underlying infrastructure is managed. → only **how you will use** the service.
* <u>Example</u>: web-based email application (Gmail, Outlook, iCloud Mail)
### 3. Cloud Computing Deployment Models
![cloud-deployment-models | 600](https://i.imgur.com/BuPaDPy.png)
There are three main cloud computing deployment models, each representing the cloud environment that your applications can be deployed in. 
1. <u>**Cloud (public cloud)**</u>: the **most common** type of cloud computing deployment. 
	* A cloud-based application is **fully deployed in the cloud**, all parts of the application will be running in the cloud.
	* The cloud resources (like servers and storage) are owned and operated by the cloud service provider and delivered over the internet→ we don’t manage any physical infrastructure.
2. <u>**Hybrid**</u>: connect your existing *on-premise* infrastructure and application to *cloud-based resources*. 
	* <u>*Example*</u>: Having your own physical servers and connecting them to AWS services. 
3. <u>**On–premises (private cloud)**</u>:
	* It uses *virtualization* and resource management tools to try and increase resource utilization.
	* While on-premises deployment does not provide many of the benefits of cloud computing, it’s sometimes sought for its ability to provide dedicates resources, strict data privacy, direct control over resources. 
	* <u>*Example*</u>: Having your own servers that you physically manage within your own facility or through a third-party data center. 
### 4. AWS vs. Traditional IT
![aws-and-traditional-it](https://i.imgur.com/IgcrpbZ.png) 
## 2. Advantages of the Cloud
1. <u>**Trade capital expenses for variable expense** </u>
![capital-variabl-expenses | 500](https://i.imgur.com/dOq6Xor.png)

* **Capital expenses (CapEx)**: **up-front** costs associated with acquiring, improving, maintaining physical assets (e.g.: buildings, machinery, equipment, vehicles, furniture, or computer hardware.) → *you pay for everything in the data center whether you use it or not.*
* **Variable expenses (VarEx)**: costs that fluctuate/change in proportion to a specific business activity or production level. → *you only pay when you consume resources and for the amount that you use.*
<br>
2. <u>**Massive economies of scale**</u>
	* Because of aggregate usage from all customers, AWS can achiever higher economies of scale and pass savings onto customer. 
	→ *Using cloud computing can help achieve a **lower variable cost** than what you can get on your own.* 
3. <u>**You can stop guessing capacity**</u>
	* Cloud computing eliminates guessing about your infrastructure capacity needs because you access as much or as little as you need, scaling up and down as required with only a few minutes notice. 
4. <u>**Increase speed and agility**</u>
	* In a cloud computing environment, information technology resources allocation is only a click away. 
	→ reduces the time it takes to make those resources available. 
5. <u>**Stop spending money on running/maintaining data center**</u>
	* Saves you the trouble of having to focus too much on infrastructure, allowing you to focus on software development. 
6. <u>**Go global in minutes**</u>
	* You can easily deploy your application in multiple AWS regions around the world. 
	→ provide lower latency and better experience for user. 
## 3. Introduction to AWS
### 1. Web Services
A **web service** is any piece of software that makes itself available over the internet and uses a **standardized format** - such as Extensible Markup Language (XML) **or** JavaScript Object Notation (**JSON**) - for the **request** and **response** of an **application programming interface (API) interaction.** 
![web-services](https://i.imgur.com/eIEOLM4.png)
### 2. Amazon Web Service
* AWS is a **secure cloud platform** that offers an ecosystem of **global cloud-based products** (e.g. EC2, S3, RDS, etc). 
* AWS provides you with **on-demand access** to computer, storage, network, database, and other IT resources and management tools. 
* AWS offers **flexibility**, AWS environment can be reconfigured, update on demand, scaled up/down automatically to meet usage patterns. 
* You to only pay for the individual services you need, for as long as you use them.
* **AWS services** work together like building blocks, you interconnect them, building scalable solutions to support your application. 
### 3. Categories of AWS Services
**AWS services fall under different categories. Each category contains one or more services that you can choose from to build your solutions.**
![aws-services | 700](https://i.imgur.com/5VvUTkD.png)

![notable-services | 700](https://i.imgur.com/QjHBCij.png)
### 4. Ways to interact with AWS
1. <u>**AWS Management Console**</u>: you use a **user interface** to the web browser to access the majority of the services and features of those services. 
2. <u>**AWS Command Line (AWS CLI)**</u>: a way of scripting your interaction with the ecosystem It provides utilities that can be launched from a command script. → you access services by discrete **commands or scripts.**
3. <u>**Software Development Kits (SDKs)**</u>: you access services **directly from your code**. 
## 4. Moving to the AWS Cloud
<u>**AWS Cloud Adoption Framework (AWS CAF)**</u>: is a document that **provides guidance and best practices** to help businesses and their organizations have a structured approach to achieving successful cloud adoption. → basically a ***road map***
* AWS CAF is organized into **6 areas of focus (6 perspectives)**: 
	* business, people, governance → **business** capabilities
	*  platform, security, operations → **technical** capabilities
* Each perspective consists of sets of **capabilities**, which covers different responsibilities that are owned/managed by cross-functional teams. → **specific guidance and steps** to help organizations navigate that particular aspect of their cloud adoption journey.
![perpectives | 700](https://i.imgur.com/7OxK8my.png)
# 2. Module 2 - Cloud Economics and Billing
> #### **Topics**
> * Fundamentals of pricing
> * Total Cost of Ownership 
> * AWS Organizations
> * AWS Billing and Cost Management
> * Technical Support
> #### **Demo**
> * Overview of the Billing Dashboard
> #### **Activities**
> * AWS Pricing Calculator
> * Support plans scavenger hunt
## 1. Fundamentals of pricing
### 1. AWS Pricing Model
There are 3 **fundamental drivers** of cost with AWS. 
1. **Compute**: charged **per hour**/second (for Linux) and **varies by instance type**. 
2. **Storage**: charged typically **per GB**. 
3. **Data transfer**: charged typically **per GB**. 
	* In most cases, there is **no charge for inbound data transfer**, data that you put into AWS is free. Data transfer between services in the same region is also free.
	* For outbound data transfers, it is **aggregated across services** and **charged at the outbound data transfer rate**. 
### 2. Pay for AWS
1. <u>**Pay for what you use**</u>: 
	* At the end of each month, you only pay for the service that you consume for as long as you use it, with no large upfront-expenses. 
	* All services are available on demand, so you can **start/stop using a service at any time**, as there are no long term contracts required. 
2. <u>**Pay less by using more**</u>:
	* You can get volume based **discounts as your usage increases**. 
	* **Tiered pricing** for services like Amazon Simple Storage Service (Amazon S3), Amazon Elastic Block Store (Amazon EBS), or Amazon Elastic File System (Amazon EFS) → ***the more you use, the less you pay per GB.*** 
	* Multiple storage services offer options to help **lower pricing** based on your needs and how frequently you access your data. 
3. <u>**Pay even less as AWS grows**</u>:
	* AWS passing savings from economies of scale to you. 
	* Since 2006, AWS has lowered pricing 75 times (as of September 2019). 
	* Future higher-performing resources replace current resources for no extra charge. 
4. <u>**Custom pricing**</u>: is available if the current pricing models don’t work for your project. 
5. <u>**AWS Free Tier**</u>: enables you to gain **free hands-on experience** with the AWS platform, products, and services. It’s free for 1 year for new customers. 
	* **Services with no charge**: Amazon VPC, Elastic Beanstalk, Auto Scaling, AWS CloudFormation, AWS Identity and Access Management. 
	* There might be charges associated with other AWS services that are used with these services. 
## 2. Total Cost of Ownership
