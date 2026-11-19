# AWS global infrastructure

## Edge locations
You'll be able to explain ==how edge locations cut latency== by ==🟢caching content near your users.==
==Edge locations== ==🟢keep copies of your content close to your users==, so ==🔵requests travel a much shorter distance. ==
1. Edge locations ==reduce latency for end users== by ==caching content near them.==
2. ==A cache hit at the edge== ==🟢skips the round trip to the origin server==.
3. ==Caching at the edge== is a ==🟢different mechanism from deploying compute in a closer Region.==

## Regions, Availability Zones and edge locations
You'll be able to explain ==how Regions, Availability Zones and edge locations fit together.==
==AWS builds its cloud in layers==: ==🟢Regions contain Availability Zones==, and ==🔵edge locations sit in a separate tier for delivering content. ==
1. ==A Region== is ==🟢a separate geographic area== that ==🔵contains multiple, isolated Availability Zones.==
2. ==An Availability Zone== is ==🟢one or more discrete data centers inside a Region.==
3. ==Edge locations== are ==🟢a separate tier that CloudFront uses== to ==🔵cache and deliver content close to users.==

## Multi-AZ for high availability
You'll be able to explain ==how spreading a workload across Availability Zones== ==keeps it running.==
==Spreading a workload across Availability Zones== ==🟢lets it keep running when one zone fails==. 
1. ==Using more than one Availability Zone== is how you ==🟢achieve high availability==.
2. A ==multi-AZ workload== ==🟢keeps operating if one AZ becomes unavailable==.
3. You must ==design the workload to span AZs==. ==🔴A Region having several AZs is not enough.==

## Availability Zone fault isolation
You'll be able to ==explain why a problem in one Availability Zone== ==🟢does not spread to another==
==Availability Zones== are ==🟢built to fail separately==, so ==🔵one zone's problem stays in that zone. ==
1. Availability Zones ==do not share single points of failure==.
2. ==Each AZ is physically separate==, ==🟢with its own power, cooling, and networking.==
3. You ==get the benefit of this isolation== by ==🟢running in more than one AZ==.

## Multi-Region for data sovereignty
You'll be able to ==explain how choosing AWS Regions== ==keeps data inside a required country or jurisdiction.==
==Some laws say== ==🟢your data must stay inside one country==, so ==🔵you choose AWS Regions that sit inside it. ==
1. ==Data sovereignty and residency rules== typically ==🟢require data to be stored and processed in a specific country or jurisdiction.==
2. You ==meet the rule== by ==🟢choosing a Region inside that jurisdiction== and ==🔵keeping the relevant data there.==
3. ==The driver is the law==, which ==🟢makes it a different reason== ==🔵from choosing a Region for latency or resilience.==

## Multi-Region for lower latency
You'll be able to explain ==how running in several Regions== ==🟢cuts delay for users around the world.==
==Putting your application in more than one Region== ==🟢brings it physically closer to users==, so ==🔵their requests travel a shorter distance. ==
1. ==Latency grows with== the ==🟢physical distance between users and the Region that serves them.==
2. ==Deploying in Regions close to your users== ==🟢shortens the network distance data must travel.==
3. ==Pair multiple Regions with routing==, such as ==🟢Route 53 latency-based routing==, so ==🔵each user reaches the closest one.==

## Multi-Region for disaster recovery
You'll be able to explain ==why a workload spans Regions== to ==🟢survive a Region-wide outage==.
==Running in more than one AWS Region== ==🟢lets your workload keep working, or come back fast==, ==🔵if a whole Region goes down== 
1. ==A multi-Region design== ==🟢lets a workload keep running, or be restored quickly==, ==🔵if an entire Region becomes unavailable.==
2. ==Disaster recovery (restore after)== and ==business continuity (operate during)== ==🟢form one combined resilience driver.==
3. ==Resilience== is ==🔴separate from the latency and data sovereignty reasons== for using multiple Regions.










