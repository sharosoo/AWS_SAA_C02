# AWS SAA02 dump

### **574**

A business wishes to implement a shared file system for its.NET application servers and Microsoft SQL Server databases that are hosted on Amazon EC2 instances running Windows Server 2016. The solution must interact with the corporate Active Directory domain, be very durable, be managed by AWS, and provide high levels of throughput and IOPS.

Which solution satisfies these criteria?

- A. Use Amazon FSx for Windows File Server.
- B. Use Amazon Elastic File System (Amazon EFS).
- C. Use AWS Storage Gateway in file gateway mode.
- D. Deploy a Windows file server on two On Demand instances across two Availability Zones.

**Answer** A

### **573**

A business uses AWS to host a three-tier environment that collects sensor data from its consumers' devices. The traffic is routed via a Network Load Balancer (NLB), then to Amazon EC2 instances for the web tier and then to Amazon EC2 instances for the application layer that conducts database calls.

What should a solutions architect do to enhance data security when it is being sent to the web tier?

- A. Configure a TLS listener and add the server certificate on the NLB.
- B. Configure AWS Shield Advanced and enable AWS WAF on the NLB.
- C. Change the load balancer to an Application Load Balancer and attach AWS WAF to it.
- D. Encrypt the Amazon Elastic Block Store (Amazon EBS) volume on the EC2 instances using AWS Key Management Service (AWS KMS).

**Answer** A

**Explain** On your AWS Free Trial, go to EC2 -> Load Balancers -> Create Network Load Balancer -> Listeners and routing -> Add Listener -> go to Protocol -> select TLS in dropdown. For the Certificate, scroll down to Secure Listener settings -> Default SSL certificate -> select Import in dropdown.

### **572**

A business utilized an AWS Direct Connect connection to transfer one petabyte of data from a colocation facility to an Amazon S3 bucket in the us-east-1 Region. The business now wishes to replicate the data in another S3 bucket located in the us-west-2 Region.

Which solution will satisfy this criterion?

- A. Use an AWS Snowball Edge Storage Optimized device to copy the data from the colocation facility to us-west-2.
- B. Use the S3 console to copy the data from the source S3 bucket to the target S3 bucket.
- C. Use S3 Transfer Acceleration and the S3 copy-object command to copy the data from the source S3 bucket to the target S3 bucket.
- D. Add an S3 Cross-Region Replication configuration to copy the data from the source S3 bucket to the target S3 bucket.

**Answer** C

**Explain** 

After you set up cross-Region replication (CRR) or same-Region replication (SRR) on the source bucket, Amazon S3 automatically and asynchronously replicates new objects from the source bucket to the destination bucket. You can choose to filter which objects are replicated using a prefix or tag. For more information on configuring replication and specifying a filter, see Replication configuration overview. After replication is configured, only new objects are replicated to the destination bucket. Existing objects aren't replicated to the destination bucket. For more information, see Replicating existing objects.

### **571**

A corporation has recruited a new cloud engineer who should not have access to the CompanyConfidential Amazon S3 bucket. The cloud engineer must have read and write permissions on an S3 bucket named AdminTools.

