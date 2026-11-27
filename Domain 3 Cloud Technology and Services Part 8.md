# Other AWS services
## Amazon EventBridge
You'll be able to explain how ==EventBridge rules route events== and ==🟢how it differs from SQS and SNS.==
==Amazon EventBridge== ==🟢checks each event against rules== and ==🔵sends it to the targets that should react.==
1. EventBridge ==uses rules that match an event's content== to ==🟢route it to one or more targets==.
2. Events can ==come from AWS services, custom applications, and SaaS partners==.
3. ==SQS queues messages== and ==🟢SNS broadcasts them==, while ==🔵EventBridge routes by rule.==

## Amazon SNS
You'll be able to explain how Amazon SNS ==fans one message out to many subscribers.==
Amazon SNS ==sends one message to many receivers at once==, using ==🟢a publish and subscribe model.==
1. Amazon SNS is a ==pub/sub service:== ==publishers send to a topic== and ==🟢all subscribers receive the message.==
2. ==Fanout means one published message is delivered to many subscribers==, such as SQS queues, Lambda functions, email or SMS.
3. SNS supports ==application-to-application== and ==🔵application-to-person messaging==.

## Amazon SQS
You'll be able to explain how Amazon SQS ==decouples application parts using a message queue.==
Amazon SQS lets ==one part of an application hand work to another through a queue==, so ==🟢neither has to wait for the other.==
1. SQS is a managed message queue that ==decouples the parts of an application.==
2. A ==producer and a consumer== ==🟢do not need to interact directly or at the same time==.
3. The q==ueue holds each message== until ==🟢a consumer retrieves and processes it==, which ==🔵buffers against a slow or unavailable consumer==.

## Amazon Connect
You'll be able to explain what Amazon Connect does and ==why it replaces on-premises call center hardware.==
Amazon Connect is ==a cloud contact center== ==🟢you set up and scale== ==🔵without buying phone hardware.==
1. Amazon Connect is a cloud-based contact center ==for customer service over voice and chat.==
2. It s==cales with demand== and ==🟢needs no on-premises telephony hardware.==
3. ==Sending email is a different job==, ==🟢handled by Amazon SES,== not by Amazon Connect.

## Amazon SES
You'll be able to explain when to ==choose Amazon SES== to ==🟢send email from an application.==
==Amazon SES== ==🟢lets your application send transactional and marketing email at scale== ==🔴without you running mail servers.==
1. Amazon SES ==sends transactional and marketing email== ==🟢from within your applications.==
2. SES is u==sed programmatically by software==, ==🔴not as an end-user inbox.==
3. SES is ==scalable==, so you can ==🔵send large volumes without running your own mail servers.==

## Choosing an AWS Support plan
You'll be able to ==match a business's response-time and advice needs== to the ==🟢right AWS Support plan.==
You ==pick an AWS Support plan ==by asking ==🟢how fast you need help== and ==🔵how much expert advice you want.==
1. Choose the plan by ==two needs==: how fast you need a response and how much advice you want.
2. A ==business with mission-critical workloads== ==🟢needs a higher tier than one that only needs account and billing help.==
3. ==Higher tiers== give ==🔵faster response times and more proactive architectural guidance.==

## AWS X-Ray
You'll be able to explain how AWS X-Ray ==traces requests== and ==🟢shows a service map to find problems.==
==AWS X-Ray== ==🟢follows a request through every part of your application== so you can ==🔵see which piece is failing or slow.==
1. AWS X-Ray is the tool for ==troubleshooting distributed, multi-service applications====.
2. It ==traces a request end to end== so you can ==🟢pinpoint the component causing a fault or slowdown.==
3. Its service map shows ==how requests flow and highlights== ==🔵where latency or errors occur.==

## AWS CodeBuild
You'll be able to explain what AWS CodeBuild does and ==tell it apart from deployment and tracing tools.==
==AWS CodeBuild== is the managed AWS service that ==compiles your code, runs your tests, and packages the result.==
1. CodeBuild ==compiles source code, runs tests, and produces packages== that are ==ready to deploy.==
2. You ==never provision or manage build servers==, because ==CodeBuild scales its capacity for you.==
3. ==Building and testing is a different job== from ==🟢deploying code or tracing a running application.==

