# Understanding AWS Core Services

Created: July 27, 2021 10:37 PM
Tags: CLF-C01, certifications, pluralsight

<aside>
2️⃣ This is part two of the CLF-C01 Pluralsight path

</aside>

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled.png)

# Course Overview

This course will cover services that we need to know before taking the Cloud Certified Practitioner exam - covering:

- Ways we interact with AWS services
- Major categories, including compute, networking and content delivery, file storage, databases, app integration, and management and governing services
- Preparing for the certification exam

---

# Interacting with AWS

<aside>
🗓️ Wednesday 28th July 2021

</aside>

## Overview

This course includes interactive exercise files, with guided notes and study guide, and AWS Services lists.

## Methods of Interacting with AWS

There are 3 different ways to interact with AWS:

1. AWS Console - Users can leverage their browser to configure resources
2. AWS CLI - Command line access for administering AWS resources
3. AWS SDK - Programmatic access to manager AWS resources

> ***AWS Management Console** - a web and app based interface for interacting with most of the 150+ AWS services. All major browsers and mobile operating systems are supported.*
> 

> ***AWS Command Line Interface (CLI)** - a tool to manage your use of AWS services from the command line on Windows, Mac and Linux. Most every task that can be done in the console can be done with the CLI.*
> 
- Example command to list users: aws iam list-users

> ***AWS Software Developer Kit (SDK)*** - Programming language-specific resources that allow you to interact with AWS services via code. This approach enables you to automate many aspects of how you interact with the platform.
> 

![AWS SDK Supported Languages](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%201.png)

AWS SDK Supported Languages

### Interacting with AWS

- Console is a great method for testing out AWS services
- Repeating tasks can be automated using the CLI or SDK
- SDK enables automation of AWS tasks within custom applications
- Most all services and actions can be performed in any of the three

## Using the AWS Console

In this demo, we'll be:

- Accessing the AWS Console in the browser
- Reviewing login differences for root and IAM users
- Selecting a specific region
- Reviewing the list of services supported in the AWS Console

By modifying the dropdown for region in the console, it will change the context the console is operating in. For example, selecting a different region will change the region we launch new resources in. This affects **most** services. 

We can use the search box to search for services.

For Route 53, region is not applicable, as it is a global service - signified in the dropdown. 

## Using the AWS CLI

In this demo, we'll be:

- Accessing AWS Access keys
- Reviewing installation instructions for the CLI
- Configuring the AWS CLI for a specific user
- Interacting with AWS utilizing the CLI

FYI: DO NOT CREATE ROOT USER ACCESS KEYS, CREATE AN IAM USER INSTEAD

Username > Security Credentials

Select 'Access keys'

Create an Access Key

**CLI Install Guide**

[https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)

## Scenario Based Review

### Scenario 1

- Roger's company runs several production workloads in AWS
    - They have a new web application that manages digital assets for marketing
    - They need to automatically create a user account in Amazon Cognito on sign-up
    - They want this step seamlessly integrated into the application
- Which interaction method would Roger's company use for this?

<aside>
✅ AWS Software Developer Kit (SDK)

</aside>

### Scenario 2

- Eliza's company is condidering transitioning to AWS
    - They want to leverage Amazon Relational Database Service
    - Eliza wants to test out a single database on the service
- What interaction method would Eliza use for this use case?

<aside>
✅ AWS Console

</aside>

### Scenario 3

- Jennifer's company is a startup
    - They created a social network for entrepreneurs with a web and mobile app
    - Jennifer has a set of tasks she needs to run on AWS each day to generate reports
- What interaction method would Jennifer use for this use case?

<aside>
✅ AWS Command Line Interface (CLI)

</aside>

## Summary

In this module, we have:

- Reviewed the ways you interact with AWS services
- Explored the AWS Console and its use
- Introduced the AWS Command Line Interface and its use
- Introduced the AWS Software Developer Kit and supported languages

---

# Compute Services

<aside>
🗓️ Wednesday 28th July 2021  |  Thursday 29th July 2021

</aside>

## Overview

> ***Compute Services** - A service that enables you to leverage cloud-based virtual machines for workloads. This could be serving web content to visitors, running a database, or calculating statistics from a data set.*
> 

We'll be looking at :

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%202.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%202.png)

- Amazon EC2 - a core, foundational service of AWS, that lets us run virtual servers.
- AWS Elastic Beanstalk (Paas) - a platform for scaling and deploying web apps and services
- AWS Lambda - Enables compute without managing any servers

We'll also be covering:

- Introducing Amazon EC2 capabilities
- Exploring pricing approaches for EC2 instances
- Introducing the capabilities of AWS Elastic Beanstalk
- Reviewing use cases for Elastic Beanstalk
- Introducing AWS Lambda

## Amazon EC2 Overview

EC2 is one of the fundamental, core services of AWS.

> ***Amazon Elastic Compute Cloud (Amazon EC2)** is a web service that provides resizable compute capacity in the cloud. It is designed to make web-scale computing easier for developers. - Amazon Web Services*
> 

### Amazon EC2 Use Cases

- Web application hosting
- Batch processing of data
- Web services endpoint
- Desktop in the cloud

### Amazon EC2 Concepts

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%203.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%203.png)

### Amazon EC2 Instance Types

- Defines the processor, memory and storage type
- Cannot be changed without downtime
- Provided in the following categories
    - General purpose
    - Compute, memory, and storage optimized
    - Accelerated computing
- Pricing is based on instance type
- Some instance types have unique capabilities

