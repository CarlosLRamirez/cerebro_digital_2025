---
created: 2024-12-30T20:43:44
modified: '"2024-12-30 20:44", "1tc/G12T+6"'
type: 
aliases: 
tags:
  - AWS
---


# AWS Certified Solution Architect - My study Notes


[00-Exam Guide (BluePrint) - SAA-CA02](00-Exam%20Guide%20(BluePrint)%20-%20SAA-CA02.md)

[01-Readiness Quizz](01-Readiness%20Quizz)



[03 AWS Fundamentals](03%20AWS%20Fundamentals)

# 04 - Identity and Access Management (IAM) 
- What is IAM?
	- IAM allows you to manage users and their level or access to the AWS console
- The `root account` is the email address you used to sign up for AWS. 
- The **root account** has full administrative access to AWS. (true or false)
	- True
- 4 steps to secure your AWS Root account
	- Enable multifactor authentication on the root account
	- Create an admin group for your administrators, and assign the appropriate permissions to this group.
	- Create users account for your administrators
	- Add your users to the admin group.
- IAM Policy Document
	- JSON file to assign permissions on AWS
- The three main value-key pairs on a Policy Document are:
	- Effect
	- Action
	- Resource
-  IAM is a Region level service (true or false)
	- False, IAM is Global level
- A `User` is a physical person that use AWS
- You create `Groups` generally by functions, such as administrators, developers, etc., and contains **users** in AWS.
- A `Role` is for internal usage within AWS. Allows one part of AWS to access another part of AWS.
- In AWS you cannot assign Policies to individual Users (true or false)
	- False, however it´s a best practice for users to inherit permissions from groups.
- What is the Users and People best practice
	- One user **equals** one physical person, never share user accounts across multiple persons.
- Describe the Principle of Least Privilege
	- Only assign a user the minimum amount of privileges they need to do their job
-  When you create a new User, by default (without adding to any Group neither assigning any Policy), has **no permissions** whatsoever. (true or false)
	- True
- What **Access Key ID** and **secret access key** are used for:
	- For programmatic access to AWS console.
- If you forget you Access Key ID, secret access key, and user password you can view again returning to users configuration (true or false)
	- False, you only get to view these once, If your lose them you have to regenerate them.
- It's a best practice to always set up password rotations (true or false)
	- True
- IAM Federation
	- The feature that allow you to use your existing account with AWS. For example, when you log on to your PC, you can use the same credentials to log in to AWS if you set up federation.
- Identity Federation:
	- Uses the SAML standard, which is Active Directory.
- ARN
	- Amazon Resource Name
	- uniquely identifies a resources in AWS
- Inline policy, what is the difference with a "Managed" policy
	- **Managed policies:** Policies shared among users and/or groups that are pre-built either by AWS or an administrator within the AWS account. When it's updated, the changes to this policy are immediately applied for all users and groups to which it's attached.
	-  **Inline policies:** Policies assigned to just one user or group that are typically used in one-off situations. 
### Study Tips
- Revisar diferentes Policy documents (especialmente de S3) y familiarizarse con ellas

# 05 - Simple Storage Service (S3)
## Flash cards
- What kind of storage is used by S3
	- Object-based
- What it means Object-based storage:
	- The data is managed as objects rather than in file system or data blocks
- For what type of data we should not use Object-based storage:
	- to run Operating systems or databases
- The total volume of data and the number of objects you can store in S3 is unlimited (true or false)
	- true
- S3 objects can range in size from a minimum of `0 bytes` to a maximum of `5 terabytes`. 
- What it means that S3 buckets are Universal Namespace
	- All AWS accounts share the S3 namespace. 
	- Each S3 buckets name is globally unique
- S3 bucket URL's format
	- `https://bucket-name.s3.Region.amazonaws.com/keyname`
- When you upload a file to an S3 bucket, you will receive an `HTTP 200` code if the upload was successful
- S3 Key-Value stores the following:
	- Key, the name of the object
	- Value, the data itself
	- Version ID, when you enable versioning
	- Metadata, data about the data your storing (e.g., content type last-modified, etc..,)
- S3 Data Availability (LSA) offered by AWS
	- 99.95 % to 99.99 % depending the S3 tier
- S3 Data Durability (LSA) offered by AWS
	- 99.999999999 % (11 nines) durability for data stored in S3
- `Availability` measures how readily available a service is, and `Durability` is used to measure the likelihood of data loss.
- S3 standard has `99.99%` availability and stored across multiple devices in at least `3` AZs.
- Amazon S3 is a global service in AWS console?
	- Yes, however buckets are created on individual regions.
- Defines rules to automatically transition objects to a cheaper storage tier or delete objects that are no longer required after a set of period of time. 
	- Lifecycle Management
- Bucket policies are bucket-wide rules (true or false)
	- true
-  S3 Object ACLs work on an individual object level (true or false)
	- true
- By default all new S3 bucket has a public access policy enabled, (true or false)
	- False,buckets are It's private by default
-  If you try to make public an Object, but the bucket has the Block Public Access policy enabled, what will happen?
	- It will give you an error
- You need to allow public access only in the bucket, but not at object-level, to allow public access on an object (true or false)
	- false, you need to do both
- Once versioning is enabled on S3, it cannot be disabled (true or false)
	- true, only can be suspended
- With versioning, all versions of an object are stored in S3, This includes all writes, and even if you delete an object (true or false)
	- true
-  How you can secure your S3 bucket from accidentally  deletion, when versioning is enabled
	- using MFA
- Previous version  of an object are not public by default, even there is a policy to make all objects public (true or false)
	- true
- S3 tier designed for frequent access
	- S3 standard
-  S3 tier that allow infrequent but rapid access to your data
	- S3 Standard-Infrequent Access
- How is the charge model for S3 standard IA
	- There is lower per-GB storage price, and a per-GB retrieval fee.
