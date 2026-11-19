# Compute Services
## EC2 instance types
You'll be able to ==match a workload to the right EC2 instance type family==.
==Pick the EC2 instance family== ==🟢whose strongest resource== ==🔵matches what your workload needs most.==
1. ==Each EC2 family== is ==🟢built around a resource mix==: ==🔵balanced, CPU, memory, or local storage.==
2. ==Match the workload's main need to the family==: ==🟢batch and transcoding to compute==, ==🔵in-memory databases to memory==, ==🟣large local datasets to storage==.
3. ==If no single resource dominates==, ==🟢general purpose is the balanced choice.==

## Amazon ECS
You'll be able to explain ==what Amazon ECS does== and ==when to pick it over Amazon EKS.==
==Amazon ECS== is the ==🟢AWS-native service== that ==🔵runs and manages your containers for you.==
1. Amazon ECS is ==a fully managed, AWS-native container orchestration service==.
2. ==ECS schedules, places and scales your containers== ==🟢across the compute you give it.==
3. ==Pick ECS== when ==🟢you do not need Kubernetes==; ==🔵pick Amazon EKS== ==🟣when you do==.

## Amazon EKS
You'll be able to explain ==when Amazon EKS is the right choice== for ==🟢running Kubernetes on AWS.==
==Amazon EKS== is the AWS service for ==🟢running standard Kubernetes without operating the Kubernetes control plane yourself.==
1. Amazon EKS is ==managed Kubernetes==: ==🟢AWS runs the control plane for you.==
2. ==It runs upstream, certified-conformant Kubernetes==, so ==🟢standard Kubernetes applications and tools carry over.==
3. ==Choose Amazon EKS ==when the ==🟢workload needs Kubernetes==; ==🔵Amazon ECS is the AWS-native alternative.==

## AWS Fargate
You'll be able to explain ==when AWS Fargate is the right way to run containers== ==🔴without managing servers.==
==Fargate== ==🟢runs your containers for you==, so you ==🔵never have to manage the servers underneath.==
1. Fargate is ==serverless compute for containers==: ==🟢no EC2 instances to provision or manage.==
2. You ==launch Fargate containers== ==🟢through Amazon ECS or Amazon EKS.==
3. ==Pick Fargate== for ==🟢containerized workloads and Lambda for event-driven functions==; ==🔵you pay for the vCPU and memory used==.

## AWS Lambda
You'll be able to explain ==when Lambda fits, how it scales, and how it is billed.==
==Lambda== ==🟢runs your code when something happens==, and ==🔵you never manage a server.==
1. Lambda ==runs code in response to events== ==🟢without you provisioning or managing servers.==
2. Lambda ==🟢scales by running more concurrent copies of your function== ==🔵as events increase.==
3. You ==pay for requests and compute time used==, ==🟢and events often come from services like Amazon S3 and Amazon SQS.==

## Load balancers
You'll be able to explain ==how a load balancer spreads traffic, checks health and keeps an app running.==
==A load balancer== ==🟢shares incoming traffic across several healthy targets==, so ==🔵one failure does not take your app down.==
1. A load balancer ==distributes incoming traffic across multiple targets== ==🟢so none is overwhelmed.==
2. It ==runs health checks and stops routing traffic to targets that fail them==.
3. ==Spreading traffic over healthy targets gives fault tolerance==, so ==🟢one failure need not interrupt the app.==

## Amazon EC2
You'll be able to ==recognize Amazon EC2== as ==🟢AWS's resizable virtual server service.==
==Amazon EC2== ==🟢gives you virtual servers in the cloud that you can resize and pay for as you use them.==
1. EC2 is ==a compute service== that ==🟢provides resizable virtual servers called instances.==
2. ==Instance types come in families==, such as ==🟢compute, memory, or storage optimized==, to ==🔵fit different needs.==
3. You ==launch from an AMI== and ==🟢pay for the capacity you use== ==🔵while scaling up, down, or out.==

## Amazon Lightsail
You'll be able to ==recognize Amazon Lightsail== as ==🟢AWS's simple, predictable-price option for small workloads.==
==Amazon Lightsail== is the easy way to ==🟢get a simple server running on AWS for a low, predictable price.==
1. Lightsail is ==an AWS compute service== that ==🟢bundles a virtual private server with storage and networking== at a ==🔵predictable monthly price==.
2. It ==fits simple workloads== such as ==🟢basic websites, blogs, and small applications.==
3. It is ==a simpler alternative to EC2==: ==🟢easier setup, less flexibility.==

## AWS Batch
You'll be able to ==recognize AWS Batch== as the ==🟢compute service that runs and scales batch jobs for you.==
==AWS Batch== is ==🟢the AWS compute service== that ==🔵runs your batch jobs and sets up the compute resources for you.==
1. AWS Batch is ==an AWS Compute service== for ==🟢batch computing workloads.==
2. It ==plans, schedules, and runs your batch jobs== ==🟢across AWS compute resources.==
3. It ==automatically provisions the right type and quantity of compute==, ==🔴so you do not manage a cluster.==

## AWS Elastic Beanstalk
You'll be able to recognize ==Elastic Beanstalk as the AWS service== that ==runs uploaded web apps for you.==
==Elastic Beanstalk== lets you ==🟢upload web application code== while ==🔵AWS sets up and runs the servers underneath.==
1. ==Elastic Beanstalk== is ==🟢a compute service and a PaaS== for ==🔵deploying and scaling web applications.==
2. ==You upload code== and ==🟢AWS handles provisioning, load balancing, and scaling for you==.
3. ==You get less direct infrastructure control than with hand-configured EC2==, ==🟢in return for simpler deployment.==

## AWS Outposts
You'll be able to explain ==what AWS Outposts is== and ==when to choose it over the AWS Region.==
==AWS Outposts== ==🟢brings AWS infrastructure, services, and tools into your own building.==
1. Outposts ==puts AWS-managed infrastructure and services== ==🟢in your own data center==.
2. You ==use the same APIs and tools as in an AWS Region.==
3. Choose it ===for low latency to local systems or data=== ==🟢that must stay on premises==.

## Amazon ECR
You'll be able to ==recognize Amazon ECR as the AWS container service== that ==stores container images.==
==Amazon ECR== is the place on AWS ==🟢where you keep your container images== ==🔵until a service needs to run them.==
1. Amazon ECR is ==a managed registry== for ==🟢storing, managing, and deploying container images.==
2. ECR is== part of the AWS containers services family.==
3. ==ECS and EKS pull images from ECR== to ==🟢run containers==; ==🔵ECR itself only stores them.==

## AWS Auto Scaling
You'll be able to ==recognize AWS Auto Scaling== and ==explain how it matches capacity to demand.==
==AWS Auto Scaling== ==🟢adds and removes capacity for you==, so ==🔵your application keeps up with demand without paying for idle resources.===
1. AWS Auto Scaling ==sits in the Management and Governance category== and ==🟢adjusts capacity automatically.==
2. It ==keeps performance steady during demand spikes== and ==🟢avoids paying for peak capacity all the time.==
3. ==One scaling configuration== can ==cover multiple services, such as EC2, ECS, and DynamoDB.==









