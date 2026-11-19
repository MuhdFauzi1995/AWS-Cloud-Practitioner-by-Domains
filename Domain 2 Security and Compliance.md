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
 
# Security, governance and compliance
## Cloud vs on-premises security
1. AWS secures the infrastructure that runs its services, so you carry less of the security and patching work than on-premises.
2. Managed services and built-in encryption give you ready-made security functions instead of tools you build and run.
3. AWS invests in security at scale, and all customers inherit those improvements.
## Compliance by geography and industry
1. Compliance requirements differ by geographic location and by industry.
2. HIPAA and PCI DSS are examples of sector-specific frameworks, for health data and payment card data.
3. AWS Artifact gives you AWS compliance reports, but you must still follow the rules that apply to you.
## AWS Security Hub
1. Security Hub gathers findings from AWS services like GuardDuty and Inspector, plus third-party tools, into one view.
2. It runs automated, continuous checks against best-practice standards such as AWS Foundational Security Best Practices.
3. On the exam, pick Security Hub when the need is a single, central view of security findings.
## AWS Shield
1. AWS Shield defends your resources against DDoS attacks that threaten availability.
2. Shield Standard is automatic, free, and covers common layer 3 and 4 attacks.
3. Shield Advanced is a paid upgrade with layer 7 protection, attack visibility and cost protection.
## Amazon GuardDuty
1. GuardDuty continuously looks for malicious or unauthorized activity using threat intelligence and anomaly detection.
2. It analyzes CloudTrail events, VPC Flow Logs, and DNS logs without separate security software.
3. GuardDuty detects signs of attacks, while a vulnerability scanner such as Amazon Inspector finds weaknesses.
## Amazon Inspector
1. Inspector scans EC2 instances, container images and more for known software vulnerabilities and unintended network exposure.
2. Inspector rescans on its own when your environment changes, so you do not rely on a one-time manual scan.
3. Inspector finds weaknesses in your own resources, while GuardDuty detects signs of suspicious activity.
## Encryption at rest
1. Encryption at rest protects stored data, such as data on a disk or in a database.
2. Without the right key, the stored data cannot be read, even if someone reaches the storage directly.
3. Services like Amazon S3 and Amazon EBS support it, often with AWS KMS managing the keys.

## Encryption in transit
1. Encryption in transit protects data while it moves across a network.
2. TLS is the common way AWS services encrypt data between your application and the service.
3. Encryption at rest protects stored data. Encryption in transit protects moving data.

## Access reports
1. Access reports give you reporting on access, which supports governance and compliance.
2. Last-used data shows which granted permissions are unused, so you can remove them.
3. An access report is a reporting tool, separate from CloudWatch monitoring and from CloudTrail, Config, and Audit Manager auditing.

## AWS CloudTrail
1. CloudTrail records who took an action, what the action was, and when it occurred.
2. The record can be reviewed after the fact to investigate an incident or verify compliance.
3. CloudTrail records that actions happened; AWS Config evaluates a resource's current state against a rule.

## AWS Audit Manager
1. Audit Manager collects evidence automatically and continually, not just before an audit.
2. It maps evidence to the controls of a compliance framework.
3. An activity log records what happened. Compliance assessment checks evidence against requirements.

## AWS Config
1. AWS Config continuously records resource configurations and how they change over time.
2. Config rules check those configurations and flag resources that become noncompliant.
3. Config shows what a resource looked like; CloudTrail shows who made the API call.

## Amazon CloudWatch
1. CloudWatch collects metrics and logs from your resources and applications and watches them in real time.
2. An alarm can send a notification or trigger an automatic action such as Auto Scaling when a threshold is breached.
3. CloudWatch monitors performance and health, while CloudTrail audits who did what through API calls.

## Compliance across AWS services
1. Compliance certifications vary from one AWS service to another.
2. Always verify that the specific service you plan to use covers the certification your workload needs.
3. HIPAA covers only a named list of eligible services, not all of AWS.

## AWS Control Tower
1. AWS Control Tower is a management and governance service that creates a landing zone, a secure multi-account environment based on blueprints.
2. Guardrails are preventive (block risky actions) or detective (alert on non-conformance) rules applied across the accounts.
3. Choose it when you provision and govern many related accounts, not for configuring a single account.

