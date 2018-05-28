# Apache Kafka

### A distributed streaming platform

---
### Why?

> Kafka® is used for building real-time data pipelines and streaming apps. It is **horizontally scalable**, **fault-tolerant**, **wicked fast**, and runs in production in thousands of companies.

+++  
### Where?  

![fits](https://www.confluent.io/wp-content/uploads/chart-kafka-infrastructure@2x.png)
+++  

### What for?  
* read & write streams of data like a messaging system  
 (pub/sub and queue messaging)
* stream processing
* store streams of data safely in distributed, replicated, fault tolerant cluster
---

### Overview
+++

![cluster](https://www.tutorialspoint.com/apache_kafka/images/fundamentals.jpg)
+++  
### Cluster
* Multiple brokers
* Horizontal scale out without downtime 
* Manage the persistence and replication of message data
+++ 
### Topic
![topic](https://kafka.apache.org/0102/images/log_anatomy.png)
* A partition is a set of segment files of equal sizes
* Each partition contains messages in an immutable ordered sequence  
* Each partition is consumed by exactly one consumer in the group
+++ 
### Producer
* Publisher of messages to one or more Kafka topics
* Send data to Kafka brokers
* Every time a msg is sent to a broker, the broker appends the message to the last segment file.  
+++ 

### Consumer
* Read data from brokers
* Subscribe to one or more topics
* Consume published messages by pulling data from the brokers
* Manages the offset (index from which one wants to read from)  
+++

### Broker
* Kafka cluster typically consists of multiple brokers to maintain load balance
 * Kafka brokers are stateless ( ZooKeeper is used for maintaining their cluster state)
  * One Kafka broker instance can handle hundreds of thousands of reads and writes per second
  * Each broker can handle TB of messages without performance impact.
  * Kafka broker leader election can be done by ZooKeeper.  
---
### Ecosystem
![ecosystem](https://kafka.apache.org/11/images/kafka-apis.png)
+++
### Connect
+++
### Stream Processors
---
## Use Cases
+++  
### Messaging
Kafka works well as a replacement for a more traditional message broker.   
+++  
### Real-Time Feeds
Kafka can be used to for creating an activity tracking pipeline as a set of real-time publish-subscribe feeds  
+++  
### Event Sourcing
Kafka's support for very large stored log data makes it an excellent backend for an application built with Event Sourcing  
+++  
### Commit Log
 With a commit log one can replicate data between nodes and acts as a re-syncing mechanism for failed nodes to restore their data.  

---
## Getting Started

---
## Wrap Up!
* performance !!!
  * handle a large number of diverse consumers
  * stable performance even with TB of messages
  * high throughput for both publishing and subscribing messages
* scalable
* distributed storage
  * immediatly written to disk and replicated (fault-tolerance)
  * strong ordering guarantees, configurable retention period
* flexible consuming
  * consumer can rewind back to an old offset / re-consume data
  * load balanced with using same consumer-group