**Pricing**

*Can vary over time, and by region*

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%204.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%204.png)

### Root Device Type

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%205.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%205.png)

Most work on EC2, we'll want to use EBS, unless we have a specific reason not to. 

### Amazon Machine Image (AMI)

*Note, this can be pronounced A.M.I or AMY*

- Template for an EC2 instance including configuration, operating system, and data
- AWS provides many AMI's that can be leveraged
- AMI's can be shared across AWS accounts
- Custom AMI's can be created based on your configuration
- Commercial AMI's area available in the AWS Marketplace

## Amazon EC2 Purchase Types

![AWS EC2 Purchase Options Diagram](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%206.png)

AWS EC2 Purchase Options Diagram

### Reserved Instances

> ***Reserved instances** - Provides discounts over the on-demand model when you can commit to a specific period of time (1 or 3 years). In addition, it provides a capacity reservation for the specific instance type that you specify.*
> 

**Types of Reserved Instance**

- **Standard**: Highest discount, works for steady workloads. The instance type is locked in for the reservation period
- **Convertible**: Enables the conversion of attributes, works for steady workloads. Attributes are convertible up to the equal value of the reserved instance
- **Scheduled**: Works for a time window you reserve, good for a predictable workload

**Standard Reserved Instance Cost Models**

- **All Upfront**: Entire cost for the 1 or 3 year period is paid upfront. Highest level of savings, but the biggest upfront investment
- **Partial Upfront**: Part of the 1 or 3 year cost is paid upfront along with a reduced monthly cost
- **No Upfront**: No upfront payment is made, but there will be a reduced monthly cost

### Savings Plan

- Similar in concept to reserved instances
- Supports compute with EC2, Fargate, and Lambda
- Unlike Reserved Instances, it does not reserve capacity
- Provide savings of up to 72%
- Comes in 1 or 3 year terms

### Spot Instances

> ***Spot instances** - Enable you to leverage excess EC2 compute capacity, that might exist within an availability zone.*
> 
- Can provide up to 90% discount over on-demand pricing
- There is a market price for instance types per availability zone called the Spot price
- When you request instances, if your bid is higher than Spot price they will launch
- If the Spot price grows to exceed your bid, the instances will be terminated
- Spot instances can be notified 2 minutes prior to termination

**This can only work for workloads that can start and stop immediately, without affecting what we're trying to do**

### Dedicated Host

> ***Dedicated Host** - The dedicated host pricing model gives you a dedicated physical server. It will be the most expensive option, but it may be required for either server software licensing or do to a compliance requirement.*
> 

### Amazon EC2 Purchase Options Review

- If you have an instance that is consistent and always needed, you should purchase a Standard or Convertible Reserved Instance
- If you have batch processing where the process can start and stop without affecting the job, you should leverage Spot Instances
- If you have an inconsistent need for instances that cannot be stopped without affecting the job, leverage On-Demand Instances
- If you have specific per-server licensing or if you have a compliance requirement for a dedicated server, you should use Dedicated Host
- If you are leveraging Lambda and/or Fargate alongside EC2 and want to achieve discounts for 1 or 3 years, choose a Savings Plan
- If you have a predictable but not steady workload in EC3, you should purchase a Scheduled Reserved Instance

### Reserved Instance EC2 Pricing Example

![Pricing subject to change](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%207.png)

Pricing subject to change

### Spot Instance EC2 Pricing Example

![Pricing subject to change](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%208.png)

Pricing subject to change

## Launching EC2 Instances

We'll need to understand EC2 for the exam, but not necessarily have experience launching an EC2 Instance. This module gives us a practical demo of launching a new AWS EC2 Instance to help us better understand the procedure. 

This demo will cover:

- Launching a new EC2 Instance based on an AWS AMI
- Exploring the EC2 launch wizard in the AWS Console
- Configuring an EC2 Instance to be used as a web server
- Terminating an EC2 Instance

### Launch Procedure

1. To launch an EC2 Instance, we need to navigate to dashboard and search for EC2, which will take us to the launch console
2. From the launch console, we need to select '**Select Launch Instance**'
3. From this page, we can choose an AMI, we're selecting the **Amazon Linux 2 AMI**, as it is free-tier eligible
4. We need to choose an instance type - we're using the **t2.micro** type, as it is free-tier eligible
5. After choosing our type, we can select '**Configure Instance Details**'.
6. In the instance details screen, we can choose how many instances we want, and if we would like it to be a spot instance:

![Instance qty & purchasing options](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%209.png)

Instance qty & purchasing options

1. We're going to choose a network, leave the default subnet and request a public IP address, so we can access our web server:

![Instance network settings](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2010.png)

Instance network settings

1. We're going to leave everything else as is, and scroll down to '**Advanced Details**'. In this section we're going to choose '**Text**', and enter a command to install a basic web server

![Installing a basic web server](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2011.png)

Installing a basic web server

1. After configuring the instance details, we're going to select '**Add Storage**', and assess the storage option

![Storage selection screen](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2012.png)

Storage selection screen

1. Then navigate into '**Tags**', and assign a tag

![Tag selection screen](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2013.png)

Tag selection screen

1. Then we'll configure the '**Security Group**'. We'll be limiting access to login to and manage the server to just our IP (**My IP**), then add an additional rule to allow HTTP traffic from anywhere

![Security group configuration screen](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2014.png)

Security group configuration screen

1. Finally, we'll review the summary page, and hit '**Launch**' 

![Instance configuration summary page](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2015.png)

