# AWS Certified Solutions Architect [SAA - C03] #

### S3 Transfer Acceleration ###
- Good for high speed
- Designed to optimize transfer speeds from across the world into S3 buckets.

### Principal OrgID ###
- Validates if the principal accessing the resource is within your organization.

## VPC ##
- Is a virtual network that closely resembles a traditional network that you'd operate in your own data center. After you create a VPC, you can add subnets.

### VPC Endpoints ###
- Allows to connect to AWS services using a private network instead using the public internet.

## Virtual private gateway ##
A virtual private gateway is the VPN endpoint on the Amazon side of your Site-to-Site VPN connection that can be attached to a single VPC.

## A VPC endpoint ##
Enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection.

## VPC and subnets overview ##
The following diagram provides an overview of the resources included in this example. The VPC has public subnets and private subnets in two Availability Zones. Each public subnet contains a NAT gateway and a load balancer node. The servers run in the private subnets, are launched and terminated by using an Auto Scaling group, and receive traffic from the load balancer. The servers can connect to the internet by using the NAT gateway. The servers can connect to Amazon S3 by using a gateway VPC endpoint.

![VPC Subnets Structure Overview](/images/vpc-subnets-structure-overview.png)

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

## S3 Standard-Infrequent Access ## 
Is for data that is accessed less frequently, but requires rapid access when needed. S3 Standard-IA offers the high durability, high throughput, and low latency of S3 Standard, with a low per GB storage price and per GB retrieval charge.


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
Is a web service that speeds up distribution of your static and dynamic web content, such as .html, .css, .js, and image files, to your users.
CloudFront improves performance for both cacheable content (such as images and videos) and dynamic content (such as API acceleration and dynamic site delivery).
CloudFront uses Edge Locations to cache content

## AWS Global Accelerator ##
AWS Global Accelerator is a networking service that helps you improve the availability, performance, and security of your public applications. Global Accelerator provides two global static public IPs that act as a fixed entry point to your application endpoints, such as Application Load Balancers, Network Load Balancers, Amazon Elastic Compute Cloud (EC2) instances, and elastic IPs.
Use Edge Locations to find an optimal pathway to the nearest regional endpoint.
Good fit for non-HTTP use cases, such as gaming (UDP), IoT (MQTT), or Voice over IP, as well as for HTTP use cases that specifically require static IP addresses

![AWS Global Accelerator](/images/aws-global-accelerator.png)

## Amazon Aurora (Aurora) ##
- Is a fully managed relational database engine that's compatible with MySQL and PostgreSQL. You already know how MySQL and PostgreSQL combine the speed and reliability of high-end commercial databases with the simplicity and cost-effectiveness of open-source databases.
- Better for read than write.
- Is 5x performance improvement over MySQL on RDS and handles more read requests than write.
- Aurora provides up to five times better latency than RDS and can scale up to ten times more packed operations per second than MySQL engine in RDS. It also offers an encrypted storage option for better data security

## The warm standby approach ##
Involves ensuring that there is a scaled down, but fully functional, copy of your production environment in another Region. This approach extends the pilot light concept and decreases the time to recovery because your workload is always-on in another Region.

## Amazon Relational Database Service (Amazon RDS) for MySQL ##
Is a fully managed, open source, relational database that makes it easier to set up, operate, and scale MySQL databases in the cloud.

## Amazon Relational Database Service (Amazon RDS) ## 
- Is a web service that makes it easier to set up, operate, and scale a relational database in the AWS Cloud. It provides cost-efficient, resizable capacity for an industry-standard relational database and manages common database administration tasks.

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

## Amazon Redshift ##
Is a fully managed, petabyte-scale data warehouse service in the cloud. Amazon Redshift Serverless lets you access and analyze data without all of the configurations of a provisioned data warehouse. Resources are automatically provisioned and data warehouse capacity is intelligently scaled to deliver fast performance for even the most demanding and unpredictable workloads.
You don't incur charges when the data warehouse is idle, so you only pay for what you use.

## IAM Role ## 
- Could be used to grant access to an EC2 Intance.

## Gateway Load Balancer endpoint ##
- Is a VPC endpoint that provides private connectivity between virtual appliances in the service provider VPC and application servers in the service consumer VPC.