Which IAM policy will satisfy these criteria?
A.
![img](https://www.examtopics.com/assets/media/exam-media/04121/0016200001.png)
B.
![img](https://www.examtopics.com/assets/media/exam-media/04121/0016300001.png)
{
C.
![img](https://www.examtopics.com/assets/media/exam-media/04121/0016300002.png)
D.
![img](https://www.examtopics.com/assets/media/exam-media/04121/0016400001.png)

**Answer** C

**Explain** 

There is no List in the question. 

List: Permission to list resources within the service to determine whether an object exists. Actions with this level of access can list objects but cannot see the contents of a resource. For example, the Amazon S3 action ListBucket has the List access level. 

Read: Permission to read but not edit the contents and attributes of resources in the service. For example, the Amazon S3 actions GetObject and GetBucketLocation have the Read access level. 

Write: Permission to create, delete, or modify resources in the service. For example, the Amazon S3 actions CreateBucket, DeleteBucket and PutObject have the Write access level. Write actions might also allow modifying a resource tag. However, an action that allows only changes to tags has the Tagging access level.

https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_understand-policy-summary-access-level-summaries.html

### **570**

A business wishes to enhance the availability and performance of a hybrid application. The application is composed of a stateful TCP-based workload that is hosted on Amazon EC2 instances across several AWS Regions, and a stateless UDP-based task that is housed on-premises.

Which activities should a solutions architect do in combination to increase availability and performance? (Select two.)

- A. Create an accelerator using AWS Global Accelerator. Add the load balancers as endpoints.
- B. Create an Amazon CloudFront distribution with an origin that uses Amazon Route 53 latency-based routing to route requests to the load balancers.
- C. Configure two Application Load Balancers in each Region. The first will route to the EC2 endpoints and the second will route to the on-premises endpoints.
- D. Configure a Network Load Balancer in each Region to address the EC2 endpoints. Configure a Network Load Balancer in each Region that routes to the on- premises endpoints.
- E. Configure a Network Load Balancer in each Region to address the EC2 endpoints. Configure an Application Load Balancer in each Region that routes to the on-premises endpoints

**Answer** A, D

**Explain** 

ALB, CloudFront is only for Layer7(HTTP & HTTPS)

### **569**

A business intends to launch a freshly developed application on AWS in a default VPC. The program will be divided into two layers: a web layer and a database layer. The web server and MySQL database were constructed in public subnets, whereas the web server and MySQL database were created in private subnets. The default network ACL settings are used to build all subnets, and the default security group in the VPC is replaced with new custom security groups.
The critical criteria are as follows:
✑ The web servers must be accessible only to users on an SSL connection.
✑ The database should be accessible to the web layer, which is created in a public subnet only.
✑ All traffic to and from the IP range 182.20.0.0/16 subnet should be blocked.

Which combination of actions satisfies these criteria? (Select two.)

- A. Create a database server security group with inbound and outbound rules for MySQL port 3306 traffic to and from anywhere (0 0.0.0/0).
- B. Create a database server security group with an inbound rule for MySQL port 3306 and specify the source as a web server security group.
- C. Create a web server security group with an inbound allow rule for HTTPS port 443 traffic from anywhere (0.0.0.0/0) and an inbound deny rule for IP range 182.20.0.0/16.
- D. Create a web server security group with an inbound rule for HTTPS port 443 traffic from anywhere (0.0.0.0/0). Create network ACL inbound and outbound deny rules for IP range 182.20.0.0/16.
- E. Create a web server security group with inbound and outbound rules for HTTPS port 443 traffic to and from anywhere (0.0.0.0/0). Create a network ACL inbound deny rule for IP range 182.20.0.0/16.

**Answer** B, D

### **568**

A major company's administrator want to monitor for and prevent cryptocurrency-related assaults on the company's AWS accounts.

Which AWS service can the administrator use to safeguard the organization from cyberattacks?

- A. Amazon Cognito
- B. Amazon GuardDuty
- C. Amazon Inspector
- D. Amazon Macie

**Answer** B

**Explain** 

- Shield
  - Shield Standard enabled by default/no need to enable 
  - Shield Standard is L3 L4 only eg.SYN/UDP floods,Reflectionattacks,etc 
  - Shield Advanced includes L7 as well 
  - Sield Advanced gives DDoS protection NOT shield Shield Standard!!! 
  - Shield Advanced includes WAF bundled with it 
  - Shield Advanced gives access to dedicated DRT(DDos Response Team) 
  - Shield advanced gives protection against high fees during usage spikes due to DDoS 

- Inspector: for ec2 
  - provides security assessments on EC2(known vulnerabilities) 
  - need to install sw(agent) on EC2 (unless using just the 'network assessment' feature--agentless)  

- Guard Duty:to analyze logs 
  - analyze Cloudtrail ,VPC flow, DNS logs 
  - No need to install any sw since only analysing logs 
  - Can protect against CryptoCurrency attacks <<<<<<<<<< 

- Macie:for S3
  - discover and protect your sensitive data(e.g. PII) in AWS
- WAF:L7 protection 
  - Deploy only on Cloudfront,ALB, API GW 
  - contains Web ACL/rules -can do rate-based rules(to count no fo events)/this also helps in DDoS protection 
  - It protects against common attacks like SQL injection and XSS(Cross Site scripting)--i.e. L7 based attacks

### **567**

A business offers an online shopping application and all orders are stored in an Amazon RDS for PostgreSQL Single-AZ database instance. Management want to remove single points of failure and has requested a solutions architect to offer a method for minimizing database downtime without modifying the application code.

Which solution satisfies these criteria?

- A. Convert the existing database instance to a Multi-AZ deployment by modifying the database instance and specifying the Multi-AZ option.
- B. Create a new RDS Multi-AZ deployment. Take a snapshot of the current RDS instance and restore the new Multi-AZ deployment with the snapshot.
- C. Create a read-only replica of the PostgreSQL database in another Availability Zone. Use Amazon Route 53 weighted record sets to distribute requests across the databases.
- D. Place the RDS for PostgreSQL database in an Amazon EC2 Auto Scaling group with a minimum group size of two. Use Amazon Route 53 weighted record sets to distribute requests across instances.

**Answer** A

**Explain** 

We need to minimize downtime. "A" creates NO downtime whatsoever. "B" will create downtime as you need to repoint your application to the new DNS record. 

Source: https://aws.amazon.com/rds/faqs/

### **566**

On AWS Lambda, a corporation has created one of its microservices that connects to an Amazon DynamoDB database called Books. A solutions architect is creating an IAM policy that will be tied to the Lambda function's IAM role, granting it the ability to insert, edit, and remove objects from the Books table. The IAM policy must prohibit the function from doing any more activities on the Books or any other table.

Which IAM policy would meet these requirements while requiring the LEAST amount of privileged access?
A.
![img](https://www.examtopics.com/assets/media/exam-media/04121/0009100001.png)
B.
![img](https://www.examtopics.com/assets/media/exam-media/04121/0009100002.png)
C.
![img](https://www.examtopics.com/assets/media/exam-media/04121/0009200001.png)
D.

**Answer** A

### **565**

A firm is developing a web application that will use Amazon S3 to store a big number of photos. Users will get access to the photographs for varying durations of time. The business wishes to:
✑ Retain all the images
✑ Incur no cost for retrieval.
✑ Have minimal management overhead.
✑ Have the images available with no impact on retrieval time.

Which solution satisfies these criteria?

- A. Implement S3 Intelligent-Tiering
- B. Implement S3 storage class analysis
- C. Implement an S3 Lifecycle policy to move data to S3 Standard-Infrequent Access (S3 Standard-IA).
- D. Implement an S3 Lifecycle policy to move data to S3 One Zone-Infrequent Access (S3 One Zone-IA).

**Answer** A

**Explain**

https://aws.amazon.com/about-aws/whats-new/2018/11/s3-intelligent-tiering/ 

- Retain all the images => “S3 Intelligent-Tiering is designed for 99.9% availability and 99.999999999% durability” 
- Incur no cost for retrieval => "There are no retrieval fees in S3 Intelligent-Tiering" 
- Have minimal management overhead. => "without performance impact or operational overhead" 
- Have the images available with no impact on retrieval time => "offers the same low latency and high throughput performance of S3 Standard"

### **564**

A business is considering migrating a commercial off-the-shelf application from its on-premises data center to Amazon Web Services (AWS). The software is licensed on a per-socket and per-core basis, with predictable capacity and uptime requirements. The corporation wants to continue using its current licenses, which were acquired earlier this year.

Which price option for Amazon EC2 is the MOST cost-effective?

- A. Dedicated Reserved Hosts
- B. Dedicated On-Demand Hosts
- C. Dedicated Reserved Instances
- D. Dedicated On-Demand Instances

**Answer** A

**Explain** 

Requirement is "software has a software licensing model using sockets and cores" 

dedicated-hosts => visibility of sockets and physical cores 

You have visibility of the number of sockets and physical cores that support your instances on a Dedicated Host.

You can use this information to manage licensing for your own server-bound software that is licensed per-socket or per-core. 

see link below https://aws.amazon.com/ec2/dedicated-hosts/

### **563**

A business maintains data in an on-premises data center, which is utilized by a variety of on-premises applications. The organization wishes to preserve its current application environment while using AWS services for data analytics and future visualizations.

Which storage service should a solutions architect propose to his or her clients?

- A. Amazon Redshift
- B. AWS Storage Gateway for files
- C. Amazon Elastic Block Store (Amazon EBS)
- D. Amazon Elastic File System (Amazon EFS)

**Answer**: B

### **562**

A business created a stateless two-tier application using Amazon EC2 in a single Availability Zone and an Amazon RDS Multi-AZ database instance. The new administration of the organization wants to guarantee that the application is highly accessible.

What actions should a solutions architect do in order to satisfy this requirement?

- A. Configure the application to use Multi-AZ EC2 Auto Scaling and create an Application Load Balancer.
- B. Configure the application to take snapshots of the EC2 instances and send them to a different AWS Region.
- C. Configure the application to use Amazon Route 53 latency-based routing to feed requests to the application.
- D. Configure Amazon Route 53 rules to handle incoming requests and create a Multi-AZ Application Load Balancer.

**Answer**: A

### **561**

A business is building an ecommerce solution that will have a load-balanced front end, a container-based application, and a relational database. A solutions architect must design a highly accessible system that requires little human intervention.

Which solutions satisfy these criteria? (Select two.)

- A. Create an Amazon RDS DB instance in Multi-AZ mode.
- B. Create an Amazon RDS DB instance and one or more replicas in another Availability Zone.
- C. Create an Amazon EC2 instance-based Docker cluster to handle the dynamic application load.
- D. Create an Amazon Elastic Container Service (Amazon ECS) cluster with a Fargate launch type to handle the dynamic application load.
- E. Create an Amazon Elastic Container Service (Amazon ECS) cluster with an Amazon EC2 launch type to handle the dynamic application load.

**Answer ** A, D

### **560** :star:

A solutions architect is reviewing the security of a newly transferred workload. The workload is a web application that is composed of Amazon EC2 instances that are part of an Auto Scaling group and are routed via an Application Load Balancer. The solutions architect must strengthen the security posture and mitigate the resource effect of a DDoS assault.

Which of the following solutions is the MOST EFFECTIVE?

- A. Configure an AWS WAF ACL with rate-based rules. Create an Amazon CloudFront distribution that points to the Application Load Balancer. Enable the WAF ACL on the CloudFront distribution.
- B. Create a custom AWS Lambda function that adds identified attacks into a common vulnerability pool to capture a potential DDoS attack. Use the identified information to modify a network ACL to block access.
- C. Enable VPC Flow Logs and store then in Amazon S3. Create a custom AWS Lambda functions that parses the logs looking for a DDoS attack. Modify a network ACL to block identified source IP addresses.
- D. Enable Amazon GuardDuty and configure findings written to Amazon CloudWatch. Create an event with CloudWatch Events for DDoS alerts that triggers Amazon Simple Notification Service (Amazon SNS). Have Amazon SNS invoke a custom AWS Lambda function that parses the logs, looking for a DDoS attack. Modify a network ACL to block identified source IP addresses.

**Answer** A

**Explain** 

### **559**

A solutions architect is developing a security solution for a firm that want to deliver individual AWS accounts to developers through AWS Organizations while retaining normal security restrictions. Due to the fact that individual developers will have root user access to their own AWS accounts, the solutions architect needs to verify that the obligatory AWS CloudTrail configuration deployed to new developer accounts is not updated.

Which activity satisfies these criteria?

- A. Create an IAM policy that prohibits changes to CloudTrail, and attach it to the root user.
- B. Create a new trail in CloudTrail from within the developer accounts with the organization trails option enabled.
- C. Create a service control policy (SCP) the prohibits changes to CloudTrail, and attach it the developer accounts.
- D. Create a service-linked role for CloudTrail with a policy condition that allows changes only from an Amazon Resource Name (ARN) in the master account.

**Answer** C

**Explain**

Service control policies (SCPs) are a type of organization policy that you can use to manage permissions in your organization. SCPs offer central control over the maximum available permissions for all accounts in your organization. SCPs help you to ensure your accounts stay within your organization’s access control guidelines. 

https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html

### **558**

A business wishes to transition its online application to Amazon Web Services (AWS). The classic web application is divided into three tiers: the web layer, the application tier, and the MySQL database. The rearchitected application must be built using technologies that eliminate the need for the administration team to manage instances or clusters.

Which service combination should a solution architect include into the overall architecture? (Select two.)

- A. Amazon Aurora Serverless
- B. Amazon EC2 Spot Instances
- C. Amazon Elasticsearch Service (Amazon ES)
- D. Amazon RDS for MySQL
- E. AWS Fargate

**Answer** A or D, E

### **557**

A solutions architect is developing a web application that will be hosted on Amazon EC2 instances and managed by an Application Load Balancer (ALB). The organization places a high premium on the application's resilience to hostile internet activities and assaults, as well as its protection against newly discovered vulnerabilities and exposures.

What recommendations should the solutions architect make?

- A. Leverage Amazon CloudFront with the ALB endpoint as the origin.
- B. Deploy an appropriate managed rule for AWS WAF and associate it with the ALB.
- C. Subscribe to AWS Shield Advanced and ensure common vulnerabilities and exposures are blocked.
- D. Configure network ACLs and security groups to allow only ports 80 and 443 to access the EC2 instances.

**Answer** C

**Explain**

AWS Shield - DDoS, WAF - Common Exploit, Shield Advanced - Shield + WAF

### **556**

A solutions architect is developing a solution that will need frequent modifications to a website hosted on Amazon S3 with versioning enabled. Due to compliance requirements, older versions of the objects will be seldom accessed and will need to be removed after two years.

What should the solutions architect propose as the CHEAPEST way to achieve these requirements?

- A. Use S3 batch operations to replace object tags. Expire the objects based on the modified tags.
- B. Configure an S3 Lifecycle policy to transition older versions of objects to S3 Glacier. Expire the objects after 2 years.
- C. Enable S3 Event Notifications on the bucket that sends older objects to the Amazon Simple Queue Service (Amazon SQS) queue for further processing.
- D. Replicate older object versions to a new bucket. Use an S3 Lifecycle policy to expire the objects in the new bucket after 2 years.

**Answer** B

### **555**

A three-tier web application is used to handle client orders. The web tier is made up of Amazon EC2 instances behind an Application Load Balancer, a middle tier made up of three EC2 instances that are isolated from the web layer through Amazon SQS, and an Amazon DynamoDB backend. During busy periods, consumers who place purchases through the site must wait much longer than usual for confirmations owing to prolonged processing delays. A solutions architect's objective should be to minimize these processing times.

Which course of action will be the MOST EFFECTIVE in achieving this?

- A. Replace the SQS queue with Amazon Kinesis Data Firehose.
- B. Use Amazon ElastiCache for Redis in front of the DynamoDB backend tier.
- C. Add an Amazon CloudFront distribution to cache the responses for the web tier.
- D. Use Amazon EC2 Auto Scaling to scale out the middle tier instances based on the SQS queue depth.

**Answer** D

**Explain** 

Scaling based on Amazon SQS 

https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-using-sqs-queue.html

### **554**

A solutions architect is in the process of implementing a distributed database across many Amazon EC2 instances. The database replicates all data across numerous instances to ensure that it can survive the loss of single instance. The database needs block storage that is low in latency and high in throughput in order to accommodate several million transactions per second per server.

Which storage option should the architect of solutions use?

- A. EBS Amazon Elastic Block Store (Amazon EBS)
- B. Amazon EC2 instance store
- C. Amazon Elastic File System (Amazon EFS)
- D. Amazon S3

**Answer** B

**Explain** 

For distributed database, resiliency and data recovery is well operated. So, for high throughput and low latency, instance store will be best choice. 

See https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/storage-optimized-instances.html

### **553**

A business hosts a web application on Amazon Web Services (AWS) utilizing a single Amazon EC2 instance that saves user-uploaded documents in an Amazon Elastic Block Store (Amazon EBS) volume. To improve scalability and availability, the organization replicated the architecture and deployed a second EC2 instance and EBS volume in a different Availability Zone, both of which were placed behind an Application Load Balancer. After this update was made, users claimed that each time they refreshed the page, they could view a portion of their papers but never all of them.

What should a solutions architect suggest to guarantee that users have access to all of their documents simultaneously?

- A. Copy the data so both EBS volumes contain all the documents.
- B. Configure the Application Load Balancer to direct a user to the server with the documents.
- C. Copy the data from both EBS volumes to Amazon Elastic File System (Amazon EFS). Modify the application to save new documents to Amazon Elastic File System (Amazon EFS).
- D. Configure the Application Load Balancer to send the request to both servers. Return each document from the correct server.

**Answer** C

### **552**

A business may have many AWS accounts for different departments. One of the departments would want to share an Amazon S3 bucket with the rest of the organization.

Which of the following solutions requires the LEAST amount of effort?

- A. Enable cross-account S3 replication for the bucket.
- B. Create a pre-signed URL for the bucket and share it with other departments.
- C. Set the S3 bucket policy to allow cross-account access to other departments.
- D. Create IAM users for each of the departments and configure a read-only IAM policy.

**Answer**: C

**Explain**:

https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-policies-s3.html

### **551**

A business is developing a new online service that will be hosted on Amazon EC2 instances with the assistance of an Elastic Load Balancer. However, many online service clients can only communicate with IP addresses that have been whitelisted on their firewalls.

What recommendations should a solutions architect provide to suit a client's needs?

- A. A Network Load Balancer with an associated Elastic IP address.
- B. An Application Load Balancer with an associated Elastic IP address
- C. An A record in an Amazon Route 53 hosted zone pointing to an Elastic IP address
- D. An EC2 instance with a public IP address running as a proxy in front of the load balancer

**Answer** A

### **550**

On AWS, a business hosts an online marketplace web application. During peak hours, the program serves hundreds of thousands of users. The business requires a scalable, near-real-time solution for sharing information about millions of financial transactions with various other internal systems. Additionally, transactions must be processed to remove sensitive data prior to being stored in a document database for fast retrieval.

What recommendations should a solutions architect make to satisfy these requirements?

- A. Store the transactions data into Amazon DynamoDB. Set up a rule in DynamoDB to remove sensitive data from every transaction upon write. Use DynamoDB Streams to share the transactions data with other applications.
- B. Stream the transactions data into Amazon Kinesis Data Firehose to store data in Amazon DynamoDB and Amazon S3. Use AWS Lambda integration with Kinesis Data Firehose to remove sensitive data. Other applications can consume the data stored in Amazon S3.
- C. Stream the transactions data into Amazon Kinesis Data Streams. Use AWS Lambda integration to remove sensitive data from every transaction and then store the transactions data in AmazonDynamoDB. Other applications can consume the transactions data off the Kinesis data stream.
- D. Store the batched transactions data in Amazon S3 as files. Use AWS Lambda to process every file and remove sensitive data before updating the files in Amazon S3. The Lambda function then stores the data in Amazon DynamoDB. Other applications can consume transaction files stored in Amazon S3.

**Answer** C

**Explain** 

near-real time -> Amazon Kinesis Data Streams

Kinesis Data Firehose can send data records to Amazon S3, Amazon Redshift, Amazon OpenSearch Service, and any HTTP endpoint.

### **549**

A business notices a rise in the cost of Amazon EC2 in its most recent bill. The billing team observes an anomaly in the vertical scaling of instance types for a few EC2 instances. A solutions architect should build a graph comparing the previous two months' EC2 charges and conduct an in-depth study to determine the core cause of the vertical scaling.

How should the solutions architect create data with the LEAST amount of operational overhead possible?

- A. Use AWS Budgets to create a budget report and compare EC2 costs based on instance types.
- B. Use Cost Explorer's granular filtering feature to perform an in-depth analysis of EC2 costs based on instance types.
- C. Use graphs from the AWS Billing and Cost Management dashboard to compare EC2 costs based on instance types for the last 2 months.
- D. Use AWS Cost and Usage Reports to create a report and send it to an Amazon S3 bucket. Use Amazon QuickSight with Amazon S3 as a source to generate an interactive graph based on instance types.

**Answer** B

**Explain**

AWS Cost Explorer is a tool that enables you to view and analyze your costs and usage. You can explore your usage and costs using the main graph, the Cost Explorer cost and usage reports, or the Cost Explorer RI reports. You can view data for up to the last 12 months, forecast how much you're likely to spend for the next 12 months, and get recommendations for what Reserved Instances to purchase. You can use Cost Explorer to identify areas that need further inquiry and see trends that you can use to understand your costs. 

https://docs.aws.amazon.com/cost-management/latest/userguide/ce-what-is.html

### **548**

A solutions architect is developing a solution that will lead customers to a backup static error page in the event that the original website becomes inaccessible. The DNS records for the major website are housed on Amazon Route 53, with the domain referring to an Application Load Balancer (ALB).

Which configuration should the solutions architect use in order to fulfill the business's requirements while reducing modifications and infrastructure overhead?

- A. Point a Route 53 alias record to an Amazon CloudFront distribution with the ALB as one of its origins. Then, create custom error pages for the distribution.
- B. Set up a Route 53 active-passive failover configuration. Direct traffic to a static error page hosted within an Amazon S3 bucket when Route 53 health checks determine that the ALB endpoint is unhealthy.
- C. Update the Route 53 record to use a latency-based routing policy. Add the backup static error page hosted within an Amazon S3 bucket to the record so the traffic is sent to the most responsive endpoints.
- D. Set up a Route 53 active-active configuration with the ALB and an Amazon EC2 instance hosting a static error page as endpoints. Route 53 will only send requests to the instance if the health checks fail for the ALB.

**Answer** B

**Explain**

Active-passive failover
Use an active-passive failover configuration when you want a primary resource or group of resources to be available the majority of the time and you want a secondary resource or group of resources to be on standby in case all the primary resources become unavailable. When responding to queries, Route 53 includes only the healthy primary resources. If all the primary resources are unhealthy, Route 53 begins to include only the healthy secondary resources in response to
DNS queries.
To create an active-passive failover configuration with one primary record and one secondary record, you just create the records and specify Failover for the routing policy. When the primary resource is healthy, Route 53 responds to DNS queries using the primary record. When the primary resource is unhealthy, Route 53 responds to DNS queries using the secondary record.
How Amazon Route 53 averts cascading failures
As a first defense against cascading failures, each request routing algorithm (such as weighted and failover) has a mode of last resort. In this special mode, when all records are considered unhealthy, the Route 53 algorithm reverts to considering all records healthy.
For example, if all instances of an application, on several hosts, are rejecting health check requests, Route 53 DNS servers will choose an answer anyway and return it rather than returning no DNS answer or returning an NXDOMAIN (non-existent domain) response. An application can respond to users but still fail health checks, so this provides some protection against misconfiguration.
Similarly, if an application is overloaded, and one out of three endpoints fails its health checks, so that it's excluded from Route 53 DNS responses, Route 53 distributes responses between the two remaining endpoints. If the remaining endpoints are unable to handle the additional load and they fail, Route 53 reverts to distributing requests to all three endpoints.
https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover-types.html 

### **547**

A financial services organization maintains a web application that is accessible to users in the United States and Europe. The program is divided into two tiers: a database layer and a web server layer. The database tier is comprised of a MySQL database that is physically located in us-east-1. Amazon Route 53 geoproximity routing is used to route traffic to the nearest Region's instances. According to a performance analysis of the system, European users are not obtaining the same degree of query performance as users in the United States.

Which improvements to the database layer should be made to increase performance?

- A. Migrate the database to Amazon RDS for MySQL. Configure Multi-AZ in one of the European Regions.
- B. Migrate the database to Amazon DynamoDB. Use DynamoDB global tables to enable replication to additional Regions.
- C. Deploy MySQL instances in each Region. Deploy an Application Load Balancer in front of MySQL to reduce the load on the primary instance.
- D. Migrate the database to an Amazon Aurora global database in MySQL compatibility mode. Configure read replicas in one of the European Regions.

**Answer** D

**Explain**

Amazon Aurora global database. There might be an alternative, Cross-Region Read Replicas for Amazon RDS.

### **546** :star:

Every 90 days, a security team must enforce the rotation of all IAM users' access keys. If an access key is discovered to be out of date, it must be rendered inactive and eliminated. A solutions architect must design a solution that will detect and remediate keys that are more than 90 days old.

Which solution satisfies these criteria with the LEAST amount of operational effort?

- A. Create an AWS Config rule to check for the key age. Configure the AWS Config rule to run an AWS Batch job to remove the key.
- B. Create an Amazon EventBridge (Amazon CloudWatch Events) rule to check for the key age. Configure the rule to run an AWS Batch job to remove the key.
- C. Create an AWS Config rule to check for the key age. Define an Amazon EventBridge (Amazon CloudWatch Events) rule to schedule an AWS Lambda function to remove the key.
- D. Create an Amazon EventBridge (Amazon CloudWatch Events) rule to check for the key age. Define an EventBridge (CloudWatch Events) rule to run an AWS Batch job to remove the key.

**Answer** C

### **545**

A business is utilizing Amazon Elastic Container Service (Amazon ECS) to host its application and want to assure high availability. The business needs to be able to update its application even if nodes in one Availability Zone are unavailable.
The application is projected to get 100 requests per second, and each container job is capable of serving at least 60 requests per second. The organization configured Amazon ECS to use a rolling update deployment mode, with the minimum healthy percent parameter set to 50% and the maximum healthy percent parameter set to 100%.

Which task and availability zone configurations satisfy these requirements?

- A. Deploy the application across two Availability Zones, with one task in each Availability Zone.
- B. Deploy the application across two Availability Zones, with two tasks in each Availability Zone.
- C. Deploy the application across three Availability Zones, with one task in each Availability Zone.
- D. Deploy the application across three Availability Zones, with two tasks in each Availability Zone.

**Answer** D

**Explain**

All Instance(2*3) One AZ down (-2) One update(-1) = (3) => 50(3/6)% health

### **544**

A business is in the process of deploying a data lake on Amazon Web Services (AWS). An architect of solutions must describe the encryption approach for data in transit and at rest. Amazon S3/ The following is stated in the company's security policy:

✑ Keys must be rotated every 90 days.
✑ Strict separation of duties between key users and key administrators must be implemented.
✑ Auditing key usage must be possible.

What solutions architect recommendations should be made?

- A. Server-side encryption with AWS KMS managed keys (SSE-KMS) with customer managed customer master keys (CMKs)
- B. Server-side encryption with AWS KMS managed keys (SSE-KMS) with AWS managed customer master keys (CMKs)
- C. Server-side encryption with Amazon S3 managed keys (SSE-S3) with customer managed customer master keys (CMKs)
- D. Server-side encryption with Amazon S3 managed keys (SSE-S3) with AWS managed customer master keys (CMKs)

**Answer** A

**Explain**

AWS managed CMKs. You cannot manage key rotation for AWS managed CMKs. AWS KMS automatically rotates AWS managed CMKs every three years (1095 days).

https://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html

### **543**

A business requires that an Amazon S3 gateway endpoint accept traffic only from trusted buckets.

Which approach should a solutions architect use in order to fulfill this requirement?

- A. Create a bucket policy for each of the company's trusted S3 buckets that allows traffic only from the company's trusted VPCs.
- B. Create a bucket policy for each of the company's trusted S3 buckets that allows traffic only from the company's S3 gateway endpoint IDs.
- C. Create an S3 endpoint policy for each of the company's S3 gateway endpoints that blocks access from any VPC other than the company's trusted VPCs.
- D. Create an S3 endpoint policy for each of the company's S3 gateway endpoints that provides access to the Amazon Resource Name (ARN) of the trusted S3

**Answer** D

### **542**

A business has a hybrid application that is hosted on a number of on-premises servers that all have static IP addresses. There is already a VPN in place that connects the VPC to the on-premises network. The corporation want to disperse TCP traffic for internet users among its on-premises servers.

What recommendations should a solutions architect make to provide a highly accessible and scalable solution?

- A. Launch an internet-facing Network Load Balancer (NLB) and register on-premises IP addresses with the NLB.
- B. Launch an internet-facing Application Load Balancer (ALB) and register on-premises IP addresses with the ALB.
- C. Launch an Amazon EC2 instance, attach an Elastic IP address, and distribute traffic to the on-premises servers.
- D. Launch an Amazon EC2 instance with public IP addresses in an Auto Scaling group and distribute traffic to the on-premises servers.

**Answer** A

**Explain**

ALB & NLB both supports IPs as targets. Questions is based on TCP traffic over VPN to on-premise. TCP is layer 4 and the , load balancer should be NLB. Then next questions does NLB supports loadbalcning traffic over VPN.

### **541**

A business wants to enhance the availability and performance of its stateless UDP-based workload. The workload is spread across various AWS Regions using Amazon EC2 instances.

What should a solutions architect suggest as a means of achieving this?

- A. Place the EC2 instances behind Network Load Balancers (NLBs) in each Region. Create an accelerator using AWS Global Accelerator. Use the NLBs as endpoints for the accelerator.
- B. Place the EC2 instances behind Application Load Balancers (ALBs) in each Region. Create an accelerator using AWS Global Accelerator. Use the ALBs as endpoints for the accelerator.
- C. Place the EC2 instances behind Network Load Balancers (NLBs) in each Region. Create an Amazon CloudFront distribution with an origin that uses Amazon Route 53 latency-based routing to route requests to the NLBs.
- D. Place the EC2 instances behind Application Load Balancers (ALBs) in each Region. Create an Amazon CloudFront distribution with an origin that uses Amazon Route 53 latency-based routing to route requests to the ALBs.

**Answer** A

**Explain**

UDP/TCP -> NLB, Non-HTTP -> Global Accelerator

### **540**

A business operates a website that is hosted on Amazon EC2 instances spread across two Availability Zones. The organization anticipates traffic increases around certain holidays and wants to provide a consistent customer experience.

How can a solutions architect satisfy this criterion?

- A. Use step scaling.
- B. Use simple scaling.
- C. Use lifecycle hooks.
- D. Use scheduled scaling.

**Answer** D

### **539** :star:

A solutions architect is tasked with the responsibility of building an architecture for a new application that demands low network latency and high network throughput across Amazon EC2 instances.

Which component of the architectural design should be included?

- A. An Auto Scaling group with Spot Instance types.
- B. A placement group using a cluster placement strategy.
- C. A placement group using a partition placement strategy.
- D. An Auto Scaling group with On-Demand instance types.

A solutions architect is tasked with the responsibility of building an architecture for a new application that demands low network latency and high network throughput across Amazon EC2 instances.

Which component of the architectural design should be included?

- A. An Auto Scaling group with Spot Instance types.
- B. A placement group using a cluster placement strategy.
- C. A placement group using a partition placement strategy.
- D. An Auto Scaling group with On-Demand instance types.

**Answer** B

**Explain**

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html#placement-groups-cluster

### **538** :star:

A business is collaborating with a third-party vendor who needs write access to the business's Amazon Simple Queue Service (Amazon SQS) queue. The vendor has their own Amazon Web Services account.

What actions should a solutions architect take to ensure least privilege access is implemented?

- A. Update the permission policy on the SQS queue to give write access to the vendor's AWS account.
- B. Create an IAM user with write access to the SQS queue and share the credentials for the IAM user.
- C. Update AWS Resource Access Manager to provide write access to the SQS queue from the vendor's AWS account.
- D. Create a cross-account role with access to all SQS queues and use the vendor's AWS account in the trust document for the role.

**Answer** A

**Explain**

https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-basic-examples-of-sqs-policies.html

### **537**

A solutions architect is tasked with the responsibility of developing a robust solution for Windows users' home directories. The solution must have fault tolerance, file-level backup and recovery, and access control, all of which must be based on the Active Directory of the business.

Which storage option satisfies these criteria?

- A. Configure Amazon S3 to store the users' home directories. Join Amazon S3 to Active Directory.
- B. Configure a Multi-AZ file system with Amazon FSx for Windows File Server. Join Amazon FSx to Active Directory.
- C. Configure Amazon Elastic File System (Amazon EFS) for the users' home directories. Configure AWS Single Sign-On with Active Directory.
- D. Configure Amazon Elastic Block Store (Amazon EBS) to store the users' home directories. Configure AWS Single Sign-On with Active Directory.

**Answer** B

### **536** :star:

A solutions architect is converting a monolithic online application for a client into a multi-tier application. The business wishes to abstain from controlling its own infrastructure. The web application's minimal requirements include high availability, scalability, and regionally low latency during peak hours. Additionally, the solution should be capable of storing and retrieving data with a millisecond latency through the application's API.

Which solution satisfies these criteria?

- A. Use AWS Fargate to host the web application with backend Amazon RDS Multi-AZ DB instances.
- B. Use Amazon API Gateway with an edge-optimized API endpoint, AWS Lambda for compute, and Amazon DynamoDB as the data store.
- C. Use an Amazon Route 53 routing policy with geolocation that points to an Amazon S3 bucket with static website hosting and Amazon DynamoDB as the data store.
- D. Use an Amazon CloudFront distribution that points to an Elastic Load Balancer with an Amazon EC2 Auto Scaling group, along with Amazon RDS Multi-AZ DB instances.

**Answer** B

**Explain**
Edge-optimized API Endpoint

### **536 - 1**

A company has 2 VPCs named Management and Production. The Management VPC uses Virtual Private Networks through customer gateway to connect to a single device in the data center. The Production VPC uses Virtual Private Gateway with two attached AWS direct connect connections. The Management and Production VPCs both use a single VPC steering connection to allow communication between applications. 

What should a solution architect do to mitigate any single point of failure in this architecture ? 

- A. Add a set of VPNs between Management and Production VPCs 
- B. Add a second virtual private gateway and attach it to Management VPC 
- C. Add a second set of VPNs to Management VPC from second customer gateway device 
- D. Add a second VPC peering connection between the Management VPC and Production VPC

**Answer** C

### **535**

The application running on Amazon EC2 instances requires access to an Amazon S3 bucket. Due to the sensitivity of the data, it cannot be sent via the internet.

What configuration should a solutions architect make for access?

- A. Create a private hosted zone using Amazon Route 53.
- B. Configure a VPC gateway endpoint for Amazon S3 in the VPC.
- C. Configure AWS PrivateLink between the EC2 instance and the S3 bucket.
- D. Set up a site-to-site VPN connection between the VPC and the S3 bucket.

**Answer** B

**Explain**

AWS S3 and DynamoDB are are the only AWS services which use VPC gateway endpoints.

### **534** :star:

A software company is launching a new software-as-a-service (SaaS) solution that will be used by a large number of Amazon Web Services (AWS) customers. The service is hosted inside a Virtual Private Cloud (VPC) behind a Network Load Balancer. The software manufacturer want to give users with access to this service with as little administrative overhead as possible and without exposing the service to the public internet.

What actions should a solutions architect take to achieve this objective?

- A. Create a peering VPC connection from each user's VPC to the software vendor's VPC.
- B. Deploy a transit VPC in the software vendor's AWS account. Create a VPN connection with each user account.
- C. Connect the service in the VPC with an AWS Private Link endpoint. Have users subscribe to the endpoint.
- D. Deploy a transit VPC in the software vendor's AWS account. Create an AWS Direct Connect connection with each user account.

**Answer** C

**Explain**

https://docs.aws.amazon.com/vpc/latest/userguide/endpoint-service.html 

VPC endpoint services (AWS PrivateLink) 

1. You can create your own application in your VPC and configure it as an AWS PrivateLink-powered service (referred to as an endpoint service). 
2. Other AWS principals can create a connection from their VPC to your endpoint service using an interface VPC endpoint or a Gateway Load Balancer endpoint, depending on the type of service. 
3. You are the service provider, and the AWS principals that create connections to your service are service consumers.

![](https://d1.awsstatic.com/product-marketing/PrivateLink/privatelink_how-it-works.a8ae3df6830296337b30a7c4e75d8eed403eb5d2.png)

### **533**

A business wants to run a web application on AWS that communicates with a database contained inside a VPC. The application should have a high degree of availability.

What recommendations should a solutions architect make?

- A. Create two Amazon EC2 instances to host the web servers behind a load balancer, and then deploy the database on a large instance.
- B. Deploy a load balancer in multiple Availability Zones with an Auto Scaling group for the web servers, and then deploy Amazon RDS in multiple Availability Zones.
- C. Deploy a load balancer in the public subnet with an Auto Scaling group for the web servers, and then deploy the database on an Amazon EC2 instance in the private subnet.
- D. Deploy two web servers with an Auto Scaling group, configure a domain that points to the two web servers, and then deploy a database architecture in multiple Availability Zones.

**Answer** B

### **532**

A business operates an automotive sales website and keeps its listings in an Amazon RDS database. When a car is sold, the listing is deleted from the website and the data is sent to other target systems.

What kind of design should a solutions architect suggest?

- A. Create an AWS Lambda function triggered when the database on Amazon RDS is updated to send the information to an Amazon Simple Queue Service (Amazon SQS) queue for the targets to consume.
- B. Create an AWS Lambda function triggered when the database on Amazon RDS is updated to send the information to an Amazon Simple Queue Service (Amazon SQS) FIFO queue for the targets to consume.
- C. Subscribe to an RDS event notification and send an Amazon Simple Queue Service (Amazon SQS) queue fanned out to multiple Amazon Simple Notification Service (Amazon SNS) topics. Use AWS Lambda functions to update the targets.
- D. Subscribe to an RDS event notification and send an Amazon Simple Notification Service (Amazon SNS) topic fanned out to multiple Amazon Simple Queue Service (Amazon SQS) queues. Use AWS Lambda functions to update the targets.

**Answer** D

**Explain**

Multiple target scenario ~= Typical Fan Out structure

D makes complete sense. Think about it, you can have sale of diffrent types of cars happening simultaneously. For ex, toyota might have its own queue. Since RDS sends notification to SNS. IT HAS TO BE D. 

https://docs.aws.amazon.com/lambda/latest/dg/services-rds.html 

https://docs.aws.amazon.com/lambda/latest/dg/with-sns.html

### **531**

AWS-hosted applications make advantage of an Amazon Aurora Multi-AZ deployment for their database. When analyzing performance measurements, a solutions architect observed that database reads are using a significant amount of I/O and increasing delay to write requests to the database.

What should the solutions architect do to distinguish between read and write requests?

- A. Enable read-through caching on the Amazon Aurora database.
- B. Update the application to read from the Multi-AZ standby instance.
- C. Create a read replica and modify the application to use the appropriate endpoint.
- D. Create a second Amazon Aurora database and link it to the primary database as a read replica.

**Answer** C

**Explain**

Amazon RDS Read Replicas -
Amazon RDS Read Replicas provide enhanced performance and durability for RDS database (DB) instances. They make it easy to elastically scale out beyond the capacity constraints of a single DB instance for read-heavy database workloads. You can create one or more replicas of a given source DB Instance and serve high-volume application read traffic from multiple copies of your data, thereby increasing aggregate read throughput. Read replicas can also be promoted when needed to become standalone DB instances. Read replicas are available in Amazon RDS for MySQL, MariaDB, PostgreSQL, Oracle, and SQL Server as well as
Amazon Aurora.
For the MySQL, MariaDB, PostgreSQL, Oracle, and SQL Server database engines, Amazon RDS creates a second DB instance using a snapshot of the source
DB instance. It then uses the engines' native asynchronous replication to update the read replica whenever there is a change to the source DB instance. The read replica operates as a DB instance that allows only read-only connections; applications can connect to a read replica just as they would to any DB instance.
Amazon RDS replicates all databases in the source DB instance.
Amazon Aurora further extends the benefits of read replicas by employing an SSD-backed virtualized storage layer purpose-built for database workloads. Amazon
Aurora replicas share the same underlying storage as the source instance, lowering costs and avoiding the need to copy data to the replica nodes. For more information about replication with Amazon Aurora, see the online documentation.
![img](https://www.examtopics.com/assets/media/exam-media/04121/0000900001.png)
Reference:
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html https://aws.amazon.com/rds/features/read-replicas/

### **530**

A business has a build server that is part of an Auto Scaling group and often runs numerous Linux instances. For tasks and setups, the build server needs stable and mountable shared NFS storage.

What kind of storage should a solutions architect recommend?

- A. Amazon S3
- B. Amazon FSx
- C. Amazon Elastic Block Store (Amazon EBS)
- D. Amazon Elastic File System (Amazon EFS)

**Answer** D

### **529**

A business has detected access requests from many dubious IP addresses. The security team determines that the requests originate from many IP addresses within the same CIDR range.

What recommendations should a solutions architect provide to the team?

- A. Add a rule in the inbound table of the security group to deny the traffic from that CIDR range.
- B. Add a rule in the outbound table of the security group to deny the traffic from that CIDR range.
- C. Add a deny rule in the inbound table of the network ACL with a lower number than other rules.
- D. Add a deny rule in the outbound table of the network ACL with a lower rule number than other rules.

**Answer** C

**Explain**

Security group: stateful, only allow

NACL: stateless, (deny, allow) rule

### **528**

A solutions architect is tasked with the responsibility of creating the architecture for a new online application. The application will be hosted on AWS Fargate containers with an Application Load Balancer (ALB) and a PostgreSQL database hosted on Amazon Aurora. The web application will largely do read-only operations on the database.

What should the solutions architect do to assure the website's scalability as traffic increases? (Select two.)

- A. Enable auto scaling on the ALB to scale the load balancer horizontally.
- B. Configure Aurora Auto Scaling to adjust the number of Aurora Replicas in the Aurora cluster dynamically.
- C. Enable cross-zone load balancing on the ALB to distribute the load evenly across containers in all Availability Zones.
- D. Configure an Amazon Elastic Container Service (Amazon ECS) cluster in each Availability Zone to distribute the load across multiple Availability Zones.
- E. Configure Amazon Elastic Container Service (Amazon ECS) Service Auto Scaling with a target tracking scaling policy that is based on CPU utilization.

 **Answer** B, E

### **527**

An Amazon EC2 instance is created in a new VPC's private subnet. Although this subnet lacks outward internet connectivity, the EC2 instance requires the ability to obtain monthly security updates from a third-party vendor.

What actions should a solutions architect take to ensure that these criteria are met?

- A. Create an internet gateway, and attach it to the VPC. Configure the private subnet route table to use the internet gateway as the default route.
- B. Create a NAT gateway, and place it in a public subnet. Configure the private subnet route table to use the NAT gateway as the default route.
- C. Create a NAT instance, and place it in the same subnet where the EC2 instance is located. Configure the private subnet route table to use the NAT instance as the default route.
- D. Create an internet gateway, and attach it to the VPC. Create a NAT instance, and place it in the same subnet where the EC2 instance is located. Configure the private subnet route table to use the internet gateway as the default route.

**Answer** B

### **526** :star:

The website of a business is used to offer things to the general public. The site is hosted on Amazon EC2 instances that are part of an Auto Scaling group and protected by an Application Load Balancer (ALB). Additionally, an Amazon CloudFront distribution is available, and AWS WAF is utilized to guard against SQL injection attacks. The ALB is where the CloudFront distribution originates. Recent security log analysis identified an external malicious IP address that should be prevented from visiting the website.

What steps should a solutions architect take to safeguard an application?

- A. Modify the network ACL on the CloudFront distribution to add a deny rule for the malicious IP address.
- B. Modify the configuration of AWS WAF to add an IP match condition to block the malicious IP address.
- C. Modify the network ACL for the EC2 instances in the target groups behind the ALB to deny the malicious IP address.
- D. Modify the security groups for the EC2 instances in the target groups behind the ALB to deny the malicious IP address.

**Answer** B

### **525**

A development team is working in collaboration with another business to produce an integrated product. The other firm requires access to an Amazon Simple Queue Service (Amazon SQS) queue stored in the account of the development team. The other corporation want to poll the queue without granting access to its own account.

How should a solutions architect manage SQS queue access?

- A. Create an instance profile that provides the other company access to the SQS queue.
- B. Create an IAM policy that provides the other company access to the SQS queue.
- C. Create an SQS access policy that provides the other company access to the SQS queue.
- D. Create an Amazon Simple Notification Service (Amazon SNS) access policy that provides the other company access to the SQS queue.

**Answer** C

**Explain**

There is one major difference between IAM and Amazon SQS policies: the Amazon SQS policy system lets you grant permission to other AWS Accounts, whereas IAM doesn't. 

https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-using-identity-based-policies.html

### **524**

A firm is building a mobile game that sends score updates to a backend processor and then publishes the results on a leaderboard. A solutions architect must develop a solution capable of handling high volumes of traffic, processing mobile game updates in the order in which they are received, and storing the processed changes in a highly accessible database. Additionally, the organization wishes to reduce the management cost associated with maintaining the solution.

What actions should the solutions architect take to ensure that these criteria are met?

- A. Push score updates to Amazon Kinesis Data Streams. Process the updates in Kinesis Data Streams with AWS Lambda. Store the processed updates in Amazon DynamoDB.
- B. Push score updates to Amazon Kinesis Data Streams. Process the updates with a fleet of Amazon EC2 instances set up for Auto Scaling. Store the processed updates in Amazon Redshift.
- C. Push score updates to an Amazon Simple Notification Service (Amazon SNS) topic. Subscribe an AWS Lambda function to the SNS topic to process the updates. Store the processed updates in a SQL database running on Amazon EC2.
- D. Push score updates to an Amazon Simple Queue Service (Amazon SQS) queue. Use a fleet of Amazon EC2 instances with Auto Scaling to process the updates in the SQS queue. Store the processed updates in an Amazon RDS Multi-AZ DB instance.

**Answer** A

**Explain**

A. Kinesis Streams captures the data in order of receipt, and we can process the updates with lambda to finally put it on a DynamoDB. Sounds like a great option. 

B. Amazon Redshift? Warehouse data? Nop 

C. SNS, way off. 

D. Could be but using EC2 instances for processing? I don't think so.

### **523**

A solutions architect must host a high-performance computing (HPC) workload on Amazon Web Services (AWS). The workload will be dispersed over hundreds of Amazon EC2 instances and will need concurrent access to a shared file system in order to facilitate distributed processing of big datasets. Multiple instances of the same dataset will be accessible concurrently. The workload demands an access latency of less than 1 millisecond. Following completion of processing, engineers will need access to the dataset for manual postprocessing.

Which solution will satisfy these criteria?

- A. Use Amazon Elastic File System (Amazon EFS) as a shared file system. Access the dataset from Amazon EFS.
- B. Mount an Amazon S3 bucket to serve as the shared file system. Perform postprocessing directly from the S3 bucket.
- C. Use Amazon FSx for Lustre as a shared file system. Link the file system to an Amazon S3 bucket for postprocessing.
- D. Configure AWS Resource Access Manager to share an Amazon S3 bucket so that it can be mounted to all instances for processing and postprocessing.

**Answer** C

**Explain**

You use Lustre for workloads where speed matters, such as machine learning, high performance computing (HPC), video processing, and financial modeling.  

https://docs.aws.amazon.com/fsx/latest/LustreGuide/what-is.html

### **522**

The application of a business is hosted on Amazon EC2 instances behind an Application Load Balancer (ALB). The instances are distributed across multiple Availability Zones via an Amazon EC2 Auto Scaling group. At midnight on the first day of each month, the application becomes significantly slower as the month-end financial calculation batch executes. This causes the CPU utilization of the EC2 instances to spike to 100% immediately, causing the application to fail.

What should a solutions architect recommend to ensure that the application can handle the workload without experiencing downtime?

- A. Configure an Amazon CloudFront distribution in front of the ALB.
- B. Configure an EC2 Auto Scaling simple scaling policy based on CPU utilization.
- C. Configure an EC2 Auto Scaling scheduled scaling policy based on the monthly schedule.
- D. Configure Amazon ElastiCache to remove some of the workload from the EC2 instances.

**Answer** C

**Explain**

Scheduled scaling allows you to set your own scaling schedule. In this case the scaling action can be scheduled to occur just prior to the time that the reports will be run each month. 

Scaling actions are performed automatically as a function of time and date. This will ensure that there are enough EC2 instances to serve the demand and prevent the application from slowing down. 

CORRECT: "Configure an EC2 Auto Scaling scheduled scaling policy based on the monthly schedule" is the correct answer.

### **521**

A multinational conglomerate with operations in North America, Europe, and Asia is developing a new distributed application to improve its worldwide supply chain and manufacturing processes. Orders placed on a single continent should be accessible to all Regions in less than a second. The database should be capable to failover with a minimal Recovery Time Objective (RTO). The application's uptime is critical to ensuring that production does not suffer.

What recommendations should a solutions architect make?

- A. Use Amazon DynamoDB global tables.
- B. Use Amazon Aurora Global Database.
- C. Use Amazon RDS for MySQL with a cross-Region read replica.
- D. Use Amazon RDS for PostgreSQL with a cross-Region read replica.

**Answer** A

**Explain**

1. RTO is comparable for both Global database and global table
2. Aurora has one primary region for Read and Write
   Other regions can only do read which means order update/write in other regions wont be possible except primary region 
   But with DynamoDB global table Instead of writing your own code, you could create a global table consisting of your three Region-specific CustomerProfiles tables. 
   DynamoDB would then automatically replicate data changes among those tables so that changes to CustomerProfiles data in one Region would seamlessly propagate to the other Regions. 
   In addition, if one of the AWS Regions were to become temporarily unavailable, your customers could still access the same CustomerProfiles data in the other Regions.

### **520**

A business has two AWS accounts: one for production and one for development. There are code modifications ready to be sent to the Production account from the Development account.
Only two senior developers on the development team need access to the Production account during the alpha phase. During the beta phase, more developers may need access to undertake testing.

What recommendations should a solutions architect make?

- A. Create two policy documents using the AWS Management Console in each account. Assign the policy to developers who need access.
- B. Create an IAM role in the Development account. Give one IAM role access to the Production account. Allow developers to assume the role.
- C. Create an IAM role in the Production account with the trust policy that specifies the Development account. Allow developers to assume the role.
- D. Create an IAM group in the Production account and add it as a principal in the trust policy that specifies the Production account. Add developers to the group.

**Answer** C

### **519**

In another Region, a business has constructed an isolated backup of its environment. The application is in warm standby mode and is protected by a load balancer (ALB). At the moment, failover is a manual operation that needs changing a DNS alias record to link to the secondary ALB in another Region.

What is the best way for a solutions architect to automate the failover process?

- A. Enable an ALB health check
- B. Enable an Amazon Route 53 health check.
- C. Crate an CNAME record on Amazon Route 53 pointing to the ALB endpoint.
- D. Create conditional forwarding rules on Amazon Route 53 pointing to an internal BIND DNS server.

**Answer** B

**Explain** 

Route53 Health Check with active-passive failover record

![](https://raw.githubusercontent.com/sharosoo-image/upload/master/images/Screen Shot 2022-06-10 at 6.42.25 PM.png)

### **518**

A business maintains an on-premises application that gathers and saves data on an on-premises NFS server. The firm just established a ten gigabit per second AWS Direct Connect connection. The company's on-site storage capacity is rapidly depleting. The organization wants to move application data from its on-premises environment to the AWS Cloud while preserving low-latency access to the data from the on-premises application.

What actions should a solutions architect take to ensure that these criteria are met?

- A. Deploy AWS Storage Gateway for the application data, and use the file gateway to store the data in Amazon S3. Connect the on-premises application servers to the file gateway using NFS.
- B. Attach an Amazon Elastic File System (Amazon EFS) file system to the NFS server, and copy the application data to the EFS file system. Then connect the on-premises application to Amazon EFS.
- C. Configure AWS Storage Gateway as a volume gateway. Make the application data available to the on-premises application from the NFS server and with Amazon Elastic Block Store (Amazon EBS) snapshots.
- D. Create an AWS DataSync agent with the NFS server as the source location and an Amazon Elastic File System (Amazon EFS) file system as the destination for application data transfer. Connect the on-premises application to the EFS file system.

**Answer** A

**Explain**

DataSync - migrate existing data to S3

File Gateway - low latency + NFS

![](https://raw.githubusercontent.com/sharosoo-image/upload/master/images/Screen Shot 2022-06-10 at 6.50.58 PM.png)

### **517**

A business's on-premises volume backup system has reached the end of its useful life. The organization wants to include AWS into a new backup solution and wishes to retain local access to all data while it is backed up on AWS. The organization want to guarantee that data backed up on AWS is moved automatically and securely.

Which solution satisfies these criteria?

- A. Use AWS Snowball to migrate data out of the on-premises solution to Amazon S3. Configure on-premises systems to mount the Snowball S3 endpoint to provide local access to the data.
- B. Use AWS Snowball Edge to migrate data out of the on-premises solution to Amazon S3. Use the Snowball Edge file interface to provide on-premises systems with local access to the data.
- C. Use AWS Storage Gateway and configure a cached volume gateway. Run the Storage Gateway software appliance on premises and configure a percentage of data to cache locally. Mount the gateway storage volumes to provide local access to the data.
- D. Use AWS Storage Gateway and configure a stored volume gateway. Run the Storage Gateway software appliance on premises and map the gateway storage volumes to on-premises storage. Mount the gateway storage volumes to provide local access to the data.

**Answer** D

**Explain**

Can not use AWS Snowball because of "maintaining local access to all the data" Keywords: store all your data locally  

Volume Gateway: 

The gateway supports the following volume configurations: 

Cached volumes – You store your data in Amazon Simple Storage Service (Amazon S3) and retain a copy of frequently accessed data subsets locally. Cached volumes offer a substantial cost savings on primary storage and minimize the need to scale your storage on-premises. You also retain low-latency access to your frequently accessed data.  

Stored volumes – If you need low-latency access to your entire dataset, first configure your on-premises gateway to store all your data locally. Then asynchronously back up point-in-time snapshots of this data to Amazon S3. This configuration provides durable and inexpensive offsite backups that you can recover to your local data center or Amazon Elastic Compute Cloud (Amazon EC2). For example, if you need replacement capacity for disaster recovery, you can recover the backups to Amazon EC2.

### **516**

A business want to run a scalable web application on Amazon Web Services. The program will be accessible by people from all around the globe.
Users of the application will be able to download and upload unique data in the gigabyte range. The development team is looking for an economical solution that minimizes upload and download latency and optimizes speed.

What actions should a solutions architect take to achieve this?

- A. Use Amazon S3 with Transfer Acceleration to host the application.
- B. Use Amazon S3 with CacheControl headers to host the application.
- C. Use Amazon EC2 with Auto Scaling and Amazon CloudFront to host the application.
- D. Use Amazon EC2 with Auto Scaling and Amazon ElastiCache to host the application.

**Answer** A

### **515**

A business is developing a payment application that must be very reliable even in the event of regional service outages. A solutions architect must provide a data storage solution that is readily replicable and deployable across several AWS Regions. Additionally, the application needs low-latency atomicity, consistency, isolation, and durability (ACID) transactions that must be accessible promptly for report generation. Additionally, the development team must use SQL.

Which data storage option satisfies these criteria?

- A. Amazon Aurora Global Database
- B. Amazon DynamoDB global tables
- C. Amazon S3 with cross-Region replication and Amazon Athena
- D. MySQL on Amazon EC2 instances with Amazon Elastic Block Store (Amazon EBS) snapshot replication

**Answer** A

### **514**

A web application development business has deployed hundreds of Application Load Balancers (ALBs) across several regions. The firm want to build an allow list for all load balancers' IP addresses on its firewall device. A solutions architect is searching for a one-time, highly available solution to this requirement that will also assist lower the number of IPs that the firewall must accept.

What recommendations should the solutions architect make to satisfy these requirements?

- A. Create a AWS Lambda function to keep track of the IPs for all the ALBs in different Regions. Keep refreshing this list.
- B. Set up a Network Load Balancer (NLB) with Elastic IPs. Register the private IPs of all the ALBs as targets to this NLB.
- C. Launch AWS Global Accelerator and create endpoints for all the Regions. Register all the ALBs in different Regions to the corresponding endpoints.
- D. Set up an Amazon EC2 instance, assign an Elastic IP to this EC2 instance, and configure the instance as a proxy to forward traffic to all the ALBs.

**Answer** C

**Explain**

![](https://raw.githubusercontent.com/sharosoo-image/upload/master/images/Screen Shot 2022-06-10 at 7.15.41 PM.png)

### **513**

A business has a multi-tier application that is hosted on six front-end web servers in an Amazon EC2 Auto Scaling group in a single Availability Zone and is protected by an Application Load Balancer (ALB). Without affecting the application, a solutions architect must adapt the infrastructure to make it highly accessible.

Which architecture should the solutions architect use to ensure maximum availability?

- A. Create an Auto Scaling group that uses three instances across each of two Regions.
- B. Modify the Auto Scaling group to use three instances across each of two Availability Zones.
- C. Create an Auto Scaling template that can be used to quickly create more instances in another Region.
- D. Change the ALB in front of the Amazon EC2 instances in a round-robin configuration to balance traffic to the web tier.

**Answer**  B

**Explain**

ASG is regional concept. High Availability ~= multiple AZ

### **512**

A business runs an application that facilitates the upload of files to an Amazon S3 bucket. After files are uploaded, they are analyzed for metadata extraction, which takes less than 5 seconds. The upload volume and frequency vary between a few files per hour to hundreds of concurrent uploads. The organization has commissioned a solutions architect to create a cost-effective architecture that satisfies these needs.

What recommendations should the solutions architect make?

- A. Configure AWS CloudTrail trails to log S3 API calls. Use AWS AppSync to process the files.
- B. Configure an object-created event notification within the S3 bucket to invoke an AWS Lambda function to process the files.
- C. Configure Amazon Kinesis Data Streams to process and send data to Amazon S3. Invoke an AWS Lambda function to process the files.
- D. Configure an Amazon Simple Notification Service (Amazon SNS) topic to process the files uploaded to Amazon S3. Invoke an AWS Lambda function to process the files.
