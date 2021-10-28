# Certified Cloud Practitioner

These are my notes from part one of the CLF-C01 Pluralsight Path

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/37cc9d0f-4825-491e-9959-487677a3c1cd/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/37cc9d0f-4825-491e-9959-487677a3c1cd/Untitled.png)

---

# Course Overview

This course will cover:

- The concept of cloud computing and the value that it provides to organizations
- The organization of AWS global infrastructure
- The economics of cloud computing
- The tools and services that AWS Provides provides

---

# Understanding Cloud Computing

Saturday 24th July 2021

## Overview

This Pluralsight course contains:

- Videos for each topic
- Study materials for each course
- An exam prep course, including tips and sample questions
- There are exercise files included alongside the course

## Setting up an AWS Account

### Creating a new personal AWS Account

1. Navigate to the [AWS Homepage](https://aws.amazon.com)
2. Select 'Create an AWS account'
3. Enter an email address, password & account name
4. Select a personal account type, and enter in your information
5. Enter a credit card number and and hit verify
6. Choose to verify the account using an sms message
7. Select the free, basic support plan

### Activating the new account

To activate the account, we sign into the portal using our email address and password

### Configuring a budget alert for the account

To configure a budget:

1. Select our username in the upper right, then select 'My Billing Dashboard'
2. Select budgets from the left hand menu, and then 'Create a budget'
3. Select cost budget
4. Enter a name for the budget, and select recurring
5. Choose fixed, and set the budget amount to 10.00

Once the budget is configured, we can configure our alerts:

1. Select 'Add an alert threshold'
2. Send alert based on 'Actual Costs'
3. Set the alert threshold to 80% of budgeted amount, which will notify us when the Actual Costs hit 800
4. Enter our email contact
5. Select confirm budget
6. Select create

This has created a budget that will notify us when we hit 8.00 of usage costs.

## Traditional Data Centers

**Requires a large up-front investment in hardware** - and either building a data center or renting space in one.

**Forecasting demand is difficult** - understanding how many users will latch onto it.

**Slow to deploy new data centers and servers** - there are times when it is difficult to get up and running in response to a change in demand.

**Maintaining data centers is expensive** - server maintenance, data center maintenance, human costs are all on-going burdens.

**You own all of the security and compliance burden** - no-one wants to be sued for being hacked. That entire responsibility rests on our shoulders.

## Benefits of Cloud Computing

**Trade capital expense for variable expense** - we don't pay for whole servers, just for cloud servers whilst we're using them.

**Benefit from massive economies of scale** - aws gets wholesale price on servers, and has figured out how to maintain them efficiently at scale. Those cost savings get passed down to the consumers.

**Stop guessing capacity** - we can grow and shrink infrastructure on demand, in response to capacity changes.

**Increase speed and agility** - we can test our ideas and systems with real users without having to collect capital beforehand.

**Stop spending money maintaining data centers** - we can shift away from the maintenance burden, as the estate is maintained by aws.

**Go global in minutes** - we don't need to wait to move to a new region, we can add new infrastructure in seconds.

Concepts we need to know:

> **\*Elasticity** is the ability to acquire resources as you need them and release resources when you no longer need them. In the cloud, you want to do this automatically.\*
> Well-Architected Framework, Amazon Web Services

> **\*Reliability** is a solution's ability to provide functionality for its users when it is needed. Amazon's global infrastructure is built to maximize reliability for your cloud workloads.\*

> **_Agility_**: _The cloud lowers the cost of trying new ideas or business processes. It reduces the time required to maintain infrastructure. The cloud also reduces risk for the organization around security and compliance, and provides access to emerging technologies._

## Types of Cloud Computing

> **\*Cloud computing** is the on-demand delivery of compute power, database storage, applications, and other IT resources through a cloud services platform via the Internet with pay-as-you-go pricing."\*
> Amazon Web Services

### Cloud Computing Models

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/48a20301-5817-455a-9793-ec81013dc974/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/48a20301-5817-455a-9793-ec81013dc974/Untitled.png)

**Infrastructure as a Service (IaaS)** - full access to cloud servers, we can completely configure them how we want, but need to fully maintain the servers ourselves.

**Platform as a Service (PaaS)** - we have a service that is configured for us, and we just need to deploy our customization onto it.

