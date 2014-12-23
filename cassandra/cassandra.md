Cassandra Tip
==========================

#Add JBoss in Eclipse
1. Install JBoss plugin for Eclipse
2. In Eclipse: Window -> Show View -> Servers
3. In Servers: Right click -> New -> Server
4. Add server runtime environment
5. Set JRE for server runtime environment

#Removing aNode

1. Node status
`notetool status`
2. Decommission a Node
`nodetool -h 192.168.1.85 -p 7199 decommission`