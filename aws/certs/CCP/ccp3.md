# Introduction to Security & Architecture

```3️⃣ This is part three of the Pluralsight CLF-C01 path```

![Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled.png](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled.png)

# Course Overview

We'll be reviewing:

- Three core concepts that affect how we use AWS:
    - AWS Well-architected Framework
    - Shared Responsibility Model
    - Acceptable Use Policy
- Security and user management
- Key architectural concepts
    - Fault-tolerance
    - High-availability
    - Disaster recovery
- Scalable and secure applications

---

# AWS Architecture Core Concepts

<aside>
🗓️ Sunday 1st August 2021

</aside>

## Security and Architecture Overview

In this module, we'll be:

- Reviewing core concepts around security and architecture
- Exploring the AWS Shared Responsibility Model
- Introducing the AWS Well Architected Framework
- Examining fault tolerance and high availability on AWS
- Understanding provided tools for compliance

### Acceptable Use Policy

> ***Acceptable Use Policy** is AWS's policy for acceptable and unacceptable uses of their cloud platform. All users must agree with this policy to have an account on the platform.*
> 
- Sending unsolicited mass emails is prohibited
- Hosting or distributing harmful content is prohibited
- Penetration tests are allowed for a list of specific services

### Least Privilege Access

> ***Least Privilege Access**: When granting permission for a user to access AWS resources, you should grant them the minimum permissions needed to complete their tasks and no more.*
> 

## Shared Responsibility Model

> *Security and Compliance is a shared responsibility between AWS and the customer. 
- Amazon Web Services, Shared Responsibility model*
> 

### Shared Responsibility Summary

![Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%201.png](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%201.png)

### Shared Responsibility Model

**AWS Responsibility**

- Access control & training for Amazon employees
- Global data centers and underlying network
- Hardware for global infrastructure
- Configuration management for infrastructure
- Patching cloud infrastructure and services

**Customer Responsibility**

- Individual access to cloud resources and training
- Data security and encryption (both in transit and at rest)
- Operating system, network, and firewall configuration
- All code deployed onto cloud infrastructure
- Patching guest operating system and custom applications

## AWS Well-architected Framework

> *The **AWS Well-architected Framework** is a collection of best practices across five key pillars for how to best create systems that create business value on AWS.*
> 

### Pillars of the Well-architected Framework

![Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%202.png](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%202.png)

### Well-architected Framework Documentation

