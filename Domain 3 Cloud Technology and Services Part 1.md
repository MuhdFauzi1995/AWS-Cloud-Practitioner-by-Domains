# Deploying and Operating in the AWS Cloud
## Infrastructure as code (IaC)
You'll be able to explain ==why IaC beats manual console steps== when you ==need the same environment again.==
==Infrastructure as code== ==🟢lets you describe your AWS resources in a file== and ==🔵build them the same way every time. ==
1. IaC ==provisions AWS resources in a repeatable, consistent way==.
2. IaC ==uses a version-controllable template or file== ==🟢instead of manual steps==.
3. ==Pick IaC== ==🟢when the same environment must be deployed many times==, ==🔴not for a one-time Console action.==

## AWS Management Console
You'll be able to say ==when the console fits an interactive, one-off admin task==.
The ==AWS Management Console== is the ==🟢point-and-click way to manage AWS from your browser. ==
1. The console is ==a browser-based, GUI-driven way== to ==🟢administer AWS==.
2. It ==fits one-off, exploratory or ad hoc tasks== because ==🟢a person does each step by hand.==
3. ==Programmatic access and infrastructure as code== are the choice ==🟢when work must be scripted or repeated.==

## Programmatic access
You'll be able to ==pick APIs, SDKs or the CLI== when ==a task must be scripted or repeated.==
==Programmatic access== ==🟢lets scripts and code talk to AWS==, so ==🔵you do not have to click through the console. ==
1. Programmatic access means ==using the AWS CLI, SDKs or APIs== ==🔴instead of the Management Console.==
2. Pick it ==for tasks that repeat or run on a schedule==, because ==🟢scripts do not need a person clicking.==
3. An ==AWS SDK== ==🟢lets a developer call AWS service APIs from their own application code.==

## One-time vs repeatable tasks
You'll be able to ==choose between== a ==🟢manual one-time task== and an ==🔵automated repeatable process.==
==Look at how often you do a task== and ==how identical each run must be==, then ==🟢pick manual or automated. ==
1. ==Decide by analyzing requirements==: ==🟢how often the task runs== and ==🔵how identical each run must be.==
2. ==Use a manual one-time operation== for an ==🟢infrequent, one-off task.==
3. ==Use a repeatable automated process== for ==🔵routine tasks or tasks that must run identically many times.==

## Cloud deployment model
You'll be able to ==explain the cloud deployment model== and ==🟢tell it apart from hybrid and on-premises.==
In the cloud deployment model, ==your whole application runs in the cloud.== 
1. A cloud deployment ==runs all parts of the application in the cloud.==
2. It can be ==built in the cloud== or ==🟢migrated there from existing infrastructure.==
3. ==Hybrid and on-premises== are ==🔵the other two deployment models you must identify==.

## ==Hybrid deployment== model
You'll be able to ==recognize a hybrid deployment== and ==🟢explain why organizations use it.==
Hybrid means ==your systems run partly on premises and partly in the cloud==, and ==🔵the two sides are connected. ==
1. Hybrid combines on-premises infrastructure with cloud infrastructure, and the two are connected.
2. It is ==one of the deployment models== you ==must be able to identify on the exam.==
3. Hybrid is ==often a first step== in a ==🟢gradual migration to the cloud.==

## ==On-premises== deployment model
You'll be able to ==explain what on-premises means== and ==who owns the hardware, upkeep and growth.==
On-premises means ==you run IT on hardware you own, in your own facility==, ==🟢without a cloud provider. ==
1. On-premises means the ==infrastructure is owned and run by your own organization on site==, with ==🔴no cloud provider involved.==
2. You must ==buy, maintain, and scale your own physical hardware==, which ==🟢often means upfront investment and ongoing upkeep.==
3. ==In a cloud model== ==🟢the provider manages the physical infrastructure==, and that is ==🔵the key contrast to remember.==

## AWS CloudFormation
You'll be able to ==explain what AWS CloudFormation does== and ==how templates describe an end state.==
==CloudFormation turns a text file into real AWS resources==, so you ==🟢describe what you want and AWS builds it. ==
1. CloudFormation ==builds and manages AWS resources== ==🟢from a YAML or JSON template.==
2. ==A template describes the desired end state==, and ==🟢CloudFormation works out the create, update or delete actions.==
3. CloudFormation is ==part of the Management and Governance category of AWS services==.

## AWS Service Catalog
You'll be able to explain ==how AWS Service Catalog gives users a curated list of approved IT services.==
==AWS Service Catalog== ==🟢lets an organization publish a list of approved IT services== that ==🔵people can launch on their own. ==
1. Service Catalog is ==a Management and Governance service== for ==🟢catalogs of approved IT services.==
2. ==Administrators curate the list and set the rules==, and ==🟢users launch from it on their own.==
3. ==Think approved and self-service== whenever a question mentions a curated list of allowed resources.

## Service Quotas
You'll be able to explain ==how Service Quotas shows and manages the limits on your AWS resources.==
==Service Quotas== is ==🟢the one place to see the limits on your AWS account== and ==🔵ask for higher ones. ==
1. Service Quotas ==lets you view and manage the limits on AWS resources in your account from one place.==
2. ==Some quotas can be raised by a request through Service Quotas==, while ==🔴hard limits cannot.==
3. Service Quotas ==belongs to the Management and Governance category of AWS services==.