**Software as a Service (SaaS)** - a piece of software that we can run with, we don't need to worry about maintenance at all.

### Cloud Deployment Models

**Public Cloud** - Deployed onto a public cloud provider like AWS/Azure/GCloud.

**On-Premise** (Private Cloud) - Cloud-like platform in a private data center.

**Hybrid** - Cloud applications connected to a private data center.

## Cloud Computing Scenarios

### Scenario 1

- Roger's company runs several production workloads in its data center.
  - They are using VMware to manage infrastructure in their data center.
  - They want to use AWS and integrate it with their data center for new workloads.
- Which cloud deployment model would they be following?

Hybrid Cloud

### Scenario 2

- Eliza's company is trying to decide whether to fund a new line of business.
  - Eliza's team is looking to monetize a new emerging technology.
  - This new line of business will require new infrastructure.
- What benefit of cloud computing would be most relevant to her company?

Agility, specifically Pay-As-You-Go

### Scenario 3

- Jennifer is the CTO at an insurance company.
  - They are considering moving to the cloud instead of colocating servers.
  - They want to make sure they have the maximum control of the cloud servers.
- Which cloud computing model would they need to leverage?

Infrastructure as a Service (IaaS)

## Summary

During this module of the course, we:

- Reviewed the course resources
- Created an AWS account for personal use
- Examined how organizations leverage traditional data centers
- Explored the benefits of cloud computing
- Reviewed cloud computing models
- Understood cloud computing deployment models

---

# AWS Global Infrastructure

Sunday 25th July 2021

## Overview

There are three types of infrastructure that we need to know for our AWS CCP exam:

1. Regions
2. Availability Zones
3. Edge Locations

This module of the course will focus on:

- Reviewing the three elements of the AWS global infrastructure
- Understanding the use of AWS Regions
- Understanding Availability Zones within AWS Regions
- Reviewing the purpose of Edge Locations
- Utilizing the AWS global infrastructure visualization

## AWS Regions and Availability Zones

### Regions

1. Each region is in a specific geographic location
2. Each geographic location is comprised of cluster of data centers
3. AWS currently has 22 launched regions - some public, some non-public **[citation needed]**

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/eef79220-2df8-4b54-8792-280a07e5c116/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/eef79220-2df8-4b54-8792-280a07e5c116/Untitled.png)

AWS Region Map

### Availability Zones

1. Each availability zone consists of one or more data centers
2. Multiple availability zones are included with each AWS Region - meaning that each region has at least 2 availability zones, each with at least one data center
3. Availability zones are within the geographic area of the AWS Region
4. Each availability zones have redundant power, networking and connectivity
5. There are currently 69 availability zones globally **[citation needed]**

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/80074112-3ae2-4aa3-b4e6-e3e486794057/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/80074112-3ae2-4aa3-b4e6-e3e486794057/Untitled.png)

AWS Region & Availability Zones map for the US

There are 6 us regions - 4 public, 2 gov-cloud. Each has multiple availability zones that make them up. US-EAST-1 has 6 availability zones.

### Availability

> **\*Availability** is the extent to which an application is fulfilling its intended business purpose. Applications that are highly-available are built in a manner where a single failure won't lessen the application's ability to be fully operational.\*

By deploying applications and experiences across multiple availability zones within an AWS Region, it minimizes the risk of a single point of failure taking the application down.

### Region and Availability Zone Naming

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/52ea276b-1450-4184-a25e-09ed10422402/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/52ea276b-1450-4184-a25e-09ed10422402/Untitled.png)

Breakdown of the naming conventions for Regions and Availability Zones (AZ)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/63212fc5-24c8-482f-a7f3-8b4c3f685b27/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/63212fc5-24c8-482f-a7f3-8b4c3f685b27/Untitled.png)

A list of AWS Regions and their Region Identifiers.

## AWS Edge Locations

1. Edge Locations are used as nodes of a global content delivery network (CDN)
2. There are two specific services that utilize AWS Edge Locations:
   1. Amazon CloudFront - Amazon's CDN service
   2. Amazon Route 53 - Amazon's DNS service
