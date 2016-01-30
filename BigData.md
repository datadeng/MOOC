#大数据导论

##welcome to big data
+ 字节转换：Kilobyte〈KB〉=1024 bytes 
Megabyte〈MB〉=1024 Kilobytes 
Gigabyte〈GB〉=1024 Megabytes 
Terabyte〈TB〉=1024 Gigabytes 
Petabyte〈PB〉=1024 terabytes 
Exabyte〈EB〉=1024 petabytes 
Zettabyte〈ZB〉=1024 exabytes 
Yottabyte〈YB〉=1024 zettabytes 
+ 数据爆炸：over 90% and less than 95% percentage of world's data was created in the last 2 years

##The Emerging Big Data Stack （新兴的大数据栈？）
+ Functional requirements：collection，integration(组织)，analysis，actions decisions
+ What we need：Real-Time（实时的），Scalable(可扩展的),High Performance（高性能的计算分析）
+ Hadoop come to exist：Compute+Storage
+ Hadoop Features：Low-Cost(廉价的),Scalable（可扩展的），Fault-Tolerant(高容错性)，Flexible(非常灵活)管理不同类型的数据
+ Basic Hadoop Components:分布式文件系统HDFS，处理框架MapReduce

#Hadoop Platform and Application Framework

##Hadoop Beginnings

###What is Hadoop
+ Apache Hadoop is an open source software framework for storage and large scale processing of data-sets on clusters of commodity hardware
+ Hadoop was created by Doug Cutting and Mike Cafarella in 2005
Named the project after son's toy elephant
+ Scalability at Hadoop’s core!（可伸缩性是hadoop核心）
+ Reliability!

##Apache Framework Hadoop Modules

###Apache Framework Basic Modules
+ **Hadoop Common**：从Hadoop 0.20版本开始，原来Hadoop项目的Core部分更名为Hadoop Common。Common为Hadoop的其他项目提供了一些常用工具，主要包括系统配置工具Configuration、远程过程调用RPC、序列化机制和Hadoop抽象文件系统FileSystem等。它们为在通用硬件上搭建云计算环境提供基本的服务，并为运行在该平台上的软件开发提供了所需的API
+ **Hadoop Distributed File System(HDFS)**：Hadoop分布式文件系统是Hadoop体系中数据存储管理的基础。它是一个高度容错的系统，能检测和应对硬件故障，用于在低成本的通用硬件上运行。HDFS简化了文件的一致性模型，通过流式数据访问，提供高吞吐量应用程序数据访问功能，适合带有大型数据集的应用程序
+ **Hadoop YARN**：Yarn是一个分布式的资源管理系统，用以提高分布式的集群环境下的资源利用率，这些资源包括内存、IO、网络、磁盘等。其产生的原因是为了解决原MapReduce框架的不足
+ **Hadoop MapReduce**：MapReduce是一种计算模型，用以进行大数据量的计算。Hadoop的MapReduce实现，和Common、HDFS一起，构成了Hadoop发展初期的三个组件。MapReduce将应用划分为Map和Reduce两个步骤，其中Map对数据集上的独立元素进行指定的操作，生成键-值对形式中间结果。Reduce则对中间结果中相同“键”的所有“值”进行规约，以得到最终结果

##Hadoop Distributed File System (HDFS)
###HDFS
+ Distributed, scalable, and portable file-system written in Java for the Hadoop framework
###Yarn
+ YARN enhances the power of a Hadoop compute cluster
+ Scalability，Improved cluster utilization，MapReduce Compatibility，Supports Other Workload

##Hadoop Ecosystem Major Components
###Apache Sqoop
+ Tool designed for efficiently transferring bulk data between Apache Hadoop and structured datastores such as relational databases

###HBASE
+ Based on Google BigTable
+ Column-oriented database managemnet system
+ Key-value store
+ Can hold extremly large data
+ Dynamic data model
+ Not a Relational DBMS

###PiG
+ High level programming on top of Hadoop MapReduce
+ Pig Latin(pig语言)
+ Data analysis problems as data flows
+ Originally developed at Yahoo 2006

###Apache Hive
+ Data warehouse software facilitates querying and managing large datasets residing in distributed storage
+ SQL-like language!
+ Facilitates querying and managing large datasets in HDFS
+ Mechanism to project structure onto this data and query the data using a SQL-like language called HiveQL

###Ooize
+ Workflow scheduler system to manage Apache Hadoop jobs
+ Oozie Coordinator jobs（协调job）
+ SupportsMapReduce, Pig, Apache Hive, and Sqoop, etc.

###Zookeeper
+ Provides operational services for a Hadoop cluster group services
+ Centralized service for:maintaining configuration information,naming services,providing distributed synchronization and providing group services(集中服务:维护配置信息,命名服务,提供分布式同步和提供组服务)
###Flume
+ Distributed, reliable, and available service for efficiently collecting, aggregating, and moving large amounts of log data（分布式、可靠和可用的服务,有效地收集、聚合和移动大量的日志数据）

##Additional Cloudera Hadoop Components
###Impala
+ Cloudera's open source massively parallel processing (MPP) SQL query engine Apache Hadoop

###Spark（内存计算）
+ Apache Spark™ is a fast and general engine for large-scale data processing
+ Multi-stage in-memory primitives provides performance up to 100 times faster for certain applications
+ Allows user programs to load data into a cluster's memory and query it repeatedly
+ Well-suited to machine learning!!!

