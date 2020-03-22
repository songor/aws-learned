# AWS Certification Exam Mistake Collection

* S3, version

  A user has not enabled versioning on an S3 bucket. What will be the version ID of the object inside that bucket?

  A. 0

  B. There will be no version attached

  **C. Null**

  D. Blank

  ***Explanation:*** [Adding Objects to Versioning-Suspended Buckets](https://docs.aws.amazon.com/AmazonS3/latest/dev/AddingObjectstoVersionSuspendedBuckets.html). Once you suspend versioning on a bucket, Amazon S3 automatically adds a `null` version ID to every subsequent object stored thereafter (using `PUT`, `POST`, or `COPY`) in that bucket.

* SQS, delete queue

  A user has created a queue named "myqueue" with SQS. There are four messages published to queue which are not received by the consumer yet. If the user tries to delete the queue, what will happen?

  A. A user can never delete a queue manually. AWS deletes it after 30 days of inactivity on queue

  B. It will initiate the delete but wait for four days before deleting until all messages are deleted automatically.

  C. It will ask user to delete the messages first

  **D. It will delete the queue**

  ***Explanation:*** [DeleteQueue](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_DeleteQueue.html). Be careful with the `DeleteQueue` action: When you delete a queue, any messages in the queue are no longer available.

* EC2, secondary IP address

  An organization has launched two applications: one for blogging and one for ECM on the same AWS Linux EC2 instance running in the AWS VPC. The organization has attached two private IPs (primary and secondary) to the above mentioned instance. The organization wants the instance OS to recognize the secondary IP address. How can the organization configure this?

  A. Use the ec2-net-utility package which updates routing tables, uses DHCP to refresh the secondary IP and adds the network interface.

  **B. Use the ec2-net-utils package which will configure an additional network interface and update the routing table**

  C. Use the ec2-ip-update package which can configure the network interface as well as update the secondary IP with DHCP

  D. Use the ec2-ip-utility package which can update the routing tables as well as refresh the secondary IP using DHCP

  ***Explanation:*** [Multiple IP Addresses](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/MultipleIP.html). After you assign a secondary private IPv4 address to your instance, you need to configure the operating system on your instance to recognize the secondary private IP address. If you are using Amazon Linux, the ec2-net-utils package can take care of this step for you. It configures additional network interfaces that you attach while the instance is running, refreshes secondary IPv4 addresses during DHCP lease renewal, and updates the related routing rules.

* SQS, messages kept default

  How long are the messages kept on an SQS queue by default?

  A. If a message is not read, it is never deleted

  B. 2 weeks

  C. 1 day

  **D. 4 days**

* SWF, decider

  Regarding Amazon SWF, the coordination logic in a workflow is contained in a software program called a ________.

  A. Handler

  **B. Decider**

  C. Coordinator

  D. Worker

  ***Explanation:*** [Introduction to Amazon SWF](https://docs.aws.amazon.com/amazonswf/latest/developerguide/swf-dg-intro-to-swf.html). The coordination logic in a workflow is contained in a software program called a *decider*.

* IAM, region

  An account owner has created an IAM user with the name examkiller. The account owner wants to give EC2 access of only the US West region to that IAM user. How can the owner configure this?

  A. While creating a policy provide the region as a part of the resources

  B. Create an IAM user in the US West region and give access to EC2

  **C. Create an IAM policy and define the region in the condition**

  D. It is not possible to provide access based on the region

  ***Explanation:*** [Easier way to control access to AWS regions using IAM policies](https://aws.amazon.com/cn/blogs/security/easier-way-to-control-access-to-aws-regions-using-iam-policies/)

* SQS, messages kept maximum

  What is the maximum time messages can be stored in SQS?

  **A. 14 days**

  B. one month

  C. 4 days

  D. 7 days

* SQS, data size

  When using Amazon SQS how much data can you store in a message?

  **A. 8 KB**

  B. 2 KB

  C. 16 KB

  D. 4 KB

* EC2, access different region

  A user has launched one EC2 instance in the US West region. The user wants to access the RDS instance launched in the US East region from that EC2 instance. How can the user configure the access for that EC2 instance?

  A. It is not possible to access RDS of the US East region from the US West region

  B. Open the security group of the US West region in the RDS security group's ingress rule

  **C. Configure the IP range of the US West region instance as the ingress security rule of RDS**

  D. Create an IAM role which has access to RDS and launch an instance in the US West region with it

  ***Explanation:*** [Working with DB Security Groups (EC2-Classic Platform)](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithSecurityGroups.html). You can't authorize an EC2-Classic security group that is in a different AWS Region than your DB instance. You can authorize an IP range, or specify an EC2-Classic security group in the same AWS Region that refers to IP address in another AWS Region. If you specify an IP range, we recommend that you use the private IP address of your Amazon EC2 instance, which provides a more direct network route from your Amazon EC2 instance to your Amazon RDS DB instance, and doesn't incur network charges for data sent outside of the Amazon network.

* CloudFormation, stack

  In regard to AWS CloudFormation, what is a stack?

  A. The set of AWS templates that are created and managed as a template

  B. The set of AWS resources that are created and managed as a template

  **C. The set of AWS resources that are created and managed as a single unit**

  D. The set of AWS templates that are created and managed as a single unit

* Elastic Beanstalk, source bundle

  When you use the AWS Elastic Beanstalk console to deploy a new application you'll need to upload a source bundle and it should ___________________________.

  A. Consist of a single .zip file

  B. Consist of a single .war file

  **C. Consist of a single .zip file or .war file**

  D. Consist of a folder with all files

  ***Explanation:*** [Create an application source bundle](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/applications-sourcebundle.html). Consist of a single `ZIP` file or `WAR` file (you can include multiple `WAR` files inside your `ZIP` file)

* S3, static website

  A user has configured a bucket S3 to host a static website. What difference will there be when static website hosting is enabled?

  A. It will help the user identify this bucket as the website root to map with the domain

  B. It will create a new version of the bucket

  C. It will not make any difference, but will help the user to configure the error page

  **D. It will provide the region specific website endpoint**

  ***Explanation:*** [Hosting a Static Website on Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html). After you configure your bucket as a static website, you can access the bucket through the AWS Region-specific Amazon S3 website endpoints for your bucket.

* SQS, visibility timeout

  How does Amazon SQS allow multiple readers to access the same message queue without losing messages or processing them many times?

  A. By identifying a user by his unique id

  B. By using unique cryptography

  **C. Amazon SQS queue has a configurable visibility timeout**

  D. Multiple readers can't access the same message queue

  ***Explanation:*** [Amazon SQS Visibility Timeout](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-visibility-timeout.html). To prevent other consumers from processing the message again, Amazon SQS sets a *visibility timeout*, a period of time during which Amazon SQS prevents other consumers from receiving and processing the message. The default visibility timeout for a message is 30 seconds. The minimum is 0 seconds. The maximum is 12 hours.

* DynamoDB, secondary index

  In DynamoDB, a secondary index is a data structure that contains a subset of attributes from a table, along with an alternate key to support ________ operations.

  A. None of the above

  B. Both

  **C. Query**

  D. Scan

  ***Explanation:*** [Improving Data Access with Secondary Indexes](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/SecondaryIndexes.html). A *secondary index* is a data structure that contains a subset of attributes from a table, along with an alternate key to support `Query` operations.

* Security, security mechanisms

  An organization is setting up their website on AWS. The organization is working on various security measures to be performed on the AWS EC2 instances. Which of the below mentioned security mechanisms will not help the organization to avoid future data leaks and identify security weaknesses?

  A. Perform SQL injection for application testing

  B. Run penetration testing on AWS with prior approval from Amazon

  C. Perform a hardening test on the AWS instance

  **D. Perform a Code Check for any memory leaks**

* SQS, delete queue without notification

  Regarding Amazon SQS, what happens if there is no activity against a queue for more than 30 consecutive days?

  A. Your account will be suspended

  B. The queue may be deleted

  C. Nothing

  **D. The queue will be deleted**

  ***Explanation:*** [Amazon Simple Queue Service Developer Guide](https://s3.cn-north-1.amazonaws.com.cn/aws-dam-prod/china/pdf/sqs-dg.pdf). Amazon SQS can delete your queue without notification if one of the following actions hasn't been performed on it for 30 consecutive days: SendMessage, ReceiveMessage, DeleteMessage, GetQueueAttributes, SetQueueAttributes, AddPermission, and RemovePermission.

* AMI, share

  Which of the below mentioned commands allows the user to share the AMI with his peers using the AWS EC2 CLI?

  A. ec2-share-image-public

  B. ec2-share-image-account

  C. ec2-share-image

  **D. ec2-modify-image-attribute**

  ***Explanation:*** [Sharing an AMI with Specific AWS Accounts](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/sharingamis-explicit.html). You can share an AMI with specific AWS accounts without making the AMI public. All you need is the AWS account IDs.

* EBS, snapshot

  A user has created a new EBS volume from an existing snapshot. The user mounts the volume on the instance to which it is attached. Which of the below mentioned options is a required step before the user can mount the volume?

  A. Run a cyclic check on the device for data consistency

  B. Create the file system of the volume

  C. Resize the volume as per the original snapshot size

  **D. No step is required. The user can directly mount the device**

  ***Explanation:*** [Amazon EBS Snapshots](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html). When you create an EBS volume based on a snapshot, the new volume begins as an exact replica of the original volume that was used to create the snapshot. The replicated volume loads data in the background so that you can begin using it immediately.

  [Making an Amazon EBS Volume Available for Use on Linux](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-using-volumes.html). After you attach an Amazon EBS volume to your instance, it is exposed as a block device. You can format the volume with any file system and then mount it.

* ELB, custom domain name

  Can a user associate and use his own DNS with ELB instead of the DNS provided by AWS ELB?

  **A. Yes, by creating a CNAME with the existing domain name provider**

  B. Yes, by configuring DNS in the AWS Console

  C. No

  D. Yes, only through Route 53 by mapping ELB and DNS

  ***Explanation:*** [Configure a Custom Domain Name for Your Classic Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/using-domain-names-with-elb.html)

* SWF, worker

  In relation to Amazon Simple Workflow Service(Amazon SWF), what is an "Activity Worker"?

  A. An individual task undertaken by a workflow

  B. The automation of a business process

  **C. A piece of software that implements tasks**

  D. All answers listed are correct

  ***Explanation:*** [Introduction to Amazon SWF](https://docs.aws.amazon.com/amazonswf/latest/developerguide/swf-dg-intro-to-swf.html). An *activity worker* is a program that receives activity tasks, performs them, and provides results back.

* Auto Scaling, new instance

  When Auto Scaling is launching a new instance based on condition, which of the below mentioned policies will it follow?

  A. Based on the criteria defined with cross zone Load balancing

  B. Launch an instance which has the highest load distribution

  **C. Launch an instance in the AZ with the fewest instances**

  D. Launch an instance in the AZ which has the highest instances

  ***Explanation:*** [Benefits of Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/auto-scaling-benefits.html). Amazon EC2 Auto Scaling attempts to distribute instances evenly between the Availability Zones that are enabled for your Auto Scaling group. Amazon EC2 Auto Scaling does this by attempting to launch new instances in the Availability Zone with the fewest instances. If the attempt fails, however, Amazon EC2 Auto Scaling attempts to launch the instances in another Availability Zone until it succeeds. For Auto Scaling groups in a VPC, if there are multiple subnets in an Availability Zone, Amazon EC2 Auto Scaling selects a subnet from the Availability Zone at random.

* SQS, secure the messages

  In regards to Amazon SQS how can you secure the messages in your queues?

  A. You can't

  **B. Amazon SQS uses either your Access Key ID or an X.509 certificate to authenticate your identity**

  C. Through your IAM access keys

  D. Don't use root access

  ***Explanation:*** [How can I secure the messages in my message queues?](https://aws.amazon.com/sqs/faqs/). Authentication mechanisms ensure that messages stored in Amazon SQS message queues are secured against unauthorized access.

  [What kinds of security credentials can IAM users have?](https://aws.amazon.com/iam/faqs/)

* RRS

  Which of the below mentioned options can be a good use case for storing content in AWS RRS?

  A. Storing mission critical data Files

  B. Storing infrequently used log files

  C. Storing a video file which is not reproducible

  **D. Storing image thumbnails**

  ***Explanation:*** [Amazon S3 Storage Classes](https://docs.aws.amazon.com/AmazonS3/latest/dev/storage-class-intro.html). The Reduced Redundancy Storage (RRS) storage class is designed for noncritical, reproducible data that can be stored with less redundancy than the S3 Standard storage class.

* SWF, activity

  When you register an activity in Amazon SWF, you provide the following information, except:

  A. a name

  B. timeout values

  **C. a domain**

  D. version

  ***Explanation:*** [Introduction to Amazon SWF](https://docs.aws.amazon.com/amazonswf/latest/developerguide/swf-dg-intro-to-swf.html). When you register the activity, you provide information such as a name and version, and some timeout values based on how long you expect the activity to take.

* IAM, policy

  A user is trying to create a policy for an IAM user from the AWS console. Which of the below mentioned options is not available to the user while configuring policy?

  A. Use policy generator to create policy

  B. Use custom policy to create policy

  **C. Use policy simulator to create policy**

  D. Assign No permission

  ***Explanation:*** The AWS Policy Generator is a tool that enables you to create policies that control access to Amazon Web Services (AWS) products and resources.

  [Test Your Roles’ Access Policies Using the AWS Identity and Access Management Policy Simulator](https://aws.amazon.com/blogs/security/test-your-roles-access-policies-using-the-aws-identity-and-access-management-policy-simulator/). The policy simulator is a tool to help you author and validate the policies that set permissions on your AWS resources.

* S3, data consistency model

  A user has an S3 object in the US Standard region with the content "color=red". The user updates the object with the content as "color="white". If the user tries to read the value 1 minute after it was uploaded, what will S3 return?

  A. It will return "color=white"

  B. It will return "color=red"

  C. It will return an error saying that the object was not found

  **D. It may return either "color=red" or "color=white" i.e. any of the value**

  ***Explanation:*** [Amazon S3 Data Consistency Model](https://docs.aws.amazon.com/AmazonS3/latest/dev/Introduction.html). Amazon S3 offers eventual consistency for overwrite PUTS and DELETES in all Regions.

  Amazon S3 achieves high availability by replicating data across multiple servers within AWS data centers.

* Elastic Beanstalk, health colors

  AWS Elastic Beanstalk will change the health status of a web server environment tier to gray color when:

  A. AWS Elastic Beanstalk detects other problems with the environment that are known to make the application unavailable

  B. Your application hasn't responded to the application health check URL within the last one hour

  C. Your application hasn't responded to the application health check URL within the last five minutes

  **D. Your application's health status is unknown because status is reported when the application is not in the ready state**

  ***Explanation:*** [Health colors and statuses](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/health-enhanced-status.html). When an instance fails health checks at least three times in any one-minute period, Elastic Beanstalk may downgrade the health of the environment.

* EBS, snapshot

  A user is creating a snapshot of an EBS volume. Which of the below statements is incorrect in relation to the creation of an EBS snapshot?

  A. Its incremental

  B. It can be used to launch a new instance

  **C. It is stored in the same AZ as the volume**

  D. It is a point in time backup of the EBS volume

  ***Explanation:*** [Amazon EBS Snapshots](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html). You can back up the data on your Amazon EBS volumes to Amazon S3 by taking point-in-time snapshots. Snapshots are *incremental* backups, which means that only the blocks on the device that have changed after your most recent snapshot are saved.

  When you create an EBS volume based on a snapshot, the new volume begins as an exact replica of the original volume that was used to create the snapshot.

* EC2, tags

  Your manager has requested you to tag EC2 instances to organize and manage a load balancer. Which of the following statements about tag restrictions is incorrect?

  A. The maximum key length is 128 Unicode characters

  B. The maximum value length is 255 Unicode characters

  C. Tag keys and values are case sensitive

  **D. The maximum number of tags per load balancer is 20**

  ***Explanation:*** [Tagging Your Amazon EC2 Resources](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Tags.html). Maximum number of tags per resource – 50

* S3, version

  A user is trying to find the state of an S3 bucket with respect to versioning. Which of the below mentioned states AWS will not return when queried?

  A. versioning-enabled

  B. versioning-suspended

  C. unversioned

  **D. versioned**

  ***Explanation:*** [Using Versioning](https://docs.aws.amazon.com/AmazonS3/latest/dev/Versioning.html). Buckets can be in one of three states: unversioned (the default), versioning-enabled, or versioning-suspended.

* DynamoDB, atomic counters

  Does Amazon DynamoDB support both increment and decrement atomic operations?

  A. No, neither increment nor decrement operations

  B. Only increment, since decrement are inherently impossible with DynamoDB's data model

  C. Only decrement, since increment are inherently impossible with DynamoDB's data model

  **D. Yes, both increment and decrement operations**

  ***Explanation:*** [Atomic Counters](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WorkingWithItems.html#WorkingWithItems.AtomicCounters). You can use the `UpdateItem` operation to implement an *atomic counter*—a numeric attribute that is incremented, unconditionally, without interfering with other write requests.

* S3, IAM

  A user is trying to configure access with S3. Which of the following options is not possible to provide access to the S3 bucket / object?

  A. Define the policy for the IAM user

  B. Define the ACL for the object

  **C. Define the policy for the object**

  D. Define the policy for the bucket

  ***Explanation:*** [Identity and Access Management in Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/dev/s3-access-control.html). [Guidelines for Using the Available Access Policy Options](https://docs.aws.amazon.com/AmazonS3/latest/dev/access-policy-alternatives-guidelines.html)

* ELB, listeners

  A user is configuring the HTTPS protocol on a front end ELB and the SSL protocol for the back-end listener in ELB. What will ELB do?

  A. It will allow you to create the configuration, but the instance will not pass the health check

  B. Receives requests on HTTPS and sends it to the back end instance on SSL

  **C. It will not allow you to create this configuration**

  D. It will allow you to create the configuration, but ELB will not work as expected

  ***Explanation:*** [Listeners for Your Classic Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-listener-config.html). If the front-end connection uses TCP or SSL, then your back-end connections can use either TCP or SSL. If the front-end connection uses HTTP or HTTPS, then your back-end connections can use either HTTP or HTTPS.

* RDS, MS SQL

  A user is planning to host MS SQL on an EBS volume. It was recommended to use the AWS RDS. What advantages will the user have if he uses RDS in comparison to an EBS based DB?

  A. Better throughput with PIOPS

  B. Automated backup

  C. MS SQL is not supported with RDS

  **D. High availability with multi AZs**

  ***Explanation:*** [Multi-AZ Deployments for Microsoft SQL Server](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_SQLServerMultiAZ.html)

* ELB, register EC2 instances

  A user is setting up an Elastic Load Balancer(ELB). Which of the below parameters should the user consider so as the instance gets registered with the ELB?

  A. ELB DNS

  **B. IP address**

  C. Security group

  D. ELB IP

  ***Explanation:*** [Register or Deregister EC2 Instances for Your Classic Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-deregister-register-instances.html). Elastic Load Balancing registers your EC2 instance with your load balancer using its IP address.

* [Step and Simple Scaling Policies for Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html). You can specify the adjustment type as a percentage of the current capacity of your Auto Scaling group, or in capacity units.

* [DB Instance Billing for Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/User_DBInstanceBilling.html)

* [DynamoDB Secondary Indexes](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.CoreComponents.html#HowItWorks.CoreComponents.SecondaryIndexes)

* EC2, launch

  When a user is launching an instance with EC2, which of the below mentioned options is not available during the instance launch console for a key pair?

  A. Proceed without the key pair

  **B. Upload a new key pair**

  C. Select an existing key pair

  D. Create a new key pair

  ***Explanation:*** [Launching an instance using the Launch Instance Wizard](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/launching-instance.html#step-7-review-instance-launch)

* EBS, volume

  A user is creating an EBS volume. He asks for your advice. Which advice mentioned below should you not give to the user for creating an EBS volume?

  A. Take the snapshot of the volume when the instance is stopped

  B. Stripe multiple volumes attached to the same instance

  **C. Create an AMI from the attached volume**

  D. Attach multiple volumes to the same instance

  ***Explanation:*** [Amazon EBS Volumes](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volumes.html). If you attach multiple volumes to a device that you have named, you can stripe data across the volumes for increased I/O and throughput performance.

  [Creating an Amazon EBS-Backed Linux AMI](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/creating-an-ami-ebs.html). If you have a snapshot of the root device volume of an instance, you can create an AMI from this snapshot using the AWS Management Console or the command line.

* DynamoDB, console

  The AWS console for DynamoDB enables you to do all the following operations, except:

  A. Set up alarms to monitor your table's capacity usage

  B. Create, update, and delete tables

  **C. Import Data from other databases or from files**

  D. View your table's top monitoring metrics on real-time graphs from CloudWatch

  ***Explanation:*** [Import and Export DynamoDB Data Using AWS Data Pipeline](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-importexport-ddb.html). [Using the Console](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/ConsoleDynamoDB.html)

* ELB, cookie

  A user has hosted a website on AWS and uses ELB to load balance the multiple instances. The user application does not have any cookie management. How can the user bind the session of the requestor with a particular instance?

  A. Bind the IP address with a sticky cookie

  B. Create a cookie at the application level to set at ELB

  C. Use session synchronization with ELB

  **D. Let ELB generate a cookie for a specified duration**

  ***Explanation:*** [Configure Sticky Sessions for Your Classic Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-sticky-sessions.html). The key to managing sticky sessions is to determine how long your load balancer should consistently route the user's request to the same instance. If your application has its own session cookie, then you can configure Elastic Load Balancing so that the session cookie follows the duration specified by the application's session cookie. If your application does not have its own session cookie, then you can configure Elastic Load Balancing to create a session cookie by specifying your own stickiness duration.

* RDS, automated backup

  A user has enabled automated backup for an RDS instance. What is the longest duration for which the user can retain the automated backup?

  A. 25 days

  B. 15 days

  C. 45 days

  **D. 35 days**

  ***Explanation:*** [Working With Backups](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithAutomatedBackups.html). You can set the backup retention period to between 0 and 35 days.

* S3 Glacier, data model

  A user is uploading archives to Glacier. The user is trying to understand key Glacier resources. Which of the below mentioned options is not a Glacier resource?

  A. Notification configuration

  **B. Archive ID**

  C. Job

  D. Archive

  ***Explanation:*** [Amazon S3 Glacier Data Model](https://docs.aws.amazon.com/amazonglacier/latest/dev/amazon-glacier-data-model.html). The Amazon S3 Glacier (S3 Glacier) data model core concepts include vaults and archives. In addition, the S3 Glacier data model includes job and notification-configuration resources.

* SWF, markers

  Regarding Amazon SWF, at times you might want to record information in the workflow history of a workflow execution that is specific to your use case. _________ enable you to record information in the workflow execution history that you can use for any custom or scenario-specific purpose.

  A. Markers

  B. Tags

  C. Hash keys

  D. Events

  ***Explanation:*** [Markers](https://docs.aws.amazon.com/amazonswf/latest/developerguide/swf-dev-adv-markers.html)

* IAM, security credentials

  An organization has created 10 IAM users. The organization wants those users to work independently and access AWS. Which of the below mentioned options is not a possible solution?

  **A. Create the access key and secret access key for each user and provide access to AWS using the console**

  B. Create the X.509 certificate for each user and provide them access to AWS CLI

  C. Enable MFA for each IAM user and assign them the virtual MFA device to access the console

  D. Provide each user with the IAM login and password for the AWS console

  ***Explanation:*** [Understanding and Getting Your Security Credentials](https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html)

* SQS, maximum size

  What is the maximum size for messages stored in SQS?

  **A. 256KB**

  B. 128KB

  C. 1024KB

  D. 64KB

  ***Explanation:*** [How do I configure the maximum message size for Amazon SQS](https://aws.amazon.com/sqs/faqs/)

* [Permitting IAM Users to Change Their Own Passwords](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_passwords_enable-user-change.html)

* CloudFormation, maximum number of stacks

  When working with AWS CloudFormation Templates what is the maximum number of stacks that you can create?

  A. 500

  B. 50

  C. 20

  D. 10

  ***Explanation:*** [AWS CloudFormation Limits](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cloudformation-limits.html). 200 stacks.

* EBS, IOPS

  A user has created an EBS volume with 1000 IOPS. What is the average IOPS that the user will get for most of the year as per EC2 SLA if the instance is attached to the EBS optimized instance?

  **A. 900**

  B. 990

  C. 950

  D. 1000

  ***Explanation:*** [What level of performance consistency can I expect to see from my Provisioned IOPS SSD (io1) volumes?](https://aws.amazon.com/ebs/faqs/). When attached to EBS-optimized instances, Provisioned IOPS SSD (io1) volumes are designed to deliver within 10% of the provisioned IOPS performance 99.9% of the time in a given year.

* DynamoDB

  Which statements about DynamoDB are true? Choose 2 answers

  A. DynamoDB uses a pessimistic locking model

  **B. DynamoDB uses optimistic concurrency control**

  **C. DynamoDB uses conditional writes for consistency**

  D. DynamoDB restricts item access during reads

  E. DynamoDB restricts item access during writes

  ***Explanation:*** [Conditional Writes](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WorkingWithItems.html#WorkingWithItems.ConditionalUpdate). Conditional writes are helpful in cases where multiple users attempt to modify the same item.

  [Optimistic Locking with Version Number](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBMapper.OptimisticLocking.html). *Optimistic locking* is a strategy to ensure that the client-side item that you are updating (or deleting) is the same as the item in Amazon DynamoDB.

* EBS, secure data

  How can you secure data at rest on an EBS volume?

  A. Attach the volume to an instance using EC2's SSL interface

  B. Write the data randomly instead of sequentially

  **C. Use an encrypted file system on top of the EBS volume**

  D. Encrypt the volume using the S3 server-side encryption service.

  E. Create an IAM policy that restricts read and write access to the volume

  ***Explanation:*** [How to Protect Data at Rest with Amazon EC2 Instance Store Encryption](https://aws.amazon.com/blogs/security/how-to-protect-data-at-rest-with-amazon-ec2-instance-store-encryption/)

* SWF

  Which of the following statements about SWF are true? Choose 3 answers

  **A. SWF tasks are assigned once and never duplicated**

  B. SWF requires an S3 bucket for workflow storage

  **C. SWF workflow executions can last up to a year**

  D. SWF triggers SNS notifications on task assignment

  **E. SWF uses deciders and workers to complete tasks**

  F. SWF requires at least 1 EC2 instance per domain

  ***Explanation:*** [Amazon SWF Limits](https://docs.aws.amazon.com/amazonswf/latest/developerguide/swf-dg-limits.html). Maximum workflow execution time – 1 year

  [Amazon SWF Tasks](https://docs.aws.amazon.com/amazonswf/latest/developerguide/swf-dev-tasks.html). Amazon SWF assigns each activity task to exactly one activity worker. Once the task is assigned, no other activity worker can claim or perform that task.

  [What are workers and deciders?](https://aws.amazon.com/swf/faqs/). Workers are programs that interact with Amazon SWF to get tasks, process received tasks, and return the results. The decider is a program that controls the coordination of tasks.

* [Common Pitfalls When Testing Elastic Load Balancing](https://aws.amazon.com/articles/best-practices-in-evaluating-elastic-load-balancing/)

  DNS Resolution - If clients do not re-resolve the DNS at least once per minute, then the new resources Elastic Load Balancing adds to DNS will not be used by clients. This can mean that clients continue to overwhelm a small portion of the allocated Elastic Load Balancing resources, while overall Elastic Load Balancing is not being heavily utilized. This is not a problem that can occur in real-world scenarios, but it is a likely problem for load testing tools that do not offer the control needed to ensure that clients are re-resolving DNS frequently.

  Sticky Sessions and Unique Clients - If sticky sessions are enabled, it is critical that the load test framework not re-use connections and clients in the tests, but rather it creates unique clients for each request. If this is not done, then the clients will constantly send traffic to the same Elastic Load Balancing resources and the same back-end instances, overwhelming what is potentially a very small amount of the available capacity.

* SNS, device tokens

  You are providing AWS consulting services for a company developing a new mobile application that will be leveraging Amazon SNS Mobile Push for push notifications. In order to send direct notification messages to individual devices each device registration identifier or token needs to be registered with SNS; however the developers are not sure of the best way to do this. You advise them to:

  A. Bulk upload the device tokens contained in a CSV file via the AWS Management Console

  B. Let the push notification service(e.g. Amazon Device Messaging) handle the registration

  C. Implement a token vending service to handle the registration

  **D. Call the CreatePlatformEndPoint API function to register multiple device tokens**

  ***Explanation:*** [Add Device Tokens or Registration IDs](https://docs.aws.amazon.com/sns/latest/dg/mobile-push-send-devicetoken.html)

  You can add device tokens and registration IDs to Amazon SNS using the following methods:

  Manually add a single token to AWS using the AWS Management Console

  Migrate existing tokens from a CSV file to AWS using the AWS Management Console

  Upload several tokens using the `CreatePlatformEndpoint` API

  Register tokens from devices that will install your apps in the future

* 

