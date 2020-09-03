# Cassandra

## Overview

- partitioned wide column storage model
- eventually consistent
- scalable, reliable and highly available
- Full multi-master database replication
- Global availability at low latency
- Scaling out on commodity hardware
- Linear throughput increase with each additional processor
- Online load balancing and cluster growth
- Partitioned key-oriented queries
- Flexible schema

## Features

CQL CQL allows users to organize data within a cluster of Cassandra nodes using:
- Keyspace: defines how a dataset is replicated.
- Table: defines the typed schema for a collection of partitions.
- Partition: defines the mandatory part of the primary key all rows in Cassandra must have.
- Row: contains a collection of columns identified by a unique primary key made up of the partition key and optionally additional clustering keys.
- Column: A single datum with a type which belong to a row.

Cassandra does not support:
- Cross partition transactions
- Distributed joins
- Foreign keys or referential integrity.

## Operating

- cassandra.yaml
- nodetool
- `auditlogviewer` is used to view the audit logs.
- `fqltool` is used to view, replay and compare full query logs.

## Dynamo

https://cassandra.apache.org/doc/latest/architecture/dynamo.html#dynamo

### Dataset Partitioning: Consistent Hashing

- Token Ring https://pdos.csail.mit.edu/papers/chord:sigcomm01/chord_sigcomm.pdf
- Multiple Tokens per Physical Node (a.k.a. vnodes)

Cassandra introduces some nomenclature to handle these concepts:
- Token: A single position on the dynamo style hash ring.
- Endpoint: A single physical IP and port on the network.
- Host ID: A unique identifier for a single “physical” node, usually present at one Endpoint and containing one or more Tokens.
- Virtual Node (or vnode): A Token on the hash ring owned by the same physical node, one with the same Host ID.

#Removing aNode
1. Node status
  `notetool status`
2. Decommission a Node
  `nodetool -h 192.168.1.85 -p 7199 decommission`
