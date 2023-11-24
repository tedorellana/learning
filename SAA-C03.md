# AWS Certified Solutions Architect [SAA - C03] #

### S3 Transfer Acceleration ###
- Good for high speed
- Designed to optimize transfer speeds from across the world into S3 buckets.

### Amazon Athena ###

- Interactive query service
- Works with Amazon Simple Storage Service (Amazon S3)
- Use standard SQL
- Can run ad-hoc queries and get result in seconds.

### Principal OrgID ###
- Validates if the principal accessing the resource is within your organization.

### VPC Endpoints ###
- Allows to connect to AWS services using a private network instead using the public internet.

### Amazon Elastic File System ###
- Store files without server
- Pay just for the storage.
- Support corss az.

### Elastic Block Store ###
- High performance access.
- Works inside az (availability zones).
- Do not support cross az.

### AWS Snowball Edge ###
- Can copy files with speed yp to 100 GBps
- Move offline data or remote storage to cloud.
- Easily migrate terabytes of data to the cloud without limits in storage capacity or compute power.

### Simple Notification Service ###
- Deliver A2A notifications to integrate and decouple distributed applications.
- Amazon Simple Notification Service (Amazon SNS) is a managed service that provides message delivery from publishers to subscribers (also known as producers and consumers). Publishers communicate asynchronously with subscribers by sending messages to a topic, which is a logical access point and communication channel.
- Clients can subscribe to the SNS topic and receive published messages using a supported endpoint type, such as Amazon Kinesis Data Firehose, Amazon SQS, AWS Lambda, HTTP, email, mobile push notifications, and mobile text messages (SMS).
![SNS Diagram](/images/simple-notification-service-diagram.png)

### Simple Queue Service ###
- Queues messages managed for microservices, distributed systems and serverless applications.

### What is Amazon S3 Glacier ###
- The Amazon S3 Glacier storage classes are purpose-built for data archiving, providing you with the highest performance, most retrieval flexibility, and the lowest cost archive storage in the cloud.

- Choose from three archive storage classes optimized for different access patterns and storage duration.

- The S3 Glacier storage classes provide virtually unlimited scalability and are designed for 99.999999999% (11 nines) of data durability.

### Amazon Elastic File System (EFS) ###
- Serverless, fully elastic file storage
- Automatically grows and shrinks as you add and remove files with no need for management or provisioning.

##  S3 Lifecycle configuration ##
Is a set of rules that define actions that Amazon S3 applies to a group of objects. There are two types of actions:

### Transition actions ###
- These actions define when objects transition to another storage class. For example, you might choose to transition objects to the S3 Standard-IA storage class 30 days after creating them, or archive objects to the S3 Glacier Flexible Retrieval storage class one year after creating them. For more information, see Using Amazon S3 storage classes.

- There are costs associated with lifecycle transition requests. For pricing information, see Amazon S3 pricing.

### Expiration actions ###
- These actions define when objects expire. Amazon S3 deletes expired objects on your behalf.

- Lifecycle expiration costs depend on when you choose to expire objects. For more information, see Expiring objects.

## S3 File Gateway ##
- Provides a seamless way to connect to the cloud in order to store application data files and backup images as durable objects in Amazon S3 cloud storage. Amazon S3 File Gateway offers SMB or NFS-based access to data in Amazon S3 with local caching.

## Amazon API Gateway ##
- Is an AWS service for creating, publishing, maintaining, monitoring, and securing REST, HTTP, and WebSocket APIs at any scale. API developers can create APIs that access AWS or other web services, as well as data stored in the AWS Cloud .

## AWS Secrets Manager ##
- Is a secrets management service that helps you protect access to your applications, services, and IT resources

## Amazon CloudFront ##
- Is a web service that speeds up distribution of your static and dynamic web content, such as .html, .css, .js, and image files, to your users.

## Amazon Aurora (Aurora) ##
- Is a fully managed relational database engine that's compatible with MySQL and PostgreSQL. You already know how MySQL and PostgreSQL combine the speed and reliability of high-end commercial databases with the simplicity and cost-effectiveness of open-source databases.
- Better for read than write.
- Is 5x performance improvement over MySQL on RDS and handles more read requests than write.

## Amazon Relational Database Service (Amazon RDS) ## 
- Is a web service that makes it easier to set up, operate, and scale a relational database in the AWS Cloud. It provides cost-efficient, resizable capacity for an industry-standard relational database and manages common database administration tasks.

