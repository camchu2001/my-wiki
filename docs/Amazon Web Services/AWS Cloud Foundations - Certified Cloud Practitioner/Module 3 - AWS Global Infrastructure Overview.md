 > #### **Topics**
> * AWS Global Infrastructure
> * AWS service and service category overview
> #### **Demo**
> * AWS Global Infrastructure

## 1. AWS Global Infrastructure
* The **AWS Global Infrastructure** is designed and built to deliver a **flexible, reliable, scalable**, and **secure** cloud computing environment with high-quality **global network performance**. 
![](https://i.imgur.com/9xs8bUX.png)
### 1. AWS Regions
An **AWS Region** is a geographical area with one or more **Availability Zones**. An availability zone consists of one ore more data centers. 
* To achieve fault tolerance and stability, AWS regions are isolated from one another. 
	* Resources in one regions are not automatically replicated to another. 
	* It is your responsibility to replicate data across regions if your business requires it. 
	* 
> AWS regions introduced before March 20th → *enabled by default*. Any regions introduced after → disabled by default (you must enable them to use them)

#### Selecting a Region