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
- Deliver A2A notificatins to integrate and decouple distributed applications.

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