3. There are 200 different Edge Locations globally, making Edge Locations the most prevalent part of infrastructure within AWS
4. Allows AWS to serve content from locations closest to users

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/567e1990-857d-4c52-9d73-5f0ce022c89b/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/567e1990-857d-4c52-9d73-5f0ce022c89b/Untitled.png)

An incomplete map of AWS Edge Locations

## Visualizing AWS Global Infrastructure

Within this demo, we'll be:

1. Reviewing the method of accessing the AWS Global Infrastructure site
2. Reviewing Regions and Availability Zones within the site
3. Reviewing Edge Locations within the site

### Accessing the Visualizations

[https://infrastructure.aws](https://infrastructure.aws) - for the new view.

[https://web.archive.org/web/20201105001550/https://www.infrastructure.aws/](https://web.archive.org/web/20201105001550/https://www.infrastructure.aws/) - for the old view.

### Points of Presence

AWS Points of Presents includes both AWS Edge Locations and AWS Edge Cache Servers

## Scenarios

### Scenario 1

- Jane's company is looking to transition to AWS
  - They are starting with a few workloads
  - It is a requirement to store backup data in multiple geographic areas
- Which element of the AWS Global Infrastructure will best suit this need?

AWS Regions

### Scenario 2

- Tim's company serves content through their site to users around the globe
  - They are looking to optimize performance to users around the world
  - They want to leverage a Content Delivery Network (CDN)
- Which element of the AWS Global Infrastructure will be used in this case?

AWS Edge Locations / CloudFront

### Scenario 3

- Ellen's company is transitioning one of their legacy applications to AWS
  - This application required uptime of at least 99.5%
  - They want to be sure any issues at a single data center don't cause an outage
- Which element of the AWS Global Infrastructure supports this need?

AWS Availability Zones

## Summary

In this module we have:

- Reviewed the three elements of the AWS Global Infrastructure
- Understood the use of AWS Regions
- Understood Availability Zones within AWS Regions
- Reviewed the purpose of Edge Locations
- Utilized the AWS Global Infrastructure visualization

---

# Understanding Cloud Economics

Monday 26th July 2021

## Economics of the Cloud

### Overview

In this module, we'll be looking at:

- Understanding funding between traditional data centers and the cloud
- Utilizing AWS tools for cost organization
- Utilizing AWS tools to make a case for moving to the cloud
- Exploring AWS costs using the AWS provided tools

Concepts we need to know:

> **\*Captialized Expenditure (CapEx)**: When building a data center, an organization invests in upfront costs for the building, servers, and supporting equipment. This type of expense to attain a fixed asset is referred to as a **Capitalized Expenditure** or **CapEx**.\*

> **\*Operating Expenditure (OpEx)**: The regular day to day expenses of a business are considered **Operating Expenditures** or **OpEx**. After the initial build of a data center, ongoing connectivity, utility, and maintenance costs would be considered OpEx.\*

### Handling Demand in Your Data Center

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2885ef8d-4e31-48c5-9710-1c6eff0530de/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2885ef8d-4e31-48c5-9710-1c6eff0530de/Untitled.png)

In the early stages of our data center, we have had to make an initial investment to cover capacity that we believe we'll use. In the early months this is **unused capacity** - wasted space. In month 4 we have a bigger problem, we have more users than our data center can handle, which is **demand over capacity**. We then make another investment to grow our data center, to provide enough capacity.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2609344b-597c-4313-ad58-dbfd31a64383/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2609344b-597c-4313-ad58-dbfd31a64383/Untitled.png)

When building out a data center, we have an incredibly large capital expenditure (capex), to create the center. In the following months, we have operational costs (opex) that are incurred by maintaining the center. In month 5, when we expand, we incur another large capital expenditure.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dc022654-0944-4dc3-9859-e894a5826be2/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dc022654-0944-4dc3-9859-e894a5826be2/Untitled.png)

In the cloud, we're able to match our capacity to demand immediately, with a small overhead - this allows us to be as efficient as possible.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5d9411e0-5512-414b-b6a0-bd22072bf5ad/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5d9411e0-5512-414b-b6a0-bd22072bf5ad/Untitled.png)

This has an effect on cost too! As this is all an operational expenditure, we have no capex, and the costs match our usage!