## AWS Artifact
1. AWS Artifact gives on-demand access to AWS compliance reports such as SOC and PCI.
2. It also lets you review and accept select agreements, such as the BAA.
3. It is self-service: you download documents yourself, and it does not check your own resources.

## AWS Resource Access Manager (RAM)
1. AWS RAM is a Security, Identity, and Compliance service that shares resources you own with other AWS accounts.
2. You can share within an AWS Organization or with accounts outside it.
3. Other accounts use the shared resource directly, so you do not duplicate it in each account.
# Access management
## Root user risks
1. The root user has complete access to every service and resource in the account.
2. You cannot limit root's permissions, while an IAM user's access is bounded by its policies.
3. A stolen root credential is a bigger risk than a stolen IAM user credential, so protect root and avoid everyday use.

## Principle of least privilege
1. Least privilege means granting only the permissions needed to do a task, and no more.
2. It limits the damage if credentials are exposed, because the attacker gets only that narrow set of permissions.
3. Start from no permissions or a managed policy, then refine based on what is actually used.

## Secrets and credential storage
1. Secrets Manager and Systems Manager Parameter Store are the AWS examples of centralized credential storage.
2. Keep secrets in the service, not in application source or configuration files.
3. Your application fetches the secret at run time with a call to the service.

## IAM access keys
1. An access key (ID plus secret) is for programmatic access through the CLI, SDKs and APIs, not console sign-in.
2. Access keys are long-lived, so a leaked key is an ongoing risk until it is rotated or deactivated.
3. Prefer temporary credentials from an IAM role over creating long-term access keys.

## IAM password policies
1. A password policy is an account-level rule set that an administrator configures for IAM user passwords.
2. Length and complexity rules lower the risk of a console password being guessed or brute-forced.
3. The policy can require rotation and block reuse of earlier passwords.

## Cross-account IAM roles
1. A cross-account role gives a principal from one account temporary access to resources in another account.
2. The access uses temporary security credentials, not long-lived access keys, and needs no duplicate IAM user.
3. Central security or operations accounts commonly use these roles to manage many member accounts.

## AWS IAM Identity Center
1. IAM Identity Center is a single sign-on service for many AWS accounts and business applications.
2. Users sign in once and see everything assigned to them in one user portal, with no separate credentials per account.
3. A cross-account IAM role reaches from one account into another. It does not centralize sign-in.

## Multi-factor authentication (MFA)
1. MFA requires a second factor, such as a code from a virtual or hardware device, in addition to a password.
2. MFA reduces the risk of unauthorized access even when a password is compromised.
3. You can enable MFA for the root user and for IAM users, and each identity has its own MFA configuration.

## Custom IAM policies
1. 1A custom IAM policy is a JSON document that allows or denies actions on specific resources.
2. 2It can be narrower than an AWS managed policy, for example by naming resource ARNs or conditions.
3. 3You trade the convenience of a managed policy for finer control over permissions.

## IAM groups and users
1. Attach a policy to a group and every member gets it.
2. Build groups by job function to keep access least-privilege.
3. A user in several groups receives the combined permissions.

## AWS managed IAM policies
1. AWS managed policies give you common, predefined permission sets.
2. AWS creates, administers and updates them, so you do not edit them.
3. They are faster to apply than writing a policy yourself.

## Tasks that require the root user
1. Some tasks need the root user, and IAM policies cannot delegate them.
2. Examples: change the account email, close the account, enable MFA on an S3 bucket, restore IAM permissions.
3. Use the root user only for these tasks; use an administrative user otherwise.

## Protecting the root user
1. Turn on MFA for the root user and give it a strong, unique password.
2. Do not use the root user for daily tasks; use IAM users or roles instead.
3. Do not create root access keys, because they would give powerful programmatic access to an identity with unrestricted access.

## Federated identity management
1. Federation means signing in with an existing identity from an external identity provider, not a native IAM user.
2. After sign-in, the federated identity gets temporary security credentials.
3. It saves you from creating and maintaining an IAM user for every person.