## Amazon Elastic Block Store (Amazon EBS) ##
- Is an easy-to-use, scalable, high-performance block-storage service designed for Amazon Elastic Compute Cloud (Amazon EC2).
- Expensive than S3 and EFS

### Amazon Elastic File System ###
- Store files without server
- Pay just for the storage.
- Support cross Availability zones.
- Cheap than EBS
- Expensive than S3

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

# CloudWatch #
- Is a monitoring and management service that provides data and actionable insights for AWS, on-premises, hybrid, and other cloud applications and infrastructure resources.
- You can send continually metrics as streams to a destination of your choice. Could be Amazon kinesis Data Firehouse.

## Amazon CloudWatch logs ##
You can use Amazon CloudWatch Logs to monitor, store, and access your log files from Amazon Elastic Compute Cloud (Amazon EC2) instances, AWS CloudTrail, Route 53, and other sources.s
CloudWatch Logs enables you to centralize the logs from all of your systems, applications, and AWS services that you use, in a single, highly scalable service. You can then easily view them, search them for specific error codes or patterns, filter them based on specific fields, or archive them securely for future analysis. CloudWatch Logs enables you to see all of your logs, regardless of their source, as a single and consistent flow of events ordered by time.

## Composite alarms ##
Determine their states by monitoring the states of other alarms. You can **use composite alarms to reduce alarm noise**. For example, you can create a composite alarm where the underlying metric alarms go into ALARM when they meet specific conditions. You then can set up your composite alarm to go into ALARM and send you notifications when the underlying metric alarms go into ALARM by configuring the underlying metric alarms never to take actions.

## Global Accelerator ##
- Is a global service that supports endpoints in multiple AWS Regions.
- Has automatic failover
- Is a good fit for non-HTTP use cases, such as gaming (UDP), IoT (MQTT), or Voice over IP, as well as for HTTP use cases that specifically require static IP addresses or deterministic, fast regional failover. Both services integrate with AWS Shield for DDoS protection.
- Improves performance for a wide range of applications over TCP or UDP by proxying packets at the edge to applications running in one or more AWS Regions. 

### Amazon Athena ###
- Interactive query service
- Works with Amazon Simple Storage Service (Amazon S3)
- Use standard SQL
- Can run ad-hoc queries and get result in seconds.
- Athena queries historical data from S3.

## Amazon Kinesis Data Firehose ##
Is a fully managed service for delivering real-time streaming data to destinations such as Amazon Simple Storage Service (Amazon S3), Amazon Redshift, Amazon OpenSearch Service, Amazon OpenSearch Serverless, Splunk, and any custom HTTP endpoint or HTTP endpoints owned by supported third-party service providers, including Datadog, Dynatrace, LogicMonitor, MongoDB, New Relic, Coralogix, and Elastic. Kinesis Data Firehose is part of the Kinesis streaming data platform, along with Kinesis Data Streams, Kinesis Video Streams, and Amazon Managed Service for Apache Flink. With Kinesis Data Firehose, you don't need to write applications or manage resources.

## Amazon Kinesis Data Streams ##
Is a fully managed streaming data service. You can continuously add various types of data such as clickstreams, application logs, and social media to a Kinesis stream from hundreds of thousands of sources. Within seconds, the data will be available for your Kinesis Applications to read and process from the stream.

## Amazon Kinesis Data Analytics ##
Enables you to quickly author SQL code that continuously reads, processes, and stores data in near real time. Using standard SQL queries on the streaming data, you can construct applications that transform and provide insights into your data.
Kinesis Data Analytics processed real-time streaming data

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
You can use AWS Lambda and Amazon EventBridge to schedule a Lambda function to stop and start the idle databases with specific tags to save on compute costs.

## Elastic File System ##
EFS is a managed elastic file system designed for use across different machines and availability zones, 

## Elastic Block Store ##
EBS is designed as a fast and reliable block storage volume for single machines

## S3 Object Lock ##
Blocks permanent object deletion during a customer-defined retention period so that you can enforce retention policies as an added layer of data protection or for regulatory compliance.

## Amazon FSx for Windows File Server ##
Provides fully managed Microsoft Windows file servers, backed by a fully native Windows file system. FSx for Windows File Server has the features, performance, and compatibility to easily lift and shift enterprise applications to the AWS Cloud.

