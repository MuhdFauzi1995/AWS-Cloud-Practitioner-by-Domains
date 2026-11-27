# Storage services
## Object storage
You'll be able to spot when ==object storage fits a workload, such as backups, media, or static websites.==
==Object storage== ==🟢keeps data as self-describing objects==, which ==🔵makes it a natural home for files== like ==🟣photos, videos, backups, and website content.==
1. Object storage ==holds unstructured data== as ==🟢objects, each with data, metadata, and a unique identifier.==
2. ==Backups, images, videos, and static website content== are ==🟢classic object storage use cases.==
3. ==Objects live in a flat bucket==, ==🔴not in a folder hierarchy and not as block volumes==.

## S3 storage classes
You'll be able to pick ==S3 Standard or S3 Standard-IA== ==🟢based on how often data is accessed.==
Pick the S3 storage class that ==matches how often you read your data== and ==🟢how fast you need it back.==
1. Choose a storage class by ==access frequency== and ==🟢retrieval needs.==
2. ==S3 Standard== fits ==🟢data that you access frequently==.
3. ==🔵S3 Standard-IA== fits data ==🟣you read less often but still need fast, and it adds a retrieval fee.==

## Persistent block storage
You'll be able to explain how ==EBS volumes keep data safe== ==🟢beyond an EC2 instance's life.==
==Amazon EBS== ==🟢gives your EC2 instances hard-drive-style storage== that ==🔵keeps your data when the instance goes away.==
1. EBS is ==block storage== that you ==🟢attach to EC2 instances== and ==🔵use like a hard drive==.
2. An EBS volume ==persists independently of the instance==, so ==🟢stopping or terminating the instance== ==🔵does not have to destroy the data==.
3. You can ==detach a volume== and ==🔵reattach it to another instance to move data.==

## Instance store
You'll be able to explain ==why instance store is fast== ==🟢but loses its data when the instance stops.==
I==nstance store== is ==🟢fast storage on the host computer behind an EC2 instance==, and ==🔵its data is lost when the instance stops or ends.==
1. Instance store is ==temporary block storage on disks== ==🟢attached to the EC2 host computer.==
2. ==Data is lost== when the ==🟢instance is stopped or terminated==, so ==🔴never keep valuable data only there.==
3. Use it ==for buffers, caches, and scratch data==, and ==🔵copy anything you need to keep to persistent storage.==

## Amazon EFS
You'll be able to explain when Amazon EFS is ==the right shared, elastic file storage for Linux workloads.==
==Amazon EFS== is ==🟢shared, elastic file storage== that ==🔵many Linux servers can use at the same time.==
1. EFS is ==managed, shared file storage== for ==🟢Linux workloads==.
2. ==Many EC2 instances or containers== can ==🟢mount the same EFS file system== at ==🔵once through NFS.==
3. ==EFS grows and shrinks automatically==, so you ==never provision capacity in advance==.

## Amazon FSx
You'll be able to explain ==when a workload needs Amazon FSx== ==🔴instead of Amazon EFS==.
==Amazon FSx== gives you ==fully managed file systems== ==🟢built on well-known file system software.==
1. Amazon FSx ==offers fully managed file systems built on== ==🟢Windows File Server, Lustre, NetApp ONTAP, and OpenZFS.==
2. ==FSx for Windows File Server== ==🟢supports SMB access and Active Directory integration.==
3. ==Choose FSx== when ==🟢a workload needs the native features of a specific file system==; ==🔵choose EFS for general-purpose Linux NFS.==

## Storage lifecycle policies
You'll be able to explain how ==lifecycle rules move data to cheaper storage== and ==🟢delete it on a schedule.==
==A lifecycle policy== ==moves your data to cheaper storage== and ==🟢deletes it for you on a schedule.==
1. Lifecycle policies ==automate data tiering and expiration==.
2. ==A transition action== ==🟢moves data to a lower-cost storage class after a set period==.
3. ==An expiration action== ==🔵deletes data after a set period==, and ==🟣the effect is permanent.==

## Amazon EBS
You'll be able to ==recognize Amazon EBS as AWS block storage== that ==🟢acts as a virtual disk for EC2.==
Amazon EBS is the ==AWS storage service== that ==🟢gives an EC2 instance a virtual disk==.
1. Amazon EBS is a ==storage service== that ==🟢provides block storage for Amazon EC2==.
2. ==An EBS volume== ==🟢attaches to an EC2 instance== and ==🔵acts like a virtual disk or hard drive.==
3. ==EBS has several volume types==, such as General Purpose SSD and Provisioned IOPS SSD, ==🔵tuned for different performance needs==.

## Amazon S3 (Simple Storage Service)
You'll be able to recognize Amazon S3 as ==AWS's durable, scalable object storage service==.
==Amazon S3== is the ==🟢AWS storage service== that ==🔵keeps any amount of data as objects, reached over the network.==
1. Amazon S3 is ==AWS object storage in the Storage category==.
2. S3 is ==designed for very high durability and virtually unlimited scale==, with ==🟢no capacity to provision first.==
3. You ==reach S3 objects over the network through an API==, unlike ==🔵block storage attached to an instance.==

## Amazon S3 Glacier
You'll be able to recognize S3 Glacier as ==low-cost archive storage== and ==🟢say when slow retrieval is acceptable.==
Amazon S3 Glacier is ==a family of low-cost storage classes== built to ==🔵archive data you must keep but rarely read.==
1. S3 Glacier is ==a group of archive storage classes== in the AWS storage services.
2. You trade ==slower retrieval for lower storage cost==.
3. Use it for rarely accessed data you must keep, such as compliance archives and long-term backups.

## AWS Backup
You'll be able to explain how ==AWS Backup centralizes and schedules backups== ==🟢across AWS services.==
==AWS Backup== is ==🟢a managed storage service== that lets you ==🔵set up and run backups for many AWS services from one place.==
1. AWS Backup is a ==fully managed service in the AWS Storage category==.
2. It ==manages backups for services== such as EBS, RDS, DynamoDB, and EFS ==🟢from a single console.==
3. A ==backup plan== ==🔵defines the schedule and the retention period.==

## AWS Elastic Disaster Recovery
You'll be able to recognize Elastic Disaster Recovery as the AWS service for ==fast server recovery.==
==AWS Elastic Disaster Recovery== ==🟢keeps a current copy of your servers in AWS== so ==🔵you can recover fast.==
1. Elastic Disaster Recovery ==sits in the AWS storage services category.==
2. It ==continuously replicates on-premises or cloud servers to AWS== so ==🟢a current replica is ready to launch.==
3. It ==minimizes downtime and data loss== compared with a traditional backup-and-restore approach.

## AWS Storage Gateway
You'll be able to explain how ==Storage Gateway links on-premises systems to AWS storage==.
==AWS Storage Gateway== is a ==🟢hybrid storage service== that ==🔵lets your on-premises applications use AWS cloud storage== ==🟣without being changed==.
1. Storage Gateway is ==a storage service== that ==🟢connects on-premises environments to AWS cloud storage.==
2. It ==uses standard protocols==, so ==🟢existing applications work without being rewritten to use AWS APIs.===
3. Pick a file, volume or tape gateway based on how your applications already store data.



