- S3 Standard-IA availability and durability LSA:
	- 99.9% Availability
	- 11 9's Durability
- S3 One Zone-Infrequent Access
	- Like S3 Standard-IA, but data is stored redundantly within a single AZ
	- Cost 20% less than regular S3 Standard-IA
	- 99.5 % Availability, 11 9's Durability
- S3 tier used only for archiving data
	- S3 Glacier
- Two options of S3 Glacier
	- Glacier
	- Glacier Deep Archive
- S3 `Glacier` provides long-term archiving with retrieval times that range from 1 minute to 12 hours.
- S3 `Glacier Deep Archive` is for archiving **rarely accessed data** with a default retrieval time of `12 hours`. 
- S3 Intelligent-Tiering
	- Unknown or unpredictable access patterns.
- `Lifecycle Management` automates moving your objects between the different storage tiers, maximizing cost effectiveness.
- What it means you can combine Lifecycle Management with Versioning
	- You can use lifecycle management o move different versions of objects to different storage tiers.
- Lifecycle Management can be applied to previous versions only (true or false)
	- false, it can be applied to current versions and previous versions.

![Pasted image 20220623234903.png](Pasted%20image%2020220623234903.png)


## S3 Object Lock and Glacier Vault Lock
- You can use S3 Object Lock to store objects using a `write once, read many (WORM)` model.
- S3 feature that can help prevent object from being deleted or modified for a fixed amount of time or indefinitely
	- S3 Object Lock
- You can use `S3 Object Lock` to meet regulatory requirements that require WORM storage, or add extra layer of protection against object changes and deletion.
- S3 Object Lock come in two modes:
	- Governance Mode
	- Compliance Mode
- In S3 Object Lock `governance` mode, users can't overwrite or delete an object version or alter it lock settings unless they have special permissions.
- On S3 Object Lock governance mode, you cant grant some users permissions to alter the retention settings or delete the object if necessary. (true or false)
	- true
- If you need some user to have the authority to delete an object if necessary on an S3 with Object Lock, you should use the mode:
	- Governance mode
- In S3 Object Lock Compliance mode, only the root user can overwrite or delete an object version. (true or false)
	- **false**, in compliance mode, a protected object version can't be overwritten or deleted by any user, including the root user of the account.
- S3 Object lock `compliance mode` ensures an object version can't be overwritten or deleted for the duration or the retention period.
- In S3 Object Lock, if an object is locked in compliance mode, it's retention mode can't be changed and its retention period can't be shortened.(true or false)
	- True
- What is a Legal Hold in an S3 Object
	- A Legal Hold prevents an object version from being overwritten or deleted, and it doesn't have a retention period associated.
	- Remains in effect util removed.
- Legal holds can be freely placed an removed by any user who has the `s3:PutObjectLegalHold` permission.
- Object Lock can be applied on individual object but not applied across the bucket as a whole (true or false)
	- false, Object lock can be applied on **individual object** or **across the bucked**.\
- `S3 Glacier Vault Lock` allows you to easily deploy and enforce compliance controls for individual S3 Glacier vaults with a vault lock policy.
- How can you  setup a WORM policy on a S3 Glacier
	- with an S3 Glacier Vault lock policy
- With S3 Glacier Vault lock, you can lock the vault lock policy from future edits, and once locked, the policy can no longer be changed. (true or false)
	- True
- Amazon S3 currently does not support enabling Object Lock after a bucket has been created. (true or false)
	- True

## Encrypting S3 Objects
- Type of Encryption
	- Encryption in Transit
		- SSL/TLS
		- HTTPS
	- Encryption at Rest: Server-Side Encryption (SSE)
	- Encryption at Rest: Client-Side Encryption
- Types of Server-Side Encryption
	- SSE-S3
	- SS3-KMS
	- SS3-C
- What is the difference between SSE-S3, SS3-KMS, and SS3-C
	- SS3-S3: S3-managed key, using AES 256 bit encryption
	- SS3-KMS: AWS Key Management Service-managed keys
	- SS3-C: Customer-provided keys
- What are the two ways to enforce Server-Side Encryption on an S3 bucket:
	- by Console (just a checkbox)
	- by a Bucket Policy
- Explain how can you enforce Server-Side encryption on a S3 bucket using a bucket policy
	- You can create a bucket policy that denies any S3 PUT request that doesn't include the **x-amz-server-side-encryption** parameter in the request header.
- What happen when you upload a file to an S3 bucket using the web console and you have enable server-side encryption
	- a PUT request is send every time you upload a file, and the **x-amz-server-side-encryption** parameter it's included in the request header.
- The two options for the **x-amz-server-side-encryption** parameters are:
	- x-amz-server-side-encryption:  AES256
	- x-amz-server-side-encryption: aws:kms

## Optimize S3 Performance
- On this example address:  S3://mybucketname/folder1/subfolder1/myfile.jpg, what part is the S3 prefix:
	- /folder1/subfolder1
	- bucketname is included in the prefix??
- How many GET/HEAD request you can do to S3:
	- 3,500 PUT/COPY/POST/DELETE and 5,500 request per second, per prefix.
- In S3, the more folders and sub-folders do you have in your bucket, the worse is the performance you can get when uploading files (true or false)
	- False
- KMS limits limits when youre using SSE-KMS to encrypt objects in S3.
	- Region-specific, however, it's either 5,500, 10,000 or 30,000 request per second.
	- Uploading/downloading will count toward the **KMS quota**
	- Currently, you **cannot** request a quota increase for KMS
-  When is recommended to use Multiparts Uploads on S3
	- Recommended for files over 100MB
- When is mandatory to use Multiparts Uploads on Se
	- Required for files over 5GB
- How do you increase the performance in S3 Downloads
	- Using S3 Byte-Range Fetches
	- Parallelize downloads by specifying byte ranges.
	- If there's a failure in the download, it's only for a specific byte range.
