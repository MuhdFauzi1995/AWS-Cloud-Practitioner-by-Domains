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