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