The documentation for the AWS Well-architected Framework can be found [here](https://aws.amazon.com/architecture/well-architected/)

## High-availability and Fault-Tolerance

> *Everything fails all the time. 
- Werner Vogels - CTO, Amazon*
> 

High-availability and Fault-Tolerance fall under the Reliability pillar of the Well-architected Framework. 

### Reliability on AWS

![Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%203.png](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%203.png)

### Building Solutions on AWS

- Most managed AWS services provide high-availability out of the box
- When building solutions directly on EC2, fault tolerance must be architected
- Multiple availability zones should be leveraged
- Some services can enable fault tolerance in your custom applications
    - Simple Queue Service (SQS)
    - Route 53
    

## Compliance

### Common Compliance Standards

![Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%204.png](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%204.png)

### Compliance Services

![Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%205.png](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%205.png)

### Demo

In this demo, we'll be:

- Examining compliance reports in AWS Artifact
- Exploring conformance packs in AWS Config

**Conformance Packs in AWS Config**

![AWS Config Dashboard](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%206.png)

AWS Config Dashboard

To deploy a conformance pack, we can enter the conformance pack dashboard from the menu, and select '**Deploy conformance pack**'

![Conformance packs dashboard](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%207.png)

Conformance packs dashboard

Here we can choose a sample or personal template - in this example we're using PCI DSS as we'll be processing credit card information

![Conformance pack template selector](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%208.png)

Conformance pack template selector

**Compliance Reports in AWS Artifact**

![AWS Artifact Dashboard](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%209.png)

AWS Artifact Dashboard

Here we can view all of our compliance reports, and any agreements that we have in place with AWS - for example if we were storing HIPAA-compliant data, we would need to have a BAA agreement in place with AWS, and we would find that here.

For some of these reports, we will need to sign a non-disclosure agreement with AWS to obtain access to them. 

## Scenario Based Review

### Scenario 1

- Jane's company is building an application to process credit cards
- They will be processing cards directly and not through a service
- Their bank needs a PCI DSS compliance report for AWS

***Where would Jane go to get this information?***

<aside>
✅ AWS Artifact

</aside>

### Scenario 2

- Tim's company is considering a transition to the cloud
- They store personal information securely in their system
- Tim's CTO has asked what the company's responsibility is for security

***What would you tell Tim's CTO?***

<aside>
✅ Review the Shared Responsibility Model

</aside>

### Scenario 3

- Ellen is a solutions architect at a startup
- They are building a new tool for digital asset management
- Ellen is curious how to best leverage the capabilities of AWS in this application

***What resources would you recommend for Ellen and her team?***

<aside>
✅ AWS Well Architected Framework

</aside>

## Summary

In this module, we have:

- Reviewed core concepts around security and architecture
- Explored the AWS Shared Responsibility Model
- Introduced the AWS Well-architected Framework
- Examined fault tolerance and high availability on AWS
- Understood provided tools for compliance

---

# AWS Identities and User Management

<aside>
🗓️ Monday 2nd August 2021

</aside>

## Overview

> ***Least Privilege Access**: When granting permission for a user to access AWS resources, you should grant them the minimum permissions needed to complete their tasks and no more.*
> 

In this module, we'll be:

- Introducing AWS Identity and Access Management (IAM)
- Reviewing the IAM identity types
- Enabling Multi-factor Authentication (MFA)
- Introducing Amazon Cognito

## Introduction to AWS IAM

- Service that controls access to AWS resources
- Using the service is free
- Manages both authentication and authorization
- Supports identity federation through SAML providers including Active Directory

### AWS IAM Identities

![AWS IAM identity types](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2010.png)

AWS IAM identity types

### Policies in AWS IAM

A AWS IAM Policy:

- A JSON document that defines permissions for an AWS IAM identity (prinicpal)
- Defines both the AWS services that the identity can access and what actions can be taken on that service
- Can be either customer managed or managed by AWS

### Example IAM Policy

![Example AWS IAM JSON Policy](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2011.png)

Example AWS IAM JSON Policy

### AWS IAM Best Practices

![Best practices for AWS IAM](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2012.png)

Best practices for AWS IAM

## Creating and Managing IAM Users

### Demo

In this demo, we'll be:

- Creating an IAM user
- Configuring permissions for IAM users
- Creating an IAM group
- Attaching permissions to an IAM group

### IAM User Procedure

We'll be navigating to the IAM Dashboard

![AWS IAM Dashboard](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2013.png)

AWS IAM Dashboard

We'll be navigating into the users pane, and selecting '**Add users**'

![IAM Users pane](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2014.png)

IAM Users pane

We'll create a demo user, give them management console permissions only, force them to reset their password, and click '**Next: Permissions**'

![Add user pane](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2015.png)

Add user pane

Here, we can add the user to a group, clone permissions from another user, or attach an existing policy. We're going to attach an existing policy

![Add user > Set permission pane](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2016.png)

Add user > Set permission pane

We'll attach the S3 administrator policy, and select '**Next: Tags**'

![Existing policy options](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2017.png)

Existing policy options

In the tags screen, we can provide the account with a tag for use later, and select **'Next: Review'**

![Tag options](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2018.png)

Tag options

After applying any tags, we can review the account, and select '**Create user**'

![New user review screen](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2019.png)

New user review screen

After creating the user, we can download their credentials either by copying them out, or downloading a CSV file

![New user credentials screen](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2020.png)

New user credentials screen

### IAM Group Procedure

We're going to navigate to the '**User groups**' pane, and select '**Create group'**

![IAM User groups pane](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2021.png)

IAM User groups pane

Here we need to name our group

![Create user group screen](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2022.png)

Create user group screen

After naming the group, we can attach policies, and select '**Create group**'

![Optional policy attachments](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2023.png)

Optional policy attachments

The group is now created!

![IAM User groups pane](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2024.png)

IAM User groups pane

Now the group is created, we can go back into the '**Users**' pane, and look at our user

![IAM User Summary](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2025.png)

IAM User Summary

We'll detach the **AmazonS3FullAccess** policy, then head into the '**Groups**' tab

![IAM User Summary > Groups Tab](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2026.png)

IAM User Summary > Groups Tab

We can select '**Add user to groups**', select the groups we wish to add the user to, then select '**Add to groups**'

![User groups selection screen](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2027.png)

User groups selection screen

Here we can see that our user has been added to the group, and their **attached permissions**

![IAM User Summary > Groups Tab](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2028.png)

IAM User Summary > Groups Tab

## Enabling Multi-factor Authentication

### Demo

In this demo, we'll be:

- Enabling MFA for the root user
- Enabling MFA for an IAM user

### Root User MFA Procedure

To activate MFA for the root user, we will need to sign into the root user account, select the account name in the top right, then '**My Security Credentials**'. From here we can select the MFA dropdown, and apply our MFA Auth

![Root User MFA configuration screen](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2029.png)

Root User MFA configuration screen

### IAM User MFA Procedure

To apply MFA to an IAM user, we navigate to the users pane from the '**My Security Credentials**' dashboard

![IAM Users pane](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2030.png)

IAM Users pane

We select our user, then the '**Security credentials**' tab, select '**Manage**' next to '**Assigned MFA device**', then apply the MFA Auth.

![IAM Users summary pane](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2031.png)

IAM Users summary pane

## Amazon Cognito

> ***Amazon Cognito** is a managed service that enables you to handle authentication and aspects of authorization for your custom web and mobile applications through AWS.*
> 

### Overview

- User directory service for custom applications
- Provides UI components for many platforms
- Provides security capabilities to control account access
- Enables controlled access to AWS resources
- Can work with social and enterprise identity providers

### Amazon Cognito Identity Providers

![Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2032.png](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2032.png)

## Scenario Based Review

### Scenario 1

- Sylvia manages a team of DevOps engineers for her company
- Each member of her team needs to have the same access to cloud systems
- It is taking her a long time to attach permissions to each user for access

***What approach would help Sylvia manage the team's permissions?***

<aside>
✅ IAM User Groups, being sure to follow Least Privilege Access

</aside>

### Scenario 2

- Edward works for a startup that is building a mapping visualization tool
- Their EC2 servers need to access data stored within S3 buckets
- Edward created a user in IAM for these servers and uploaded keys to the server

***Is Edward following best practices for this approach? If not, what should he do?***

<aside>
✅ No. Utilize an IAM Role with EC2 to grant the servers access to the buckets

</aside>

### Scenario 3

- William is leading the effort to transition his organization to the cloud
- His CIO is concerned about securing access to AWS resources with a password
- He asks William to research approaches for additional security

***What approach would you recommend to William for this additional security?***

<aside>
✅ Multi Factor Authentication

</aside>

## Summary

In this module we have:

- Introduced AWS Identity and Access Management (IAM)
- Reviewed the IAM identity types
- Enabled Multi-factor Authentication (MFA)
- Introduced Amazon Cognito

---

# Data Architecture on AWS

<aside>
🗓️ Tuesday 3rd August 2021

</aside>

## Overview

In this module, we'll be:

- Reviewing approaches for integrating data from your own data center
- Examining approaches for processing data
- Exploring data analysis approaches
- Integrating machine learning and AI into data analysis
- 

## Integrating On-premise Data

There are two different solutions for integrating on-premise data:

![Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2033.png](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2033.png)

### AWS Storage Gateway

- Integrates cloud storage into your local network
- Deployed as a VM or specific hardware applicance
- Integrates with S3 and EBS
- Supports three different gateway types:
    - Tape Gateway
    - Volume Gateway
    - File Gateway

**Gateway Types**

![AWS Storage Gateway Types](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2034.png)

AWS Storage Gateway Types

### AWS DataSync

- Leverages the DataSync agent deployed as a VM on your network
- Integrates with S3, EFS and FSx for Windows File Server on AWS
- Greatly improved speed of transfer due to custom protocol and optimizations
- Charged per GB of data transferred

## Processing Data

We're going to be looking at three different services:

![Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2035.png](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2035.png)

### AWS Glue

- Fully managed ETL (extract, transform, and load) service on AWS
- Supports data in Amazon RDS, DynamoDB, Redshift and S3
- Supports a serverless model of execution

### Amazon Elastic Map Reduce (EMR)

- Enables big-data processing on Amazon EC2 and S3
- Supports popular open-source frameworks and tools
- Operates in a clustered environment without additional configuration (you don't have to manually configure the environment)
- Supports many different big-data use cases

**Supported Amazon EMR Frameworks**

![AWS EMR Frameworks](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2036.png)

AWS EMR Frameworks

### AWS Data Pipeline

- Fully managed ETL (extract, transform, and load) service on AWS
- Manages data workflow through AWS services
- Supports S3, EMR, Redshift, DynamoDB and RDS
- Can integrate on-premise data stores

## Analyzing Data

### Data Analysis Services

![AWS Data Analysis Services](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2037.png)

AWS Data Analysis Services

### Amazon Athena

- Fully-managed serverless service
- Enables querying of large-scale data stored within Amazon S3
- Queries are written using standard SQL
- Charged based on data scanned for query (qty of data touched)

### Amazon Quicksight

- Fully-managed business intelligence service
- Enables dynamic data dashboard based on data stored in AWS
- Charged on a per-user and per-session pricing model
- Multiple versions provided based on needs (standard vs enterprise etc)

**Example Quicksight Dashboard**

![Example dashboard from Amazon Quicksight](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2038.png)

Example dashboard from Amazon Quicksight

### Amazon CloudSearch

- Fully-managed search service on AWS
- Support scaling of search infrastructure to meet demand
- Charged per hour and instance type of search infrastructure
- Enables developers to integrate search into custom applications

## Integrating AI and Machine Learning

We're not covering all of the AI and Machine Learning services, just the ones we'll need to know for the exam. We're looking at three different services:

![AWS AI and Machine Learning Services](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2039.png)

AWS AI and Machine Learning Services

### Amazon Rekognition

- Fully-managed image and video recognition deep learning service
- Identifies objects in images
- Identifies objects and actions in videos
- Can detect specific people using facial analysis
- Supports custom labels for your business objects

### Amazon Translate

- Fully-managed service for translation of text
- Currently supports 54 languages
- Can perform language identification
- Works both in batch and real-time

### Amazon Transcribe

- Fully-managed speech recognition service
- Recorded speech is converted into text in custom applications
- Includes a specific sub-service for medical use
- Supports batch and real-time transcription
- Currently supports 31 languages

## Scenario Based Review

### Scenario 1

- Ruth is a data scientist for a financial services company
- Large-scale data sets need to be processed before analysis
- Ruth doesn't want to manage servers but just wants to define processing

***What service would you recommend to Ruth?***

<aside>
✅ Amazon Glue

</aside>

### Scenario 2

- Jessi is a member of the IT team for a biotech company
- She is currently working to identify an approach for controlled lab access
- She wants to leverage AI to determine access based on facial imaging

***Is there an AWS service that can help with this approach?***

<aside>
✅ Amazon Rekognition

</aside>

### Scenario 3

- Roger's company sells custom services around machine learning
- His head of sales is trying to find a great way to visualize their sales data
- This data is currently stored in Redshift as their data warehouse

***What AWS service would allow this access to the data by non-technical resources?***

<aside>
✅ Amazon Quicksight

</aside>

## Summary

In this module, we've:

- Reviewed approaches for integrating data from your own data center
- Examined approaches for processing data
- Explored data analysis approaches
- Integrated machine learning and AI into data analysis

---

# Disaster Recovery on AWS

<aside>
🗓️ Wednesday 4th August 2021

</aside>

## Overview

> ***Disaster recovery** (DR) is about preparing for and recovering from a disaster. Any event that has a negative impact on a company's business continuity or finances could be termed a disaster. This includes hardware or software failure, a network outage, a power outage, physical damage to a building like fire or flooding, human error or some other significant event.
- Amazon Web Services*
> 

### Needs for Disaster Recovery

![Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2040.png](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2040.png)

Loss of data center / failure of cloud services

### Module Overview

We'll be:

- Understanding the need for a disaster recovery strategy
- Reviewing the four different disaster recovery approaches on AWS
- Exploring the factors to know when selecting an approach
- Examining specific scenarios and disaster recovery needs

## Disaster Recovery Architectures

![Disaster Recovery Scenarios](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2041.png)

Disaster Recovery Scenarios

### Backup and Restore

- Production data is backed up into Amazon S3
- Data can be stored in either standard or archival storage classes
- EBS data can be stored as snapshots in Amazon S3 also
- In a Disaster Recovery event, a process is started to launch a new environment
- This approach has the longest recovery time, but the least cost

### Pilot Light

> *The **Pilot Light** method gives you a quicker recovery time than the backup-and-restore method because the core pieces of the system are already running and are continually kept up to date.
- Amazon Web Services*
> 
- Key infrastructure components are kept running in the cloud
- Designed to reduced recovery time over the Backup and Restore approach
- Does incur cost of this infrastructure continually running in the cloud
- AMI's are prepared for additional systems and can be launched quickly

### Warm Standby

- A scaled-down version of the full environment is running in the cloud
- Critical systems can be running on less capable instance types
- Instance types and other systems can be ramped up for Disaster Recovery events
- Does incur cost of this infrastructure continually running in the cloud

### Multi Site

- Full environment is running in the cloud at all times
- Utilizes instance types needed for production not just recovery
- Provides a near seamless recovery process
- Incurs the most cost over the other approaches

## Selecting a Disaster Recovery Architecture

![DR Approach Considerations](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2042.png)

DR Approach Considerations

### Recovery Time Objective (RTO)

> ***Recovery Time Objective** is the time it takes to get your systems back up and running to the ideal business state after a disaster recovery event.*
> 

### Recovery Point Objective (RPO)

> *Recovery Point Objective is the amount of data loss (in terms of time) for a production system during a disaster recovery event.*
> 

### Disaster Recovery Scenarios

![Disaster Recovery Scenarios Diagram](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2041.png)

Disaster Recovery Scenarios Diagram

- Multi Site has the lowest RTO & RPO, but the most cost
- Backup and Restore has the highest RTO & RPO, but the least cost
- Pilot Light & Warm standby can be customized based on your RTO & RPO needs (i.e. production databases but scaled down)

## Scenario Based Review

### Scenario 1

- Roger’s company runs several production workloads in AWS
- Roger is tasked with architecting the disaster recovering approach
- His organization wants there to be a seamless transition during an event

***Which disaster recovery approach would Roger’s company use for this?***

<aside>
✅ Multi Site

</aside>

### Scenario 2

- Jennifer’s company is a startup
- They do not currently have a disaster recovery approach
- In this case, minimizing cost is more critical than minimizing RTO

***What disaster recovery approach would you recommend to Jennifer?***

<aside>
✅ Backup and Restore

</aside>

### Scenario 3

- Eliza is documenting her company’s disaster recovery approach
- They keep a few key servers up an running in AWS in case of an event
- These servers have smaller instance types than what production would need

***Which disaster recovery approach most closely matches this scenario?***

<aside>
✅ Pilot Light - as it's a few key servers

</aside>

## Summary

In this module, we've:

- Understood the need for a disaster recovery strategy
- Reviewed the four different disaster recovery approaches on AWS
- Explored the factors to know when selecting an approach
- Examined specific scenarios and disaster recovery needs

---

# Architecting Applications on Amazon EC2

<aside>
🗓️ Thursday 5th August 2021

</aside>

## Overview

In this module, we'll be:

- Reviewing scaling approaches and services for Amazon EC2
- Examining approaches for controlling access to Amazon EC2 instances
- Exploring services to protect infrastructure from hacking and attacks
- Introducing developer tools on AWS
- Reviewing approaches for launching pre-defined solutions on amazon EC2

## Scaling EC2 Infrastructure

![Infrastructure scaling types](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2043.png)

Infrastructure scaling types

![Amazon EC2 Horizontal Scaling Services](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2044.png)

Amazon EC2 Horizontal Scaling Services

### Amazon EC2 Auto-Scaling Group

- Launch template defines the instance configuration for the group
- Define the minimum, maximum, and desired number of instances
- Performs health checks on each instance (can check URLs to retrieve a status code and take action based on returned codes)
- Exists within 1 or more availability zones in a single region
- Works with on-demand and spot instances.

**Amazon EC2 Horizontal Scaling Example**

![**Amazon EC2 Horizontal Scaling Example**](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2045.png)

**Amazon EC2 Horizontal Scaling Example**

In this example, we have an Auto-Scaling Group running across 2 availability zones. Our desired number of instances is 2, so the group has scaled appropriately across the zones. In-between the users and our instances is an Application Load Balancer, which routes users to an available server. 

In this example, we lose the instance in availability zone a, and the load balancer will stop sending traffic to the server, until the Auto-Scaling Group can terminate the server, and spin up a new server in its place.

### AWS Secrets Manager

- Secure way to integrate credentials, API keys, tokens, and other secret content (prevents us storing them on the servers)
- Integrates natively with RDS, DocumentDB, and Redshift
- Can auto-rotate credentials with integrated services
- Enables fine-grained access control to secrets

## Controlling Access to EC2 Instances

![Security in Amazon VPC](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2046.png)

Security in Amazon VPC

### Security Groups

- Serve as a firewall for your EC2 instances
- Control inbound and outbound traffic
- Works at the instance level
- EC2 instances can belong to multiple security groups
- VPC's have default security groups
- Must be explicitly associated with an EC2 instance
- By default all outbound traffic is allowed

### Network ACL's

- Works at the subnet level with a VPC (every instance in the subnet gets the ACL)
- Enables you to allow and deny traffic
- Each VPC has a default ACL that allows all inbound and outbound traffic
- Custom ACL's deny all traffic until rules are added

### AWS VPN

- Creates an encrypted tunnel into your VPC
- Can be used to connect your data center or even individual client machines
- Supported in two services:
    - Site-to-site VPN (connecting a data center)
    - Client VPN

**AWS Site-to-Site VPN Example**

![Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2047.png](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2047.png)

In this example of a Site-to-Site VPN, the corporate data center has a customer gateway, to direct traffic, and the VPC has a VPN gateway to receive traffic.

This is different to AWS Direct Connect, as you do not have a direct connection to the AWS Global Infrastructure, traffic travels over the public internet, and is encrypted the entire way. 

## Protecting Infrastructure from Attacks

### AWS Security Services

![Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2048.png](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2048.png)

> ***Distributed Denial of Service (DDoS)** is a type of attach where a server or group of servers are flooded with more traffic than they can handle in a coordinated effort to bring the system down.*
> 

### AWS Shield

- Provides protection against DDoS attacks for apps running on AWS
- Enables on-going threat detection and mitigation
- Has two different service levels:
    - Standard
    - Advanced

### Amazon Macie

- Utilizes machine learning to analyze data stored in Amazon S3
- It can detect personal information and intellectual property in S3
- Provides dashboards that show how data is being stored and accessed
- Enables alerts if it detects anything unusual about data access

### Amazon Inspector

- Enables scanning of Amazon EC2 instances for security vulnerabilities
- Charged by instance per assessment run
- Two types of rules packages:
    - Network reachability assessment
    - Host assessment

## Deploying Pre-defined Solutions

![Deployment Solutions](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2049.png)

Deployment Solutions

### AWS Service Catalog

- Targeted to serve as an organizational service catalog for the cloud
- Can include single server image to multi-tier custom applictations
- Enables organizations to leverage services that meet compliance
- Supports a lifecycle for services released in the catalog

### AWS Marketplace

- Curated catalog of third-party solutions for customers to run on AWS
- Provides AMI's, CloudFormation stacks, and Saas based solutions
- Enables different pricing options to overcome licensing in the cloud
- Charges appear on your AWS bill

**AWS Marketplace Example**

![AWS Marketplace](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2050.png)

AWS Marketplace

## Developer Tools

![AWS Developer Services ](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2051.png)

AWS Developer Services 

### AWS CodeCommit

- Managed source control service
- Utilizes Git for repositories
- Control access with IAM policies
- Serves an alternative to Github and Bitbucket (AWS can use Github with the other tools if you don't use CodeCommit)

### AWS CodeBuild

- Fully managed build and continuous integration service on AWS
- Don't have to worry about infrastructure
- Charged per minute for compute resources you utilize

### AWS CodeDeploy

- Managed deployment service for deploying your custom applications
- Deploys to Amazon EC2, AWS Fargate, AWS Lambda, and on-premise servers
- Provides dashboard for deployments in the AWS Console

### AWS CodePipeline

- Fully-managaged continuous delivery service on AWS
- Provides the capabilities to automate building, testing, and deploying
- Integrates with other developer tools as well as Github

### AWS CodeStar

- Workflow tool that automates the use of the other developer services
- Creates a complete continuous delivery toolchain for a custom application
- Provides custom dashboards and configurations in the AWS Console
- You are only charged for the other services you leverage

## Scenario Based Review

### Scenario 1

- Ellen is a solutions architect at a traditional financial services company
- They recently transitioned to AWS
- They want to be sure each department follows best practices
- They want to create compliant IT services that other departments can use

***What service would you recommend for Ellen and her team?***

<aside>
✅ AWS Service Catalog

</aside>

### Scenario 2

- Tim’s company leverages AWS for multiple production workloads
- Recently they have had downtime due to one of their applications failing on EC2
- Tim is looking to avoid downtime if an instance stops responding

***What approach would you recommend for Tim to solve this issue?***

<aside>
✅ AWS Auto-Scaling Groups + AWS Elastic Load Balancer

</aside>

### Scenario 3

- Jane’s company deals with sensitive information from its users
- They have put reasonable policies in place for data stored in S3
- Jane is worried if some of those policies accidentally get changed
- She is also worried of a breach going unnoticed

***What service would you recommend to Jane and her company?***

<aside>
✅ Amazon Marcie

</aside>

## Summary

In this module, we've:

- Reviewed scaling approaches and services for Amazon EC2
- Examined approaches for controlling access to Amazon EC2 instances
- Explored services to protect infrastructure from hacking and attacks
- Introduced developer tools on AWS
- Reviewed approaches for launching predefined solutions on Amazon EC2

---

# The Certification Exam

<aside>
🗓️ Friday 6th August 2021

</aside>

## The Exam

- The exam is a 90 minute, proctored exam
- There are 2 types of question:
    - Multiple choice
    - Multiple answer (select correct/incorrect options from list)
- The test is scored 100 to 1000, and anything over 750 is a passing grade

### Certification Areas of Focus

![Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2052.png](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2052.png)

**Cloud concepts: 26%**

- General information about the cloud

**Technology: 22%**

- AWS Global Infrastructure
- AWS Services

**Security / Compliance: 25%**

- Shared Responsibility Model
- AWS compliance reports

**Billing / Pricing: 16%**

- Cost Explorer
- TCO calculator
- Simple Monthly Calculator
- How these services provide value

## Registering for the Exam

- Navigate to the certified cloud practitioner page
- Schedule an exam through the training and certification portal
- Choose the correct exam
- Can select an online, at-home exam or a proctored test centre

## Studying for and Taking the Exam

![Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2053.png](Introduction%20to%20Security%20and%20Architecture%20on%20AWS%202eb1275312a74ea1ae4b90fd7e7867fa/Untitled%2053.png)

### Study

**Reviewing Cloud Concepts**

- Review how cloud platforms differ from traditional data centers
- Review how AWS organizes its infrastructure globally
- Understand how scalability differs in the cloud from traditional data centers
- Review CapEx and OpEx expenditures

**Reviewing Security** 

- Understand the Shared Responsibility Model from AWS
- Review highlighted best practices for securing your AWS account & resources
- Review options for securing traffic within a VPC
- Review IAM and identity types
- Understand Least Privilege Access

**Reviewing Billing & Pricing**

- Review tools that help you understand AWS costs
- Understand the most cost-effective ways to leverage core services
- Review how costs differ from traditional data centers
- Review ways that organizations can manage and review costs
- Understand different support plan levels

**Reviewing Technology**

- Review each of the AWS services that are included int he services lists
- Implement basic solutions using the services we covered
- Review architectural principles for fault tolerance & high availability
- Analyze scalability approaches

### Taking the Exam

**Testing Best Practices**

- Take time to analyze each question for its intent
- Review what is required for the answer on each question
- Skip a question if it takes too much time
- Leverage the review capability
- Guess if you don't know the answer after the review phase
- Examine the clock after each 10 questions

## Important Next Steps

Go through the exam prep course! It'll help cement the knowledge from the path, and walk us through 2 sets of exam questions.

Memorize the services lists and guided notes.

Once we're passing the practice tests we can sign up to take the exam!
