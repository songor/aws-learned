# AWS Certification Exam Mistake Collection

* S3, version

  A user has not enabled versioning on an S3 bucket. What will be the version ID of the object inside that bucket?

  A. 0

  B. There will be no version attached

  **C. Null**

  D. Blank

* SQS, delete queue

  A user has created a queue named "myqueue" with SQS. There are four messages published to queue which are not received by the consumer yet. If the user tries to delete the queue, what will happen?

  A. A user can never delete a queue manually. AWS deletes it after 30 days of inactivity on queue

  B. It will initiate the delete but wait for four days before deleting until all messages are deleted automatically.

  C. It will ask user to delete the messages first

  **D. It will delete the queue**

* EC2, secondary IP address

  An organization has launched two applications: one for blogging and one for ECM on the same AWS Linux EC2 instance running in the AWS VPC. The organization has attached two private IPs (primary and secondary) to the above mentioned instance. The organization wants the instance OS to recognize the secondary IP address. How can the organization configure this?

  A. Use the ec2-net-utility package which updates routing tables, uses DHCP to refresh the secondary IP and adds the network interface.

  **B. Use the ec2-net-utils package which will configure an additional network interface and update the routing table**

  C. Use the ec2-ip-update package which can configure the network interface as well as update the secondary IP with DHCP

  D. Use the ec2-ip-utility package which can update the routing tables as well as refresh the secondary IP using DHCP

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

  Explanation: [Easier way to control access to AWS regions using IAM policies](https://aws.amazon.com/cn/blogs/security/easier-way-to-control-access-to-aws-regions-using-iam-policies/)

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

  Explanation: The user can authorize an IP range or specify an Amazon EC2 security group in the same region that refers to an IP address in another region.

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

  Explanation: https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/applications-sourcebundle.html

* S3, static website

  A user has configured a bucket S3 to host a static website. What difference will there be when static website hosting is enabled?

  A. It will help the user identify this bucket as the website root to map with the domain

  B. It will create a new version of the bucket

  C. It will not make any difference, but will help the user to configure the error page

  **D. It will provide the region specific website endpoint**

* SQS, visibility timeout

  How does Amazon SQS allow multiple readers to access the same message queue without losing messages or processing them many times?

  A. By identifying a user by his unique id

  B. By using unique cryptography

  **C. Amazon SQS queue has a configurable visibility timeout**

  D. Multiple readers can't access the same message queue

* DynamoDB, secondary index

  In DynamoDB, a secondary index is a data structure that contains a subset of attributes from a table, along with an alternate key to support ________ operations.

  A. None of the above

  B. Both

  **C. Query**

  D. Scan

* 