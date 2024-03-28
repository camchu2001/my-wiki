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

→ provide the ability to operate applications and databases that are more highly available, fault-tolerant, and scalable than they would be in a single data center. 

→ when an application is partitioned across availability zones, applications are better isolated and protected from issues. (e.g. a failure of an availability zone doesn’t affect the entire application)

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