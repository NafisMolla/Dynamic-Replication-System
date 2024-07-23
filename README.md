# Dynamic-Replication-System


## Project Overview

This project involves the development of a distributed key-value store system utilizing Apache Thrift and Apache ZooKeeper. The system is designed to be fault-tolerant and scalable, offering high availability and reliability for storing and retrieving key-value pairs. This README provides a high-level overview of the project components and their technical highlights.

## Components

- **ClientPool**: Manages a pool of clients for the key-value service, enabling efficient connection handling and resource management.
- **CreateZNode**: Interfaces with ZooKeeper to create nodes that represent server instances, allowing for dynamic cluster management.
- **KeyValueHandler**: Implements the key-value storage logic, handling get and put requests, ensuring data consistency, and managing primary and backup roles within the system.
- **StorageNode**: Acts as a server node that uses Thrift for communication and integrates with ZooKeeper for cluster management and role assignment.
- **Watcher**: Monitors changes in the ZooKeeper node hierarchy to dynamically adjust the cluster configuration and handle failover scenarios.

## Technical Achievements

- **Thrift Integration**: Utilizes Apache Thrift for efficient cross-language service development, allowing the key-value store to be easily extended and maintained.
- **ZooKeeper Coordination**: Implements ZooKeeper for cluster management, ensuring that nodes are aware of each other's state and can take over responsibilities in case of failures.
- **Concurrent Data Handling**: Uses concurrent data structures and synchronization mechanisms to ensure thread safety and data consistency across multiple server instances.
- **Dynamic Role Assignment**: Automatically assigns and adjusts roles (primary or backup) for nodes based on the cluster state, enhancing the system's resilience to node failures.
- **Efficient Client Pooling**: Implements a client pool to manage connections to the key-value service efficiently, reducing connection overhead and resource usage.

## Highlights

- **Scalability**: Designed to scale horizontally by adding more nodes to the cluster, which automatically integrate into the system with minimal configuration.
- **Fault Tolerance**: Achieves high availability through redundant storage and failover mechanisms, ensuring that the system remains operational even if individual nodes fail.
- **Performance Optimization**: Utilizes framed transport and binary protocols in Thrift to optimize network communication and data serialization, resulting in fast response times for client requests.
- **Automatic Recovery**: Includes mechanisms to detect failed nodes and automatically redistribute their responsibilities to other nodes in the cluster, minimizing downtime and data loss.

## Conclusion

This project showcases the capabilities of integrating Apache Thrift and ZooKeeper to build a robust, scalable, and fault-tolerant distributed key-value store. It demonstrates advanced concepts in distributed systems design, such as dynamic cluster management, role handling, and efficient resource utilization.
