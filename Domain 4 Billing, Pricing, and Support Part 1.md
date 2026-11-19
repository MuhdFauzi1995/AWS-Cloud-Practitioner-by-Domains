# Pricing Models
## On-Demand Capacity Reservations
- You'll be able to pick a Capacity Reservation when a question is about guaranteed capacity, not savings.
- An On-Demand Capacity Reservation guarantees EC2 capacity in one Availability Zone, but it does not lower your price.
1. A Capacity Reservation guarantees EC2 capacity in a specific Availability Zone for as long as you hold it.
2. It has no term commitment for immediate use and no pricing discount of its own.
3. Combine it with a Savings Plan or Regional Reserved Instance when you also want a discount.
## Dedicated Hosts
- You'll be able to pick a Dedicated Host when software licenses are tied to a physical server.
- A Dedicated Host is a whole physical server that is yours alone, and you choose it when a software license is tied to a specific server.
1. A Dedicated Host is a physical server dedicated entirely to you.
2. It shows sockets and physical cores, so you can track server-bound licenses.
3. Choose it when per-socket, per-core, or per-VM license terms must be tied to a specific server.
# Dedicated Instances
- You'll be able to pick Dedicated Instances when a rule demands isolated hardware but not host control.
- Dedicated Instances give you hardware that no other AWS customer shares, without handing you control of the physical server.
1. Dedicated Instances run on hardware dedicated to one customer, so other accounts never share it.
2. You get no visibility into or control over the specific physical host.
3. Choose them for physical isolation needs; choose Dedicated Hosts when you need host-level licensing or control.
## On-Demand Instances
- You'll be able to pick On-Demand Instances for unpredictable or short-term workloads.
- On-Demand Instances let you pay for EC2 compute only while you use it, with no contract.
1. You pay by the hour or second with no upfront payment and no long-term commitment.
2. Choose On-Demand when your compute needs are unpredictable or short-term, so you never pay for a term you do not use.
3. You can start and stop capacity as your needs change, because there is no commitment to cancel.
## Reserved Instances 
- You'll be able to pick Reserved Instances for steady, predictable workloads and spot when they are a poor fit.
- A Reserved Instance is a one-year or three-year commitment that gives you a lower rate for work that runs steadily.
1. A Reserved Instance trades a one-year or three-year commitment for a discount compared with On-Demand pricing.
2. Choose it for steady, predictable workloads that run continuously for the committed term.
3. You pay for the whole term regardless of use, so unsteady demand means paying for unused capacity.
## Savings Plans
- You'll be able to decide when a Savings Plan fits better than a Reserved Instance.
- A Savings Plan trades a steady hourly spend commitment for lower compute prices and the freedom to change what you run. 
1. A Savings Plan commits you to a dollar amount of compute per hour, not to a specific instance configuration.
2. Choose it when spend is predictable but the instance family, size, OS or Region may change.
3. It offers more flexibility than a Reserved Instance for the same kind of one or three year term.
## Spot Instances
- You'll be able to decide when interruption-tolerant work belongs on Spot Instances.
- Spot Instances are the cheapest way to run EC2 compute, but only if your work can survive being stopped without warning. 
1. Spot Instances use spare EC2 capacity at discounts of up to 90% compared to On-Demand prices.
2. EC2 can interrupt a Spot Instance with two minutes of notice when it needs the capacity back.
3. Choose Spot only for work that tolerates interruption, such as batch jobs and fault-tolerant distributed workloads.
## Convertible vs standard Reserved Instances
- You'll be able to ==choose Convertible or Standard Reserved Instances== by ==flexibility and discount.==
- ==Standard Reserved Instances give the biggest discount==, while ==Convertible ones trade some discount for flexibility==. 
1. ==Convertible Reserved Instances== can be ==exchanged for a different family, OS, tenancy, or payment option.==
2. ==Standard Reserved Instances cannot be exchanged==, but they can be ==sold on the Reserved Instance Marketplace.==
3. The ==flexibility of Convertible== comes with a ==smaller discount than Standard.==
## Reserved Instance size flexibility
- You'll be able to explain how one Regional Reserved Instance can cover several instance sizes in a family.
- Size flexibility lets one Regional Reserved Instance discount cover different sizes in the same instance family. 
1. Size flexibility applies a Regional RI discount to other sizes in the same instance family.
2. Each size has a normalization factor, so one RI covers a proportional amount of usage at another size.
3. Zonal RIs have no size flexibility because they are tied to one Availability Zone and one size.
## Reserved Instances across accounts
- You'll be able to ==explain how RI discounts and capacity reservations are shared in AWS Organizations.==
- ==When your company uses several AWS accounts==, a ==Reserved Instance bought in one account can lower the bill for the others==. 
1. A Regional RI discount can ==apply to matching, unused usage in any member account of the organization.==
2. ==RI sharing is on by default==, and the ==management account can turn it off for an account.==
3. ==On-Demand Capacity Reservations== can be ==shared across member accounts==, but a ==Regional RI does not reserve capacity.==
## Inbound vs outbound data transfer
- You'll be able to ==explain why data into AWS is free== but ==data out to the internet is billed.==
- ==Sending data into AWS is generally free==, but ==sending it out to the internet is generally billed per GB.== 
1. Inbound (ingress) data transfer ==from the internet into AWS== is ==generally not charged==.
2. Outbound (egress) data transfer ==to the internet is generally billed, typically on a tiered per-GB basis.
3. ==The free-in, billed-out pattern== shows up across AWS services, so ==expect it when you estimate any workload.==
## Inter-Region data transfer
- You'll be able to explain who pays when data moves between AWS Regions and why it varies.
- Moving data from one AWS Region to another costs money, and the Region that sends the data is the one that bills you. 
1. The sending Region bills inter-Region transfer at an outbound rate, and the receiving Region adds no charge for incoming data.
2. Inter-Region transfer typically costs more than transfer inside one Region.
3. The rate is tied to the sending Region, so it is not one flat global rate.
## Intra-Region data transfer
- You'll be able to ==explain which data transfer inside one AWS Region is free== and ==which is billed.==
- ==Traffic that stays inside one Availability Zone is free==, but ==traffic that crosses Availability Zones in the same Region is billed. ==
1. Data moving ==inside a single Availability Zone is free==.
2. Data moving ==between Availability Zones in the same Region is billed==.
3. ==Being in the same Region== ==🔴**does not** make transfer free==.
## EBS volume pricing
- You'll be able to ==match an EBS volume type to a workload== by ==🟢weighing performance against price.==
- ==Each EBS volume type trades price against performance==, so you ==🟢pick the cheapest type that still meets the workload's needs==. 
1. ==gp3 charges for capacity==, and ==🟢IOPS and throughput are provisioned and priced separately.==
2. ==io2 costs more than gp3== and is ==for IOPS-intensive workloads that need consistent performance.==
3. ==st1 is for large sequential throughput==, and sc1 is ==the lowest-cost type for rarely accessed data.==
## EFS storage class pricing
- You'll be able to explain how ==EFS Standard and Infrequent Access trade storage price for access fees.==
- ==EFS charges less to store cold files==, but it ==🔴charges you when you read them==. 
1. ==EFS Standard costs more per GB== because it is ==🟢built for frequently used data and fast access==.
2. ==EFS Infrequent Access has lower storage prices== but ==🔴adds a data access charge when you read a file.==
3. ==EFS Lifecycle Management moves files between classes automatically== ==🔵based on last-accessed time.==
## S3 Glacier retrieval pricing
- You'll be able to ==match each S3 Glacier tier to its speed, storage cost, and early-deletion rule.==
- The ==three S3 Glacier tiers== ==🟢trade storage price against how fast you can get your data back. ==
1. ==🟢Instant Retrieval is fastest (milliseconds)== and ==🟢costs the most to store of the Glacier tiers.==
2. ==🟡Flexible Retrieval is cheaper to store==, with ==retrieval in minutes to hours==.
3. ==🔴Deep Archive is the cheapest to store== and ==🔴slowest to retrieve==, and ==🔴early deletion adds a prorated charge.==
## S3 storage class pricing
- You'll be able to explain ==how S3 storage classes trade storage cost against retrieval and monitoring fees.==
- ==Each S3 storage class lowers one cost by adding another==, so the ==🟢right choice depends on how often you read your data.== 
1. ==🟢Use S3 Standard for data you read often==, because the ==🟢infrequent access classes add a retrieval fee.==
2. ==S3 One Zone-IA is cheaper than Standard-IA== because it ==stores data in only one Availability Zone.==
3. ==🔴S3 Intelligent-Tiering== ==🔴moves objects between tiers automatically for a small monthly per-object monitoring fee==.

# AWS License Manager
- You'll be able to explain ==how AWS License Manager tracks licenses and prevents overuse==
- AWS License Manager ==helps you track the software licenses you own== and ==keep your usage within what you paid for.==
1. ==License Manager is a Management and Governance service== that ==tracks and manages software licenses.==
2. It helps ==control licensing costs== by ==🟢preventing license overuse before it happens==.
3. It can ==track BYOL software== that ==🟢runs on Dedicated Hosts or Dedicated Instances==.


















































