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