Instance configuration summary page

1. To be able to manage the server, we'll need to create a key pair, download it, and save it out

![Key Pair creation/selection screen](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2016.png)

Key Pair creation/selection screen

After downloading the key pair, we can launch the instance

1. This tool tip shows us that we have successfully launched an instance, and we can select the id value to see the instance status:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2017.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2017.png)

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2018.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2018.png)

1. To test our web server, we can copy our DNS name to the clipboard, and navigate to it! 

![Web server test page](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2019.png)

Web server test page

1. To destroy our instance, we need to select it in the Instance dashboard, select '**Instance State**' and '**Terminate Instance**'. To confirm the destruction of the instance, we will select '**Terminate**'

![Instance termination confirmation screen](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2020.png)

Instance termination confirmation screen

## AWS Elastic Beanstalk Overview

- Automates the process of deploying and scaling workloads on EC2 (Pass)
- Supports a specific set of technologies
- Leverages existing AWS servicews
- Only pay for the other services you leverage
- Handles provisioning, load balancing, scaling, and monitoring

### Supported Application Platforms

- Java
- .NET
- PHP
- Node.js

- Python
- Ruby
- Go
- Docker

### Elastic Beanstalk Features

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2021.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2021.png)

### Elastic Beanstalk Use Cases

- Deploy an application with minimal knowledge of other services
- Reduce the overall maintenance needed for the application
- Few customizations are required

## Launching an App on Elastic Beanstalk

In this demo, we'll be:

- Accessing the sample Elastic Beanstalk applications
- Launching a sample application on Elastic Beanstalk
- Deleting a deployed Elastic Beanstalk application

### Creation Procedure

1. Download a sample application from: [https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/tutorials.html](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/tutorials.html)
    
    We're choosing **node.js**
    
2. Open the AWS Console, and navigate to **Elastic Beanstalk**
3. Select '**Create Application**' 
4. Name the application:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2022.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2022.png)

1. Select a platform type:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2023.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2023.png)

6: Check 'Upload your code' and upload the zip

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2024.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2024.png)

1. Select '**Configure more options**'
2. We're leaving all values in place, and ensuring that we're on a Free Tier Eligible Instance:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2025.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2025.png)

1. Select '**Create app**'
2. The onscreen console will display the process of launching the application:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2026.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2026.png)

1. Once the application has loaded, we will see an application dashboard:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2027.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2027.png)

1. We can navigate to our application, using the included url: [http://sampleapp-env.eba-jts2nned.eu-west-2.elasticbeanstalk.com/](http://sampleapp-env.eba-jts2nned.eu-west-2.elasticbeanstalk.com/)

### Elastic Beanstalk Dashboard Options

We can view logs:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2028.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2028.png)

We can view the instances health: 

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2029.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2029.png)

We can look at monitoring for our application:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2030.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2030.png)

We can configure alarms too:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2031.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2031.png)

### Destruction Procedure

1. We can destroy our application by selecting '**Actions**' > '**Terminate Environment**':

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2032.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2032.png)

1. We then enter the name of the environment, and select '**Terminate**':

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2033.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2033.png)

1. After the environment has terminated, we can delete it by selecting the application, selecting '**Actions**', then '**Delete application**'

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2034.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2034.png)

1. We then enter the application name, and select 'Delete'

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2035.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2035.png)

## AWS Lambda Overview

> ***AWS Lambda** lets you run code without provisioning or managing servers. You pay only for the compute time you consume. You can run code for virtually any type of application or backend service - all with zero administration. - Amazon Web Services*
> 
- Enables the running of code without provisioning infrastructure
- Only charged for usage based on execution time
- Can configure available memory from 128MB to 3008MB
- Integrates with many AWS services
- Enables event-driven workflows (when x happens do y)
- Primary service for serverless architecture

### AWS Lambda Advantages

- Reduced maintenance requirements
- Enables fault tolerance without additional work
- Scales based on demand
- Pricing is based on usage

## Scenario Review

### Scenario 1

- Sylvia's company is in the process of moving multiple workloads into AWS
    - One workload is an application that will be leveraged for at least 5 more years
    - The organization is looking to be as cost efficient as possible for its EC2 usage
- What EC2 purchase option should be chosen for this application?

<aside>
✅ Reserved Instance (All Upfront - 3 Years)

</aside>

### Scenario 2

- Edward is looking to deploy his PHP web application to a virtual server
    - He doesn't have experience managing EC2 instances on AWS
    - He needs the ability to scale this application to meet user demand
- What is the best compute option for Edward based on this criteria?

<aside>
✅ AWS Elastic Beanstalk

</aside>

### Scenario 3

- Cindy's company is transitioning to the cloud for its data processing workloads
    - These workloads happen daily and can start or stop without a problem
    - This workload will be leveraged for at least one year
- What EC2 purchase option would be the most cost efficient choice?

<aside>
✅ Spot Instances

</aside>

## Summary

In this module, we have:

- Introduced Amazon EC2 capabilities
- Explored pricing approaches for EC2 instances
- Introduced the capabilities of AWS Elastic Beanstalk
- Reviewed use cases for Elastic Beanstalk
- Introduced AWS Lambda

---

# Content and Network Delivery Services

<aside>
🗓️ Thursday 29th July 2021  |  Friday 30th July 2021

</aside>

## Overview

Networking & Content Delivery Services refers to six different services:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2036.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2036.png)

Inside this module, we'll be:

- Introducing Virtual Private Clouds on AWS
- Understanding the purpose of AWS Direct Connect
- Examining DNS with Amazon Route 53
- Reviewing Amazon CloudFront
- Reviewing API Gateway
- Introducing Elastic Load Balancing and scaling approaches.

## Amazon VPC and Direct Connect

### Amazon VPC

> ***Amazon Virtual Private Cloud (VPC)** is a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define.*
> 
- Enables virtual networks in AWS
- Supports IPv4 and IPv6
- Allows for configuration of
    - IP address range
    - Subnets
    - Route tables
    - Network gateways
- Supports public & private subnets
- Can utilize NAT for private subnets
- Enables a connection to your data center
- Can connect to other VPC's
- Supports private connections to many AWS services

### AWS Direct Connect

> ***AWS Direct Connect** is a cloud service solution that makes it easy to establish a dedicated network connection from your data center to AWS.*
> 

## Amazon Route 53

- Domain name service (DNS)
- Global AWS service (not regional)
- Highly available (minimal downtime)
- Enables global resource routing

> ***DNS** translates more readily memorized domain names to the numerical IP addresses needed for the locating and identifying computer services and devices with the underlying network protocols. - Wikipedia*
> 

In the console, Route 53 is marked as 'Global' - 'Route 53 does not require region selection.'

DNS changes take time to propagate globally. 

We can configure Route 53 to have automatic failover, pointing traffic from an unavailable region to an available one. 

## Elastic Load Balancing

> ***Elasticity** is the ability for the infrastructure supporting an application to grow and contract based on how much it is used at a point in time.*
> 

To route users to the correct infrastructure, we can use Elastic Load Balancing.

### Elastic Load Balancing

- Distributes traffic across multiple targets
- Integrates with EC2, ECS, and Lambda
- Supports one or more AZ's in a region
- Has three types of load balancers:
    - Application Load Balancer (ALB)
    - Network Load Balancer (NLB)
    - Classic Load Balancer (Classic / ELB)

### Scaling on Amazon EC2

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2037.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2037.png)

Vertical Scaling is changing the instance type to a larger one. 

Horizontal Scaling is adding additional instance clones to handle the the application load. 

**Horizontal Scaling is the preferred choice, as it incurs no downtime.** 

## Amazon CloudFront and API Gateway

### Amazon CloudFront

- Content delivery network (CDN)
- Enables users to get content from server closest to them
- Supports static and dynamic content
- Utilizes AWS Edge Locations
- Includes advanced security features
    - AWS Shield for DDoS
    - AWS Web Application Firewall (WAF)

CloudFront leverages the AWS Edge Locations to deliver your content globally in a matter of minutes.

![AWS Edge Location Map](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2038.png)

AWS Edge Location Map

### Amazon API Gateway

- Fully managed API management service
- Directly integrates with multiple AWS services
- Provides monitoring & metrics on API calls
- Supports VPC and on-premise private applications

## AWS Global Accelerator

> *AWS Global Accelerator is a networking service that sends your user's traffic through Amazon Web Service's global network infrastructure, improving your internet user performance by up to 60%. - Amazon Web Services*
> 
- Utilizes IP addresses that route to edge locations
- Once request reaches edge locations, traffic is routed through AWS network
- Can route requests to many AWS resources:
    - Network Load Balancer (NLB)
    - Application Load Balancer (ALB)
    - EC2 Instances
    - Elastic IP address

### Performance Improvements

- Distance between user and initial endpoint is minimized by using edge locations
- Traffic is optimized by using AWS network instead of public Internet
- Results in improvement of first byre latency, jitter, and throughput
- Provides superior fault tolerance by not relying on DNS resolution

### AWS Global Accelerator Use Cases

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2039.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2039.png)

- UPD = Gaming / MWTT = IOT, VOIP = Voice

## Scenario Based Review

### Scenario 1

- Jane's company maintains two corporate data centers
    - They want their data centers to work alongside AWS for specific workloads
    - She is wondering if there is a way to have a persistent connection to AWS
- What service from AWS would you recommend her company implement?

<aside>
✅ AWS Direct Connect

</aside>

### Scenario 2

- Tim's company serves content through their site to users around the globe
    - They are looking to optimize performance to users around the world
    - They want to leverage a Content Delivery Network (CDN)
- Which service would enable optimized performance globally for their content?

<aside>
✅ Amazon CloudFront

</aside>

### Scenario 3

- Ellen's company has an internal application that runs on an EC2 server
    - Currently there is downtime as demand is greater than capacity for the server
    - Ellen is trying to decide if she should use bigger servers or more servers
- Which scaling approach would you recommend and what services should they use?

<aside>
✅ Horizontal Scaling & Elastic Load Balancing

</aside>

## Summary

In this module, we have:

- Introduced Virtual Private Clouds on AWS
- Understood the purpose of AWS Direct Connect
- Examined DNS with Amazon Route 53
- Reviewed Amazon CloudFront
- Reviewed API Gateway
- Introduced Elastic Load Balancing and scaling approaches

---

# File Storage Services

<aside>
🗓️ Friday 30th July 2021

</aside>

## Overview

The file storage services in AWS are:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2040.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2040.png)

In this module, we'll be:

- Reviewing the storage services on AWS
- Examining Amazon S3 and its capabilities
- Implementing a static website on Amazon S3
- Exploring archive capabilities with Glacier and Glacier Deep Archive
- Reviewing EC2 storage with EBS and EFS
- Examining large-scale data transfer services into AWS

## Amazon S3 Overview