-  What else is used for the S3 Byte-Range Fetches:
	- Can be used to download partial amounts of the file (e.g., header information)

## Backing up Data with S3 Replication
- What is S3 Replication
	- A way to replicate object from one bucket to another
- Versioning must be enabled on both the source and destination buckets, to use S3 Replication (true or false)
	- true
- When you turn on replication on an S3 buckets, all existing object are replicated automatically (true or false)
	- false, only subsequent updated object will be replaced automatically
	- ... however, On Feb 2022, AWS announced a new Amazon S3 Batch Replication feature which allows replication of existing object to different buckets on demand.
	- ![Pasted image 20220623232824.png](Pasted%20image%2020220623232824.png)
- Delete markers on an S3 bucket are not replicated by default when you activate replication (True or False)
	- True,  but you can enable it.


Object Ownership #toinvestigate 






# 06 - Elastic Cloud Compute (EC2)
## EC2 Overview
## Demo: Launching an EC2 instance
## AWS Command line
## Using Roles
## Security groups and bootstrap script
- `Security groups` are virtual firewalls for EC2 instances. By default, everything is `blocked`. 
- Changes to security group takes effect after the next reboot of the EC2 instance (true or false)
	- False, they take effect inmediately
- You can have any number of EC2 instances within a security group (true or false)
	- True
- You can have multiple security groups attached to EC2 instances
	- True
- On a security group, all inbound traffic is `blocked` and all outbound traffics is `allowed`, by default.
- `A bootstrap script` is a script that runs when the instance first runs. It passes user data to the EC2 instance and can be used to install applications (like web servers and databases), as well as do updates and more.
- Another name for the bootstrap script on an EC2 instnace
	- user data
## EC2 Metadata and User Data
- What EC2 metadata is:
	- it's simply data about your EC2 instance.
	- this can include information such as private IP address, public IP address, hostname, security groups, etc.
- Which command we use to retrieve metadata about our EC2 instance
	- curl
- Example of the path where we can retrieve the meta-data on an EC2 instance
	- http://169.254.169.254/latest/meta-data/public-ipv4 
- Example of the path where we can retrieve the user-data on an EC2 instance
	- http://169.254.169.254/latest/user-data
- User data is simply the bootstrap script (true or false)
	- true
- The **"magic"** IP address used to retrieve _user data_ and _instance metadata_ specific to a instance, in AWS:
	- 169.254.169.254

## Networking with EC2
- You can attach 3 different types of virtual networking cards to your EC2 instance:
	- Elastic Network Interface (ENI)
	- Enhanced Networking (EN)
	- Elastic Fabric Adapter (EFA)
- EC2 virtual networking card type for basic, day-to-day networking
	- Elastic Network Interface (ENI)
- EC2 virtual networking card type that uses single root I/O virtualization (SR-IOV) to provide high performance
	- Enhanced Networking (EN)
- EC2 virtual networking card type for that accelerates High Performance Computing (HCP) and machine learning applications.
	- Elastic Fabric Adapter (EFA)
- Depending on you instance type, enhanced networking can be enabled using this options:
	- Elastic Network Adapter (ENA)
	- Intel 82599 Virtual Function (VF) Interface
- Elastic Network Adapter (ENA) supports network speeds up to `100 Gbps` for supported instances types.
	- Always choose ENA for scenario questions, is faster, modern, better.
- Intel 82599 VF Interfaces supports network speeds up to `10 Gbps` for supported instances types.
- `OS-bypass` enables HPC and machine learning applications to bypass the operating system kernel and communicate directly with the EFA device.
	- Not currently supported with Windows - only Linux.
- If you need a separate management network from your production network, and at low cost, which virtual network adapter type you use:
	- Elastic Network Interface (ENI)
- If you need to accelerate High Performance Computing (HPC) and machine learning applications, which virtual network adapter type you use:
	- Elastic Fabric Adapter (EFA)
- Which network adapter support OS-bypass
	- Elastic Fabric Adapter (EFA)
- If you need speeds between 10Gbps and 100Gbps, reliable and high throughput, which virtual adapter type you need to use:
	- Enhanced Networking (EN)

## Optimizing with EC2 Placement Groups
- What it means EC2 Placement Group
	- It's just a way to logically grouping your EC2 instance depending of you applications needs.
- The 3 types of EC2 Placement Groups are:
	- Cluster
	- Spread
	- Partition
- What is a EC2 Cluster Placement Group?
	- It means grouping of instance within a single Availability Zone,  in order to achieve low network latency, high network throughput or both.
- All EC2 instance types can be launched into a cluster placement group. (True or False)
	- False, only certain instance types can be launched into a cluster placement group.
- What is a EC2  Spread Placement Group?
	- is a group of instances that are each placed on distinct underlying hardware.
- For which scenario an EC2 Spread Placement Group is recommended?
	- for applications that have small number of critical instances that should be kept separate from each other.
	- Used for individual instances
- Explain the EC2 Partition Placement Group
	- EC2 divides each group into logical segments called **partitions.**
	- Each partition placement group has its own set of racks.
	- Each rack has its own network and power source.
- For which scenario is recommended the EC2 Partition Placement Group
	- Used for Multiple Instances
	- When you want to isolate the impact of hardware failure in your applications.
	- HDFS, HBase and Cassandra *
- A cluster placement group can't span multiple Availability Zones, whereas a spread placement group and partition group can (True or False)
	- True
- Which types of instances can be launched in a placement group
	- Compute optimized
	- GPU optimized
	- Memory optimized
	- Storage optimized
- AWS recommends homogeneous instance within cluster placement group (True or False)
	- True
- You can merge placement groups, with any problem (True or False)
	- False, you cannot
- You never can move an existing EC2 instance into a placement group
	- False
- How you can move an existing EC2 instance into a placement groups
	- The instance must be in the stopped state
	- You can move or remove an instance using the AWS CLI or an AWS SDK, but you can't do it via the console yet

