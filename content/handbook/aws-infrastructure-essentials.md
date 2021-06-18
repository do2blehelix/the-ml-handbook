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
  _In AWS, these virtual machines are called Amazon Elastic Compute Cloud or Amazon EC2_
* Container Services
* Serverless

#### Container Services

* ECS = Elastic Container Service
* EKS = Elastic Kubernetes Service

ECS and EKS run on clusters of EC2 instances

Lambda = Serverless

Fargate is a serverless compute platform for ECS or EKS

##### Containers vs Virtual Machines

Containers share the same operating system and kernel as the host they exist on, whereas virtual machines contain their operating system. Since each virtual machine has to maintain a copy of an operating system, there’s a degree of wasted space. A container is more lightweight. They spin up quicker, almost instantly. This difference in startup time becomes instrumental when designing applications that need to scale quickly during input/output (I/O) bursts. While containers can provide speed, virtual machines offer you the full strength of an operating system and offer more resources, like package installation, a dedicated kernel, and more.

Serverless: You cannot see or access the underlying infrastructure that are hosting your solution. _AWS Fargate_

* Software and OS patching is not required
* Scaling and Fault tolerance is built-in
* Much more convenient than EC2 instances (or ECS/EKS)
* Only for code that requires runtime of less than 15 mins

AWS Lambda sits on top of Fargate

### When to run what?

* If you run your code on Amazon EC2, AWS is responsible for the physical hardware and you are responsible for the logical controls, such as guest operating system, security and patching, networking, security, and scaling.
* If you run your code in containers on Amazon ECS and Amazon EKS, AWS is responsible for more of the container management, such as deploying containers across EC2 instances and managing the container cluster. However, when running ECS and EKS on EC2, you are still responsible for maintaining the underlying EC2 instances.
* If you want to deploy your workloads and applications without having to manage any EC2 instances, you can do that on AWS with _serverless_ compute.

There are three primary components of a Lambda function:

* trigger
* code
* configuration

***

## AWS Network

IGW = Internet Gateway. Required to establish a connection with the internet

Subnets = Groups of IP addresses

***

## AWS Storage

* Block Storage: divides the file into chunks of data to store
* Object Storage: stores the entire file as a chunk of data

Storage Types:

* EC2 Instance Store - form of directly attached storage. data is deleted if the EC2 instance stops. high speed temporary storage data
* EBS (Elastic Block Store) - similar to an external hard disk attached to the server

  EBS can only be attached to EC2 instances
* S3

### Policies

When IAM policies are attached to IAM users, groups, and roles, the policies define which actions they can perform. IAM policies are not tied to any one AWS service and can be used to define access to nearly any AWS action.

S3 bucket policies are similar to IAM policies, in that they are both defined using the same policy language in a JSON format. The difference is IAM policies are attached to users, groups, and roles, whereas S3 bucket policies are only attached to buckets. S3 bucket policies specify what actions are allowed or denied on the bucket.

### Storage

There are six S3 storage classes.

1. **Amazon S3 Standard:** This is considered general purpose storage for cloud applications, dynamic websites, content distribution, mobile and gaming applications, and big data analytics.
2. **Amazon S3 Intelligent-Tiering:** This tier is useful if your data has unknown or changing access patterns. S3 Intelligent-Tiering stores objects in two tiers, a frequent access tier and an infrequent access tier. Amazon S3 monitors access patterns of your data, and automatically moves your data to the most cost-effective storage tier based on frequency of access.
3. **Amazon S3 Standard-Infrequent Access (S3 Standard-IA):** S3 Standard-IA is for data that is accessed less frequently, but requires rapid access when needed. S3 Standard-IA offers the high durability, high throughput, and low latency of S3 Standard, with a low per-GB storage price and per-GB retrieval fee. This storage tier is ideal if you want to store long-term backups, disaster recovery files, and so on.
4. **Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA):** Unlike other S3 storage classes which store data in a minimum of three Availability Zones (AZs), S3 One Zone-IA stores data in a single AZ and costs 20% less than S3 Standard-IA. S3 One Zone-IA is ideal for customers who want a lower-cost option for infrequently accessed data but do not require the availability and resilience of S3 Standard or S3 Standard-IA. It’s a good choice for storing secondary backup copies of on-premises data or easily re-creatable data.
5. **Amazon S3 Glacier:** S3 Glacier is a secure, durable, and low-cost storage class for data archiving. You can reliably store any amount of data at costs that are competitive with or cheaper than on-premises solutions. To keep costs low yet suitable for varying needs, S3 Glacier provides three retrieval options that range from a few minutes to hours.
6. **Amazon S3 Glacier Deep Archive:** S3 Glacier Deep Archive is Amazon S3’s lowest-cost storage class and supports long-term retention and digital preservation for data that may be accessed once or twice in a year. It is designed for customers—particularly those in highly regulated industries, such as the Financial Services, Healthcare, and Public Sectors—that retain data sets for 7 to 10 years or longer to meet regulatory compliance requirements.