### Financial Implications

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3a239c10-5c36-4acd-8093-7452163f2731/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3a239c10-5c36-4acd-8093-7452163f2731/Untitled.png)

## Organizing and Optimizing AWS Costs

### AWS Cost Explorer

- User Interface for exploring your AWS costs
- Provides breakdowns including:
  - By service
  - By cost tag
- Provides predictions for the next three months of costs
- Gives recommendations for cost optimizaiton
- Can be accessed via API

AWS Cost Explorer works hand-in-hand with AWS Budgets, which:

Utilizes data from AWS Cost Explorer to plan and track your usage across AWS Services. It can track cost per service, service usage, reserved instance utilization and coverage, and Savings Plan utilization and coverage.

### AWS Cost Planning Tools

> **\*AWS TCO Calculator**: Enables an organization to determine what could be saved by leveraging cloud infrastructure\*

> **\*AWS Simple Monthly Calculator**: Enables an organization to calculate the cost of running specific AWS infrastructure\*

### AWS Resource Tags

- Metadata assigned to a specific AWS resource
- Includes a name and an optional value
- Common use cases include department, environment, or project
- Cost allocation report includes costs grouped by active tags
- Tags can be leveraged within the AWS Costs Explorer

### AWS Organizations

- Allows organizations to manage multiple accounts under a single master account
- Provides organizations with the ability to leverage Consolidated Billing for all accounts
- Enables organizations to centralize logging and security standards across accounts

## Using the AWS TCO Calculator

TCO = Total Cost of Ownership

The TCO Calculator helps organizations understand what it would cost them to move a workload into the cloud, and can show cloud costs vs physical costs.

### Demo

In this demo, we will be:

- Accessing the AWS TCO Calculator utility
- Estimating costs savings for an organization using the TCO Calculator
- Downloading a summary report from the TCO Calculator

