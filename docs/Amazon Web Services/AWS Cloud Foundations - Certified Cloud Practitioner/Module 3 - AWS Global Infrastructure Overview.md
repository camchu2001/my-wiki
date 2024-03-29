 > #### **Topics**
> * AWS Global Infrastructure
> * AWS service and service category overview
> #### **Demo**
> * AWS Global Infrastructure

## 1. AWS Global Infrastructure
* The **AWS Global Infrastructure** is designed and built to deliver a **flexible, reliable, scalable**, and **secure** cloud computing environment with high-quality **global network performance**. 
![](https://i.imgur.com/9xs8bUX.png)
### 1. AWS Regions
An **AWS Region** is a geographical area with one or more **Availability Zones**. An availability zone consists of one or more data centers. 
* To achieve **fault tolerance and stability**, AWS regions are <u>**isolated**</u> from one another. 
	* Resources in one region are not automatically replicated to another. 
	* It is your responsibility to replicate data across regions if your business requires it. 
	
> AWS regions introduced before March 20th → *enabled by default*. Any regions introduced after → disabled by default (you must enable them to use them)
#### 1. Selecting a Region
* It’s imperative to consider **data governance** and **legal requirements** when selecting an AWS region. Local laws might require that certain information be kept within geographical boundaries. 
* It’s desirable to store your data in regions that are **close to your users** as possible. → reduce the latency for users and the systems trying to access your AWS resources. 
	* To test this latency between the location and your AWS region, you can use Cloud Ping. 
* **Not all AWS services are available in all regions**. 
* There’s variation to the cost of running services, which can depend on which region you choose. 
#### 2. Availability Zones
An AWS region has **multiple isolated locations** that are known as **availability zones**. 
* They provide the ability to operate applications and databases that are more highly **available, fault-tolerant, and scalable** than they would be in a single data center. 
* When an application is partitioned across availability zones, applications are **better isolated and protected from issues**. (e.g. a failure of an availability zone doesn’t affect the entire application)

Every availability zone can **include multiple data centers**, typically **three**. Each availability zone is a **fully isolated partition** of AWS Global Infrastructure:
* There are currently 69 availability zones worldwide. 
* Availability zones consist of discrete **data centers**. 
* They are designed for fault isolation. 
* They are interconnected with other availability zones by using high-speed private networking. 
* You choose your availability zones. 
* **AWS recommends replicating data and resources across availability zones** for resiliency. 
![availability-zone|300](https://i.imgur.com/uvJ7139.png)
#### 3. AWS Data Centers
The foundation for AWS infrastructure is the **data centers**, the *location where actual data resides*. 
* Customers do not specify a data center for the deployment of a resource because **an availability zone is the most granular level of specification**. 

AWS data centers are **designed for security**. 
* Each location is evaluated to **mitigate environmental risk**. 
* Data centers are designed with failure in mind. → critical system components are **backed up** across multiple availability zones. 
* To ensure capacity, AWS monitors service usage to deploy infrastructure and support of availability. 
* Data centers **locations are not disclosed** and all access to them is restricted. 
* A data center typically has 50,000 to 80,000 physical servers. 
#### 4. Points of Presence
![](https://i.imgur.com/AvQ7dfY.png)
AWS **Points of Presence** are located in most of the major cities around the world. 
* By continuously measuring internet connectivity, performance and computing to **find the best way to route requests**, the Points of Presence deliver a better near real-time user experience.
* They are used by many AWS services, including **Amazon CloudFront**, **Amazon Route 53**, AWS Shield, and AWS Web Application Firewall (AWS WAF) services.
* Consists of **edge locations** and a much smaller number of **Regional edge caches**. 

1. **Edge locations** are endpoints for CloudFront where content is cached and delivered to end users.
	* When a user requests content, CloudFront routes the request to the nearest edge location. 
	* If the content is already cached at that edge location, CloudFront delivers it directly to the user. 
	* If the content is not cached, CloudFront retrieves it from the origin server and then delivers it to the user.
2. **Regional edge caches** are used by default with Amazon CloudFront. 
	* Used when you have content that is not accessed frequently enough to remain in an edge location.
	* Regional edge caches absorb this content and provide an alternative to that content having to be fetched from the origin server.

> - **Amazon CloudFront**, a content delivery network used to distribute content to end-users in order to *reduce latency*. 
> - **Amazon Route 53** is a Domain Name System (DNS) service. 
> - Requests going to either one of these services will be routed to the nearest edge location automatically in order to lower latency.
#### 5. AWS Infrastructure Benefits
* **Elasticity and scalability**: 
	* Elastic infrastructure, dynamic adaption of capacity. 
	* Scalable infrastructure, adapts to accommodate growth. 
* **Fault-tolerance**: 
	* Continues operating properly in the presence of a failure. 
	* Built-in redundancy of components. 
* **High availability**: 
	* High level of operational performance.
	* Minimized downtime
	* No human intervention
## 2. AWS Services & Service Category
![](https://i.imgur.com/vltGW6m.png)
### 1. AWS Foundational Services
**AWS Global Infrastructure** can be broken down into three elements: **Regions, Availability Zones, and Points of Presence**, which include edge locations.
* Provides the platform for a broad set of services, such as networking, storage, compute services, and databases. 
* Delivered as an on demand utility that is available in seconds, with pay-as-you-go pricing. 
### 2. AWS Categories of Services
![](https://i.imgur.com/x8kcd9P.png)

There are **23** different product or service categories, and each category consists of one or more service.
#### 1. <u>Storage</u> Service Category
* **Amazon Simple Storage Service (Amazon S3)**, object storage service offering scalability data availability, security, and performance. 
* **Amazon Elastic Block Store (Amazon EBS)**, high performance block storage designed for use with Amazon EC2, for both *throughput and transaction-intensive* workloads.
* **Amazon Elastic File System (Amazon EFS)**, scalable fully managed elastic network file system (NFS), for use within AWS Cloud Services and on-premise resources. 
* **Amazon Simple Storage Services Glacier**, secure, durable, and extremely low cost AWS S3 Cloud storage class for data archiving and long-term *backup*. 
#### 2. <u>Compute</u> Service Category
* **Amazon Compute Cloud (Amazon EC2)**, provides resizable compute capacity as virtual machines in the cloud. 
* **Amazon EC2 Auto Scaling Service**, enables automatically adding/removing EC2 instances according to the conditions that you define. 
* **Amazon Elastic Container Service (Amazon ECS)**, highly scalable, highly performance  container orchestration service that provides *Docker containers*. 
* **Amazon EC2 Container Registry (Amazon ECR)**, is a fully managed Docker container registry that makes it easier to store, manage, and deploy Docker container images. 
* **AWS Elastic Beanstalk**, a service for deploying and scaling web applications and services on familiar servers (Apache, Microsoft IIS).  
* **AWS Lambda**, enables you to run your code without provisioning or managing servers and pay only when your code is running. 
* **Amazon Elastic Kubernetes Service (Amazon EKS)**, makes it easy to deploy, manage, and scale containerized applications that use Kubernetes on AWS. 
* **AWS Fargate**, a compute engine for Amazon ECS, allows running containers  without having to manage servers/clusters. 
#### 3. <u>Database</u> Service Category
* **Amazon Relational Database Service (Amazon RDS)**, relational database in the cloud, providing resizable capacity while automating time-consuming administration (hardware provisioning, database setup, patching, and backups). 
* **Amazon Aurora**, a MySQL and PostgreSQL compatible relational database, set up to be 5 times faster than standard MySQL databases, 3 times faster than PostgreSQL databases. 
* **Amazon Redshift**, enables running analytic queries against petabytes of data stored locally in Amazon, delivers fast performance at any scale. 
* **Amazon DynamoDB**, NoSQL database that delivers single-digit millisecond performance at any scale with built-in security, backup, and restore, and in-memory caching. 
#### 4. <u>Networking & Content Delivery</u> Service Category
* **Amazon Virtual Private Cloud (Amazon VPC)**, enables provision of logically isolated sections of the AWS Cloud to launch AWS resources in a virtual network that you define. 
* **Elastic Load Balancing**, automatically distributes incoming application traffic across multiple targets (Amazon EC2 instances, containers, IP addresses, Lambda functions). 
* **Amazon CloudFront (CDN)**, delivery network that security delivers data, videos, applications, and application programming interfaces (APIs), to customer globally with low latency and high transfer speed. 
* **Amazon Transit Gateway**, connect Amazon Virtual Private Cloud and on-premises networks to a single centrally managed gateway. 
* **Amazon Route 53**, scalable cloud domain name system web service to reliably route end suers to the Internet application. (DNS)
* **AWS Direct Connect**, establish a dedicated private network connection, from your data center/office to AWS → to reduce costs and increase bandwidth throughput. 
* **AWS VPN**, provides a private tunnel for network/device to the AWS global network. 
#### 5. <u>Security, identity, and compliance</u> Service Category
* **AWS Identity and Access Management (IAM)**, manage access to AWS services and resources securely. 
* **AWS Organizations**, restrict what services and actions are allowed in your accounts. 
* **Amazon Cognito**, allows adding user authentication and access control to your web and mobile apps. 
* **AWS Artifact**, provides on-demand access to AWS security and compliance reports, online agreements. 
* **AWS Key Management Service (AWS KMS)**, create/manage encryption keys. 
* **AWS Shield**, safeguards application running on AWS. 
#### 6. <u>Cost Management</u> Service Category
* **AWS Cost and Usage Report**, *comprehensive* set of AWS cost usage data available. 
* **AWS Budgets**, set custom budgets alert when AWS costs/usage exceeds budgeted amount. 
* **AWS Cost Explorer**, visualize and manage AWS cost and usage overtime.
#### 7. <u>Manage and Governance</u> Service Category
* **AWS Management Console**, web-based user interface for accessing your AWS account. 
* **AWS Config**, helps track resource inventory and changes. 
* **AWS Cloud Watch**, monitor resources and applications. 
* **AWS Auto Scaling**, allows scaling multiple resources to meet demand. 
* **AWS Command Line Interface (AWS CLI)**, unified tool to manage AWS services. 
* **AWS Trusted Advisor**, online tool to help optimize performance and security using AWS best practices. 
* **AWS Well-Architected Tool**, help reviewing and improving workloads. 
* **AWS Cloud Trail**, tracks users’ activities and API usage across AWS accounts