> ***Amazon Simple Storage Service (S3)***
> 
- Stores files as objects in buckets
- Provides different storage classes for different use cases
- Stores data across multiple availability zones
- Enables URL access for files
- Offers configurable rules for data lifecycle
- Can serve as a static website host

### Amazon S3 Non-Archival Storage Classes

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2041.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2041.png)

- S3 Standard-IA (Infrequent Access)

### S3 Intelligent-Tiering Storage Class

- Automatically moves files based on access
- Moves between frequent and infrequent access
- Same performance as S3-Standard

### S3 Lifecycle Policies

- Objects in a bucket can transition or expire based on your criteria
- Transitions can enable objects to move to another storage class based on time
- Expiration can delete objects based on age
- Policies can also factor in versions of a specific object in the bucket

### S3 Transfer Acceleration

> ***S3 Transfer Acceleration** is a feature that can be enabled per bucket that allows for optimized uploading of data using the AWS Edge Locations as a part of Amazon CloudFront.*
> 

## Hosting a Website on Amazon S3

In this demo, we'll be:

- Creating a new S3 bucket
- Uploading objects to an S3 bucket
- Accessing objects from an S3 bucket using a URL
- Configuring a bucket for website hosting

### Bucket Creation Procedure

1. Launch S3 from the AWS Console
2. Select '**Create bucket**'
3. Enter a unique name and region. Bucket names must be **globally unique:**

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2042.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2042.png)

1. We're choosing to **not** set any versioning or logging options
2. By default, buckets are private, so we need to unblock public access and acknowledge the warning:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2043.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2043.png)

1. Once we review the settings, we can click '**Create bucket**', and see the bucket in the bucket dashboard:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2044.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2044.png)

### Website Creation Procedure

1. We need to enter our bucket from the dashboard, and select '**Upload**'
2. We're going to upload the demo files:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2045.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2045.png)

1. We're can change the object ACL's here (we're going to leave them as is):

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2046.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2046.png)

1. We can choose our Storage Class here too (we're going to leave it as Standard): 

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2047.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2047.png)

1. We're going to opt to use an encryption key, and let AWS manage the key for us. This ensures the data is encrypted at rest:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2048.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2048.png)

1. Now we've confirmed our settings, we can select '**Upload**'
2. We can view the files in our bucket: 

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2049.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2049.png)

1. By clicking into the file, we can see it's properties, and even open it's URL:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2050.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2050.png)

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2051.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2051.png)

When we view the file in the bucket, we get an access denied error, as we have not yet provisioned permissions. 

1. To define permissions, we need to select the '**Permissions**' tab, then '**Edit**':

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2052.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2052.png)

1. We're going to grant public access to this file, and select '**Save changes**':

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2053.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2053.png)

1. Reloading the file URL reveals the file!

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2054.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2054.png)

1. To enable static website hosting, we're going back to the bucket page, into '**Properties**', then scroll down to '**Static website hosting**'

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2055.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2055.png)

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2056.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2056.png)

1. To configure the hosting options, we're going to select '**Edit**' then select '**Enable**'

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2057.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2057.png)

1. We're going to opt to host a static website, and choose our index document - here we can optionally set an error page too:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2058.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2058.png)

1. We're not going to enter any redirection rules, and select '**Save**'
2. The bucket dashboard will now display our website URL. Because we haven't yet set any permissions for the index.html, we're going to receive an error when navigating to it:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2059.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2059.png)

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2060.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2060.png)

1. We'll provision permissions to allow '**Everyone**' to access the index.html file, and select '**Save**'
2. Our URL will now successfully display our website!

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2061.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2061.png)

## Glacier and Glacier Deep Archive

- Designed for archiving of data within S3 as separate storage classes
- Offers configurable retrieval times
- Can send files directly or through lifecycle rules in S3
- Provides two different storage classes:
    - S3 Glacier
    - S3 Glacier Deep Archive

### S3 Glacier

- Designed for archival data
- 90 day minimum storage duration change
- Can be retrieved in either minutes or hours (pricing difference)
- You pay a retrieval fee per GB retrieved
- Over 5 times less expensive than S3 Standard storage class

### S3 Glacier Deep Archive

- Designed for archival data
- 180 day minimum storage duration change
- Can be retrieved in hours
- You pay a retrieval fee per GB retrieved
- Over 23 times less expensive than S3 Standard storage class

> *The AWS Management console can be used to quickly set up Amazon S3 Glacier. Data can then be uploaded and retrieved programmatically. - Amazon Web Services*
> 

## Elastic Block Store

### Amazon EC2 File Storage Services

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2062.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2062.png)

> ***Amazon Elastic Block Store (EBS)** is block storage designed to be connected to a single EC2 instance that can scale to support petabytes of data and supports multiple volume types based on need.*
> 

### Amazon Elastic Block Store (EBS)

- Enables redundancy within an AZ
- Allows users to take snapshots of its data
- Offered encryption of its volumes (not by default)
- Provides multiple volume types:
    - General purpose SSD
    - Provisioned IOPS SSD
    - Throughput optimized HDD
    - Cold HDD
    

### Amazon EBS Volume Types

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2063.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2063.png)

## Elastic File system

- Fully managed NFS file system
- Designed for Linux workloads
- Supports up to petabyte scale
- Stores data across multiple AZ's
- Provides two different storage classes
    - Standard
    - Infrequent Access (IA)
- Provides configurable lifecycle data rules

### EFS Example

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2064.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2064.png)