## Solving Licensing Issues with Dedicated Hosts
- Pricing models for EC2
	- On-Demand
	- Reserved
	- Spot
	- Dedicated
- Why you should need a Dedicated host?
	- Compliance
	- Licensing
- The two ways to purchase a Dedicated host?
	- On-Demand (hourly)
	- Reserved (save 70%) 
- On any scenario where you have an special licencing requirements, you should always use a `Dedicated Host`

## Timing Workloads with Spot Instances and Spot Fleets
- When to use spot instances?
	- Where you have stateless, fault-tolerant, or flexible applications
	- Example: bid data, containerized workloads, CI/CD, high-performance computing (HPC), and other test and development workloads.
- Spot instances save up to `90%` of the cost of On-Demand instances.
- To use Spot Instances, you must first decide on your `maximum` Spot price.
- The hourly Spot price varies depending on:
	- capacity and region
- What is a Spot block:
	- Allows to stop your Spot Instance for being terminated even if the Spot price goes over your max Spot price
- You can set Spot blocks for between `1 to 6 hours` currently.
- Spot instance are good for persistent workload (true or false)
	- False
- Spot instances are good for Critical Jobs (true or false)
	- False
- Spot instances are good for Databases (true or false)
	- False
- How spot request works
	- read the guide https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-requests.html
- A collection of Spot instances and (optionally) On-Demand Instance
	- Spot fleet
- Spot Fleets will try and match the target capacity with your price restraints (True or False)
	- True
- You can have the following strategies with Spot Fleets
	- capacityOptimized
	- diversified
	- lowestPrice
	- InstancePoolsToUseCount

## EC2 Exam Tips
- You pay by the hour or the second, depending on the type of instance you run. Great for flexibility
	- On-Demand
- Purchase unused capacity at a discount of up to 90%. Prices fluctuate with supply and demand. Great for applications with flexible start and end times
	- Spot
- Reserved capacity for 1 or 3 years. Up to 72% discount on the hourly charge. Great if you have known, fixed requirements.
	- Reserved
- A  physical EC2 server dedicated for your use. Great if you have server-bound to reuse or compliance requirements.
	- Dedicated host
- You can attach and detach roles to running EC2 instances without having to stop or terminate these instances. (True or False)
	- True
- You can update a policy attached to a role and will take immediate effect (True or False)
	- True
- `Roles` allow you to provide access without the use of access key IDs and secret access keys.

# 07 - Elastic Block Storage (EBS) and Elastic File System (EFS)
## EBS Overview
- High available and scalable storage volume you can attach to an EC2 instance.
	- Elatic Block Storage (EBS)
- EBS is automatically replicated within a single Availability Zone to protect against hardware failures (true or false)
	 - True, as is designed for mission-critical workloads
 - Types of EBS SSD drives
	 - gp2 & gp3
	 - Provisioned IOPS SSD: io1 & io2
 - Type of EBS HDD drives
	 - Throughput Optimized HDD: st1
	 - Cold HDD: sc1
 - Measures the number of read and write operations per second
	 - IOPS
 - Measures the number of bits read or written per second (MB/s)
	 - Throughput
 - If your looking for the ability to action reads and writes very quickly, which type of EBS you need to choose?
	 - Provisioned IOPS SSD (io1 or io2)
 - If your looking for the ability to deal with large datasets, which type of EBS you need to choose?
	 - Throughput Optimized HDD (st1)
 - If your looking for a EBS volume suitable for boot disk and general applicaton, which one you need to chose?
	 - General Purpose SSD (gp2)
 - Which EBS volume you choose, if you need more than 16,000 IOPS per volume?
	 - Provisiones IOPS SSD like io1 or io2
 - EBS Throughput Optimized HDD st1 can be used as boot volume (true or false)
	 - false, st1 cannot be a boot volume
 - Which is the lowest cost EBS volume?
	 - sc1, Cold HDD

## Volumes and Snapshots
- Volume as simple `virtual hard disks`.
- EBS Snapshots exist on S3 (true or false)
	- true
- For a consistent snapshot, it is recommended you `stop the instance` and take a snap.
- If you take a snapshot of an encrypted EBS volume, the snapshot will be encrypted automatically (true or false)
	- true
- You can share snapshots in AWS?
	- Yes, but only in the region in which they were created.
	- To share to other regions,you will need to copy them to the destination region first.
- EBS volumes can be in a different AZ as the EC2 instance with it is attached (true or fase)
	- false, EBS volumes will always be in the same AZ as the EC2
- You can resize EBS volume on the fly (true or false)
	- True, you do not need to stop or restart the instance, however you will need to extend the filesystem in the OS so the OS can see the resized volume.
- You cannot change volume types on the fly (e.g. from gp2 to io2) (true or false)
	- False, you can switch volume type on the fly

## Protecting EBS Volumes with Encryption
- Which are the steps to encrypt and un-encrypted volume
	- Create a snapshot of the unencrypted root device volume
	- Create a copy of the snapshot and select the encrypt option
	- Create an AMI from the encrypted snapshot
	- Use that AMI to launch new encrypted instances.
- What it means you have end-to-end EBS Volumes encryption
	- Data at rest is encrypted inside the volume
	- All data in flight moving between the instance and the volume is encrypted
	- All snapshots are encrypted
	- All volumes created from the snapshot are encrypted

## EC2 Hibernation
- If an EC2 instance is terminated, they by default what happen with the root device volume?
	- will also be terminated (although this is configurable in the EC2 creation)
- What happen with EC2 hibernation
	- The instance boots much faster.
	- The operating system does need to reboot because the in-memory (RAM) is preserved.
- Instance RAM must be less than `150 GB` to allow EC2  Hibernation to work.
- Instance families that support EC2 Hibernation
	- C3, C4, C5
	- M3, M4, M5
	- R3, R4, R5