## Amazon FSx File Gateway (FSx File Gateway) ##
Is a new File Gateway type that provides low latency and efficient access to in-cloud FSx for Windows File Server file shares from your on-premises facility

## Joining the FSx for Windows File Server file system to the on-premises Active Directory  ## 
will allow the company to use the existing Active Directory groups to restrict access to the file shares, folders, and files after the move to AWS. This option allows the company to continue using their existing access controls and management structure, making the transition to AWS more seamless.

## Amazon Comprehend ##
Is a natural-language processing (NLP) service that uses machine learning to uncover valuable insights and connections in text.

## Amazon Rekognition ##
Makes it easy to add image and video analysis to your applications. You just have to provide an image or video to the Amazon Rekognition API, and the service can:

- Identify labels (objects, concepts, people, scenes, and activities) and text*
- Detect inappropriate content
- Provide highly accurate facial analysis, face comparison, and face search capabilities

## Amazon Textract ## 
Is a machine learning (ML) service that automatically extracts text, handwriting, and data from scanned documents.

## Amazon Transcribe ##
Converts audio input into text, which opens the door for various text analytics applications on voice input. For instance, by using Amazon Comprehend on the converted text data from Amazon Transcribe, you can perform sentiment analysis or extract entities and key phrases.

## Amazon SageMaker ##
Is a fully managed machine learning service. With SageMaker, data scientists and developers can quickly and easily build and train machine learning models, and then directly deploy them into a production-ready hosted environment

## AWS Fargate ## 
Is a technology that you can use with Amazon ECS to run containers without having to manage servers or clusters of Amazon EC2 instances. With Fargate, you no longer have to provision, configure, or scale clusters of virtual machines to run containers.

## ChangeMessageVisibility ##
In case of SQS - multi-consumers if one consumer has already picked the message and is processing, in meantime other consumer can pick it up and process the message there by two copies are added at the end. To avoid this the message is made invisible from the time its picked and deleted after processing. This visibility timeout is increased according to max time taken to process the message

## RDS Proxy is a fully-managed ##
Highly available, and easy-to-use database proxy feature of Amazon RDS that enables your applications to: 1) improve scalability by pooling and sharing database connections; 2) improve availability by reducing database failover times by up to 66% and preserving application connections
RDS Proxy: RDS Proxy is designed to manage database connections, pooling, and failover, improving database scalability and performance. It helps reduce the number of open connections to the database, which can be a common source of performance issues.
Minimizing Changes: RDS Proxy can be introduced without significant changes to the application's architecture. It acts as an intermediary between the application and the database, handling connection pooling and reducing the load on the database.

## Recovery time objective (RTO) ##
Is the maximum acceptable time that an application, computer, network, or system can be down after an unexpected disaster, failure, or comparable event takes place. RTO captures the maximum allowable time between restoration of normal service levels and resumption of typical operations and the unexpected failure or disaster. RTO defines a turning point, after which time the consequences of interruption from a disaster or failure become unacceptable.

## Recovery point objective (RPO) ###
Is defined as the maximum amount of data – as measured by time – that can be lost after a recovery from a disaster, failure, or comparable event before data loss will exceed what is acceptable to an organization.

## Amazon DynamoDB point-in-time recovery ## 
Enables you to back up your table data continuously by using point-in-time recovery (PITR). When you enable PITR, DynamoDB backs up your table data automatically with per-second granularity so that you can restore to any given second in the preceding 35 days

## AWS DataSync ##
Is a fully managed data transfer service that simplifies, automates, and accelerates transferring data between on-premises storage systems and Amazon S3, Amazon EFS, or Amazon FSx for Windows File Server.
Is a data transfer service that uses network optimization techniques to transfer data efficiently and securely between on-premises storage systems and Amazon S3 or other storage targets. When used over AWS Direct Connect, DataSync can provide a dedicated and secure network connection between your on-premises data center and AWS. This can help to ensure a more reliable and secure data transfer compared to using the public internet.

## Amazon DynamoDB ##
Is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability. DynamoDB lets you offload the administrative burdens of operating and scaling a distributed database so that you don't have to worry about hardware provisioning, setup and configuration, replication, software patching, or cluster scaling. DynamoDB also offers encryption at rest, which eliminates the operational burden and complexity involved in protecting sensitive data. For more information, see DynamoDB encryption at rest.

