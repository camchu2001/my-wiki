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
### 1. On Premises vs. Cloud 
1. An **on-premises** infrastructure is installed on a company’s own computers and servers. There are several **fixed costs (capital expenses)** associated with this traditional infrastructure: 
	* facilities, hardware, licenses, maintenance staff, etc
	* scaling up can be expensive and time-consuming, scaling down does not reduce fixed costs.  

To <u>evaluate</u> an on-premise solution, consider **capital expenditure** and **long planning cycles**.  

2. A **cloud infrastructure** is purchased from a ***service provider*** who builds and maintains the facilities hardware, and maintenance staff. 
	* a customer pays for what’s used, so scaling up down is simple
	* costs are easy to estimate because they depend on service use. 

To <u>evaluate</u> AWS Cloud solutions, considers flexibility, agility, **consumption-based costs**. 
### 2. Total Cost of Ownership
**Total Cost of Ownership (TCO)** is the financial *estimate* to help identify direct and indirect costs of a system. 
* TCO considers the **cost of a service + all the costs associated with owning the service**. 
![tco-considerations](https://i.imgur.com/xGrI1IZ.png)

We use TCO to: 
* **compare the costs** of running an entire infrastructure environment on specific workload **on premises vs. on AWS**. 
* to budget and making decisions for moving to the cloud. 

1. <u>**Cloud**</u>: most costs are **upfront** and **readily calculated** using metrics such as RAM, storage, bandwidth, etc. → certainty over pricing estimates. 
2. <u>**On-premises**</u>: must consider all direct and indirect costs of running, maitaining a physical server. 

<u>Example</u>: On-premises vs. All-in-cloud
→You cloud save up to **96%** a year by moving your infrastructure to AWS, saving **$159,913** total.
![](https://i.imgur.com/DkS7RnA.png)
### 3. AWS Pricing Calculator
Use the **AWS Pricing Calculator** to: 
* Estimate monthly costs. 
* Identify opportunities to reduce monthly costs. 
* Model your solutions before building them. 
* Explore price points and calculations behind your estimates. 
* Find the available instance types and contract terms that meet your needs. 
* Name your estimate and create and name groups of services. 