- EC2 instances can't be hibernated for more than `60 days`.

### EFS Overview
- Describe Amazon Elastic File System
	- A managed NFS (network file system) than can be mounted on many EC2 instances.
-  EFS works with EC2 instances in multiple Availability Zones within a region (True False)
	- True
- EFS his highly available and scalable; however it is `expensive`
- EFS use cases
	- Content Management
	- Web Servers
- AWS EFS uses `NFSv4` protocol
- AWS EFS is compatible with Windows (true or false)
	- false, only with Linux-based AMI
- EFS Storage Tiers
	- Standard
	- Infrequently Accessed

## FSX Overview
- What is FSx for Windows
	- A managed Windows Server that runs Windows Server Message Block (SMB)-based file services
- What is FSx for Lustre
	- High performance Network File system
	- used for AI and ML
- What you use if you need distributed, highly resilent storage for Linux instances and Linux-based applications
	- EFS
- What you use when you need centralized storage for Windows-based applications, such as SharePoint, Microsoft SQL Server, Workspaces, IIS Web Server, or any other native Microsoft application.
	- Amazon FSx for Windows
- What you use when you need high-speed, high-capacity distributed storage. This will be for applications that do high performance computing (HCP), financial modeling, etc.
	- Amazon FSx for Lustre
- FSx for Lustre can store data directly on S3 (true or false)
	- True

## Amazon Machine Images: EBS vs. Instance Store
- An `Amazon Machine Image (AMI)` provides the information required to launch an instance.
- You can base your AMI on the following things:
	- Region
	- Operating system
	- Architecture (32-bit or 64-bit)
	- Launch permissions
	- Storage for root device (root device volume)
- All AMIs are categorized as either backed by:
	- Amazon EBS volumes
	- Instance Store  volumes
- Instance store volumes are sometimes called `ephemeral storage`
- Instance store volumes `cannot` be stopped.
	- If the underlying host fails, you will lose your data
-  EBS-backed instance can be stopped. You will not lose the data on this instance if it is stopped. (true or false)
	- True
- If you reboot a EBS volume EC2 you will not loose your data, but if you reboot an Instance Store voluce EC2 you will. (True or false)
	-  False, on both cases you **will not** loose your data if you reboot the instance.
- With EBS volumes,  you can tell AWS to keep the rood device volume whey you terminate your instance (true or false)
	- True

## AWS Backup
- What is AWS Backup?
	- Backup allows you to **consolidate** your backups across multiple AWS services, such as:
		- EC2
		- EBS 
		- EFS 
		- Amazon FSx for Lustre
		- Amazon FSx for Windows File Server
		- AWS Storage Gateway
		- It can interlude other services like databases
	- AWS Backup can be used with AWS Organizations to back up multiple AWS accounts in your organization (true or false)
		- True
	- Benefits of AWS Backups
		- Central Management
		- Automation
		- Improved Compliance

## EBS Exam Tips
- True or False? Amazon Machine Images are Region specific. To use one in another Region, it needs to be explicitly copied there.
	- True
- True or False? EBS volumes are encrypted by default.
	- False
- What is the purpose of an Amazon Machine Image (AMI)?
	- It's a type of database structure that can be deployed to RDS.
	- It provides you with an always-up-to-date OS for your EC2 instance.
	- It's a type of EC2 instance that you'll select during creation of an instance.
	- `It's a template to create a new EC2 instance from.`

# 08-Databases
## Relational Database Service (RDS) Overview
- Relational Databases engines available in RDS
	- SQL server
	- Oracle
	- MySQL
	- PostgreSQL
	- MariaDB
	- Amazon Aurora
- Amazon RDS features
	- Up and Running in Minutes
	- Multi-AZ
	- Fail-over capability
	- Automated backups
- What OLTP stands for:
	- Online Transaction Processing
- What OLAP stands for:
	- Online Analytical Processing
- It processes data from transactions in real time, it's all about data processing and completing large number of small transactions in real time
	- OLTP
- It processes complex queries to analyze historical data, is all about data analysis using large amounts of data, as well of complex queries that take a long time to complete
	- OLAP
- Amazon RDS database is generally used for online transaction processing (OLTP) workloads. True or false?
	- True
- Amazon RDS is suitable for analyzing large amounts of data
	- False, use a data warehouse like Redshift, which is optimized for OLAP
- Aurora RDS is Multi-AZ by default. True or False?
	- True
- with RDS Multi-AZ feature you can improve your performance, by having two active databases.  True of False?
	- False, Multi-AZ is for **disaster recovery**, so you cannot connect to the standby when the primary database is active

## Increasing Read Performance with Read Replicas
- A `read replica` is a read-only copy of your primary database.
- The main purpose of read replica is `scalability`, whereas the main purpose for Multi-AZ deployments is `availability`.
- You can use a read replica for disaster recovery of the source DB instance either in the same AWS Region or in another Region. True or False?
	- True
- Read replica can be cross-AZ but not cross-region. True or False?
	- False, you can create Read Repllicas in another AZ or in another Region.
- Each read replica has its own DNS endpoint. True or False?
	- True
- Read replicas can be promoted to be their own database.
	- True, this breaks the replication
- You can have up to `5` read replicas to each DB instance.

- ![Pasted image 20220702102630.png](Pasted%20image%2020220702102630.png)

## What is Amazon Aurora
- What is Aurora?
	- is a MySQL-and PostgreSQL-compatible relational database engine, created by Amazon
- Amazon Aurora size model:
	- Start with 10GB. Scales in 10-GB increments to 128 TB (storage  Auto Scaling)
- Amazon Aurora resource capacity:
	- Compute resources can scale up to 96 vCPUs and 768 GB of memory
- Amazon Aurora availability features:
	- 2 copies or your data are contained in each Availability Zone, with a minimum of 3 Availability Zones, there is always **6 copies of your data.**
