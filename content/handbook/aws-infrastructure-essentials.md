---
title: AWS Infrastructure Essentials
description: AWS Infrastructure Essentials
date: 2021-05-04T13:30:00.000+00:00
weight: 1
collapsible: false

---
# AWS Infrastructure Essentials

AWS stands for Amazon Web Services. It is one of the leading platforms for data hosting and server management

Now, lets look at hosting an application. The primary components of hosting are:

* Well you need to build the application
* And you need the application to be hosted somewhere that keeps it running 24/7
* You need to store the incoming user generated data somewhere, right.
* Once your application is up, you need to monitor and check for scaling of the application
* And last but not the least, you need to have separate access to specific users.

***

## AWS Acronyms

Now, when you are starting with AWS, you would be bombarded with a lot of acronyms. Here's listing some of the common acronyms that will ease your learning journey. Make sure to read and remember them.

##### To Build Application

* **VPC** = Virtual Private Cloud

##### To Host Application

* **EC2** = Elastic Compute Cloud :: _EC2 offers virtual machines on AWS_

##### To Store Data

* **RDS** = Relational Database Service
* **DynamoDB**
* **S3** = Simple Storage Service :: _Used for Object Storage_

##### To Monitor the solution

* **Amazon CloudWatch** :: _To ensure app is fault tolerant and scalable_
* **ELB** = Elastic Load Balancer :: _To distribute the load between multiple EC2 instances_
* **EC2 Auto Scaling** :: _To scale in or out depending on load_

##### For Identity Management

* **IAM** = Identity and Access Management

### AWS Global Infrastructure

**Data Centers** store our data on the cloud

**Availability Zone** clusters Data Centers together

**Regions** cluster Availability Zones together

_These are done as contingencies with redundant power, networking, and connectivity. AWS allows you to choose a particular region (named after physical locations)_

To choose a region, the 4 factors can play an important role

* **Compliance**: Eg company requires you to operate data within USA
* **Latency**: High latency can cause application slowdown
* **Price**: Basis the region, the pricing is affected
* **Service Availability**: What services are available in a particular region

### Interacting with AWS

* AWS Management Console: Web based console that you can login through your browser
* AWS Command Line Interface: Run commands through a command prompt
* AWS Software Development Kits

***

### Identity and Access Management

* Can handle access to login to AWS Account and give permissions to API calls
* However, it cannot handle Application Level Access Control

***

### Compute as a Service

AMI : Amazon Machine Image contains information about how to configure the os and apps.

There are fundamentally 3 types of compute options:

* Virtual Machines  
  In AWS, these virtual machines are called Amazon Elastic Compute Cloud or Amazon EC2
* Container Services
* Serverless

ECS = Elastic Container Service

EKS = Elastic Kubernetes Service

Lambda = Serverless