EFS works across multiple zones, acting a network filesystem, with a mount point in each zone. 

### Amazon FSx for Windows File Server

- Fully managed native Windows file system
- Includes native Windows features including
    - SMB support
    - Active Directory integration
    - Windows NTFS
- Utilizes SSD drives for low latency

## Data Transfer with AWS Snowball

AWS provides two Large-Scale Data Transfer Services:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2065.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2065.png)

### AWS Snowball

- Designed for large-scale data transfer
- Supports petabyte scale transfer
- Physical device is delivered by AWS
- You connect the Snowball to your network and upload your data
- Device is returned by local carrier
- AWS receives device and loads your data into S3

### AWS Snowmobile

- Designed for large-scale data transfer
- Supports exabyte scale transfer
- Ruggedized shipping container is delivered to your location
- AWS sets up a connection to your network
- You load your data onto the Snowmobile
- AWS will load data into S3 when the container is received at an AWS location

## Scenario Based Review

### Scenario 1

- Elaine launched a site that offers daily tutorials for developers
    - She uses S3 to store the assets needed per tutorial
    - These assets are very popular within the week the tutorial is launched
    - After this initial week, these assets are rarely accessed
- ***How could Elaine reduce her S3 costs while maintaining durability?***

<aside>
✅ S3 lifecycle rules with S3-Standard IA storage class

</aside>

### Scenario 2

- Esteban works for a social networking company and they are moving to AWS
    - They have 2PB of user-generated content that they need to migrate
    - Esteban is trying to determine if there is a faster way than uploading over the internet
- ***Would there be another approach you would recommend for Esteban's company?***

<aside>
✅ AWS Snowball

</aside>

### Scenario 3

- Emily works for a company that produces a messaging app
    - She is looking for a shared file system that will connect between 8 different Linux EC2 instances
    - The file system would need to support roughly 1PB of data
- ***What approach would you recommend for Emily?***

<aside>
✅ Amazon Elastic File System (EFS)

</aside>

## Summary

In this module, we have:

- Reviewed the storage services on AWS
- Examined Amazon S3 and its capabilities
- Implemented a static website on Amazon S3
- Explored archive capabilities with Glacier and Glacier Deep Archive
- Reviewed EC2 storage with EBS and EFS
- Examined large-scale data transfer services into AWS

---

# Database Services and Utilities

<aside>
🗓️ Saturday 31st July 2021

</aside>

## Overview

### Amazon Databases & Related Services

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2066.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2066.png)

### Cloud Computing Models

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2067.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2067.png)

- Database on EC2 gives us control over the OS
- If we want control over the database but don't need it over the infrastructure, we can use Relational Database Service
- If we just want a SaaS solution, we can utilize DynamoDB, Redshift or Elasticache

In this module, we'll be:

- Reviewing the cloud computing models for databases on AWS
- Introducing the Relational Database Service (RDS)
- Examining the capabilities of Amazon Aurora
- Introducing the DynamoDB service
- Reviewing the Elasticache service
- Examining data warehousing of data on AWS

## Amazon Relational Database Service

- Fully managed service for relational databases
- Handles provisioning, patching, backup, and recovery of your databases
- Supports deployment across multiple availability zones (multi-AZ)
- Some platforms support read replicas
- Launches into a VPC
- Provides both general purpose SSD and provisioned IOPS SSD drive options

### Amazon RDS Platforms

- MySQL
- PostgreSQL
- MariaDB

- Oracle Database
- SQL Server
- Amazon Aurora

> ***Amazon Aurora** is a MySQL and PostgresSQL-compatible relational database built for the cloud. that combines the performance and availability of traditional enterprise databases with the simplicity and cost-effectiveness of open source databases. - Amazon Web Services*
> 

### Amazon Database Migration Service (DMS)

- Enables you to move data into AWS from existing databases
- Supports both one time and continual migration of data
- Supports many popular commercial and open source databases
- You only pay for the compute leveraged in the migration process

## Amazon DynamoDB Overview

> ***DynamoDB** can handle more than 10 trillion requests per day and can support peaks of more than 20 million requests per second. - Amazon Web Services*
> 
- Fully managed NoSQL database service (Saas)
- Provides both key-value and document database
- Enables extremely low latency at virtually any scale
- Supports automated scaling based on configuration - can scale for both predicted usage and automatic usage
- Offers in-memory cache with the DynamoDB Accelerator (DAX)

### DynamoDB Use Cases

- Scale without excessive maintenance
- Serverless applications
- Implementations where low latency is key
- Data models without BLOB storage

## Amazon Elasticache and Redshift

### Amazon Elasticache

- Fully managed in-memory data stores
- Supports both Memcached and Redis
- Provides low latency in response times
- Enables scaling and replicas to meet application demand
- Handles common use cases including:
    - Database layer caching
    - Session storage

### Amazon Redshift

- Scalable data warehouse service
- Supports petabyte scale warehousing of data
- Leverages high performance disks and columnar storage
- Offers the ability to fully encrypt contents
- Provides isolation with a VPC
- Enables querying of exabytes of data in Amazon S3 using Redshift Spectrum

## Scenario Based Review

### Scenario 1

- Jennifer is an IT executive in a financial services company
- They are transitioning their data warehouse to AWS for analysis
- The data warehouse would need to ******support up to 2PB of data

***What approach would you recommend for Jennifer?***

<aside>
✅ Amazon Redshift

</aside>

### Scenario 2

- Sam is a DevOps engineer at a tech company
- Sam needs to launch a MySQL database for a new web application
- They need to have direct access to the virtual server that MySQL is running on