- 3 types of Aurora Replicas available:
	- Aurora replicas (15)
	- MySQL replicas (5)
	- PostgreSQL replicas (5)
- Amazon Aurora Serverless
	- An Aurora Serverless DB automatically starts up, shuts down, and scales capacity up or down based on your application's needs.
- You can share Aurora snapshots with other AWS accounts. True or False?
	- True
- Automated failover is available on MySQL replicas and PostgreSQL as well. True or False?
	- False, automated failover is only available with Aurora replicas.
- If you want a simple, cost-effective option for infrequent, intermittent, or unpredictable workloads, with the benefits of Amazon Aurora, you should use:
	- Amazon Aurora Serverless

## DynamoDB Overview
- What is DynamoDB?
	- Amazon proprietary NoSQL database service 
	- Fully managed database
	- Supports both document and key-value data models.
	- Provides consistent single-digit millisecond latency at any scale.
- DynamoDB is stored on SSD storage. True or False?
	- True
- DynamoDB is spread across 3 geographically distinct data centers. True or False?
	- True
- DynamoDB supports eventually and strongly consistent reads. True or False?
	- True, eventually consistent reads by default.
- Consistency across all copies of data is usually reached within a second. Repeating a read after a short time should return the updated data. Best read performance.
	- Eventually consistent reads.
- Returns a result that reflects all write that received a successful response prior to the read.
	- Strongly consistent read.
- DynamoDB Accelerator (DAX)
	- in-memory cache for DynamoDB
- DynamoDb use encryption at rest using `KMS`

## When Do We Use DynamoDb Transactions
 - What it mean ACID methodology for databases?
	 - Atomic
	 - Consistent
	 - Isolated
	 - Durable
 - DynamoDB `transactions` provide developers atomacity, consistency, isolation, and durability (ACID) across 1 or more tables within a single AWS account and region.
 - ACID basically means `all or nothing`.
 - DynamoDB 3 options for reads:
	 - eventual consistency
	 - strong consistency
	 - transactional
 - Dynamo DB 2 options for writes:
	 - standard
	 - transactional.

## Saving your Data with DynamoDB backups
- DynamoDB On-Demand backups an restore features?
	- Full backups at any time
	- Zero impact on table performance avilability
	- Consistent within seconds and **retained util deleted.**
	- Operates within same region as the source table.r
- DynamoDB point-in-Time Recovery (PITR) features
	- Protects again accidental writes or delete
	- Restore to any point in the last 35 days.
	- Incremental backups
	- Not enabled by default
	- Latest restorable: 5 minutes in the past

## Taking Your Data Global with DynamoDb streams, and Global Tables
- DynamoDB Streams
	- Time-ordered sequence of item-level changes in in a table
	- Stored for 24 hours
	- Inserts, updates,and deletes
	- Combine with Lambda function for functionality like stored procedures.
- DynamoDB Global Tables
	- Managed Multi-Master, Multi-Region Replication
	- Needs to have DynamoDB streams enabled
	- Replication latency under one second
	- 

# 09-VPC Overview
## VPC Introduction
- What is a VPC?
	- Think a VPC as a virtual data center in the cloud
	- Logically isolated part of AWS Cloud where you can define your own networks
	- A fully Customizable  network inside AWS
- A VPC consist of:
	- Internet gateways
	- Virtual private gateways
	- Route tables
	- Network Access Control Lists
	- Subnets
	- Security Groups.
- You can have subnets that spans multiple availability zones in AWS (True or False)
	- False, 1 subnet is always 1 AZ.
- Classic 3-Tier architecture (example)
	- Web Tier
	- Application Tier
	- Database Tier
- The smallest subnet size you can have on AWS is:
	- /28 (16 usable addresses)
- The largest subnet size you can have on AWS is:
	- /16
- You can use `network access control lists (NACLs)` to block specific IP addresses.
- Default VPC characteristics:
	- All subnets in default VPC have a route out to the internet
	- Each EC2 instance has both a public and private IP address
-  When you create an AWS account, it already comes with a default VPC for every region (True or false)
	- True
- When you create a new VPC, it automatically creates a default subnet (true or false)
	- False, no subnets are created, 
- When you create a new VPC, it automatically creates a security group, routing table and network ACLs. (True or False)
	-    True
- A /24 subnet on AWS has `251` available IP addresses.
- Besides the network and broadcast addresses, AWS reserves the `first 3` addresses on each subnet.
	- 1st address reserved by AWS for the VPC router.
	- 2nd address: reserved by AWS for DNS server.
	- 3rd address: reserved by AWS for future use.
- Broadcast traffic in a VPC is not supported on AWS. (true or false)
	- True 
- You can only have 1 Internet Gateway attached per VPC (True or False)
	- True
## Using NAT Gateways for Internet Access
- What NAT Gateways are used for?
	- You can use a network address translation (NAT) gateway to enable instances in a private subnet to connect to the internet or other AWS services while preventing the internet from initiating a connection with these instances.
- Nat Gateways Facts
	- Redundant inside the Availablity Zone
	- Starts at 5Gbps and scales currently to 45 Gbps
	- No need to patch
	- Not associated with security groups
	- Automatically assigned a public IP addrese
- NAT Gateways are redundant inside the Availability Zone (True or False)
	- True
- Network ACSs are the first line of defense
	- True
- The only weay to be able to block an IP address is through network ACLs, not Security Groups
	- True
- If you have resources in multiple Availability Zones and they share a NAT gateway, in the event the NAT gateway's Availability Zone is down, resources in the other Availability Zone lose internet Access. (True or False)
	- True,to create an Availability Zone-independent architecture, create a NAT gateway in each Availability Zone and configure your routing to ensure resources using the NAT gateway in the same Availability Zone.
## Security Groups and Network ACLs
- Security Groups are `statefull` and NACLs are `stateless` 
- Default Network ACL allows all outbound and inbound traffic. (True or False)
	- True