## DAX stands for DynamoDB Accelerator ## 
It's like a turbo boost for your DynamoDB tables. It's a fully managed, in-memory cache that speeds up the read and write performance of your DynamoDB tables, so you can get your data faster than ever before

## AWS Backup ##
Is a fully managed backup service that makes it easy to centralize and automate the backup of data across AWS resources. It allows you to create backup policies and schedules to automatically back up your DynamoDB tables on a regular basis. You can also specify retention policies to ensure that your backups are retained for the required period of time. This solution is fully automated and requires minimal maintenance, making it the most operationally efficient option.
NO Glacier Deep is supported by AWS Backup.

## On-demand mode ##
Is a good option if any of the following are true:
- You create new tables with unknown workloads.
- You have unpredictable application traffic.
- You prefer the ease of paying for only what you use.

## Spot Instances ##
A Spot Instance is an instance that uses spare EC2 capacity that is available for less than the On-Demand price. Because Spot Instances enable you to request unused EC2 instances at steep discounts, you can lower your Amazon EC2 costs significantly. The hourly price for a Spot Instance is called a Spot price.

## AWS Spot Fleet ##
Is a service that lets you create a fleet of EC2 instances that can help make your application more reliable and significantly cheaper to run. A fleet is composed of both Spot and On-Demand Instances.

## S3 Object Lock ##
Used to store objects using a write-once-read-many (WORM) model. Object Lock can help prevent objects from being deleted or overwritten for a fixed amount of time or indefinitely. You can use S3 Object Lock to meet regulatory requirements that require WORM storage, or add an extra layer of protection against object changes and deletion.
Versioning is required and automatically activated as Object Lock is enabled.

## Amazon FSx for Lustre ##
Is a fully managed file system that is designed for high-performance workloads, such as gaming applications. It provides a high-performance, scalable, and fully managed file system that is optimized for Lustre clients, and it is fully integrated with Amazon EC2. It is the only option that meets the requirements of being fully managed and able to support Lustre clients.

## AWS Glue ##
Is a serverless data integration service that makes it easy for analytics users to discover, prepare, move, and integrate data from multiple sources. You can use it for analytics, machine learning, and application development. It also includes additional productivity and data ops tooling for authoring, running jobs, and implementing business workflows.
Parquet format.

## The Object Lock legal hold operation ##
Enables you to place a legal hold on an object version. Like setting a retention period, a legal hold prevents an object version from being overwritten or deleted. However, a legal hold doesn't have an associated retention period and remains in effect until removed

## Using AWS Web Application Firewall (WAF) ##
Has several benefits. Additional protection against web attacks using criteria that you specify. You can define criteria using characteristics of web requests such as the following:
Presence of SQL code that is likely to be malicious (known as SQL injection).
Presence of a script that is likely to be malicious (known as cross-site scripting).

## AWS Firewall Manager ##
Simplifies your administration and maintenance tasks across multiple accounts and resources for a variety of protections.

## SSL termination ##
Refers to the process of decrypting encrypted traffic before passing it along to a web server.

## A target tracking policy ##
Allows the Auto Scaling group to automatically adjust the number of EC2 instances in the group based on a target value for a metric. In this case, the target value for the CPU utilization metric could be set to 40% to maintain the desired performance of the application. The Auto Scaling group would then automatically scale the number of instances up or down as needed to maintain the target value for the metric.

## Origin access identity ##
Is a special CloudFront user that you can associate with Amazon S3 origins, so that you can secure all or just some of your Amazon S3 content.

## Amazon RDS Custom for Oracle ##
Has access to the underlying OS and it provides less operational overhead. 

## WS Database Migration Service (AWS DMS) ##
Is a managed migration and replication service that helps move your database and analytics workloads to AWS quickly, securely, and with minimal downtime and zero data loss.

## Amazon MQ ##
Is a managed message broker service for Apache ActiveMQ and RabbitMQ that streamlines setup, operation, and management of message brokers on AWS.

## EC2 Instance Savings plan ##
Saves up to 72%.
EC2 Savings Plans support EC2 only.
Not applied to Fargate or Lambda.

## Compute Savings Plans ##
Cmpute Savings Plans provide the most flexibility and help to reduce your costs by up to 66%.
These plans automatically apply to EC2 instance usage regardless of instance family, size, AZ, region, OS or tenancy, and also apply to Fargate and Lambda usage." EC2 instance Savings Plans are not applied to Fargate or Lambda

