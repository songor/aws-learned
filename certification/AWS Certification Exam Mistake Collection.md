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

  [IAM Policy Elements: Variables and Tags](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_variables.html). Use AWS Identity and Access Management (IAM) policy variables as placeholders when you don't know the exact value of a resource or condition key when you write the policy.

* S3, data consistency model

  A user has an S3 object in the US Standard region with the content "color=red". The user updates the object with the content as "color="white". If the user tries to read the value 1 minute after it was uploaded, what will S3 return?

  A. It will return "color=white"

  B. It will return "color=red"

  C. It will return an error saying that the object was not found

  **D. It may return either "color=red" or "color=white" i.e. any of the value**

  ***Explanation:*** [Amazon S3 Data Consistency Model](https://docs.aws.amazon.com/AmazonS3/latest/dev/Introduction.html). Amazon S3 offers eventual consistency for overwrite PUTS and DELETES in all Regions.

  Amazon S3 achieves high availability by replicating data across multiple servers within AWS data centers. If a PUT request is successful, your data is safely stored. However, information about the changes must replicate across Amazon S3, which can take some time.

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

* SQS, SetQueueAttributes

  [SetQueueAttributes](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_SetQueueAttributes.html)

  | Request Parameters            | Valid values                                                 |
  | :---------------------------- | :----------------------------------------------------------- |
  | DelaySeconds                  | An integer from 0 to 900 (15 minutes). Default: 0.           |
  | MaximumMessageSize            | An integer from 1,024 bytes (1 KiB) up to 262,144 bytes (256 KiB). Default: 262,144 (256 KiB). |
  | MessageRetentionPeriod        | An integer representing seconds, from 60 (1 minute) to 1,209,600 (14 days). Default: 345,600 (4 days). |
  | ReceiveMessageWaitTimeSeconds | An integer from 0 to 20 (seconds). Default: 0.               |
  | VisibilityTimeout             | An integer from 0 to 43,200 (12 hours). Default: 30.         |

  [Amazon SQS Short and Long Polling](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-short-and-long-polling.html)

  Long polling offers the following benefits:

  Eliminate empty responses by allowing Amazon SQS to wait until a message is available in a queue before sending a response.

  Eliminate false empty responses by querying all—rather than a subset of—Amazon SQS servers.

  Return messages as soon as they become available.

* S3, bucket limit

  What is the maximum number of S3 Buckets available per AWS account?

  A. 100 per region

  B. there is no limit

  C. 100 per account

  D. 500 per account

  E. 100 per IAM user

  ***Explanation:*** [Bucket Restrictions and Limitations](https://docs.aws.amazon.com/AmazonS3/latest/dev/BucketRestrictions.html). By default, you can create up to 100 buckets in each of your AWS accounts. If you need additional buckets, you can increase your account bucket limit to a maximum of 1,000 buckets by submitting a service limit increase.

* [Using Elastic Beanstalk with other AWS services](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/AWSHowTo.html)

* [What is the format of structured notification messages sent by Amazon SNS?](https://aws.amazon.com/sns/faqs/)

* DynamoDB, scan

  When using a large Scan operation in DynamoDB, what technique can be used to minimize the impact of a scan on a table's provisioned throughput?

  **A. Set a smaller page size for the scan**

  B. Use parallel scans

  C. Define a range index on the table

  D. Prewarm the table by updating all items

  ***Explanation:*** [Best Practices for Querying and Scanning Data](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/bp-query-scan.html). Instead of using a large `Scan` operation, you can use the following techniques to minimize the impact of a scan on a table's provisioned throughput.

  Reduce page size. Because a Scan operation reads an entire page (by default, 1 MB), you can reduce the impact of the scan operation by setting a smaller page size.

  Isolate scan operations.

  [Scan](https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_Scan.html). `Scan` uses eventually consistent reads when accessing the data in a table; therefore, the result set might not include the changes to data in the table immediately before the operation began.

  [Rate-Limited Scans in Amazon DynamoDB](https://aws.amazon.com/blogs/developer/rate-limited-scans-in-amazon-dynamodb/). When you scan your table in Amazon DynamoDB, you should follow the DynamoDB best practices for [avoiding sudden bursts of read activity](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/QueryAndScanGuidelines.html). You may also want to limit a background `Scan` job to use a limited amount of your table’s provisioned throughput, so that it doesn’t interfere with your more important operations. Fortunately, the Google Guava libraries for Java include a RateLimiter class, which makes it easy to limit the amount of provisioned throughput you use.

* DynamoDB, partition key

  You are writing to a DynamoDB table and receive the following exception: " ProvisionedThroughputExceededException". Though according to your CloudWatch metrics for the table, you are not exceeding your provisioned throughput. What could be an explanation for this?

  A. You haven't provisioned enough DynamoDB storage instances

  B. You're exceeding your capacity on a particular Range Key

  **C. You're exceeding your capacity on a particular Hash Key**

  D. You're exceeding your capacity on a particular Sort Key

  E. You haven't configured DynamoDB Auto Scaling triggers

  ***Explanation:*** [Choosing the Right DynamoDB Partition Key](https://aws.amazon.com/blogs/database/choosing-the-right-dynamodb-partition-key/). DynamoDB evenly distributes [provisioned throughput](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.ProvisionedThroughput.html)—read capacity units (RCUs) and write capacity units (WCUs)—among partitions and automatically supports your access patterns using the throughput you have provisioned. However, if your access pattern  exceeds 3000 RCU or 1000 WCU [for a single partition key value](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/bp-partition-key-design.html), your requests might be throttled with a `ProvisionedThroughputExceededException` error.

* S3, naming schema

  If an application is storing hourly log files from thousands of instances from a high traffic web site, which naming scheme would give optimal performance on S3?

  A. Sequential

  B. instanceID_log-HH-DD-MM-YYYY

  C. instanceID_log-YYYY-MM-DD-HH

  **D. HH-DD-MM-YYYY-log_instanceID**

  E. YYYY-MM-DD-HH-log_instanceID

  ***Explanation:*** [Best Practices Design Patterns: Optimizing Amazon S3 Performance](https://docs.aws.amazon.com/AmazonS3/latest/dev/optimizing-performance.html). For example, previously Amazon S3 performance guidelines recommended randomizing prefix naming with hashed characters to optimize performance for frequent data retrievals. You no longer have to randomize prefix naming for performance, and can use sequential date-based naming for your prefixes.

* [Share an Object with Others](https://docs.aws.amazon.com/AmazonS3/latest/dev/ShareObjectPreSignedURL.html). All objects by default are private. Only the object owner has permission to access these objects. However, the object owner can optionally share objects with others by creating a presigned URL, using their own security credentials, to grant time-limited permission to download the objects.

* VPC, NAT

  After launching an instance that you intend to serve as a NAT (Network Address Translation) device in a public subnet you modify your route tables to have the NAT device be the target of internet bound traffic of your private subnet. When you try and make an outbound connection to the Internet from an instance in the private subnet, you are not successful. Which of the following steps could resolve the issue?

  A. Attaching a second Elastic Network interface (ENI) to the NAT instance, and placing it in the private subnet

  B. Attaching a second Elastic Network Interface (ENI) to the instance in the private subnet, and placing it in the public subnet

  **C. Disabling the Source/Destination Check attribute on the NAT instance**

  D. Attaching an Elastic IP address to the instance in the private subnet

  ***Explanation:*** [NAT Instances](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_NAT_Instance.html). Each EC2 instance performs source/destination checks by default. This means that the instance must be the source or destination of any traffic it sends or receives. However, a NAT instance must be able to send and receive traffic when the source or destination is not itself. Therefore, you must disable source/destination checks on the NAT instance.

* DynamoDB, pricing

  In DynamoDB, if you create a table and request 10 units of write capacity and 200 units of read capacity of provisioned throughput, how much would you be charged in US East (Northern Virginia) Region?

  A. $0.05 per hour

  B. $0.10 per hour

  **C. $0.03 per hour**

  D. $0.15 per hour

  ***Explanation:*** [Pricing for Provisioned Capacity](https://aws.amazon.com/dynamodb/pricing/provisioned/). 0.00065 * 10 + 0.00013 * 200 = 0.0325

  For example, a strongly consistent read of an 8 KB item would require two RCUs, an eventually consistent read of an 8 KB item would require one RCU, and a transactional read of an 8 KB item would require four RCUs.

  For example, a standard write request of a 1 KB item would require one WCU, a standard write request of a 3 KB item would require three WCUs, and a transactional write request of a 3 KB item would require six WCUs.

* EC2, security

  Which of the below mentioned pointers will not help the organization achieve better security arrangement?

  A. Apply the latest patch of OS and always keep it updated

  **B. Allow only IAM users to connect with the EC2 instances with their own secret access key**

  C. Disable the password based login for all the users. All the users should use their own keys to connect with the instance securely

  D. Create a procedure to revoke the access rights of the individual user when they are not required to connect to EC2 instance anymore for the purpose of application configuration

  ***Explanation:*** [Tips for Securing Your EC2 Instance](https://aws.amazon.com/articles/tips-for-securing-your-ec2-instance/)

* DynamoDB, operation

  Which one of the following operations is NOT a DynamoDB operation?

  A. BatchWriteItem

  B. DescribeTable

  C. BatchGetItem

  **D. BatchDeleteItem**

  ***Explanation:*** [DynamoDB API](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.API.html)

* Elastic Beanstalk

  Which of the following platforms are supported by Elastic Beanstalk? Choose 2 answers

  **A. Apache Tomcat**

  **B. .NET**

  C. IBM Websphere

  D. Oracle JBoss

  E. Jetty

  ***Explanation:*** [Elastic Beanstalk supported platforms](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/concepts.platforms.html)

* EC2, AMIs

  Which EC2 API call would you use to retrieve a list of Amazon Machine Images (AMIs)?

  A. DescnbeInstances

  **B. DescribeAMls**

  C. DescribeImages

  D. GetAMls

  E. You cannot retrieve a list of AMIs as there are over 10,000 AMIs

* EC2, monitoring

  In Amazon EC2, which of the following is the type of monitoring data for Amazon EBS volumes that is available automatically in 5-minute periods at no charge?

  A. Primary

  **B. Basic**

  C. Initial

  D. Detailed

  ***Explanation:*** [Enable or Disable Detailed Monitoring for Your Instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-cloudwatch-new.html)

* EC2, terminate

  A user has launched an EC2 instance. However, due to some reason the instance was terminated. If the user wants to find out the reason for termination, where can he find the details?

  **A. The user can get information from the AWS console, by checking the Instance description under the State transition reason label**

  B. The user can get information from the AWS console, by checking the Instance description under the Instance Termination reason label

  C. The user can get information from the AWS console, by checking the Instance description under the Instance Status Change reason label

  D. It is not possible to find the details after the instance is terminated

  ***Explanation:*** [Instance Terminates Immediately](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/troubleshooting-launch.html#troubleshooting-launch-internal)

* RDS, PIOPS

  A user has created a MySQL RDS instance with PIOPS. Which of the below mentioned statements will help user understand the advantage of PIOPS?

  A. The user can achieve additional dedicated capacity for the EBS I/O with an enhanced RDS option

  **B. It uses optimized EBS volumes and optimized configuration stacks**

  C. It provides a dedicated network bandwidth between EBS and RDS

  D. It uses a standard EBS volume with optimized configuration the stacks

  ***Explanation:*** [Amazon RDS DB Instance Storage](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Storage.html). DB instances for Amazon RDS for MySQL, MariaDB, PostgreSQL, Oracle, and Microsoft SQL Server use Amazon Elastic Block Store (Amazon EBS) volumes for database and log storage. Depending on the amount of storage requested, Amazon RDS automatically stripes across multiple Amazon EBS volumes to enhance performance.

  Provisioned IOPS storage is a storage type that delivers predictable performance, and consistently low latency.

  [Amazon EBS–Optimized Instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-optimized.html). An Amazon EBS–optimized instance uses an optimized configuration stack and provides additional, dedicated capacity for Amazon EBS I/O.

* IAM, role

  Which of the following items are required to allow an application deployed on an EC2 instance to write data to a DynamoDB table? Assume that no security keys are allowed to be stored on the EC2 instance. Choose 2 answers.

  A. Create an IAM User that allows write access to the DynamoDB table

  **B. Add an IAM Role to a running EC2 instance**

  C. Add an IAM User to a running EC2 Instance

  **D. Launch an EC2 Instance with the IAM Role included in the launch configuration**

  **E. Create an IAM Role that allows write access to the DynamoDB table**

  F. Launch an EC2 Instance with the IAM User included in the launch configuration

  ***Explanation:*** [Attach an IAM role to your existing Amazon EC2 instance](https://aws.amazon.com/cn/about-aws/whats-new/2017/02/new-attach-an-iam-role-to-your-existing-amazon-ec2-instance/)

* DynamoDB, limit

  Is there a limit to how much throughput you can get out of a single table in DynamoDB?

  A. Yes, not more than 1,000 writes/second or 1,000 reads/second

  B. No

  C. Yes, not more than 10,000 writes/second or 10,000 reads/second

  **D. No, but If you wish to exceed throughput rates of 10,000 writes/second or 10,000 reads/second, you must first contact AWS**

  ***Explanation:*** [Read/Write Capacity Mode and Throughput](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Limits.html#default-limits-throughput-capacity-modes). Per table - 40,000 read capacity units and 40,000 write capacity units, Per account - 80,000 read capacity units and 80,000 write capacity units.

  You can increase `ReadCapacityUnits` or `WriteCapacityUnits` as often as necessary, using the AWS Management Console or the `UpdateTable` operation.

* Microsoft SQL Server, Multi-AZ

  A user has setup Multi AZ with the MS SQL RDS instance. Which of the below mentioned functionalities can be achieved by the user?

  **A. High availability**

  B. Scalability

  C. MS SQL does not support Multi AZ

  D. Disaster recovery

  ***Explanation:*** [Multi-AZ Deployments for Microsoft SQL Server](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_SQLServerMultiAZ.html)

* [Tutorial: Create a Classic Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-getting-started.html)

* EC2, metadata

  An organization is having an application which can start and stop an EC2 instance as per schedule. The organization needs the MAC address of the instance to be registered with its software. The instance is launched in EC2-CLASSIC. How can the organization update the MAC registration every time an instance is booted?

  A. The instance MAC address never changes. Thus, it is not required to register the MAC address every time

  **B. The organization should write a boot strapping script which will get the MAC address from the instance metadata and use that script to register with the application**

  C. AWS never provides a MAC address to an instance; instead the instance ID is used for identifying the instance for any software registration

  D. The organization should provide a MAC address as a part of the user data. Thus, whenever the instance is booted the script assigns the fixed MAC address to that instance

  ***Explanation:*** [Instance Metadata Categories](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instancedata-data-categories.html). mac - The instance's media access control (MAC) address. In cases where multiple network interfaces are present, this refers to the eth0 device (the device for which the device number is 0).

  local-ipv4 - The private IPv4 address of the instance.

  public-ipv4 - The public IPv4 address. If an Elastic IP address is associated with the instance, the value returned is the Elastic IP address.

  [Running Commands on Your Linux Instance at Launch](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/user-data.html#user-data-shell-scripts). When you launch an instance in Amazon EC2, you have the option of passing user data to the instance that can be used to perform common automated configuration tasks and even run scripts after the instance starts.

* RDS, storage

  A user has launched an RDS instance. The user has created 3 databases on the same server. What can the maximum size be for each database?

  A. The size of each DB cannot be more than 3 TB

  B. It is not possible to have more than one DB on a single instance

  **C. The total instance storage size cannot be more than 3 TB**

  D. The size of each DB cannot be more than 1 TB

  ***Explanation:*** [Amazon RDS DB Instance Storage](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Storage.html). You can create MySQL, MariaDB, and PostgreSQL RDS DB instances with up to 64 TiB of storage. You can create Oracle RDS DB instances with up to 64 TiB of storage. You can create SQL Server RDS DB instances with up to 16 TiB of storage. 

  Magnetic storage - Limited to a maximum size of 3 TiB.

* IAM, Identity federation

  An organization has 10000 employees. The organization wants to give restricted AWS access to each employee. How can the organization achieve this?

  A. Create an IAM user for each employee and make them a part of the group

  B. It is not recommended to support 10000 users with IAM

  C. Use STS and create the users run time

  **D. Use Identity federation with SSO**

  ***Explanation:*** [IAM and STS Limits](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_iam-limits.html). Users in an AWS account - 5000

  [Temporary Security Credentials](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_temp.html). You can provide access to your AWS resources to users without having to define an AWS identity for them. Temporary credentials are the basis for roles and identity federation.

  [Identity Providers and Federation](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers.html). If you already manage user identities outside of AWS, you can use IAM *identity providers* instead of creating IAM users in your AWS account. With an identity provider (IdP), you can manage your user identities outside of AWS and give these external user identities permissions to use AWS resources in your account.

  [Creating IAM Identity Providers](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_create.html). When you want to configure federation with an external identity provider (IdP) service, you create an IAM *identity provider* to inform AWS about the IdP and its configuration. This establishes "trust" between your AWS account and the IdP.

  [About Web Identity Federation](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_oidc.html).They can receive an authentication token, and then exchange that token for temporary security credentials in AWS that map to an IAM role with permissions to use the resources in your AWS account.

  If you don't use Amazon Cognito, then you must write code that interacts with a web IdP, such as Facebook, and then calls the `AssumeRoleWithWebIdentity` API to trade the authentication token you get from those IdPs for AWS temporary security credentials.

  [About SAML 2.0-based Federation](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_saml.html). This feature enables federated single sign-on (SSO), so users can log into the AWS Management Console or call the AWS API operations without you having to create an IAM user for everyone in your organization.

* SNS, user notification

  In Amazon SNS, to send push notifications to mobile devices using Amazon SNS and ADM, you need to obtain the following, except:

  A. Client secret

  **B. Client ID**

  C. Device token

  D. Registration ID

  ***Explanation:*** [How User Notifications Work](https://docs.aws.amazon.com/sns/latest/dg/sns-how-user-notifications-work.html). The difference is that Amazon SNS communicates using the push notification services in order for the subscribed mobile endpoints to receive push notification messages sent to the topic.

  [Prerequisites for Amazon SNS User Notifications](https://docs.aws.amazon.com/sns/latest/dg/sns-prerequisites-for-mobile-push-notifications.html). Generally speaking, you need the required credentials for connecting to the push notification service, a device token or registration ID (representing your mobile device and mobile app) received from the push notification service, and the mobile app registered with the push notification service.

* EC2, block device

  How many types of block devices does Amazon EC2 support?

  A. 5

  B. 1

  **C. 2**

  D. 4

  ***Explanation:*** [Block Device Mapping](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/block-device-mapping-concepts.html#block-device-mapping-def)

  Instance store volumes (virtual devices whose underlying hardware is physically attached to the host computer for the instance)

  EBS volumes (remote storage devices)

* Auto Scaling, terminate

  Auto Scaling is configured with 3 AZs. Each zone has 5 instances running. If Auto Scaling wants to terminate an instance based on the policy action, which instance will it terminate first?

  A. Terminate the first launched instance

  **B. Randomly select the instance for termination**

  C. Terminate the instance from the AZ which does not have a high AWS load

  D. Terminate the instance from the AZ which has instances running near to the billing hour

  ***Explanation:*** [Controlling Which Auto Scaling Instances Terminate During Scale In](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html)

* [Improving Data Access with Secondary Indexes](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/SecondaryIndexes.html)

  Global secondary indexes can be created at the same time that you create a table. You can also add a new global secondary index to an existing table, or delete an existing global secondary index.

  Local secondary indexes are created at the same time that you create a table. You cannot add a local secondary index to an existing table, nor can you delete any local secondary indexes that currently exist.

* VPC, scenario

  Can you SSH to your private machines that reside in a VPC from outside without elastic IP?

  **A. Yes, but only if you have direct connect or vpn**

  B. Only if you are using a non-US region

  C. Only if you are using a US region

  D. No

  ***Explanation:*** [What is AWS Site-to-Site VPN?](https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html). By default, instances that you launch into an Amazon VPC can't communicate with your own (remote) network. You can enable access to your remote network from your VPC by creating an AWS Site-to-Site VPN (Site-to-Site VPN) connection, and configuring routing to pass traffic through the connection.

  [VPC with Public and Private Subnets (NAT)](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Scenario2.html). The configuration for this scenario includes a virtual private cloud (VPC) with a public subnet and a private subnet.

  [VPC with a Private Subnet Only and AWS Site-to-Site VPN Access](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Scenario4.html). The configuration for this scenario includes a virtual private cloud (VPC) with a single private subnet, and a virtual private gateway to enable communication with your own network over an IPsec VPN tunnel.

* [Setting Up for Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_SettingUp.html#CHAP_SettingUp.Requirements)

  On Amazon RDS, a Multi-AZ deployment creates a primary DB instance and a secondary standby DB instance in another Availability Zone for failover support. We recommend Multi-AZ deployments for production workloads to maintain high availability. For development and test purposes, you can use a deployment that isn't Multi-AZ.

* [Working With Backups](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithAutomatedBackups.html)

  During the automatic backup window, storage I/O might be suspended briefly while the backup process initializes (typically under a few seconds). You might experience elevated latencies for a few minutes during backups for Multi-AZ deployments.

  If you don't specify a preferred backup window when you create the DB instance, Amazon RDS assigns a default 30-minute backup window. This window is selected at random from an 8-hour block of time for each AWS Region.

* DynamoDB, data type

  Which one of the following data types does Amazon DynamoDB not support?

  **A. Arrays**

  B. String

  C. Binary

  D. Number Set

  ***Explanation:*** [Data Types](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.NamingRulesDataTypes.html#HowItWorks.DataTypes)

* IAM, identity

  A corporate web application is deployed within an Amazon VPC, and is connected to the corporate data center via IPSec VPN. The application must authenticate against the on-premise LDAP server. Once authenticated, logged-in users can only access an S3 key space specific to the user. Which two approaches can satisfy the objectives? Choose 2 answers

  A. The application authenticates against LDAP. The application then calls the IAM Security Service to login to IAM using the LDAP credentials. The application can use the IAM temporary credentials to access the appropriate S3 bucket

  **B. The application authenticates against LDAP, and retrieves the name of an IAM role associated with the user. The application then calls the IAM Security Token Service to assume that IAM Role. The application can use the temporary credentials to access the appropriate S3 bucket**

  C. The application authenticates against IAM Security Token Service using the LDAP credentials. The application uses those temporary AWS security credentials to access the appropriate S3 bucket

  **D. Develop an identity broker which authenticates against LDAP, and then calls IAM Security Token Service to get IAM federated user credentials. The application calls the identity broker to get IAM federated user credentials with access to the appropriate S3 bucket**

  E. Develop an identity broker which authenticates against IAM Security Token Service to assume an IAM Role to get temporary AWS security credentials. The application calls the identity broker to get AWS temporary security credentials with access to the appropriate S3 bucket

  ***Explanation:*** Imagine that in your organization, you want to provide a way for users to copy data from their computers to a backup folder. You build an application that users can run on their computers. On the back end, the application reads and writes objects in an S3 bucket. Users don’t have direct access to AWS. Instead, the application communicates with an identity provider (IdP) to authenticate the user. The IdP gets the user information from your organization’s identity store (such as an LDAP directory) and then generates a SAML assertion that includes authentication and authorization information about that user. The application then uses that assertion to make a call to the `AssumeRoleWithSAML` API to get temporary security credentials. The app can then use those credentials to access a folder in the S3 bucket that’s specific to the user.

* CloudFormation, pseudo parameters

  Which of these is not a Pseudo Parameter in AWS CloudFormation?

  A. AWS::StackName

  B. AWS::AccountId

  **C. AWS::StackArn**

  D. AWS::NotificationARNs

  ***Explanation:*** [Pseudo Parameters Reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/pseudo-parameter-reference.html)

* S3, replication

  A Developer has created an S3 bucket s3://mycoolapp and has enabled server across logging that points to the folder s3://mycoolapp/logs. The Developer moved 100 KB of Cascading Style Sheets (CSS) documents to the folder s3://mycoolapp/css, and then stopped work. When the developer came back a few days later, the bucket was 50 GB. What is the MOST likely cause of this situation?

  A. The CSS files were not compressed and S3 versioning was enabled

  **B. S3 replication was enabled on the bucket**

  C. Logging into the same bucket caused exponential log growth

  D. An S3 lifecycle policy has moved the entire CSS file to S3 Infrequent Access

* SAM

  [Deploying Serverless Applications](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-deploying.html#serverless-sam-cli-using-package-and-deploy). After you develop and test your serverless application locally, you can deploy your application by using the `sam package` and `sam deploy` commands.

  Both the `sam package` and `sam deploy` commands described in this section are identical to their AWS CLI equivalent commands `aws cloudformation package` and `aws cloudformation deploy`, respectively.

  `package` - Packages the local artifacts (local paths) that your AWS CloudFormation template references. The command uploads local artifacts, such as source code for an AWS Lambda function or a Swagger file for an AWS API Gateway REST API, to an S3 bucket. The command returns a copy of your template, replacing references to local artifacts with the S3 location where the command uploaded the artifacts.

  Use this command to quickly upload local artifacts that might be required by your template. After you package your template's artifacts, run the deploy command to `deploy` the returned template.

  [Deploying Serverless Applications Gradually](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/automating-updates-to-serverless-apps.html). With just a few lines of configuration, AWS SAM does the following for you:

  Deploys new versions of your Lambda function, and automatically creates aliases that point to the new version.

  Gradually shifts customer traffic to the new version until you're satisfied that it's working as expected, or you roll back the update.

  Defines pre-traffic and post-traffic test functions to verify that the newly deployed code is configured correctly and your application operates as expected.

  Rolls back the deployment if CloudWatch alarms are triggered.

* Step Functions

  [What Is AWS Step Functions?](https://docs.aws.amazon.com/step-functions/latest/dg/welcome.html). Step Functions offers a graphical console to visualize the components of your application as a series of steps. It automatically triggers and tracks each step, and retries when there are errors, so your application executes in order and as expected, every time.

  [Creating a Step Functions State Machine That Uses Lambda](https://docs.aws.amazon.com/step-functions/latest/dg/tutorial-creating-lambda-state-machine.html). Lambda is well suited for implementing `Task` states, because Lambda functions are *stateless* (they have a predictable input-output relationship), easy to write, and don't require deploying code to a server instance.

* [In-Memory Acceleration with DynamoDB Accelerator (DAX)](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DAX.html)

  DAX is a DynamoDB-compatible caching service that enables you to benefit from fast in-memory performance for demanding applications.

* [AWS Lambda Function Scaling](https://docs.aws.amazon.com/lambda/latest/dg/invocation-scaling.html)

  As more events come in, Lambda routes them to available instances and creates new instances as needed. When the number of requests decreases, Lambda stops unused instances to free up scaling capacity for other functions.

* [Request Quotas for each AWS KMS API operation](https://docs.aws.amazon.com/kms/latest/developerguide/requests-per-second.html#rps-table)

* Lambda, log

  A Developer created a Lambda function for a web application backend. When testing the Lambda function from the AWS Lambda console, the Developer can see that the function is being executed, but there is no log data being generated in Amazon CloudWatch Logs, even after several minutes. What could cause this situation?

  A. The Lambda function does not have any explicit log statements for the log data to send it to CloudWatch Logs

  B. The Lambda function is missing CloudWatch Logs as a source trigger to send log data

  **C. The execution role for the Lambda function is missing permissions to write log data to the CloudWatch Logs**

  D. The Lambda function is missing a target CloudWatch Log group

  ***Explanation:*** [Monitoring and Troubleshooting Lambda Applications](https://docs.aws.amazon.com/lambda/latest/dg/lambda-monitoring.html). If your Lambda function code is executing, but you don't see any log data being generated after several minutes, this could mean that your execution role for the Lambda function didn't grant permissions to write log data to CloudWatch Logs.

* [How the Amazon SQS FIFO API Works](https://aws.amazon.com/blogs/developer/how-the-amazon-sqs-fifo-api-works/)

  Mix up a few different MessageGroupIds. This makes sense, for example, if you are tracking data from several different customers. The idea is if you use the customer ID as the MessageGroupId, the records for each customer will be delivered in order; there’s no particular ordering between records from different customers.

* [Using the Default Credential Provider Chain](https://docs.aws.amazon.com/sdk-for-java/v1/developer-guide/credentials.html)

* [Advanced environment customization with configuration files (`.ebextensions`)](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/ebextensions.html). You can add AWS Elastic Beanstalk configuration files (`.ebextensions`) to your web application's source code to configure your environment and customize the AWS resources that it contains. Configuration files are YAML- or JSON-formatted documents with a `.config` file extension that you place in a folder named `.ebextensions` and deploy in your application source bundle.

* DynamoDB, throughput

  Which option has the highest read throughput?

  A. Eventually consistent reads of 5 read capacity units reading items that are 4 KB in size

  B. Strongly consistent reads of 5 read capacity units reading items that are 4 KB in size

  **C. Eventually consistent reads of 15 read capacity units reading items that are 1 KB in size**

  D. Strongly consistent reads of15 read capacity units reading items that are 1 KB in size

  ***Explanation:*** 1 read capacity = 1 strongly consistent = 2 eventually consistent. Any item of 1KB and an item of 4KB will consume the same amount of RCU.

  A - 5 * 2 = 10 items; B - 5 items; C - 15 * 2 = 30 items; D - 15 items

* Lambda, layer

  A Developer is creating a Lambda function and will be using external libraries that are not included in the standard Lambda libraries. What action would minimize the Lambda compute time consumed?

  A. Install the dependencies and external libraries at the beginning of the Lambda function

  B. Create a Lambda deployment package that includes the external libraries

  C. Copy the external libraries to Amazon S3, and reference the external libraries to the S3 location

  **D. Install the external libraries in Lambda to be available to all Lambda functions**

  ***Explanation:*** [Best Practices for Working with AWS Lambda Functions](https://docs.aws.amazon.com/lambda/latest/dg/best-practices.html)

  **Minimize your deployment package size to its runtime necessities.** This will reduce the amount of time that it takes for your deployment package to be downloaded and unpacked ahead of invocation.

  **Reduce the time it takes Lambda to unpack deployment packages** authored in Java by putting your dependency `.jar` files in a separate /lib directory.

  [AWS Lambda Deployment Package in Java](https://docs.aws.amazon.com/lambda/latest/dg/java-package.html). To keep your deployment package size small, package your function's dependencies in layers. Layers let you manage your dependencies independently, can be used by multiple functions, and can be shared with other accounts.

  [AWS Lambda Layers](https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html). You can configure your Lambda function to pull in additional code and content in the form of layers. A layer is a ZIP archive that contains libraries, a custom runtime, or other dependencies. With layers, you can use libraries in your function without needing to include them in your deployment package.

* [Deployment policies and settings](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.rolling-version-deploy.html)

  **All at once** – Deploy the new version to all instances simultaneously. All instances in your environment are out of service for a short time while the deployment occurs.

  **Rolling** – Deploy the new version in batches. Each batch is taken out of service during the deployment phase, reducing your environment's capacity by the number of instances in a batch.

  **Rolling with additional batch** – Deploy the new version in batches, but first launch a new batch of instances to ensure full capacity during the deployment process.

  **Immutable** – Deploy the new version to a fresh group of instances by performing an immutable update.

* [GenerateDataKey](https://docs.aws.amazon.com/kms/latest/APIReference/API_GenerateDataKey.html). Generates a unique symmetric data key. This operation returns a plaintext copy of the data key and a copy that is encrypted under a customer master key (CMK) that you specify. You can use the plaintext key to encrypt your data outside of AWS KMS and store the encrypted data key with the encrypted data.

* [Retrieving Instance Metadata](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instancedata-data-retrieval.html)

  To view all categories of instance metadata from within a running instance, use the following URI.

  `http://169.254.169.254/latest/meta-data/`

  The IP address `169.254.169.254` is a link-local address and is valid only from the instance.

* Lambda, improve the performance

  The Lambda function below is being called through an API using Amazon API Gateway. The average execution time for the Lambda function is about 1 second. What two actions can be taken to improve the performance of this Lambda function without increasing the cost of the solution? (Select two)

  ```c
  include "3rd party encryption module"
  include "match module"
  lambda_handler(event, context)
      # Connect to the RDS Database
      # Perform some processing reading data from the RDS database
  ```

  **A. Package only the modules the Lambda function requires**

  B. Use Amazon DynamoDB instead of Amazon RDS

  **C. Move the initialization of the variable Amazon RDS connection outside of the handler function**

  **D. Implement custom database connection pooling with the Lambda function**

  **E. Implement local caching of Amazon RDS data so Lambda can re-use the cache**

  ***Explanation:***

  [AWS Lambda Execution Context](https://docs.aws.amazon.com/lambda/latest/dg/runtimes-context.html). The execution context is a temporary runtime environment that initializes any external dependencies of your Lambda function code, such as database connections or HTTP endpoints. This affords subsequent invocations better performance because there is no need to "cold-start" or initialize those external dependencies.

  Objects declared outside of the function's handler method remain initialized, providing additional optimization when the function is invoked again. For example, if your Lambda function establishes a database connection, instead of reestablishing the connection, the original connection is used in subsequent invocations. We suggest adding logic in your code to check if a connection exists before creating one.

  Each execution context provides 512 MB of additional disk space in the `/tmp` directory. The directory content remains when the execution context is frozen, providing transient cache that can be used for multiple invocations. You can add extra code to check if the cache has the data that you stored.

  [Best Practices for AWS Lambda Container Reuse](https://medium.com/capital-one-tech/best-practices-for-aws-lambda-container-reuse-6ec45c74b67e)

  [Using Amazon RDS Proxy with AWS Lambda](https://aws.amazon.com/blogs/compute/using-amazon-rds-proxy-with-aws-lambda/). Your Lambda functions interact with RDS Proxy instead of your database instance. It handles the connection pooling necessary for scaling many simultaneous connections created by concurrent Lambda functions. This allows your Lambda applications to reuse existing connections, rather than creating new connections for every function invocation.

  [Database Caching](https://aws.amazon.com/caching/database-caching/). The three most common types of database caches are the following:

  Database Integrated Caches: Some databases such as Amazon Aurora offer an integrated cache that is managed within the database engine and has built-in write-through capabilities. When the underlying data changes on the database table, the database updates its cache automatically, which is great.

  Local Caches: A local cache stores your frequently used data within your application. This not only speeds up your data retrieval but also removes network traffic associated with retrieving data, making data retrieval faster than other caching architectures.

  Remote caches: Remote caches are stored on dedicated servers and typically built upon key/value NoSQL stores such as Redis and Memcached. They provide hundreds of thousands to up-to a million requests per second per cache node.

* API Gateway, mapping template

  A legacy service has an XML-based SOAP interface. The Developer wants to expose the functionality of the service to external clients with the Amazon API Gateway. Which technique will accomplish this?

  **A. Create a RESTful API with the API Gateway; transform the incoming JSON into a valid XML message for the SOAP interface using mapping templates**

  B. Create a RESTful API with the API Gateway; pass the incoming JSON to the SOAP interface through an Application Load Balancer

  C. Create a RESTful API with the API Gateway; pass the incoming XML to the SOAP interface through an Application Load Balancer

  D. Create a RESTful API with the API Gateway; transform the incoming XML into a valid message for the SOAP interface using mapping templates

* CodeBuild, build details

  A company is using AWS CodeBuild to compile a website from source code stored in AWS CodeCommit. A recent change to the source code has resulted in the CodeBuild project being unable to successfully compile the website.How should the Developer identify the cause of the failures?

  A. Modify the buildspec.yml file to include steps to send the output of build commands to Amazon CloudWatch

  B. Use a custom Docker image that includes the AWS X-Ray agent in the AWS CodeBuild project configuration

  **C. Check the build logs of the failed phase in the last build attempt in the AWS CodeBuild project build history**

  D. Manually re-run the build process on a local machine so that the output can be visualized

* Lambda, limits

  A company has written a Java AWS Lambda function to be triggered whenever a user uploads an image to an Amazon S3 bucket. The function converts the original image to several different formats and then copies the resulting images to another Amazon S3 bucket. The Developers find that no images are being copied to the second Amazon S3 bucket. They have tested the code on an Amazon EC2 instance with 1GB of RAM, and it takes an average of 500 seconds to complete. What is the MOST likely cause of the problem?

  A. The Lambda function has insufficient memory and needs to be increased to 1 GB to match the Amazon EC2 instance

  B. Files need to be copied to the same Amazon S3 bucket for processing, so the second bucket needs to be deleted

  **C. Lambda functions have a maximum execution limit of 300 seconds, therefore the function is not completing**

  D. There is a problem with the Java runtime for Lambda, and the function needs to be converted to node.js

  ***Explanation:*** [AWS Lambda Limits](https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-limits.html). Function [timeout](https://docs.aws.amazon.com/lambda/latest/dg/configuration-console.html) - 900 seconds (15 minutes); Function [memory allocation](https://docs.aws.amazon.com/lambda/latest/dg/configuration-console.html) - 128 MB to 3,008 MB, in 64 MB increments.

* [Add a Manual Approval Action to a Pipeline in CodePipeline](https://docs.aws.amazon.com/codepipeline/latest/userguide/approvals-action-add.html). You can add an approval action to a stage in a CodePipeline pipeline at the point where you want the pipeline to stop so someone can manually approve or reject the action.

* AWS, legacy application

  You are tasked with moving a legacy application from a virtual machine running inside your datacenter to an Amazon VPC. Unfortunately this app requires access to a number of on-premises services and no one who configured the app still works for your company. Even worse there's no documentation for it. What will allow the application running inside the VPC to reach back and access its internal dependencies without being reconfigured? (Choose 3 answers)

  **A. An AWS Direct Connect link between the VPC and the network housing the internal services**

  B. An Internet Gateway to allow a VPN connection

  C. An Elastic IP address on the VPC instance

  **D. An IP address space that does not conflict with the one on-premises**

  **E. A VM Import of the current virtual machine**

  ***Explanation:*** A - correct, you could use this to have the instance you migrated into the VPC communicate back to the legacy on-premises servers. (You could also use a VPN instead of a circuit if you wanted).

  B - incorrect, virtual private gateway.

  C - incorrect, there is nothing in the question to indicate anything needs to communicate over the Internet.

  D - correct, you would totally need to make sure there were no private IP conflicts between your VPC CIDR and your internal on-premises networks if you wanted the instance in the VPC to talk to the legacy on-premises servers.

  E - correct, you would definitely want to leverage this in order to easily migrate the VM from on-premises to AWS.

* EC2, enhanced networking

  You have multiple Amazon EC2 instances running in a cluster across multiple Availability Zones within the same region. What combination of the following should be used to ensure the highest network performance (packets per second), lowest latency, and lowest jitter? Choose 3 answers

  A. Amazon EC2 placement groups

  **B. Enhanced networking**

  C. Amazon PV AMI

  **D. Amazon HVM AMI**

  E. Amazon Linux

  **F. Amazon VPC**

  ***Explanation:*** [Enhanced Networking](https://aws.amazon.com/ec2/features/). In order to take advantage of Enhanced Networking, you should launch an HVM AMI in VPC, and install the appropriate driver.

* EC2, placement group

  A group of researchers is studying the migration pattern of a beetle that eats and destroys gram. The researchers must process massive amounts of data and run statistics. Which one of the following options provides the high performance computing for this purpose?

  A. Configure an Autoscaling Scaling group to launch dozens of spot instances to run the statistical analysis simultaneously

  B. Launch AMI instances that support SR-IOV in a single Availability Zone

  C. Launch compute optimized (C4) instances in at least two Availability Zones

  **D. Launch enhanced network type instances in a placement group**

  ***Explanation:*** [Placement Groups](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html). *Cluster* – packs instances close together inside an Availability Zone. This strategy enables workloads to achieve the low-latency network performance necessary for tightly-coupled node-to-node communication that is typical of HPC(High Performance Computing) applications.

* CloudWatch, alarm

  A user is running a batch process on EBS backed EC2 instances. The batch process starts a few instances to process Hadoop Map reduce jobs, which can run between 500 - 600 minutes or sometimes for more time. The user wants to configure that the instance gets terminated only when the process is completed. How can the user configure this with CloudWatch?

  **A. Setup the CloudWatch action to terminate the instance when the CPU utilization is less than 5%**

  B. Setup the CloudWatch with Auto Scaling to terminate all the instances

  C. Setup a job which terminates all instances after 600 minutes

  D. It is not possible to terminate instances automatically

  ***Explanation:*** [Create Alarms to Stop, Terminate, Reboot, or Recover an Instance](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/UsingAlarmActions.html). Using Amazon CloudWatch alarm actions, you can create alarms that automatically stop, terminate, reboot, or recover your EC2 instances. You can use the stop or terminate actions to help you save money when you no longer need an instance to be running.

* CloudWatch, permission

  An AWS account owner has setup multiple IAM users. One IAM user only has CloudWatch access. He has setup the alarm action, which stops the EC2 instances when the CPU utilization is below the threshold limit. What will happen in this case?

  A. It is not possible stop the instance using the CloudWatch alarm

  B. CloudWatch will stop the instance when the action is executed

  C. The user cannot set an alarm on EC2 since he does not have the permission

  **D. The user can setup the action but it will not be executed if the user does not have EC2 rights**

  ***Explanation:*** [Create Alarms to Stop, Terminate, Reboot, or Recover an Instance](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/UsingAlarmActions.html). If you have read/write permissions for Amazon CloudWatch but not for Amazon EC2, you can still create an alarm but the stop or terminate actions aren't performed on the instance. However, if you are later granted permission to use the associated Amazon EC2 API actions, the alarm actions you created earlier are performed.

* IAM, access the AWS Management Console

  Your company has recently extended its datacenter into a VPC on AWS to add burst computing capacity as needed. Members of your Network Operations Center need to be able to go to the AWS Management Console and administer Amazon EC2 instances as necessary. You don't want to create new IAM users for each NOC member and make those users sign in again to the AWS Management Console. Which option below will meet the needs for your NOC members?

  A. Use OAuth 2.0 to retrieve temporary AWS security credentials to enable your NOC members to sign in to the AWS Management Console

  B. Use Web Identity Federation to retrieve AWS temporary security credentials to enable your NOC members to sign in to the AWS Management Console

  **C. Use your on-premises SAML 2.0-compliant identity provider (IDP) to grant the NOC members federated access to the AWS Management Console via the AWS single sign-on (SSO) endpoint**

  D. Use your on-premises SAML 2.0-compliant identity provider (IDP) to retrieve temporary security credentials to enable NOC members to sign in to the AWS Management Console

  ***Explanation:*** [Enabling SAML 2.0 Federated Users to Access the AWS Management Console](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_enable-console-saml.html). This specific use of SAML differs from the more general one illustrated at [About SAML 2.0-based Federation](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_saml.html) because this workflow opens the AWS Management Console on behalf of the user. This requires the use of the AWS SSO endpoint instead of directly calling the `AssumeRoleWithSAML` API. The endpoint calls the API for the user and returns a URL that automatically redirects the user's browser to the AWS Management Console.

* IAM, identity

  Your fortune 500 company has under taken a TCO analysis evaluating the use of Amazon S3 versus acquiring more hardware. The outcome was that all employees would be granted access to use Amazon S3 for storage of their personal documents. Which of the following will you need to consider so you can set up a solution that incorporates single sign-on from your corporate AD or LDAP directory and restricts access for each user to a designated user folder in a bucket? (Choose 3 Answers)

  **A. Setting up a federation proxy or identity provider**

  **B. Using AWS Security Token Service to generate temporary tokens Tagging each folder in the bucket**

  C. Tagging each folder in the bucket

  **D. Configuring IAM role**

  E. Setting up a matching IAM user for every user in your corporate directory that needs access to a folder in the bucket

* CloudWatch, RDS metrics

  You run a web application with the following components Elastic Load Balancer (ELB), 3 Web/Application servers, 1 MySQL RDS database with read replicas, and Amazon Simple Storage Service (Amazon S3) for static content. Average response time for users is increasing slowly. What three CloudWatch RDS metrics will allow you to identify if the database is the bottleneck? Choose 3 answers

  **A. The number of outstanding IOs waiting to access the disk**

  **B. The amount of write latency**

  C. The amount of disk space occupied by binary logs on the master

  D. The amount of time a Read Replica DB Instance lags behind the source DB Instance

  **E. The average number of disk I/O operations per second**

  ***Explanation:*** [Overview of Monitoring Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/MonitoringOverview.html). A - DiskQueueDepth; B - WriteLatency; C - BinLogDiskUsage; D - ReplicaLag; E - ReadIOPS / WriteIOPS.

  [Monitoring RDS MySQL performance metrics](https://www.datadoghq.com/blog/monitoring-rds-mysql-performance-metrics/)

  [Working with Read Replicas](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html). Amazon RDS then uses the asynchronous replication method for the DB engine to update the Read Replica whenever there is a change to the source DB instance.

* [Troubleshooting Applications on Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/APITroubleshooting.html). Typically, you want your application to check whether a request generated an error before you spend any time processing results. The easiest way to find out if an error occurred is to look for an `Error` node in the response from the Amazon RDS API.

* RDS, event notification

  A sys admin is planning to subscribe to the RDS event notifications. For which of the below mentioned source categories the subscription cannot be configured?

  A. DB security group

  B. DB snapshot

  **C. DB options group**

  D. DB parameter group

  ***Explanation:*** [Using Amazon RDS Event Notification](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Events.html). Amazon RDS groups these events into categories that you can subscribe to so that you can be notified when an event in that category occurs. You can subscribe to an event category for a DB instance, DB snapshot, DB parameter group, or DB security group. 

  You can easily turn off notification without deleting a subscription by choosing **No** for **Enabled** in the Amazon RDS console or by setting the `Enabled` parameter to `false` using the AWS CLI or Amazon RDS API.

* RDS, Oracle Database license

  What is the name of licensing model in which I can use your existing Oracle Database licenses to run Oracle deployments on Amazon RDS?

  **A. Bring Your Own License**

  B. Role Bases License

  C. Enterprise License

  D. License Included

  ***Explanation:*** [What types of licensing options are available with Amazon RDS for Oracle?](https://aws.amazon.com/rds/oracle/faqs/)

* RDS, data transfer pricing

  What is the minimum charge for the data transferred between Amazon RDS and Amazon EC2 Instances in the same Availability Zone?

  A. USD 0.10 per GB

  **B. No charge. It is free**

  C. USD 0.02 per GB

  D. USD 0.01 per GB

  ***Explanation:*** [Data Transfer](https://aws.amazon.com/rds/mysql/pricing/). Data transferred between Amazon RDS and Amazon EC2 Instances in the same Availability Zone is free.

* RDS, access

  Does Amazon RDS allow direct host access via Telnet, Secure Shell (SSH), or Windows Remote Desktop Connection?

  A. Yes

  **B. No**

  C. Depends on if it is in VPC or not

  ***Explanation:*** [Amazon RDS DB Instances](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.DBInstance.html). Amazon RDS supports access to databases using any standard SQL client application. Amazon RDS does not allow direct host access.

* [Q: What are the different delivery formats/transports for receiving notifications?](https://aws.amazon.com/sns/faqs/)

* [CodeDeploy AppSpec File Reference](https://docs.aws.amazon.com/codedeploy/latest/userguide/reference-appspec-file.html#appspec-reference-server). An AppSpec file must be a YAML-formatted file named `appspec.yml` and it must be placed in the root of the directory structure of an application's source code. Otherwise, deployments fail.

* [Tutorial: Using AWS Lambda with Amazon S3](https://docs.aws.amazon.com/lambda/latest/dg/with-s3-example.html). Suppose you want to create a thumbnail for each image file that is uploaded to a bucket. You can create a Lambda function (`CreateThumbnail`) that Amazon S3 can invoke when objects are created. Then, the Lambda function can read the image object from the source bucket and create a thumbnail image target bucket.

* API Gateway, Swagger

  A Developer must repeatedly and consistently deploy a serverless RESTful API on AWS. Which techniques will work? (Choose two)

  A. Define a Swagger file. Use AWS Elastic Beanstalk to deploy the Swagger file

  B. Define a Swagger file. Use AWS CodeDeploy to deploy the Swagger file

  **C. Deploy a SAM template with an inline Swagger definition**

  **D. Define a Swagger file. Deploy a SAM template that references the Swagger file**

  E. Define an inline Swagger definition in a Lambda function. Invoke the Lambda function

  ***Explanation:*** [How to deploy a Swagger specification to Amazon API Gateway using CloudFormation](https://sookocheff.com/post/api/deploying-swagger-to-api-gateway/). Amazon’s API Gateway supports the direct importing of Swagger specification files using CloudFormation rules. To do this, you have two choices. Injecting the `swagger.json` or `swagger.yaml` file directly into the `Body` field of the CloudFormation template, or uploading the `swagger.json` or `swagger.yaml` file to an S3 location and setting that location as the `BodyS3Location` field of the CloudFormation template.

* [AWS Systems Manager Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html). AWS Systems Manager Parameter Store provides secure, hierarchical storage for configuration data management and secrets management. You can store data such as passwords, database strings, Amazon EC2 instance IDs, Amazon Machine Image (AMI) IDs, and license codes as parameter values. You can store values as plain text or encrypted data. You can reference Systems Manager parameters in your scripts, commands, SSM documents, and configuration and automation workflows by using the unique name that you specified when you created the parameter.

* [Enabling API Caching to Enhance Responsiveness](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-caching.html). A client of your API can invalidate an existing cache entry and reload it from the integration endpoint for individual requests. The client must send a request that contains the `Cache-Control: max-age=0` header. The client receives the response directly from the integration endpoint instead of the cache, provided that the client is authorized to do so. This replaces the existing cache entry with the new response, which is fetched from the integration endpoint.

* S3, HTTPS

  An application running on EC2 instances is storing data in an S3 bucket. Security policy mandates that all data must be encrypted in transit. How can the Developer ensure that all traffic to the S3 bucket is encrypted?

  A. Install certificates on the EC2 instances

  B. Create a bucket policy that allows traffic where SecureTransport is true

  C. Create an HTTPS redirect on the EC2 instances

  **D. Create a bucket policy that denies traffic where SecureTransport is false**

  ***Explanation:*** [How to Use Bucket Policies and Apply Defense-in-Depth to Help Secure Your Amazon S3 Data](https://aws.amazon.com/blogs/security/how-to-use-bucket-policies-and-apply-defense-in-depth-to-help-secure-your-amazon-s3-data/)

* ECS

  A company is developing a new online game that will run on top of Amazon ECS. Four distinct Amazon ECS services will be part of the architecture, each requiring specific permissions to various AWS services. The company wants to optimize the use of the underlying Amazon EC2 instances by bin packing the containers based on memory reservation. Which configuration would allow the Development team to meet these requirements MOST securely?

  A. Create a new Identity and Access Management (IAM) instance profile containing the required permissions for the various ECS services, then associate that instance role with the underlying EC2 instances

  B. Create four distinct IAM roles, each containing the required permissions for the associated ECS service, then configure each ECS service to reference the associated IAM role

  C. Create four distinct IAM roles, each containing the required permissions for the associated ECS service, then, create an IAM group and configure the ECS cluster to reference that group

  **D. Create four distinct IAM roles, each containing the required permissions for the associated ECS service, then configure each ECS task definition to reference the associated IAM role**

  ***Explanation:*** [Help Secure Container-Enabled Applications with IAM Roles for ECS Tasks](https://aws.amazon.com/blogs/compute/help-secure-container-enabled-applications-with-iam-roles-for-ecs-tasks/). With the introduction of the newly-launched IAM roles for ECS tasks, you can now secure your infrastructure further by assigning an IAM role directly to the ECS task rather than to the EC2 container instance. This way, you can have one task that uses a specific IAM role for access to S3 and one task that uses an IAM role to access a DynamoDB table.

  [Amazon ECS Task Definitions](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definitions.html)

* S3, SSE

  A company needs to encrypt data at rest, but it wants to leverage an AWS managed service using its own master key. Which of the following AWS service can be used to meet these requirements?

  A. SSE with Amazon S3

  **B. SSE with AWS KMS**

  C. Client-side encryption

  D. AWS IAM roles and policies

  ***Explanation:*** [Protecting Data Using Server-Side Encryption](https://docs.aws.amazon.com/AmazonS3/latest/dev/serv-side-encryption.html). You have three mutually exclusive options, depending on how you choose to manage the encryption keys.

  **Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3)**. When you use Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3), each object is encrypted with a unique key. As an additional safeguard, it encrypts the key itself with a master key that it regularly rotates.

  SSE-S3 requires that Amazon S3 manage the data and master encryption keys.

  **Server-Side Encryption with Customer Master Keys (CMKs) Stored in AWS Key Management Service (SSE-KMS)**. Additionally, you can create and manage customer managed CMKs or use AWS managed CMKs that are unique to you, your service, and your Region.

  SSE-KMS requires that AWS manage the data key but you manage the [customer master key](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#master_keys) (CMK) in AWS KMS.

  **Server-Side Encryption with Customer-Provided Keys (SSE-C)**. With Server-Side Encryption with Customer-Provided Keys (SSE-C), you manage the encryption keys and Amazon S3 manages the encryption, as it writes to disks, and decryption, when you access your objects. 

  SSE-C requires that you manage the encryption key.

* DynamoDB Streams

  A Developer must trigger an AWS Lambda function based on the item lifecycle activity in an Amazon DynamoDB table. How can the Developer create the solution?

  A. Enable a DynamoDB stream that publishes an Amazon SNS message. Trigger the Lambda function synchronously from the SNS message

  B. Enable a DynamoDB stream that publishes an SNS message. Trigger the Lambda function asynchronously from the SNS message

  **C. Enable a DynamoDB stream, and trigger the Lambda function synchronously from the stream**

  D. Enable a DynamoDB stream, and trigger the Lambda function asynchronously from the stream

  ***Explanation:*** [DynamoDB Streams and AWS Lambda Triggers](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.Lambda.html). Amazon DynamoDB is integrated with AWS Lambda so that you can create *triggers*—pieces of code that automatically respond to events in DynamoDB Streams. With triggers, you can build applications that react to data modifications in DynamoDB tables.

  If you enable DynamoDB Streams on a table, you can associate the stream Amazon Resource Name (ARN) with an AWS Lambda function that you write. Immediately after an item in the table is modified, a new record appears in the table's stream. AWS Lambda polls the stream and invokes your Lambda function synchronously when it detects new stream records.

*  Cognito

  A social media company is using Amazon Cognito in order to synchronize profiles across different mobile devices, to enable end users to have a seamless experience. Which of the following configurations can be used to silently notify users whenever an update is available on all other devices?

  A. Modify the user pool to include all the devices which keep them in sync

  B. Use the SyncCallback interface to receive notifications on the application

  C. Use an Amazon Cognito stream to analyze the data and push the notifications

  **D. Use the push synchronization feature with the appropriate IAM role**

  ***Explanation:*** [Push Sync](https://docs.aws.amazon.com/cognito/latest/developerguide/push-sync.html). Amazon Cognito automatically tracks the association between identity and devices. Using the push synchronization, or push sync feature, you can ensure that every instance of a given identity is notified when identity data changes. Push sync ensures that, whenever the sync store data changes for a particular identity, all devices associated with that identity receive a silent push notification informing them of the change.

* [Caching Strategies](https://docs.aws.amazon.com/AmazonElastiCache/latest/mem-ug/Strategies.html). cache-aside = lazy loading

* CloudFront, encryption in transit

  An organization is using Amazon CloudFront to ensure that its users experience low-latency access to its web application. The organization has identified a need to encrypt all traffic between users and CloudFront, and all traffic between CloudFront and the web application. How can these requirements be met? (Choose two)

  A. Use AWS KMS to encrypt traffic between CloudFront and the web application

  **B. Set the Origin Protocol Policy to "HTTPS Only"**

  C. Set the Origin's HTTP Port to 443

  **D. Set the Viewer Protocol Policy to "HTTPS Only" or "Redirect HTTP to HTTPS"**

  E. Enable the CloudFront option Restrict Viewer Access

  ***Explanation:*** [Encryption in Transit](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/data-protection-summary.html#data-protection-summary-encryption-in-transit)

  [Requiring HTTPS for Communication Between Viewers and CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-https-viewers-to-cloudfront.html)

  [Requiring HTTPS for Communication Between CloudFront and Your Custom Origin](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-https-cloudfront-to-custom-origin.html)

* DynamoDB

  Queries to an Amazon DynamoDB table are consuming a large amount of read capacity. The table has a significant number of large attributes. The application does not need all of the attribute data. How can DynamoDB costs be minimized while maximizing application performance?

  A. Batch all the writes, and perform the write operations when no or few reads are being performed

  **B. Create a global secondary index with a minimum set of projected attributes**

  C. Implement exponential backoffs in the application

  D. Load balance the reads to the table using an Application Load Balancer

* ECR, login

  AWS CodeBuild builds code for an application, creates the Docker image, pushes the image to Amazon Elastic Container Registry (Amazon ECR), and tags the image with a unique identifier. If the Developers already have AWS CLI configured on their workstations, how can the Docker images be pulled to the workstations?

  A. Run the following: docker pull REPOSITORY URI : TAG

  **B. Run the output of the following: aws ecr get-login and then run: docker pull REPOSITORY URI : TAG**

  C. Run the following: aws ecr get-login and then run: docker pull REPOSITORY URI : TAG

  D. Run the output of the following: aws ecr get-download-url-for-layer and then run: docker pull REPOSITORY URI : TAG

  ***Explanation:*** [get-login](https://docs.aws.amazon.com/cli/latest/reference/ecr/get-login.html). This command retrieves a token that is valid for a specified registry for 12 hours, and then it prints a `docker login` command with that authorization token. You can execute the printed command to log in to your registry with Docker. After you have logged in to an Amazon ECR registry with this command, you can use the Docker CLI to push and pull images from that registry until the token expires.

* DynamoDB, TTL

  A company caches session information for a web application in an Amazon DynamoDB table. The company wants an automated way to delete old items from the table. What is the simplest way to do this?

  A. Write a script that deletes old records; schedule the scripts as a cron job on an Amazon EC2 instance

  **B. Add an attribute with the expiration time; enable the Time To Live feature based on that attribute**

  C. Each day, create a new table to hold session data; delete the previous day's table

  D. Add an attribute with the expiration time; name the attribute ItemExpiration

  ***Explanation:*** [Expiring Items Using Time to Live (TTL)](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/TTL.html). Time to Live (TTL) for Amazon DynamoDB lets you define when items in a table expire so that they can be automatically deleted from the database.

* [Using AWS CLI Pagination Options](https://docs.aws.amazon.com/cli/latest/userguide/cli-usage-pagination.html)

* KMS

  An application running on Amazon EC2 instances must access objects within an Amazon S3 bucket that are encrypted using server-side encryption using AWS KMS encryption keys (SSE-KMS). The application must have access to the customer master key (CMK) to decrypt the objects. Which combination of steps will grant the application access? (Select TWO)

  A. Write an S3 bucket policy that grants the bucket access to the key

  **B. Grant access to the key in the IAM EC2 role attached to the application's EC2 instances**

  **C. Write a key policy that enables IAM policies to grant access to the key**

  D. Grant access to the key in the S3 bucket's ACL

  E. Create a Systems Manager parameter that exposes the KMS key to the EC2 instances

  ***Explanation:*** [How to use KMS and IAM to enable independent security controls for encrypted data in S3](https://aws.amazon.com/blogs/security/how-to-use-kms-and-iam-to-enable-independent-security-controls-for-encrypted-data-in-s3/)

* X-Ray, ECS

  A Developer wants to enable AWS X-Ray for a secure application that runs in an Amazon ECS environment. What combination of steps will enable X-Ray? (Select THREE)

  **A. Create a Docker image that runs the X-Ray daemon**

  **B. Add instrumentation to the application code for X-Ray**

  C. Install the X-Ray daemon on the underlying EC2 instance

  D. Configure and use an IAM EC2 instance role

  E. Register the application with X-Ray

  **F. Configure and use an IAM role for tasks**

  ***Explanation:*** [Running the X-Ray daemon on Amazon ECS](https://docs.aws.amazon.com/xray/latest/devguide/xray-daemon-ecs.html). In Amazon ECS, create a Docker image that runs the X-Ray daemon, upload it to a Docker image repository, and then deploy it to your Amazon ECS cluster. You can use port mappings and network mode settings in your task definition file to allow your application to communicate with the daemon container.

  [AWS X-Ray use cases and requirements](https://docs.aws.amazon.com/xray/latest/devguide/xray-usage.html). To instrument your application code, you use the **X-Ray SDK**. The SDK records data about incoming and outgoing requests and sends it to the X-Ray daemon, which relays the data in batches to X-Ray.

* [AWS::Lambda::Function Code](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lambda-function-code.html). Changes to a deployment package in Amazon S3 are not detected automatically during stack updates. To update the function code, change the object key or version in the template.

* [Amazon SQS Quotas](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-quotas.html). Message size.

  The minimum message size is 1 byte (1 character). The maximum is 262,144 bytes (256 KB).

  To send messages larger than 256 KB, you can use the [Amazon SQS Extended Client Library for Java](https://github.com/awslabs/amazon-sqs-java-extended-client-lib). This library allows you to send an Amazon SQS message that contains a reference to a message payload in Amazon S3. The maximum payload size is 2 GB.

* [How do I give internet access to my Lambda function in a VPC?](https://aws.amazon.com/premiumsupport/knowledge-center/internet-access-lambda-function/)

* Kinesis Data Streams, Lambda

  A Developer is creating an AWS Lambda function to process a stream of data from an Amazon Kinesis Data Stream. When the Lambda function parses the data and encounters a missing field, it exits the function with an error. The function is generating duplicate records from the Kinesis stream. When the Developer looks at the stream output without the Lambda function, there are no duplicate records. What is the reason for the duplicates?

  A. The Lambda function did not advance the Kinesis stream pointer to the next record after the error

  B. The Lambda event source used asynchronous invocation, resulting in duplicate records

  **C. The Lambda function did not handle the error, and the Lambda service attempted to reprocess the data**

  D. The Lambda function is not keeping up with the amount of data coming from the stream

  ***Explanation:*** [Handling Duplicate Records](https://docs.aws.amazon.com/streams/latest/dev/kinesis-record-processor-duplicates.html). There are two primary reasons why records may be delivered more than one time to your Amazon Kinesis Data Streams application: producer retries and consumer retries.

  Consider a producer that experiences a network-related timeout after it makes a call to `PutRecord`, but before it can receive an acknowledgement from Amazon Kinesis Data Streams.

  Consumer (data processing application) retries happen when record processors restart.

  [Error Handling](https://docs.aws.amazon.com/lambda/latest/dg/with-kinesis.html#services-kinesis-errors). If the function receives the records but returns an error, Lambda retries until the records in the batch expire, exceed the maximum age, or reach the configured retry limit.

* [Using Instance Profiles](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_switch-role-ec2_instance-profiles.html). An instance profile is a container for an IAM role that you can use to pass role information to an EC2 instance when the instance starts.

* Cognito, user pools and identity pools

  A company is creating an application that will require users to access AWS services and allow them to reset their own passwords. Which of the following would allow the company to manage users and authorization while allowing users to reset their own passwords?

  A. Amazon Cognito identify pools and AWS STS

  B. Amazon Cognito identity pools and AWS IAM

  C. Amazon Cognito user pools and AWS KMS

  **D. Amazon Cognito user pools and identity pools**

  ***Explanation:*** [Cognito User Pool vs Identity Pool](https://serverless-stack.com/chapters/cognito-user-pool-vs-identity-pool.html). [What's the difference between Amazon Cognito user pools and identity pools?](https://aws.amazon.com/premiumsupport/knowledge-center/cognito-user-pools-identity-pools/)

* CodeDeploy, deployment groups

  A company has three different environments: Development, QA, and Production. The company wants to deploy its code first in the Development environment, then QA, and then Production. Which AWS service can be used to meet this requirement?

  A. Use AWS CodeCommit to create multiple repositories to deploy the application

  B. Use AWS CodeBuild to create, configure, and deploy multiple build application projects

  C. Use AWS Data Pipeline to create multiple data pipeline provisions to deploy the application

  **D. Use AWS CodeDeploy to create multiple deployment groups**

  ***Explanation:*** [Working with Deployment Groups in CodeDeploy](https://docs.aws.amazon.com/codedeploy/latest/userguide/deployment-groups.html#deployment-group-server). You can associate more than one deployment group with an application in CodeDeploy. This makes it possible to deploy an application revision to different sets of instances at different times. For example, you might use one deployment group to deploy an application revision to a set of instances tagged `Test` where you ensure the quality of the code. Next, you deploy the same application revision to a deployment group with instances tagged `Staging` for additional verification. Finally, when you are ready to release the latest application to customers, you deploy to a deployment group that includes instances tagged `Production`.

  [What is AWS Data Pipeline?](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/what-is-datapipeline.html). AWS Data Pipeline is a web service that you can use to automate the movement and transformation of data.

* CloudWatch

  A Development team has pushed out 10 applications running on several Amazon EC2 instances. The Operations team is asking for a graphical representation of one key performance metric for each application. These metrics should be available on one screen for easy monitoring. Which steps should the Developer take to accomplish this using Amazon CloudWatch?

  **A. Create a custom namespace with a unique metric name for each application**

  B. Create a custom dimension with a unique metric name for each application

  C. Create a custom event with a unique metric name for each application

  D. Create a custom alarm with a unique metric name for each application

  ***Explanation:*** [Amazon CloudWatch Concepts](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html)

  A *namespace* is a container for CloudWatch metrics.

  *Metrics* are the fundamental concept in CloudWatch. A metric represents a time-ordered set of data points that are published to CloudWatch. Think of a metric as a variable to monitor, and the data points as representing the values of that variable over time.

  A *dimension* is a name/value pair that is part of the identity of a metric. You can assign up to 10 dimensions to a metric.

  You can use an *alarm* to automatically initiate actions on your behalf. An alarm watches a single metric over a specified time period, and performs one or more specified actions, based on the value of the metric relative to a threshold over time.

* [Set Up API Keys Using the API Gateway Console](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-setup-api-key-with-console.html). To set up API keys, do the following: Configure API methods to require an API key. Create or import an API key for the API in a region.

* [How are compute resources assigned to an AWS Lambda function?](https://aws.amazon.com/lambda/faqs/). In the AWS Lambda resource model, you choose the amount of memory you want for your function, and are allocated proportional CPU power and other resources. For example, choosing 256MB of memory allocates approximately twice as much CPU power to your Lambda function as requesting 128MB of memory and half as much CPU power as choosing 512MB of memory.

* SAM

  To include objects defined by the AWS Serverless Application Model (SAM) in an AWS CloudFormation template, in addition to Resources, what section MUST be included in the document root?

  A. Conditions

  B. Globals

  **C. Transform**

  D. Properties

  [AWS SAM Template Anatomy](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/sam-specification-template-anatomy.html). Templates include several major sections. `Transform` and `Resources` are the only required sections.

* 

