# Benefits of AWS Cloud
1. Speed of deployment
2. Global reach
3. Agility
4. Elasticity
5. High availability

## Speed of deployment
1. You can deploy resources into a new Region within minutes, with just a few clicks.
2. Deployment speed is a different benefit from global reach and low latency.
3. Speed removes the weeks or months of waiting for hardware that on-premises capacity needs.
## Global reach
1. AWS global infrastructure lets one provider serve users in many parts of the world.
2. Reach comes from AWS spreading its infrastructure across many geographic locations, and you pick the Regions closest to your users.
3. Without AWS, you would have to build and operate your own infrastructure in each geography.
## Agility
1. Agility means resources arrive in minutes, not weeks.
2. Experimenting costs less time and money, so you can test more ideas.
3. You can drop an idea that fails without a heavy upfront investment behind it.
## Elasticity
1. Elasticity means scaling capacity up or down to match actual demand.
2. Elasticity is not agility: agility is speed of provisioning, elasticity is fit to demand.
3. You scale out for spikes and back in afterward, so you avoid paying for idle capacity.
## High availability
1. High availability means a system keeps operating correctly despite component failures.
2. Elasticity matches capacity to demand, which is a different goal from surviving failure.
3. Agility is about speed of provisioning and experimenting, not about continuing through failure.

# Design Principles of AWS Cloud

## 6 Well-Architected Pillars
1. Cost optimization
2. Operational excellence
3. Performance efficiency
4. Reliability
5. Security
6. Sustainability
### Cost optimization pillar
1. Cost optimization is one of the six Well-Architected pillars.
2. It focuses on avoiding unnecessary costs.
3. It means right resources, right amount, and scaling without overspending.
### Operational excellence pillar
1. Operational excellence is one of six separate Well-Architected pillars.
2. It covers running and monitoring systems to deliver business value and continually improving processes and procedures.
3. Key practices include frequent, small, reversible changes and automating responses to operational events.
### Performance efficiency pillar
1. Performance efficiency is one of the six Well-Architected pillars.
2. It is about using computing resources efficiently to meet requirements, and staying efficient as demand and technology change.
3. Experimenting with different resource types and configurations helps you find the best fit for a workload.
### Reliability pillar
1. Reliability is one of the six Well-Architected pillars.
2. It is about recovering from failure and still doing the intended job correctly and consistently.
3. Automatic recovery and horizontal scaling are core reliability practices.
### Security pillar
1. Security is one of the six Well-Architected pillars.
2. The pillar is about protecting data, systems and assets, guided by seven design principles.
3. Two key principles are a strong identity foundation and security at every layer.
### Sustainability pillar
1. Sustainability is one of the six Well-Architected pillars.
2. The pillar focuses on minimizing the environmental impact of running workloads.
3. 3Maximizing utilization of provisioned resources reduces the energy needed to support a workload.
## Telling the pillars apart
1. Reliability asks whether the workload keeps working and recovers from failure. Performance efficiency asks whether the resources fit the workload.
2. Cost optimization and sustainability can overlap, so choose by the primary concern: unnecessary spending or environmental impact.
3. The security pillar is a design guide for protecting data and systems. It is not the same as the shared responsibility model or compliance programs.
## AWS Well-Architected Tool
1. The tool is available at no additional charge; you pay only for the underlying AWS resources.
2. It reviews a workload against the Well-Architected Framework pillars through a set of questions.
3. It returns a plan of improvements, and AWS lists it under Management and Governance.