## AWS CodePipeline
You'll be able to explain how CodePipeline ==automates a release through stages and other developer tools.==
==AWS CodePipeline== ==automates your release process==, ==🔵from a code change all the way to deployment.==
1. CodePipeline is the AWS tool that ==orchestrates the end-to-end release process (continuous delivery).==
2. A ==pipeline is a series of stages==, such as source, build, test, and deploy, and ==🟢each stage holds actions.==
3. CodePipeline can ==run other AWS developer tool==s, such as CodeBuild, as ==🟢stages in the same pipeline.==

## Amazon AppStream 2.0
You'll be able to explain how AppStream 2.0 ==streams applications to any device without local installs.==
==AppStream 2.0== ==🟢runs an application on AWS== and ==🔵streams what it shows to the user's device.==
1. AppStream 2.0 ==presents the output of virtual machines on the user's device.==
2. It is an ==application streaming service==, while ==🟢WorkSpaces provides a persistent cloud desktop.==
3. ==Users get the same app on different devices== with ==🔴no local install or upkeep==.

## Amazon WorkSpaces
You'll be able to explain when Amazon WorkSpaces is the right way to ==deliver persistent cloud desktops.==
==Amazon WorkSpaces== gives each user ==🟢a persistent, full desktop in the cloud== ==🔵that they can reach from many devices.==
1. WorkSpaces ==provides a persistent full desktop== ==🟢with its own operating system and applications.==
2. It ==removes the need to buy and manage physical desktop hardware==.
3. ==🔴Do not confuse it with AppStream 2.0==, which streams applications, or ==🔴WorkSpaces Secure Browser==, which gives browser-only access.

## Amazon WorkSpaces Secure Browser
You'll be able to explain how Secure Browser ==gives safe, browser-only access to internal web apps.==
==Amazon WorkSpaces Secure Browser== lets people reach ==🟢private web apps through a hosted browser== ==🔴instead of a full virtual desktop==.
1. Secure Browser ===streams a hosted browser to the user===, so ==🟢private web apps stay isolated in AWS.==
2. It gives ==browser-only access==, not a full virtual desktop, so it is a ==🟢lighter option than Amazon WorkSpaces.==
3. Admins ==control sessions== with ==🟢URL allow and block lists, clipboard, file transfer and printer settings, and IP access controls.==

## AWS Amplify
You'll be able to explain what AWS Amplify ==does for web and mobile apps== and ==when to choose it.==
==AWS Amplify== helps developers ==🟢build, host and release whole web and mobile apps, frontend and backend together.==
1. Amplify ==creates and deploys frontend and mobile apps==.
2. It combines ==hosting, backend setup and CI/CD in one toolchain==.
3. It adds ==ready-made features like authentication and storage==, so it ==🟢covers the whole app, not just an API.==

## AWS AppSync
You'll be able to ==explain what AWS AppSync does== and ==why apps use it for GraphQL APIs.==
==AWS AppSync== is ==🟢a managed service for building GraphQL APIs==, so ==🔵your app can fetch data from many places in one request.==
1. AppSync is a managed service for ==building GraphQL APIs.==
2. ==One GraphQL query== can ==🟢pull data from several sources==, ==🔴instead of many REST calls==.
3. ==AppSync is the API layer between your app and your data==, nothing more.

## AWS Step Functions
You'll be able to explain what Step Functions does and ==spot it in Application Integration questions.==
==Step Functions is a serverless service== that ==🟢runs several AWS services in a set order as one workflow.==
1. Step Functions is ==an Application Integration service== and it is ==🟢serverless.==
2. It ==orchestrates many AWS services into one workflow==, ==🟢defined as a state machine.==
3. The state machine ==sets the order of steps== and ==🔵how errors and retries are handled==.

## AWS CLI
You'll be able to explain what the AWS CLI is and ==why it suits scripts and repeatable tasks.==
The ==AWS CLI ==lets you ==manage AWS== by ==🟢typing commands instead of clicking in the console.==
1. The AWS CLI is ==one unified command-line tool== for ==🟢managing many AWS services.==
2. The same commands ==work in a terminal or in a script==.
3. Scripts make the CLI ==a good fit for automation and repeatable tasks.==

## AWS IoT Core
You'll be able to recognize AWS IoT Core as ==the service that connects devices to AWS and routes their data.==
==AWS IoT Core== ==🟢connects internet-connected devices to AWS and to each other==, then ==🔵routes their data onward==.
1. AWS IoT Core is ==a managed service in the Internet of Things (IoT) category==.
2. It ==lets connected devices securely interact with AWS services== and ==🟢with each other==.
3. It ==processes and routes data from huge numbers of devices== to ==🔵other AWS services for storage or analysis.==



























