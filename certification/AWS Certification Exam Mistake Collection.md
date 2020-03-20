# AWS Certification Exam Mistake Collection

* S3, version

  A user has not enabled versioning on an S3 bucket. What will be the version ID of the object inside that bucket?

  A. 0

  B. There will be no version attached

  **C. Null**

  D. Blank

  *Explanation:* [Adding Objects to Versioning-Suspended Buckets](https://docs.aws.amazon.com/AmazonS3/latest/dev/AddingObjectstoVersionSuspendedBuckets.html). Once you suspend versioning on a bucket, Amazon S3 automatically adds a `null` version ID to every subsequent object stored thereafter (using `PUT`, `POST`, or `COPY`) in that bucket.

* SQS, delete queue

  A user has created a queue named "myqueue" with SQS. There are four messages published to queue which are not received by the consumer yet. If the user tries to delete the queue, what will happen?

  A. A user can never delete a queue manually. AWS deletes it after 30 days of inactivity on queue

  B. It will initiate the delete but wait for four days before deleting until all messages are deleted automatically.

  C. It will ask user to delete the messages first

  **D. It will delete the queue**

  *Explanation:* [DeleteQueue](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/API_DeleteQueue.html). Be careful with the `DeleteQueue` action: When you delete a queue, any messages in the queue are no longer available.

* EC2, secondary IP address

  An organization has launched two applications: one for blogging and one for ECM on the same AWS Linux EC2 instance running in the AWS VPC. The organization has attached two private IPs (primary and secondary) to the above mentioned instance. The organization wants the instance OS to recognize the secondary IP address. How can the organization configure this?

  A. Use the ec2-net-utility package which updates routing tables, uses DHCP to refresh the secondary IP and adds the network interface.

  **B. Use the ec2-net-utils package which will configure an additional network interface and update the routing table**

  C. Use the ec2-ip-update package which can configure the network interface as well as update the secondary IP with DHCP

  D. Use the ec2-ip-utility package which can update the routing tables as well as refresh the secondary IP using DHCP

  *Explanation:* [Multiple IP Addresses](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/MultipleIP.html). After you assign a secondary private IPv4 address to your instance, you need to configure the operating system on your instance to recognize the secondary private IP address. If you are using Amazon Linux, the ec2-net-utils package can take care of this step for you. It configures additional network interfaces that you attach while the instance is running, refreshes secondary IPv4 addresses during DHCP lease renewal, and updates the related routing rules.

* SQS, messages kept default

  How long are the messages kept on an SQS queue by default?

  A. If a message is not read, it is never deleted

  B. 2 weeks

  C. 1 day

  **D. 4 days**

* IAM, region

  An account owner has created an IAM user with the name examkiller. The account owner wants to give EC2 access of only the US West region to that IAM user. How can the owner configure this?

  A. While creating a policy provide the region as a part of the resources

  B. Create an IAM user in the US West region and give access to EC2

  **C. Create an IAM policy and define the region in the condition**

  D. It is not possible to provide access based on the region

  *Explanation:* [Easier way to control access to AWS regions using IAM policies](https://aws.amazon.com/cn/blogs/security/easier-way-to-control-access-to-aws-regions-using-iam-policies/)

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

  *Explanation:* [Working with DB Security Groups (EC2-Classic Platform)](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithSecurityGroups.html). You can't authorize an EC2-Classic security group that is in a different AWS Region than your DB instance. You can authorize an IP range, or specify an EC2-Classic security group in the same AWS Region that refers to IP address in another AWS Region.

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

  *Explanation:* [Create an application source bundle](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/applications-sourcebundle.html). Consist of a single `ZIP` file or `WAR` file (you can include multiple `WAR` files inside your `ZIP` file)

* S3, static website

  A user has configured a bucket S3 to host a static website. What difference will there be when static website hosting is enabled?

  A. It will help the user identify this bucket as the website root to map with the domain

  B. It will create a new version of the bucket

  C. It will not make any difference, but will help the user to configure the error page

  **D. It will provide the region specific website endpoint**

  *Explanation:* [Hosting a Static Website on Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html). After you configure your bucket as a static website, you can access the bucket through the AWS Region-specific Amazon S3 website endpoints for your bucket.

* SQS, visibility timeout

  How does Amazon SQS allow multiple readers to access the same message queue without losing messages or processing them many times?

  A. By identifying a user by his unique id

  B. By using unique cryptography

  **C. Amazon SQS queue has a configurable visibility timeout**

  D. Multiple readers can't access the same message queue

  *Explanation:* [Amazon SQS Visibility Timeout](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-visibility-timeout.html). To prevent other consumers from processing the message again, Amazon SQS sets a *visibility timeout*, a period of time during which Amazon SQS prevents other consumers from receiving and processing the message. The default visibility timeout for a message is 30 seconds. The minimum is 0 seconds. The maximum is 12 hours.

* DynamoDB, secondary index

  In DynamoDB, a secondary index is a data structure that contains a subset of attributes from a table, along with an alternate key to support ________ operations.

  A. None of the above

  B. Both

  **C. Query**

  D. Scan

  *Explanation:* [Improving Data Access with Secondary Indexes](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/SecondaryIndexes.html). A *secondary index* is a data structure that contains a subset of attributes from a table, along with an alternate key to support `Query` operations.

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

  *Explanation:* [Amazon Simple Queue Service Developer Guide](https://s3.cn-north-1.amazonaws.com.cn/aws-dam-prod/china/pdf/sqs-dg.pdf). Amazon SQS can delete your queue without notification if one of the following actions hasn't been performed on it for 30 consecutive days: SendMessage, ReceiveMessage, DeleteMessage, GetQueueAttributes, SetQueueAttributes, AddPermission, and RemovePermission.

* AMI, share

  Which of the below mentioned commands allows the user to share the AMI with his peers using the AWS EC2 CLI?

  A. ec2-share-image-public

  B. ec2-share-image-account

  C. ec2-share-image

  **D. ec2-modify-image-attribute**

  *Explanation:* [Sharing an AMI with Specific AWS Accounts](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/sharingamis-explicit.html). You can share an AMI with specific AWS accounts without making the AMI public. All you need is the AWS account IDs.

* EBS, snapshot

  A user has created a new EBS volume from an existing snapshot. The user mounts the volume on the instance to which it is attached. Which of the below mentioned options is a required step before the user can mount the volume?

  A. Run a cyclic check on the device for data consistency

  B. Create the file system of the volume

  C. Resize the volume as per the original snapshot size

  **D. No step is required. The user can directly mount the device**

  *Explanation:* [Amazon EBS Snapshots](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html). When you create an EBS volume based on a snapshot, the new volume begins as an exact replica of the original volume that was used to create the snapshot. The replicated volume loads data in the background so that you can begin using it immediately.

  [Making an Amazon EBS Volume Available for Use on Linux](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-using-volumes.html). After you attach an Amazon EBS volume to your instance, it is exposed as a block device. You can format the volume with any file system and then mount it.

* ELB, custom domain name

  Can a user associate and use his own DNS with ELB instead of the DNS provided by AWS ELB?

  **A. Yes, by creating a CNAME with the existing domain name provider**

  B. Yes, by configuring DNS in the AWS Console

  C. No

  D. Yes, only through Route 53 by mapping ELB and DNS

  *Explanation:* [Configure a Custom Domain Name for Your Classic Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/using-domain-names-with-elb.html)

* SWF, worker

  In relation to Amazon Simple Workflow Service(Amazon SWF), what is an "Activity Worker"?

  A. An individual task undertaken by a workflow

  B. The automation of a business process

  **C. A piece of software that implements tasks**

  D. All answers listed are correct

  *Explanation:* [Introduction to Amazon SWF](https://docs.aws.amazon.com/amazonswf/latest/developerguide/swf-dg-intro-to-swf.html). An *activity worker* is a program that receives activity tasks, performs them, and provides results back.

* 