# S3 Lock mmodes #

## Compliance Mode. ##
Set the specific rule tou want to be applied.

## Governance Mode ##
Is that there are NO users that can override the retention periods set or delete an object, and that also includes your AWS root account which has the highest privileges.

## Field-level encryption ##
Allows you to enable your users to securely upload sensitive information to your web servers. The sensitive information provided by your users is encrypted at the edge, close to the user, and remains encrypted throughout your entire application stack

## AWS Transfer Family ##
Securely scales your recurring business-to-business file transfers to AWS Storage services using SFTP, FTPS, FTP, and AS2 protocols.

## Elastic Beanstalk ##
With Elastic Beanstalk, you can quickly deploy and manage applications in the AWS Cloud without having to learn about the infrastructure that runs those applications. Elastic Beanstalk reduces management complexity without restricting choice or control. You simply upload your application, and Elastic Beanstalk automatically handles the details of capacity provisioning, load balancing, scaling, and application health monitoring.

## AWS CloudFormation ##
Is a service that helps you model and set up your AWS resources so that you can spend less time managing those resources and more time focusing on your applications that run in AWS. You create a template that describes all the AWS resources that you want (like Amazon EC2 instances or Amazon RDS DB instances), and CloudFormation takes care of provisioning and configuring those resources for you. You don't need to individually create and configure AWS resources and figure out what's dependent on what; CloudFormation handles that. The following scenarios demonstrate how CloudFormation can help.

## Amazon Cognito ##
It's a user directory, an authentication server, and an authorization service for OAuth 2.0 access tokens and AWS credentials. With Amazon Cognito, you can authenticate and authorize users from the built-in user directory, from your enterprise directory, and from consumer identity providers like Google and Facebook.

## Amazon Pinpoint ## 
Is an AWS service that you can use to engage with your customers across multiple messaging channels. You can use Amazon Pinpoint to send push notifications, in-app notifications, emails, text messages, voice messages, and messages over custom channels.

## AWS ElastiCache ##
Is a managed in-memory data store service that is well-suited for managing session data in a distributed architecture. It provides high-performance, scalable, and durable storage for session data, allowing multiple EC2 instances to access and share session data seamlessly. By using ElastiCache, the application can offload the session management workload from the EC2 instances and leverage the distributed caching capabilities of ElastiCache for improved scalability and performance.
While Amazon ElastiCache can improve performance by caching frequently accessed data, it's not specifically designed to address database read performance issues caused by connection management.


# Amazon ROute 53 #
Amazon Route 53 is a highly available and scalable Domain Name System (DNS) web service. Route 53 connects user requests to internet applications running on AWS or on-premises.

## multivalue answer routing policy in Route 53 ## 
Allows you to configure multiple values for a DNS record, and Route 53 responds to DNS queries with multiple random values. This enables the distribution of traffic randomly among the available EC2 instances.

## Failover routing ##
Is designed to direct traffic to a backup resource or secondary location only when the primary resource or location is unavailable.

## weighted routing policy ##
Allows you to distribute traffic across multiple EC2 instances, it does not ensure random distribution

![Amazon Route 53](/images/amazon-route-53.png)

## Access control lists (ACLs) ##
Are one of the resource-based options (see Overview of managing access) that you can use to manage access to your buckets and objects. You can use ACLs to grant basic read/write permissions to other AWS accounts.

## Security Groups ##
AWS Security Groups help you secure your cloud environment by controlling how traffic will be allowed into your EC2 machines. With Security Groups, you can ensure that all the traffic that flows at the instance level is only through your established ports and protocols.

## Classless Inter-Domain Routing (CIDR) ##
Is an IP address allocation method that improves data routing efficiency on the internet. Every machine, server, and end-user device that connects to the internet has a unique number, called an IP address, associated with it. Devices find and communicate with one another by using these IP addresses. Organizations use CIDR to allocate IP addresses flexibly and efficiently in their networks.

## Amazon EMR (previously called Amazon Elastic MapReduce) ##
Is a managed cluster platform that simplifies running big data frameworks, such as Apache Hadoop and Apache Spark , on AWS to process and analyze vast amounts of data.