## VPC ##
- Is a virtual network that closely resembles a traditional network that you'd operate in your own data center

## AWS Network Firewall ##
- Is a managed firewall service that provides filtering for both inbound and outbound network traffic. It allows you to create rules for traffic inspection and filtering, which can help protect your production VPC.

## Amazon GuardDuty ##
- Is a threat detection service, not a traffic inspection or filtering service.

## Traffic Mirroring ##
- Is a feature that allows you to replicate and send a copy of network traffic from a VPC to another VPC or on-premises location. It is not a service that performs traffic inspection or filtering.

## AWS Firewall Manager ##
- Is a security management service that helps you to centrally configure and manage firewalls across your accounts. It is not a service that performs traffic inspection or filtering.

## QuickSight ##
- Is used to created dashboard from S3, RDS, Redshift, Aurora, Athena, OpenSearch, Timestream.
- Serveless BI.

## IAM Role ## 
- Could be used to grant access to an EC2 Intance.

## Gateway Load Balancer endpoint ##
- Is a VPC endpoint that provides private connectivity between virtual appliances in the service provider VPC and application servers in the service consumer VPC.

## Amazon Elastic Block Store (Amazon EBS) ##
- Is an easy-to-use, scalable, high-performance block-storage service designed for Amazon Elastic Compute Cloud (Amazon EC2).

## Amazon CloudFront ##
- Is a web service that speeds up distribution of your static and dynamic web content, such as .html, .css, .js, and image files, to your users. CloudFront delivers your content through a worldwide network of data centers called edge locations. When a user requests content that you're serving with CloudFront, the request is routed to the edge location that provides the lowest latency (time delay), so that content is delivered with the best possible performance.

  - If the content is already in the edge location with the lowest latency, CloudFront delivers it immediately.

  - If the content is not in that edge location, CloudFront retrieves it from an origin that you've defined—such as an Amazon S3 bucket, a MediaPackage channel, or an HTTP server (for example, a web server) that you have identified as the source for the definitive version of your content.

## S3 Intelligent-Tiering ##

- Amazon S3 Intelligent Tiering is a storage class that automatically moves data to the most cost-effective storage tier based on access patterns. It can store objects in two access tiers: the frequent access tier and the infrequent access tier. The frequent access tier is optimized for frequently accessed objects and is charged at the same rate as S3 Standard. The infrequent access tier is optimized for objects that are not accessed frequently and are charged at a lower rate than S3 Standard.
- S3 Intelligent Tiering is a good choice for storing media files that are accessed frequently and infrequently in an unpredictable pattern because it automatically moves data to the most cost-effective storage tier based on access patterns, minimizing storage and retrieval costs. It is also resilient to the loss of an Availability Zone because it stores objects in multiple Availability Zones within a region.

## Amazon S3 Glacier Deep Archive ##
- Is a secure, durable, and extremely low-cost Amazon S3 storage class for long-term retention of data that is rarely accessed and for which retrieval times of several hours are acceptable. It is the lowest-cost storage option in Amazon S3, making it a cost-effective choice for storing backup files that are not accessed after 1 month.

## AWS Cost Explorer ##
- Is a tool that enables you to view and analyze your costs and usage. You can explore your usage and costs using the main graph, the Cost Explorer cost and usage reports, or the Cost Explorer RI reports.
- Is a paid service ($0.01 per query). By using cost explorer you can dig down into the finer details of expenditure, such as on a region, service, usage type or even tag based level. Using this you can identify costs by targeting your query to be specific enough to identify these charges. Additionally you can make use of hourly billing to get the most accurate upto date billing
  
## AWS Billing and Cost Management ##
- Is a web service that provides features that helps you pay your bills and optimize your costs. Amazon Web Services bills your account for usage, which ensures that you pay only for what you use.
- Provides a summarised view of spending i.e. what you spent so far this month, and the predicted end of month bill, this is quite static and gives you a high level overview of spending. In addition you can configure your billing details from here. All of these features are free to use with no charge for accessing the interface.

## AWS Config ##
- Helps you record configuration changes to software within EC2 instances in your AWS account and also virtual machines (VMs) or servers in your on-premises environment. The configuration information recorded by AWS Config includes Operating System updates, network configuration, and installed applications.

