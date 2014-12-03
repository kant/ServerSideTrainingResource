JBoss training step
==========================

#Install
[Download JBoss](http://www.jboss.org/products/eap/download/)

#Add admin user
Windows: `$JBOSS_HOME\bin\add-user.bat`

Linux: `$JBOSS_HOME/bin/add-user.sh`

#Add JBoss in Eclipse
1. Install JBoss plugin for Eclipse
2. In Eclipse: Window -> Show View -> Servers
3. In Servers: Right click -> New -> Server
4. Add server runtime environment
5. Set JRE for server runtime environment

#Create Maven JBoss project
[Maven archetypes for JBoss](http://mvnrepository.com/artifact/org.jboss.spec.archetypes)