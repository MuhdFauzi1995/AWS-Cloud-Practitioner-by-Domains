# Network services
## VPC components
You'll be able to explain ==how subnets and an internet gateway fit inside an Amazon VPC==.
A ==VPC== is ==🟢your private network in AWS==, ==🔵built from subnets and gateways that work together==.
1. A ==subnet== is ==🟢a smaller segment of the VPC's IP address range==.
2. A subnet is ==public when its route table points to an internet gateway,== and ==🔵private when it does not.==
3. The ==internet gateway attaches to the VPC==, and ==🟢routing decides which subnets can use it.==

## Network ACLs
You'll be able to explain ==how a network ACL filters subnet traffic== and ==🟢how it differs from a security group.==
==A network ACL== is ==🟢a stateless filter== that ==🔵guards the edge of a subnet with ordered allow and deny rules.==
1. A network ACL ==filters traffic at the subnet boundary==, ==🔴not at the instance==.
2. It is stateless, so ==return traffic needs its own explicit rule==.
3. ==Rules can allow or deny== and ==🟢are evaluated by rule number==, ==🔵lowest first==.

## Security groups
You'll be able to explain ==how security groups filter traffic== for ==🟢individual instances==.
A ==security group== is ==🟢a virtual firewall that you attach to a resource==, such as an EC2 instance, to ==🔵control what traffic can reach it and leave it==.
1. A security group ==filters traffic at the instance level==, ==🔴not the subnet level.===
2. Security groups are ==stateful==, so ==🟢return traffic for an allowed request is automatically allowed.==
3. Security groups have ==allow rules only==, with ==🔴no explicit deny==.

Network ACLs and Security groups are almost opposite to one another.
## AWS Direct Connect
You'll be able to explain how ==Direct Connect links your network to AWS privately==, ==🟢without the internet==.
==Direct Connect== is ==🟢a dedicated, private link== ==🔵between your own network and AWS==.
1. Direct Connect is ==a dedicated, private connection== ==🟢from your on-premises network to AWS.==
2. Its traffic ==bypasses the public internet==.
3. It ==gives more consistent performance and bandwidth== than an internet-based connection such as a VPN.

## AWS VPN
You'll be able to explain ==when AWS VPN is the right way to link a network or a user to AWS==.
==AWS VPN== ==🟢gives you an encrypted connection to AWS over the public internet==, ==🔵with no dedicated cable to install.==
1. AWS VPN ==builds an encrypted connection to AWS over the public internet==.
2. It has ==two types==: ==🟢AWS Site-to-Site VPN for networks== and ==🔵AWS Client VPN for users.==
3. ==Choose it (AWS VPN) for fast setup with no dedicated line==; ==🟢choose AWS Direct Connect for a dedicated private link.==

## Amazon API Gateway
You'll be able to recognize ==API Gateway as the managed front door== that ==🟢exposes REST and WebSocket APIs.==
==Amazon API Gateway== is the ==🟢managed front door== that ==🔵lets clients call your application's backend through an API.==
1. API Gateway is ==a managed service== for ==creating, publishing, maintaining, monitoring, and securing APIs.==
2. It is often the ==front door for a serverless application==, ==🟢routing requests to backend compute such as Lambda.==
3. It s==upports RESTful APIs and WebSocket APIs==, and ==🟢AWS lists it under Networking and Content Delivery.==

## Amazon CloudFront
You'll be able to explain ==what CloudFront is== and ==🟢how its edge caching eases the load on your origin.==
==CloudFront== is ==🟢the AWS content delivery network== that ==🔵serves your content from locations close to your users.==
1. ==CloudFront is a CDN== in the ==🟢Networking and Content Delivery category==.
2. It ==serves static and dynamic content from origins== such as Amazon S3 or Amazon EC2.
3. ==Cached copies at edge locations== mean ==🟢fewer requests reach your origin==.

## Amazon Route 53
You'll be able to ==recognize Route 53== as the ==AWS DNS, domain and health check service.==
==Route 53== ==🟢turns friendly domain names into addresses== and ==🔵steers users to healthy resources.==
1. Route 53 is the ==managed DNS service in Networking and Content Delivery,== and it ==🟢can also register domain names.==
2. ==Routing policies like weighted and latency== decide ==🟢how DNS queries are answered across multiple resources.==
3. ==Health checks== let Route 53 route ==🔴traffic away from an endpoint that is failing==.

## Amazon VPC
You'll be able to explain ==what a VPC is== and ==how it connects to other networks.==
==Amazon VPC== gives you ==🟢your own logically isolated virtual network inside AWS==.
1. A VPC is ==a logically isolated virtual network== that ==🟢you define in AWS==.
2. ==EC2 instances and other resources== are ==🟢launched inside a VPC==, and ==🔵its configuration controls their isolation and connectivity.==
3. A VPC ==connects to the internet, other VPCs or on-premises networks== ==🟢through added components such as gateways or peering.==

## AWS Client VPN
You'll be able to explain how AWS Client VPN ==lets individual remote users reach AWS and on-premises resources.==
==AWS Client VPN== ==🟢gives each remote user a secure, managed VPN connection== ==🔵into your AWS and on-premises networks.==
1. Client VPN ==connects individual users' devices== to ==🟢AWS and on-premises resources==.
2. It is ==a fully managed service== that ==🟢scales with demand== and ==🔵uses OpenVPN-based clients.==
3. For ==networks or offices instead of single users==, think ==🟢Site-to-Site VPN==.

## AWS Global Accelerator
You'll be able to explain ==what AWS Global Accelerator does== and ==🟢why its static IP addresses matter.==
==Global Accelerator== ==🟢sends your users onto the AWS global network at the nearest edge==, ==🔵behind fixed IP addresses==.
1. Global Accelerator is ==a Networking and Content Delivery service.==
2. It ==routes user traffic over the AWS global network== ==🔴instead of the public internet.==
3. ==Static anycast IP addresses give you a fixed entry point== and ==🟢simplify failover across Regions.==

## AWS PrivateLink
You'll be able to recognize AWS PrivateLink as ==the way to reach services privately==, ==🟢off the internet.==
==AWS PrivateLink== ==🟢lets your VPC reach a service privately==, ==🔵without sending traffic over the public internet.==
1. PrivateLink is ==a Networking and Content Delivery service== that ==🔵connects VPCs and AWS services privately.==
2. ==Traffic does not cross the public internet==, and ==🟢you need no internet gateway or public IP address.==
3. You ==create a VPC endpoint in your subnets==, and ==🟢the service then acts as if it were local to your VPC.==

## AWS Site-to-Site VPN
You'll be able to explain how Site-to-Site VPN ===links an on-premises network to a VPC===.
==Site-to-Site VPN== ==🟢links your office or data center network to your AWS network== ==🔵through an encrypted connection.==
1. Site-to-Site VPN ==creates an encrypted IPsec connection== ==🟢between an on-premises network and a VPC.==
2. It ==connects two whole networks==, ==🔴not individual users==.
3. ==Client VPN== is ==🟢the service for individual remote users' devices==.

## AWS Transit Gateway
You'll be able to recognize AWS Transit Gateway as ==the central hub== that ==🟢connects your VPCs and on-premises networks.==
==AWS Transit Gateway== is ==🟢a central hub that links your VPCs and on-premises networks ==so ==🔵each one connects only once.==
1. Transit Gateway is ==a Networking and Content Delivery service.==
2. It is ==a central hub== that ==🟢connects multiple VPCs and on-premises networks.==
3. It ==replaces a mesh of VPC peering connections==, because ==🟢each network connects to the hub once.==





































