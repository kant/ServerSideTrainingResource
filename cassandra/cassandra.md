# Cassandra

## Overview

- partitioned wide column storage model
- eventually consistent
- scalable, reliable and highly available

#Removing aNode
1. Node status
  `notetool status`
2. Decommission a Node
  `nodetool -h 192.168.1.85 -p 7199 decommission`