## CloudWatch ##
- Is a monitoring and management service that provides data and actionable insights for AWS, on-premises, hybrid, and other cloud applications and infrastructure resources.

## Global Accelerator ##
- Is a global service that supports endpoints in multiple AWS Regions.
- Has automatic failover
- Is a good fit for non-HTTP use cases, such as gaming (UDP), IoT (MQTT), or Voice over IP, as well as for HTTP use cases that specifically require static IP addresses or deterministic, fast regional failover. Both services integrate with AWS Shield for DDoS protection.

## Amazon Kinesis Data Firehose ##
Is a fully managed service for delivering real-time streaming data to destinations such as Amazon Simple Storage Service (Amazon S3), Amazon Redshift, Amazon OpenSearch Service, Amazon OpenSearch Serverless, Splunk, and any custom HTTP endpoint or HTTP endpoints owned by supported third-party service providers, including Datadog, Dynatrace, LogicMonitor, MongoDB, New Relic, Coralogix, and Elastic. Kinesis Data Firehose is part of the Kinesis streaming data platform, along with Kinesis Data Streams, Kinesis Video Streams, and Amazon Managed Service for Apache Flink. With Kinesis Data Firehose, you don't need to write applications or manage resources.

## Amazon Kinesis Data Streams ##
Is a fully managed streaming data service. You can continuously add various types of data such as clickstreams, application logs, and social media to a Kinesis stream from hundreds of thousands of sources. Within seconds, the data will be available for your Kinesis Applications to read and process from the stream.

## CloudTrail ##
Track user activity and API call history.

## Config ##
Assess, audits, and evaluates the configuration and relationships of tag resources.

## AWS Shield Advanced ## 
Provides expanded DDoS attack protection for your Amazon EC2 instances, Elastic Load Balancing load balancers, CloudFront distributions, Route 53 hosted zones, and AWS Global Accelerator standard accelerators.

## Multi-region KMS keys. ##
A new capability that lets you replicate keys from one region into another. With multi-region keys, you can more easily move encrypted data between regions without having to decrypt and re-encrypt with different keys in each region

## AWS KMS keys (KMS keys) ##
Are the primary resource in AWS KMS. You can use a KMS key to encrypt, decrypt, and re-encrypt data. It can also generate data keys that you can use outside of AWS KMS. Typically, you'll use symmetric encryption KMS keys, but you can create and use asymmetric KMS keys for encryption or signing, and create and use HMAC KMS keys to generate and verify HMAC tags.

## An AWS KMS key ##
Is a logical representation of a cryptographic key. A KMS key contains metadata, such as the key ID, key spec, key usage, creation date, description, and key state. Most importantly, it contains a reference to the key material that is used when you perform cryptographic operations with the KMS key.

## Session Manager ##
Is a fully managed AWS Systems Manager capability that lets you manage your EC2 instances, on-premises instances, and virtual machines (VMs) through an interactive one-click browser-based shell or through the AWS CLI.

## Provisioned IOPS volumes, backed by solid-state drives (SSDs) ## 
Are the highest performance Amazon Elastic Block Store (Amazon EBS) storage volumes designed for your critical, IOPS-intensive and throughput-intensive workloads that require low latency.

## Amazon AppFlow ##
Is a fully managed integration service that enables you to securely transfer data between Software-as-a-Service (SaaS) applications like Salesforce, SAP, Zendesk, Slack, and ServiceNow, and AWS services like Amazon S3 and Amazon Redshift, in just a few clicks

## Gateway VPC endpoint ##
- Gateway VPC endpoints provide reliable connectivity to Amazon S3 and DynamoDB without requiring an internet gateway or a NAT device for your VPC. Gateway endpoints do not use AWS PrivateLink, unlike other types of VPC endpoints.
- There is no additional charge for using gateway endpoints.
- Deploying a gateway VPC endpoint for Amazon S3 is the most cost-effective way for the company to avoid Regional data transfer charges. 
- A gateway VPC endpoint is a network gateway that allows communication between instances in a VPC and a service, such as Amazon S3, without requiring an Internet gateway or a NAT device.
- Data transfer between the VPC and the service through a gateway VPC endpoint is free of charge, while data transfer between the VPC and the Internet through an Internet gateway or NAT device is subject to data transfer charges. By using a gateway VPC endpoint, the company can reduce its data transfer costs by eliminating the need to transfer data through the NAT gateway to access Amazon S3. This option would provide the required connectivity to Amazon S3 and minimize data transfer charges.

