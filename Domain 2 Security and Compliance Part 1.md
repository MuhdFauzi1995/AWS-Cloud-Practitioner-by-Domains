# The AWS shared Responsibility Model
## Security OF the cloud vs IN the cloud
1. There are exactly two components: 
	1. security of the cloud (AWS) and 
	2. security in the cloud (you).
2. AWS protects the infrastructure that runs every service. You protect your configuration, applications and data.
3. Both components apply to every service. The service you choose changes the size of your share, not whether you have one.
## Data protection
1. You classify your own data by sensitivity.
2. You decide how your data is encrypted and who holds the keys.
3. This stays your job even when AWS runs the service, such as Amazon S3.
## Guest OS patching
1. You patch and configure the guest OS and the applications on your own EC2 instances.
2. EC2 is infrastructure as a service, so the guest OS is your side of the shared responsibility model.
3. AWS manages the host OS and virtualization layer, and tools like Patch Manager help but do not take over your duty.
## IAM configuration
1. Creating IAM users, groups, and roles, and assigning their permissions, is your responsibility.
2. A policy that grants overly broad access is a customer-side security gap, not an AWS failure.
3. AWS secures the infrastructure; you secure how people and services access your account.
## Network protection rules
1. Configuring security groups and network ACLs for your own resources is a customer responsibility.
2. A security group that is open to all inbound traffic is the customer's misconfiguration, not an AWS failure.
3. Follow least privilege: allow only the network access you actually need.
## Network and virtualization layer
1. AWS secures the global network that links Regions, Availability Zones, and edge locations.
2. AWS secures the hypervisor that isolates one customer's instances from another's.
3. You cannot inspect or patch the hypervisor, because it belongs to AWS's side of the model.
## Physical infrastructure
1. AWS is responsible for the physical security of the data centers that house its infrastructure.
2. AWS maintains hardware and securely decommissions storage devices before they leave its control.
3. AWS restricts and monitors physical access to data centers, so you do not manage it.
## Shared controls
1. A shared control applies to both AWS and you, in separate contexts, so neither side holds it alone.
2. The three examples are patch management, configuration management, and awareness and training.
3. In each one AWS handles its own infrastructure and people, and you handle your guest OS, applications, settings and staff.
## Managed and serverless services
1. AWS takes on more responsibility for managed and serverless services than for services like Amazon EC2.
2. With Amazon RDS, AWS handles tasks such as operating system patching, and with AWS Lambda you have no servers to manage.
3. With Amazon EC2 you manage the guest operating system and the software above it.
## Infrastructure services
1. On EC2, you manage the guest OS, patches, your applications and the security group.
2. AWS still runs the host OS, virtualization layer and physical facilities.
3. With Amazon RDS, AWS patches the database engine, so your share is smaller.