## AWS Systems Manager
1. Systems Manager is a Management and Governance service for visibility and control of EC2 and on-premises servers.
2. Session Manager connects you to an instance with no inbound ports and no SSH keys.
3. Parameter Store holds configuration data and secrets for applications and instances to retrieve.

## Amazon Cognito
1. Cognito manages sign-up, sign-in and identity for the end users of your web or mobile app.
2. A user pool is the user directory that handles sign-up and sign-in.
3. An identity pool hands users temporary AWS credentials so they can use other AWS services directly.

## AWS Directory Service
1. Directory Service is a security, identity, and compliance service that provides managed Microsoft Active Directory.
2. It can let AWS resources use existing on-premises Active Directory credentials.
3. AWS removes the work of installing and maintaining directory servers that you would carry yourself on EC2.

## AWS IAM
1. IAM controls who is authenticated and what they are authorized to do in your AWS account.
2. IAM manages users, groups, roles, and policies, and policies define the permissions.
3. IAM is global, so its identities are not scoped to a single Region.

## AWS Secrets Manager
1. Secrets Manager securely stores secrets such as database credentials and API keys.
2. It can automatically rotate a secret on a schedule you define.
3. Applications fetch the secret at runtime through an API call instead of hardcoding it.


# Security components and resources
## AWS Firewall Manager
1. 1Firewall Manager centrally manages firewall rules, such as AWS WAF rules and security groups, across accounts.
2. 2Protections are set up once and applied automatically, including to new accounts and resources.
3. 3AWS WAF defines the web rules, and Firewall Manager deploys and manages them across many accounts.

## AWS WAF
1. AWS WAF filters web requests at the application layer to help stop exploits such as SQL injection and cross-site scripting.
2. Rules can match IP addresses, request content, or request rate, and then allow, block, or count the traffic.
3. Firewall Manager deploys WAF rules across accounts, and Shield covers network and transport layer DDoS attacks.

## AWS security guidance
1. Three AWS-provided sources are named: the Knowledge Center, the Security Center, and the Security Blog.
2. The Security Blog publishes ongoing articles on security announcements, features, and best practices.
3. You can go straight to AWS resources for security guidance instead of relying only on third parties.

## Trusted Advisor security checks
1. Trusted Advisor is a service for identifying security issues.
2. It flags things like security group rules open to the whole internet on specific ports.
3. It checks configuration against best practices, not live threats or software flaws.

## AWS Trusted Advisor
1. Trusted Advisor inspects your account and recommends actions across categories like cost, performance, security, and fault tolerance.
2. It compares your configuration against AWS best practices.
3. Your AWS Support plan decides how many checks you get.


## Amazon Detective
1. Detective sits in the Security, Identity, and Compliance category and helps you find the root cause of a security issue.
2. It automatically collects and correlates data such as AWS CloudTrail logs and GuardDuty findings.
3. It investigates findings that already exist. It does not detect threats.

## Amazon Macie
1. Macie uses machine learning and pattern matching to find sensitive data such as PII in Amazon S3.
2. Macie also evaluates the security and access controls of your S3 buckets.
3. Macie reports what it finds as findings that show the type and location of the sensitive data.

## AWS Certificate Manager (ACM)
1. ACM is a Security, Identity, and Compliance service that provisions, manages, and deploys SSL/TLS certificates.
2. ACM manages renewal so you do not renew certificates by hand.
3. Certificates used with integrated services such as Elastic Load Balancing or CloudFront are free.

## AWS CloudHSM
1. CloudHSM provides dedicated, single-tenant hardware security modules for your cryptographic keys.
2. The HSMs are validated against government standards such as FIPS 140-2 level 3 or FIPS 140-3 level 3.
3. You control the HSMs directly, so you also take on more responsibility than with a fully managed service.

## AWS KMS
1. AWS KMS creates and manages the cryptographic keys that encrypt and decrypt your data.
2. Many AWS services integrate with AWS KMS to give you server-side encryption of data at rest.
3. AWS KMS performs cryptographic operations for you, and you never see the plaintext key material.



