***What approach would you recommend for Sam's company?***

<aside>
✅ Database on EC2 (they want to manage the underlying server)

</aside>

### Scenario 3

- Frank is the CTO at a gaming company
- They are trying to determine how to store realtime user analytics
- They need low latency and the ability to scale to handle up to 1 million players
- Frank wants to minimize the amount of time it takes to maintain the database

***Which AWS approach would you recommend for Frank?***

<aside>
✅ Amazon DynamoDB

</aside>

## Summary

In this module, we have:

- Reviewed the cloud computing models for databases on AWS
- Introduced the Relational Database Service (RDS)
- Examined the capabilities of Amazon Aurora
- Introduced the DynamoDB service
- Reviewed the Elasticache service
- Examined data warehousing of data on AWS

---

# App Integration Services

<aside>
🗓️ Saturday 31st July 2021

</aside>

## Overview

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2068.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2068.png)

In this module we'll be:

- Introducing Amazon Simple Notification Service (SNS)
- Introducing Amazon Simple Queue Service (SQS)
- Exploring architectures leveraging SNS and SQS
- Examining AWS Step Functions
- Reviewing sample AWS Step Function usage

## AWS Messaging Services

### Amazon Simple Notification Service (SNS)

- Fully managed pub/sub messaging service (publish & subscribe)
- Enables you to create decoupled applications
- Organizes information according to topics
- Integrates with multiple AWS services
- Provides end user notification across SMS, email and push notifications

**Example Amazon SNS Architecture**

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Screenshot_2021-07-31_at_21.53.22.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Screenshot_2021-07-31_at_21.53.22.png)

We've connected our user signup process to an SNS topic. This topic integrates the user into our CRM using a Lambda function, adds the user into an SQS queue to allow our salespeople to follow up with them, and sends out an email to the regional sales director for that area. 

SNS notifications are ephemeral - if a service isn't listening for a notification, it will miss it forever.

### Amazon Simple Queue Service (SQS)

- Fully managed message queue service
- Enables you to build decoupled and fault tolerant applications
- Supports up to 256KB data payload
- Allows messages to be stored up to 14 days
- Provides two types of queues:
    - Standard queue - no order
    - FIFO (first in, first out)

### Example SNS & SQS Architecture

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2069.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2069.png)

A user order comes into our e-commerce platform. The order notification goes into an SNS Topic, which fans out to multiple places:

1. The fulfilment SQS queue which stores our orders, and pushes them into the order fulfilment service, which fulfils the order.
2. The analytics SQS queue, which stores the information about which items users are ordering, for a BI function. To drop it into our data warehouse, we have an Analytics Ingestion Service that uses Lambda to process data ingestion. 

**SQS Fault Tolerance**

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2070.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2070.png)

We encounter an issue with our Analytics Ingestion Service, and it goes offline. Whilst this service is offline, the SQS queue is continuing to store notifications, ready for the service to come online.

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Screenshot_2021-07-31_at_21.56.58.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Screenshot_2021-07-31_at_21.56.58.png)

We encounter an issue with the server hosting our Order Fulfilment Service, and the server goes offline. Whilst the server is offline, the SQS queue is continuing to store notifications, ready for the service to come back online. 

This is what we describe as fault-tolerant infrastructure.

## AWS Step Functions

- Enables orchestration of workflows through a fully manages service
- Supports a serverless architectures
- Can support complex workflows including error handling
- Charged per state transition along with the other AWS services leveraged - if we have 4 steps in our function, we'll be charged each time we change steps. If this is running on Lambda, we'll be charged the standard Lambda rates too.
- Workflows are defined using Amazon States Language

### Example Step Function & States Language

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2071.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2071.png)

The States Language is defined using JSON.

### AWS Step Function Integrations

- Compute services
- Database services
- Messaging services
- Data processing services
- Machine learning services

## Scenario Based Review

### Scenario 1

- Ruth started a non-profit that assigns volunteers to opportunities
- Recently their database server went down and users were unable to signup
- While the situation is better, there is still some downtime expected in the future
- She wants to explore an AWS service that could prevent lost user signups

***What service would you recommend to Ruth?***

<aside>
✅ Amazon SQS

</aside>

### Scenario 2

- Jessi created a list of onboarding steps for new customers for their new app
- These steps detail integrations with their with their CRM emails to the user, and analytics
- Jessi is worried about the time it will take to build all of this from scratch

***Is there an AWS service that can help with this approach?***

<aside>
✅ Step Functions

</aside>

### Scenario 3

- Roger's company is an e-commerce company building a custom platform
- They are still adding new functionality
- He wants aspects of the platform to listen for events like orders and refunds
- They don't yet know all of the elements that would need to respond to events

***Is there a service that would allow current and future parts of the platform to listen for these events?***

<aside>
✅ Amazon SNS

</aside>

## Summary

In this module, we:

- Introduced Amazon Simple Notification Service (SNS)
- Introduced Amazon Simple Queue Service (SQL)
- Explored architectures leveraging SNS and SQS
- Examined AWS Step Functions
- Reviewed sample AWS Step Function usage

---

# Management and Governance Services

<aside>
🗓️ Saturday 31st July 2021

</aside>

## Overview

Management & Governance Services refers to 6 different services:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2072.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2072.png)

In this module, we'll be:

- Reviewing the ecosystem of services that are provided for management
- Examining how to create an audit trail with AWS CloudTrail
- Exploring how you track infrastructure with CloudWatch and Config
- Introducing infrastructure automation with CloudFormation
- Looking at operational insights with Systems Manager
- Reviewing AWS Organizations leveraging Control Tower

## AWS CloudTrail

> *With **CloudTrail**, you can loc, continuously monitor, and retain account activity related to actions across your AWS infrastructure. CloudTrail provides event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command line tools, and other AWS services.* 
- Amazon Web Services
> 
- Inserts audit trial in an S3 bucker or into CloudWatch Logs
- Logs events in the regions in which they occur
- Meets many compliance requirements for infrastructure auditing
- As a best practice, it should be enabled on every AWS account
- Can be consolidated into an Organizational trail using AWS Organizations

### AWS CloudTrail Use Cases

- Compliance requirement
- Forensic analysis
- Operational analysis
- Troubleshooting

## Amazon CloudWatch and AWS Config

### Managing Infrastructure

These are the key services that we will need to know for our AWS CPP Exam:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2073.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2073.png)

### Amazon CloudWatch

- Monitoring and management service
- Collects logs, metrics, and events from most AWS services - most services integrate with CloudWatch by default
- Enables alarms based on metrics
- Provides visualization capabilities for metrics
- Allows for custom dashboards based on collected metrics

**Sample CloudWatch Dashboard**

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Screenshot_2021-07-31_at_22.00.50.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Screenshot_2021-07-31_at_22.00.50.png)

### AWS Config

> ***AWS Config** continuously monitors and records your AWS resource configurations and alls you to automate the evaluation of recorded configurations against desired configurations.* 
- Amazon Web Services
> 
- Provides configuration history for infrastructure
- Works against rules that you can customize or even create custom validations
- Includes conformance packs for compliance standards including PCI-DSS
- Can work with AWS Organizations for both cross-region and cross-account setup
- Provides remediation steps for infrastructure not meeting criteria

## AWS Systems Manager

> ***AWS Systems Manager** provides a unified user interface so you can view operational data from multiple AWS services and allows you to automate operational tasks across your AWS Resources.*
- Amazon Web Services
> 
- Provides multiple tools that make it easier to manage your AWS infrastructure
- Enables automation tasks for common maintenance actions
- Gives a secure way to access servers using only AWS credentials
- Stores commonly used parameters securely for operational use (e.g. instead of providing applications with a database password, they can contact systems manager for auth)

## AWS CloudFormation

- Managed service for provisioning infrastructure based on templates
- No additional charge - only pay for the resources that we launch
- Templates can be YAML or JSON
- Enables infrastructure as code
- Manages dependencies between resources
- Provides drift detection to find changes in your infrastructure

### Example Cloud Formation YAML

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Screenshot_2021-07-31_at_22.01.53.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Screenshot_2021-07-31_at_22.01.53.png)

The code above, if placed in a CloudFormation template, would create a single S3 bucket.

## AWS OpsWorks

- Configuration management service
- Provides managed instances of Chef and Puppet
- Configuration is defined as code for servers
- Chef and Puppet manage the lifecycle of those configuration changes with servers
- Works in a hybrid cloud architecture for both cloud-based and on-premise servers

### OpsWorks Services

OpsWorks is made up of 3 services:

![Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2074.png](Understanding%20AWS%20Core%20Services%2029f55b24d27946dab38fbf3ba6199c6a/Untitled%2074.png)

- OpsWorks Stacks enables us to define applications in layers, and use those recipes in Chef Solo

## AWS Organizations and Control Tower

### AWS Organizations

- Allows organizations to manage multiple accounts under a single master account
- Provides organizations with the ability to leverage Consolidated Billing for all accounts
- Enables organizations to centralize loggin gand security standards across accounts

### AWS Control Tower

> ***AWS Control Tower** is a service to create a multi-account environment on AWS that follows the recommended best practices in operational efficiency, security, and governance*
> 
- Centralizes users across all AWS accounts
- Provides a way to create new AWS accounts based on templates
- Integrates Guardrails for accounts - forces rules for child accounts
- Includes a dashboard to gain operational insights from a single view

## Scenario Based Review

### Scenario 1

- Elliot is an operations engineer at a financial services company
- He recently discovered that someone had disabled a security setting on a server
- He is concerned that events liek this might go unnoticed until a breach

***Which service would allow the organization to continually track configuration of infrastructure?***

<aside>
✅ AWS Config

</aside>

### Scenario 2

- James is the lead architect at a SaaS company
- They will be launching a new application that includes several components
- He is looking to minimize manual work required when creating infrastructure

***What service would enable James to automate much of this effort?***

<aside>
✅ AWS CloudFormation

</aside>

### Scenario 3

- Candace is the CTO at a manufacturing company
- A cloud server needed to support their manufacturing process was deleted
- They want to make sure they follow up with the person who deleted this instance, to ensure it doesn't happen again

***Which service could show the individual that deleted this specific server?***

<aside>
✅ AWS CloudTrail

</aside>

## Summary

In this module, we have:

- Reviewed the ecosytem of services that are provided for management
- Examined how to create an audit trail with AWS CloudTrail
- Explored how you track infrastructure with CloudWatch and Config
- Introduced infrastructure automation with CloudFormation
- Looked at operational insights with Systems Manager
- Reviewed AWS Organizations leveraging Control Tower

## Preparing for the Exam

- Don't sign up for the exam just yet!
- Move onto the next course: Introduction to Security and Architecture on AWS
- What we need to study:
    - All of the guided notes
    - The provided services list