# Migration to AWS Cloud
## 4 Business Benefits of adopting AWS CAF
1. Improved ESG performance
2. Improved Operational efficiency
3. Improved Revenue
4. Reduced business risk
### Improved ESG performance
1. Improved ESG performance, meaning environmental, social, and governance, is one of the four business benefits tied to adopting the AWS CAF. 
2. AWS describes it as using insights to improve sustainability and corporate transparency. 
3. One example is a smaller energy footprint, because your workloads share AWS power, cooling, networking, and facilities instead of running on separate on-premises equipment.
### Increased operational efficiency
1. Operational efficiency is one of the four business outcomes the AWS CAF points to, along with reduced risk, better ESG performance, and increased revenue. 
2. It means lower operating costs, higher productivity, and a better experience for employees and customers. 
3. A key source of it is cutting undifferentiated infrastructure work, such as patching servers, so staff can spend their time on higher-value work.
### Increased revenue
1. Adopting the AWS CAF is associated with increased revenue, which is one of four named benefits. 
2. The framework gives structured guidance on cloud adoption, which cuts time and effort and brings a faster time-to-market for new products. 
3. Launching sooner lets a business create new products, reach new customers and enter new market segments, and that growth is how revenue increases.
### Reduced business risk
1. Adopting the AWS CAF is associated with reduced business risk, which AWS links to better reliability, performance, and security. 
2. It is a separate benefit from improved ESG performance, increased revenue, and increased operational efficiency. 
3. It can include a stronger disaster recovery posture, because the cloud offers more availability and recovery options than depending only on aging on-premises infrastructure.
## Migration of Data
### Database replication
1. Database replication copies the existing data to AWS and then continuously applies changes, so the source and target databases stay synchronized. 
2. Because the source keeps running, you get minimal downtime and a short cutover when you switch. Choose it over a one-time bulk transfer when downtime must be minimized. 
3. It moves data over the network, unlike AWS Snowball, which ships a physical device.
### AWS Snowball
1. AWS Snowball moves large volumes of data to AWS by loading it onto a physical device that you ship to AWS, rather than sending it over the network. 
2. You choose it when your bandwidth is too limited for an online transfer, since a very large transfer could take months. 
3. The AWS Snow Family has devices sized for different data volumes, and unlike database replication, which keeps systems in sync continuously online, Snowball is a bulk offline transfer.
### AWS Application Discovery Service
1. Application Discovery Service collects usage and configuration data from your on-premises servers. 
2. You use that data to build an inventory of your infrastructure, which helps you plan a migration to AWS.
3. It can collect data without agents through a collector in VMware vCenter, or with an agent on each host for richer data such as running processes. It is part of the Migration and Transfer category.
### AWS Application Migration Service
1. AWS Application Migration Service automates lift-and-shift rehosting, so you move servers to AWS without changing the applications. 
2. It can migrate physical, virtual, and cloud-based servers, and it is designed for minimal downtime. 
3. It continuously replicates each source server to a staging area in AWS, so you can launch test instances and verify them before the final cutover.
### AWS Migration Hub
1. AWS Migration Hub is a single place to track the progress of your application migrations to AWS.
2. It works across multiple AWS and partner migration tools, which send it status updates, and it falls under the Migration and transfer services. 
3. It organizes tracking by application, grouping the servers and databases that make up each one so you see the whole application's progress.
### Migration Evaluator
1. Migration Evaluator builds a data-driven business case for moving to AWS.
2. It analyzes your on-premises servers and estimates the costs of running them on AWS compared with today.
3. The exam guide groups it with Migration and Transfer, but it is not the tool that does the moving.
# Cloud economics
## Fixed and variable costs
1. CapEx is a fixed upfront purchase. OpEx on AWS is variable and pay-as-you-go.
2. Your cost follows your actual usage instead of a purchase made ahead of time.
3. You do not have to forecast capacity far in advance, because you can provision resources as you need them.
## On-premises costs
1. Total cost includes ongoing costs, not just the initial hardware purchase.
2. Power, cooling, security, staff, and hardware refresh keep costing money over time.
3. Planning for peak demand can leave idle capacity that you still pay for.
## License-included pricing
1. License-included means the license cost is bundled into the AWS service price.
2. It is the counterpart to BYOL and fits when you do not already hold an eligible license.
3. You pay for the license through the usage-based rate, so only while the resource runs.
## Rightsizing
1. 1Rightsizing matches provisioned capacity to actual workload demand.
2. 2It saves money by removing capacity the workload does not need.
3. 3It can also mean adding capacity when an under-provisioned resource is a bottleneck.
## Automation
1. Automating operations reduces costs by freeing people for higher value work.
2. Automation improves efficiency by cutting manual tasks and making deployments consistent.
3. Fewer human errors in repetitive tasks is a separate benefit from cost and efficiency.
## Economies of scale
1. 1Economies of scale come from AWS aggregating usage across a huge customer base.
2. 2AWS passes the savings to you as lower pay-as-you-go prices.
3. 3Repeated price reductions over time are the visible result.



















































