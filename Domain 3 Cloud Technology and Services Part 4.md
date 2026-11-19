# Database Services
## Self-managed vs AWS managed databases
You'll be able to ==choose between a self-managed EC2 database== and ==🟢an AWS managed database service.==
Choosing between running your own database on Amazon EC2 and using a managed AWS database ==comes down to how much operational work you want to own==. 
1. The choice is ==mostly about operational overhead==: ==🟢how much admin work you want to do yourself.==
2. ==On EC2== ==🟢you install, patch, back up, and scale the database==. ==🔵A managed service like Amazon RDS== ==🟣does those tasks for you.==
3. ==Pick self-managed only== when you ==🟢need engine configuration or OS-level access that a managed service does not give you==.

## Amazon Aurora
You'll be able to explain what Aurora is and ==when to pick it over a standard managed relational database.==
==Amazon Aurora== is ==🟢a managed relational database== that ==🔵works with MySQL and PostgreSQL== and is ==🟣built for high performance and availability==. 
1. Aurora is ==a managed relational database== ==🟢compatible with MySQL and PostgreSQL.==
2. It is ==built for higher performance and availability==, ==🟢with data copied across three Availability Zones.==
3. Pick Aurora ==when a relational workload needs more throughput or availability== ==🔴than a standard managed MySQL or PostgreSQL database==.

## Amazon RDS
You'll be able to explain what Amazon RDS is, ==which engines it runs==, and ==how Multi-AZ works.==
==Amazon RDS== ==🟢runs familiar relational database engines for you==, and ==🔵Multi-AZ keeps a standby copy ready in another Availability Zone. ==
1. RDS is ==a managed service== for ==standard relational engines such as MySQL, PostgreSQL, and SQL Server.==
2. ==AWS handles routine tasks== like patching, backup, and failure detection, ==🟢so you do not run the database server yourself.==
3. ==Multi-AZ keeps a synchronously replicated standby== ==🟢in a different Availability Zone for high availability.==

## Relational databases
You'll be able to explain ==when a relational database is the right fit== and ==🟢how it differs from NoSQL.==
A ==relational database== ==stores structured data in linked tables== and ==fits transactional work. ==
1. Relational databases ==hold structured data in tables with a fixed schema==, ==linked by primary and foreign keys.==
2. They ==suit transactional workloads== that ==need strong consistency and joins across tables.==
3. ==NoSQL databases use flexible data models== and ==🔵are tuned for performance and scale instead.==

## NoSQL databases
You'll be able to explain ==when a NoSQL database fits better than a relational one==.
A ==NoSQL database== ==🟢suits apps whose data changes shape often== and ==🔵whose traffic can grow very large. ==
1. ==NoSQL databases use flexible schemas==, so ==🟢items do not all need the same fixed structure.==
2. NoSQL databases are ==typically designed to scale out==, which ==🟢suits very high request volumes.==
3. ==Amazon DynamoDB is the AWS NoSQL service to remember== for ==🔵flexible, high-scale workloads.==

## In-memory databases and caching
You'll be able to explain when ==an in-memory cache speeds up reads and shields your main database.==
An ==in-memory cache== ==🟢keeps frequently used data in fast memory==, so ==🔵reads come back quickly and your main database does less work==. 
1. ==Use an in-memory cache or database== to ==🟢reduce latency for read-heavy workloads.==
2. ==Memory is faster than disk-based storage==, so ==🟢frequently accessed data is served from memory.==
3. ==A cache in front of a primary database== ==🔵reduces the read load that reaches that database.==

## AWS Database Migration Service (DMS)
You'll be able to explain ==how AWS DMS moves a database to AWS with little downtime==.
==AWS DMS== ==🟢moves a database to AWS== ==🔵while your old database keeps running. ==
1. AWS DMS ==migrates data from a source database to a target database== ==🟢while the source stays operational.==
2. ==Keeping the source running== helps ==🟢minimize downtime for your applications.==
3. It supports ==same-engine (homogeneous)== and ==🟢different-engine (heterogeneous) migrations.==

## AWS Schema Conversion Tool (SCT)
You'll be able to explain ==when AWS SCT is needed== and ==🟢what it converts when you migrate between database engines.==
==AWS SCT== ==🟢rewrites a database's structure== ==🔵so a different database engine can use it==. 
1. AWS SCT ==converts a source database's schema== ==🟢into a format the target engine can use.==
2. You need AWS SCT ==🟢when the source and target engines differ (heterogeneous migration).==
3. ==AWS SCT handles the schema==, and ==🔵AWS DMS moves the data.==

## Amazon ==DocumentDB==
You'll be able to ==recognize Amazon DocumentDB== as ==the managed, MongoDB-compatible document database.==
==Amazon DocumentDB== is ==🟢the AWS database service== for ==🔵running MongoDB-style document workloads== ==🟣without managing the servers yourself==. 
1. DocumentDB is ==an AWS Database service.==
2. It is ==a fully managed, MongoDB-compatible document database==.
3. Pick it ==when a question mentions MongoDB or JSON document data==.

## Amazon DynamoDB
You'll be able to recognize ==DynamoDB as AWS's serverless NoSQL database== and say when to pick it.
==Amazon DynamoDB== is the AWS database service ==🟢for fast, serverless key-value and document data. ==
1. DynamoDB is ==a fully managed, serverless NoSQL database== with ==🟢key-value and document models.==
2. It ==aims for single-digit millisecond performance at any scale== and ==🟢scales without you managing servers.==
3. It has ==no JOIN operator==, so ==🟢complex joins point you to a relational database instead.==

## Amazon ElastiCache
You'll be able to explain what Amazon ElastiCache is and ==when to use it as a managed cache.==
==Amazon ElastiCache== is ==🟢a managed in-memory caching service== that ==🔵speeds up your applications by serving data from RAM. ==
1. ElastiCache is ==a managed in-memory caching service== in ==🟢the AWS database category.==
2. It is ==compatible with the Redis and Memcached engines==, ==🔵and with Valkey==.
3. ==Serving data from memory instead of disk== ==🟢improves speed== and ==🔵reduces the load on your database.=

## Amazon Neptune
You'll be able to recognize ==Amazon Neptune== as ==the managed graph database for connected data.==
Amazon Neptune is ==the AWS database== to pick ==🟢when the links between your data matter as much as the data. ==
1. Neptune is ==a managed graph database in the AWS Database category.==
2. Use it ==for highly connected data== such as ==🟢social networks and recommendation engines.==
3. It ==uses graph query languages== such as ==🟢Gremlin, openCypher and SPARQL==, ==🔴not SQL joins.==