[awstcocalculator.com](http://awstcocalculator.com)

This tool no longer exists, and has been replaced with the AWS Pricing calculator.

## Using the AWS Pricing Calculator

The AWS Pricing Calculator has replaced the AWS Simple Monthly Calculator (Deprecated) - if the AWS Simple Monthly Calculator is mentioned on an exam, it is important to know that we can do the exact same things with the AWS Pricing Calculator.

### Demo

We will be:

- Accessing the AWS Pricing Calculator
- Estimating costs for a workload on the cloud using the calculator
- Saving and sharing the results with other individuals.

The AWS Pricing Calculator can be accessed at [calculator.aws](http://calculator.aws)

Our demo estimate: [https://calculator.aws/#/estimate?id=ef33cd5fc5f8107939656837861cdf5b9d63d819](https://calculator.aws/#/estimate?id=ef33cd5fc5f8107939656837861cdf5b9d63d819)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c3fbee70-edcd-4065-9de4-3ce0e60b207c/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c3fbee70-edcd-4065-9de4-3ce0e60b207c/Untitled.png)

## Reviewing Costs with the Cost Explorer

### Demo

We'll be:

- Accessing the AWS Cost Explorer within an AWS Account
- Reviewing charges by service for an AWS Account
- Utilizing pre-defined reports included with the Cost Explorer
- Downloading data from the AWS Cost Explorer

To access the cost explorer, load the console, select our username, then Billing Dashboard.

Select Cost Explorer > Launch Cost Explorer

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/565ba540-6677-4288-9f37-fada89a49139/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/565ba540-6677-4288-9f37-fada89a49139/Untitled.png)

To explore costs further, we can select explore costs.

We can select a date range and breakdown type (daily), then group by different options.

Groups:

- **Service** is the service that lead to the charge
- **Linked Account** is accounts linked to our organization

Reports:

- AWS has generated reports for us, such as 'monthly costs by service'
- We can also download reports as csv files.

## Applying Cloud Economics

### Scenario 1

- Oscar's company has multiple departments that work within AWS
  - Finance is asking for a clean separation of AWS costs between departments
  - Currently all single resources are included within a single AWS account
- What approach would meet this need for future costs with minimal effort?

AWS Resource Tags (tag per department)

### Scenario 2

- Cindy's company is considering a transition to the cloud
  - They currently have two physical data centers that they own and maintain
  - Stakeholders are questioning whether this approach will save money
- Which approach should Cindy take to make a case for the cloud?

Utilize the AWS TCO Calculator (and provide reports to stakeholders)

### Scenario 3

- William is a web developer at his company
  - Given some recent downtime he is looking at moving their site to the cloud
  - Finance is asking for an estimate of the costs for this transition to AWS
- What approach should William take to get this data to his finance team?

Utilize the AWS Pricing Calculator and its share functionality

## **Summary**

In this module, we have:

- Understood funding between traditional data centers and the cloud
- Utilized AWS tools for cost organization
- Utilized AWS tools to make a case for moving to the cloud
- Explored AWS costs using the AWS provided tools

---

# Supporting AWS Infrastructure

Tuesday 27th July 2021

## Support Resources

### Overview

In this module, we'll be:

- Understanding the tools provided by AWS to support workloads in the cloud
- Reviewing AWS Support plan tiers
- Reviewing AWS Trusted Advisor recommendations
- Exploring the AWS Personal Health Dashboard

### Supporting Tools

Support, at a high level refers to AWS Support, the service that enables to file support requests with AWS Support.

There are 2 additional services made available to us:

1. AWS Personal Health Dashboard
2. AWS Trusted Advisor

### AWS Support

- Enables support form AWS resources for workloads running in the cloud
- Provided in different tiers based on the need and scope
- Includes tools to provide automated answers and recommendations

### AWS Personal Health Dashboard

> Provides alerts and remediation guidance when AWS is experiencing events that may impact you. - Amazon Web Services

For example, if there was a partial service outage in our region, the Personal Health Dashboard would allow us to gain insight into this.

### AWS Trusted Advisor

- Automated tool to check your AWS Usage against best practices
- Accessed from the AWS console
- Different checks are provided based on the AWS Support plan tier
- All AWS customers get access to seven core checks.

The core checks are divided into 5 categories

- Cost Optimization
- Performance
- Security
- Fault Tolerance
- Service Limits

## AWS Support Plan Tiers

There are 4 different support plans. The difference between the support plan tiers falls into 4 categories:

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f110f098-7f9c-4919-bf24-d456401a6513/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f110f098-7f9c-4919-bf24-d456401a6513/Untitled.png)

### AWS Basic Support

- Provided for all AWS customers
- Access to Trusted Advisor (7 Core Checks)
- 24x7 Access to customer service, documentation, forums & whitepapers
- Access to AWS Personal Health Dashboard
- No monthly cost

### AWS Developer Support

- Includes all features of Basic Support
- Business hours email access to support engineers
- Limited to 1 primary contact
- Starts at $29 per month (tied to AWS usage - cost can increase with additional usage/resources)

### AWS Business Support

- Includes all features of Developer Support
- Full set of Trusted Advisor checks
- 24x7 phone, email and chat access to support engineers
- Unlimited contacts
- Provides third-party software support
- Starts at $100 per month (tied to AWS usage)

### AWS Enterprise support

- Includes all features of Business Support
- Includes designated Technical Account Manager (TAM)
- Includes concierge support team
- Starts at $15,000 per month (tied to AWS usage)

### Support Response Times

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2a2a850b-808a-490d-9ab5-a23540f0109d/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2a2a850b-808a-490d-9ab5-a23540f0109d/Untitled.png)

AWS Support Response Times

## AWS Support Tools

In this demo, we'll be:

- Accessing AWS Trusted Advisor in the console
- Reviewing AWS Trusted Advisor Recommendations
- Accessing the AWS Personal Health Dashboard
- Reviewing information provided in the AWS Personal Health Dashboard

### Trusted Advisor

Trusted Advisor can be accessed from the console, using the search bar.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7fcac8a7-9393-4fae-8e96-54376b35eb08/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7fcac8a7-9393-4fae-8e96-54376b35eb08/Untitled.png)

Trusted Advisor will show a check for all five groups:

- Cost Optimization
- Performance
- Security
- Fault Tolerance
- Service Limits

For accounts with basic support only, we will only see recommendations in Security and Service Limits. Business and Enterprise support plans will show recommendations for all 5 categories.

Example Check:

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1afa4dcd-3656-47bd-9e29-ccb2fe417cc4/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1afa4dcd-3656-47bd-9e29-ccb2fe417cc4/Untitled.png)

