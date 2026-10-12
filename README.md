# Apache Kafka (MOM)

## Overview Architecture

Kafka is a distributed event-streaming platform enabling asynchronous communication between applications.

### Main Components
- **Producer:** Publishes messages (events) to Kafka Topics.
- **Broker:** Kafka server that receives and stores messages.
- **Topic:** Logical category where related messages are stored.
- **Consumer:** Subscribes to Topics and reads messages.

### Architecture Diagram
![Kafka Architecture](images/i1.png)

### Key Benefits
- Asynchronous communication
- Loose coupling
- Scalability
- Fault tolerance

## Kafka Topics, Partitions & Consumer Groups

### Topics & Partitions
- **Topic:** Logical category for storing related messages.
- **Partition:** Ordered sequence of messages within a topic.
- A topic can contain multiple partitions.
- Message ordering is guaranteed within each partition.

### Consumer Groups
- **Consumer Group:** Multiple consumers working together to process messages.
- Each partition is assigned to only one consumer within a group.
- Different consumer groups can read the same partitions independently.
- If consumers > partitions, some consumers remain idle (for a single topic).

### Key Benefits
- **Parallelism:** Process partitions simultaneously.
- **Scalability:** Distribute partitions across multiple brokers.
- **Load balancing:** Distribute partition assignments among consumers.

### Architecture Diagram
![Kafka Partitions and Consumer Groups](images/i2.png)