## A NAT gateway is a Network Address Translation (NAT) service ##
You can use a NAT gateway so that instances in a private subnet can connect to services outside your VPC but external services cannot initiate a connection with those instances. When you create a NAT gateway, you specify one of the following connectivity types:

- Public – (Default) Instances in private subnets can connect to the internet through a public NAT gateway, but cannot receive unsolicited inbound connections from the internet. You create a public NAT gateway in a public subnet and must associate an elastic IP address with the NAT gateway at creation. You route traffic from the NAT gateway to the internet gateway for the VPC. Alternatively, you can use a public NAT gateway to connect to other VPCs or your on-premises network. In this case, you route traffic from the NAT gateway through a transit gateway or a virtual private gateway.

- Private – Instances in private subnets can connect to other VPCs or your on-premises network through a private NAT gateway. You can route traffic from the NAT gateway through a transit gateway or a virtual private gateway. You cannot associate an elastic IP address with a private NAT gateway. You can attach an internet gateway to a VPC with a private NAT gateway, but if you route traffic from the private NAT gateway to the internet gateway, the internet gateway drops the traffic.

## AWS Direct Connect ##
Is a network service that allows you to establish a dedicated network connection from your on-premises data center to AWS. This connection bypasses the public Internet and can provide more reliable, lower-latency communication between your on-premises application and Amazon S3. By directing backup traffic through the AWS Direct Connect connection, you can minimize the impact on your internet bandwidth and ensure timely backups to S3.

## To prevent or mitigate future accidental deletions, consider the following features ##

- Enable versioning to keep historical versions of an object.
- Enable Cross-Region Replication of objects.
- Enable MFA delete to require multi-factor authentication (MFA) when deleting an object version.

## Amazon Macie ##
Is a data security service that discovers sensitive data using machine learning and pattern matching, provides visibility into data security risks, and enables automated protection against those risks.

## Patch Manager ##
The primary focus of Patch Manager, a capability of AWS Systems Manager, is on installing operating systems security-related updates on managed nodes. By default, Patch Manager doesn't install all available patches, but rather a smaller set of patches focused on security. (Ref https://docs.aws.amazon.com/systems-manager/latest/userguide/patch-manager-how-it-works-selection.html)


## AWS Systemss Run Command ##
Run Command allows you to automate common administrative tasks and perform one-time configuration changes at scale.

## Amazon EventBridge ##
EventBridge is a serverless service that uses events to connect application components together, making it easier for you to build scalable event-driven applications. Event-driven architecture is a style of building loosely-coupled software systems that work together by emitting and responding to events. Event-driven architecture can help you boost agility and build reliable, scalable applications.

## Elastic File System ##
EFS is a managed elastic file system designed for use across different machines and availability zones, 

## Elastic Block Store ##
EBS is designed as a fast and reliable block storage volume for single machines

## S3 Object Lock ##
Blocks permanent object deletion during a customer-defined retention period so that you can enforce retention policies as an added layer of data protection or for regulatory compliance.

## Amazon FSx for Windows File Server ##
Provides fully managed Microsoft Windows file servers, backed by a fully native Windows file system. FSx for Windows File Server has the features, performance, and compatibility to easily lift and shift enterprise applications to the AWS Cloud.

## Amazon Comprehend ##
Is a natural-language processing (NLP) service that uses machine learning to uncover valuable insights and connections in text.

## Amazon Rekognition ##
Makes it easy to add image and video analysis to your applications. You just have to provide an image or video to the Amazon Rekognition API, and the service can:

- Identify labels (objects, concepts, people, scenes, and activities) and text*
- Detect inappropriate content
- Provide highly accurate facial analysis, face comparison, and face search capabilities

## Amazon SageMaker ##
Is a fully managed machine learning service. With SageMaker, data scientists and developers can quickly and easily build and train machine learning models, and then directly deploy them into a production-ready hosted environment

## AWS Fargate ## 
Is a technology that you can use with Amazon ECS to run containers without having to manage servers or clusters of Amazon EC2 instances. With Fargate, you no longer have to provision, configure, or scale clusters of virtual machines to run containers.