- Custom Network ACL allows all outbout and inboudn traffic (True or False)
	- False, denies all
- Each subnet in your VPC must be associated with a network ACL. (True or False)
	- True
- What happen when you associate a network ACL with a subnet that is already associated.
	- the previous association is removed
## Building Solutions across VPCs with Peering
- VPC Peering
	- Allows you to connect 1 VPC with another via a direct network route using private IP addresses.
- Transitive VPC Peering is not supported (True or False)
	- True, This must always be in a hub-and-spoke model.
- You cannot do VPC peering between regions (True or False)
	- False 
- VPC will not work if you have overlapping CIDR address ranges. (True or False)
	- True
## Network Privacy with AWS PrivateLink
- To open our applications up to other VPCs, we can either:
	- Open the VPC up to the Internet
	- Use VPC peering
	- AWS PrivateLink (at scale)
 - If you want to expose a service VPC to tens, hundreds, or thousands of **customer VPCs**, you can use:
	 - AWS PrivateLink
 - an AWS PrivateLink requires these two elements:
	 - Network Load Balancer on the Service VPC
	 - Elastic Network Interface (ENI) on the customer VPC
 ## Securing Your Network with VPN CloudHub
- If you have multiple sites, each with its own VPN connection, you can use AWS `VPN CloudHub` to connect those sites together.
- AWS VPC CloudHub it's similar to VPC peering in that i works on a `hub-and-spoke` model.
## Connection On-Premises with Direct Connect
- `AWS Direct Connect` is a cloud service solution that makes it easy to establish a dedicated network connection from your premises to AWS.
- There are to Types of Direct Connect Connection:
	- Dedicated Connection
	- Hosted Connection (throught a Partner)
- VPN vs Direct Connect differences
	- VPNs traverses the public internet
	- VPNs are secure both slow
	- DirectConnect is fast, secure, reliable, massive throughput.
- Direct Connect is not encrypted by default (True or False)
	- True
## Simplifying Networks using Transit Gateways
- `AWS Transit Gateways` connects VPCs and on-premises networks through a **central hub**. This simplifies your network and puts an end to complex peering relationships.
- AWS Transit Gateway works with Direct Connect but not with VPN connections.(True or False)
	- False, work with both
- AWS Transit Gateway supports IP multicast (not supported by any other AWS service) (True or False).
	- True
## VPC Networking Exam Tips





Today, I practice how to create a simple Wordpress site on AWS, with an EC2 and a RDS database, 


# 10-Route 53
## Route 53 Overview
- ".com", ".uk", ".gov", are examples of:
	- top-level domains (TLD)
- In the domain name "primerminister.gov.uk", the .gov is called
	- second-level domain
- The place where all the TLD are stored, is called:
	- root zone database
-  The authority that can assign domain names directly under one or more top-level domains is called:
	- Domain Registars
- Each domain name becomes registered in a central databae known as:
	- WHOIS databaase
- DNS SOA Record type stores information about:
	- The name of the server that supplied the data for the zone
	- The administrator of the zone
	- The current version of the data file
	- The default number of second of the TTL file on resource records.
- `NS records` are used by top-level domain servers to direct traffic to the content DNS server that contains the authoritative DNS records.
- `A record` is the fundamental type of DNS record. 
- The length that a DNS record is cached on either to resolving server or the user's own local PC is called?
	- Time-to-live (TTL)
- A `CNAME (canonical name)` can be used to resolve one domain name to another. 
	- for example m.cloudguru.com to mobile.cloudguru.com
- `Alias Records` are used to map resource record sets in your hosted zone to load balancers, CloudFront distributions, or S3 buckets that are configured as websites.
	- AWS only
- CNAME cannot be used for naked domain names (zone apex record) (True or False)
	- True
- A Record or Alias record can be used for a naked domain name (zona apex record) (True or False)
	- True
- 7 Routing Policies available with Route 53
	- Simple routing
	- Weighted routing
	- Latency-based routing
	- Failover routing
	- Geolocation routing
	- Geoproximity routing (Traffic Flow Only)
	- Multivalue answer routing


## Register a Domain Name
- You can buy domain names directly with AWS (True or False)
	- True
- Route 53 is a global-level service (True or False)
	- True

## Demo: Using a Simple Routing Policy
- You can only have  one record with multiple IP addresses. If you specify multiple values in a record, Route 53 returns all values to the user in a random order.
	- Simple Routing Policy
## Demo: Using a Weighted Routing Policy
- You need to setup health checks before configure Weighted routing policies (True or False)
	- True

## Demo: Using a Failover Routing Policy


## Demo: Using a Geolocation Routing Policy

## Demo: Using a Geoproximity Routing Policy

## Demo: Using a Latency Routing Policy

## Demo: Using a Multivalue Answer Routing Policy

## Route 53 Exam Tips


# 11-Elastic Load Balancing (ELB)
- `Elastic Load Balancing` automatically distribute incoming application traffic across multiple targets, such as Amazon EC2 instances.
- ELB can be done across multiple AZs (True or False)?
	- True
- There are 3 different types of Load Balancers
	- Application Load Balancer (ALB)
	- Network Load Balancer (NLB)
	- Classic Load Balancer (CLB)
- Best suited for load balancing or HTTP and HTTPS traffic. They operate at Layer 7 and are application-aware
	- Application Load Balancer
- Operates at the connection level (Layer 4), they are capable of handling millions of request per second, while maintaining ultra-low latencies
	- Network Load Balancers
- Legacy load balancers, You can load balance HTTP/HTTPS applications and use Layer 7-specific feature, such as X-Fowarded and sticky sessions.
	- Classic Load Balancer
- The Load Balancer type most suitable for Test/Dev environments.
	- Classic Load Balancer
- You can use `health checks` to route traffic to instances or targets that are healthy.
- The two status that a Heath Checks reports over an instance are?
	- InService
	- OutOfService
