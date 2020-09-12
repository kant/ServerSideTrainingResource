# Elastcisearch

## Overview

- Elasticsearch is the distributed search and analytics engine.

## Data in

- document
- index, an optimized collection of documents and each document is a collection of fields, which are the key-value pairs that contain your data.

## Information out

- search, built on the Apache Lucene search engine library.
- analyze

### search

- structured queries, Structured queries are similar to the types of queries you can construct in SQL.
- full text queries, Full-text queries find all documents that match the query string and return them sorted by relevance

### analyze

## Scalability and resilience

<https://www.elastic.co/guide/en/elasticsearch/reference/current/scalability.html>

- clusters
- nodes
- shards, primaries and replicas

### Cluster

All Elasticsearch clusters require

- One elected master node node
- At least one node for each role.
  - Master-eligible node
  - Data node, hold data and perform data related operations
  - Ingest node
  - Machine learning node
- At least one copy of every shard.

## Text analysis

Elasticsearch performs text analysis when indexing or searching `text` fields.

use case:

- Build a search engine
- Mine unstructured data
- Fine-tune search for a specific language
- Perform lexicographic or linguistic research

flow:

- character filters (zero or more)
- tokenizer(one), breaking a text down into smaller chunks
- token filters(zero or more), normalize tokens into a standard format

## Search Data

### relevance

- Term Frequency
- Inverse Document Frequency
- Field Length Normalization

### Search API

`_search`

- match
- term

### Aggregate

- bucketing
- metric
- matrix
- pipeline