### Personal Health Dashboard

The Personal Health Dashboard can be accessed from the console, using the search bar.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0bc016b1-9963-47f9-a8e3-6479a2d24e94/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0bc016b1-9963-47f9-a8e3-6479a2d24e94/Untitled.png)

We can see all of the current issues from this dashboard. For a log of issues, we can select event log, which will show us the status of any events, and if it affects any of our resources.

## Infrastructure Support Scenarios

### Scenario 1

- Sylvia's company is in the process of moving multiple workloads into AWS
  - One of these workloads is a mission critical application
  - Her CTO says that they need to be able to call support 24 hours a day
- What is the most cost effective support plan that meets this criteria?

Business Support Plan

### Scenario 2

- Edward's company is evaluating AWS for future workloads
  - One of the workloads supports multiple offices globally
  - The company needs to be a able to call, text, or email support if an issue occurs
  - The company also need a response from support in 15 minutes
- What is the most cost effective support plan that meets this criteria?

Enterprise Support Plan

### Scenario 3

- William has an AWS account for a personal project
  - He doesn't expect to need technical guidance from AWS
  - He does want access to the AWS Trusted Advisor core checks
- What is the most cost effective support plan that meets this criteria?

Basic Support Plan

## When You Need Help

There are several resources that can help if we're wondering whether we're doing AWS right, and that can help us migrate to the cloud:

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0da42b23-bf6c-43b6-95e2-0ee9ca2ecaaa/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0da42b23-bf6c-43b6-95e2-0ee9ca2ecaaa/Untitled.png)

- AWS Quick Start - each quick start provides step-by-step deployment guidance for a common technology platform into AWS . A great place for organisations that are using a common platform, and just want to know if they're doing it the right way.
- AWS Partner Network Consulting Partners - Provides access to vetted third-party consultants that can assist with AWS. They don't work for directly for AWS.
- AWS Professional Services - AWS's own PS team. They can assist with all things AWS.

## Summary

During this module, we have:

- Understood the tools provided by AWS to support workloads in the cloud
- Reviewed AWS Support Plan tiers
- Reviewed AWS Trusted Advisor recommendations
- Explored the AWS Personal Health Dashboard

## Preparing for the Exam

Don't sign up for the certification until completing the path! The path will cover getting signed up for the exam, and how to get ready for taking the plan.

Study the notes, including the downloaded notes package!

Don't skip the last course in the path!

---

# Path Learning Check

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/00306180-4a0c-4f42-8211-621c39e3effe/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/00306180-4a0c-4f42-8211-621c39e3effe/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c12856ba-958a-43ef-a373-c91a6fa443d9/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c12856ba-958a-43ef-a373-c91a6fa443d9/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e022bde6-09c7-4210-90bc-53ac7a6e7d7e/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e022bde6-09c7-4210-90bc-53ac7a6e7d7e/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ac822760-fdcb-473e-b0d0-ef06e05f794f/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ac822760-fdcb-473e-b0d0-ef06e05f794f/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5bd1d38e-bd2c-4ee8-979b-a33e4381cf17/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5bd1d38e-bd2c-4ee8-979b-a33e4381cf17/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9398b3a7-cfa9-4e02-b27a-48dd619a80df/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9398b3a7-cfa9-4e02-b27a-48dd619a80df/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ddf93bb2-d49d-4e80-b6b9-93f0f7129918/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ddf93bb2-d49d-4e80-b6b9-93f0f7129918/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/152f2b89-c508-4f49-9fe5-ac054a795c22/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/152f2b89-c508-4f49-9fe5-ac054a795c22/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/120e2235-9e2c-4a9f-95e5-ea8c4937ca6a/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/120e2235-9e2c-4a9f-95e5-ea8c4937ca6a/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dfd82d20-cb21-4f58-921f-4a8b4b5a4940/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dfd82d20-cb21-4f58-921f-4a8b4b5a4940/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0c00f184-c57f-4250-8f4a-6dc5b979f685/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0c00f184-c57f-4250-8f4a-6dc5b979f685/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/61e0b053-ecc4-4000-b462-a31a07ea323a/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/61e0b053-ecc4-4000-b462-a31a07ea323a/Untitled.png)