- The load balancer will not resume routing request to the instance when it has been restores to healthy states. (True or False)
	- False
- What a ELB Listeners do?
	- A listener checks for connection request from clients, using the protocol and port you configure
- They determine how the load balancer routes requests to its registered targets. 
	- Load Balancer Rules
- Each ELB rules consist of:
	- a priority
	- one or more actions
	- one or more conditions
- You must define a default rule for each listener. (True or False)
	- True. and you can define more roules
- A `Target Group` is one or more targets, for an specific port number, and you assign a health check.
- An Application Load Balancer only support HTTP and HTTPS (True or False)
	- True
- To use an HTTPS listener, you must deploy at least one SSL/TLS server certificate on you load balancer. (True or False)
	- True
- When you use HTTPS listener on an Application Load Balancer, where the decryption occurs?
	- on the ELB
- There are not rules on Network Load Balancers (True or False)
	- True
- You can use TLS listener to offload the encryption and decryption to a Network Load Balancer (True or False)
	- True
- On a Network Load Balancer, If the listener protocol is TLS, you must deploy exactly one SSL server certificate on the listener.
	- True or False
- The ELB type most suited for load balancing of TCP traffic
	- Network Load Balancer
- The ELB type used for extreme performance
	- Network Load Balancer
- Network Load Balancer operate at Layer `4`
- With `Classic Load Balancers`, you can load balance HTTP/HTTPS applications and use Layer 7-specific features, such as X-Forwarded-For and sticky sessions.
- What instance will a NLB load balancer send traffic to if no hosts are healthy?
	- It will send traffic to all the instances, hoping one is online.
- With Classic Load Balancers you can also use strict Layer 4 load balancing for applications that rely purely on the TCP protocol. (True or False)
	- True
- Explain X-Forwarded-For header
	- is used when you need to look for the IPv4 address of your end user. #toinvestigatemore
- If you application stops responding, the Classic Load Balancer responds with a `504 error`
- What are Sticky Sessions on a load balancer?
	- Sticky sessions allow you to bind a user's session to a specific EC2 instance.
- On an scenario when you want you store information locally on a in instance behind a Load Balancer, which feature should you use?
	- Sticky sessions
- You can enable sticky sessions for Application Load Balancer as well. (True or False)
	- True, but the traffic will be sent at the target group level.
- In a scenario when you remove an EC2 instance from a pool, but the load balancer continues to direct traffic to that EC2 instance, what do yo solve it?
	- disabling the sticky sessions.
- What is Deregistration Delay?
	- Deregistration delay allow Load Balancer to keep existing connection open if the EC2 instance are de-registered or become unhealthy
- Another name for Deregistration delay is `Connection draining`.
- 

# 12-Monitoring
- 'CloudWatch' is a monitoring and observability platform that was designed to give us insight into our AWS architecture.
- What Tool Do we use to *monitoring* in AWS?
	- CloudWatch
- CloudWatch can be used for on-premise infrastructure. (True or False)
	- True
- CloudWatch Features
	- System Metrics
	- Application Metrics
	- Alarms
- AWS CloudWatch type of Metrics
	- Default
	- Custom, need agent installed
- AWS CloudWatch Default metrics example:
	- CPU Utilization
	- Network Throughput
- EC2 Memory Utilization is a Default AWS CloudWatch Metric (True or False)
	- False, it´s a custom metric, an agent need to be installed
- EBS Storage Capacity is a Custom CloudWatch metric. (True or False)
	- True
- There are some default CloudWatch alarms alredy set up. (True or False)
	- False
- CloudWatch default alarms can't see past the hypervisor level for EC2 instances. (true or false)
	- True, that is why you need to install an agent for custom metrics.
- The more managed a service is, the more CloudWatch checks you get out of the box. (true or false)
	- True
- CloudWatch standard checks are '5-minutes' interval, whereas detailed is '1-minute' interval.
- Detail metrics has additional cost in CloudWatch. (True or False)
	- True
- You cannot create an alarm to stop, terminate or recover an EC2 instace?
- 'CloudWatch Logs' is a tool that allows you to monitor, store, and access log files from a variety of different sources. It gives you the ability to query your logs to look for potential issues or data that is relevant you you. 
- A 'Log Event' is the record of what happened. It contains a timestamp and the data.
- A collection of log events from the same source create a 'log stream'
- This is collection of log streams.
	- Log Groups
- You group all your Apache web server logs across host all together. this is an example of:
	- Log Groups
- CloudWatch Logs feature that allows you to look for specific term in your logs, such as 400 errors in your web server logs:
	- Filter Patterns
- CloudWatch Logs feature that allows you to query all your logs using a SQL-like interactive solution
	- CloudWatch Logs Insights
- CloudWatch Logs has an Alarm feature. (True or False)
	- True
- Logs should go to CloudWatchLogs, however on situations where we don´t need to process them. Then, they shoud go strainght to:
	- S3
- Which service can act as a source for CloudWatch logs?
	- EC2
	- Lambda
	- RDS
	- CloudTrail
	- On-premises
- Are CloudWath logs, real time?
	- Generally speaking, they are near real time, for real-time scenarios you should consider Kinesis.
- CloudWatch Logs are agent-based. (True or False)
	- True
- Research about AWS Config
	- System and App level monitoring: CloudWach
	- AWS standarsds and best practive level monitoring: AWS Config
- A 'Period' is the lenght of time associated with a specific Amazon Cloud Watch statistics.
- The default period value for Amazon CloudWatch is:
	- 60 seconds
- True or False? Amazon EventBridge (formerly called Amazon CloudWatch Events) event patterns rules use event patterns to select events and route them to targets.
	- True [](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-event-patterns.html#eb-create-pattern)

https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html

https://aws.amazon.com/cloudwatch/faqs/

# 13-High Availability and Scaling
- 



