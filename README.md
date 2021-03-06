# Triangle MUG - Back to Basic: Replica Sets

## Getting everybody on the same page
* Creating a 3-member Replica Set
* Member Roles
* Replica Set settings
* Changing Replica Set settings
* Connection String

## Preparing your lab environment
* mkdir -p mdb/{3_Node_Arbiter,3_Node,5_Node}

* mlaunch init --replicaset --nodes 2 --arbiter --dir mdb/3_Node_Arbiter
* mlaunch stop --dir mdb/3_Node_Arbiter

* mlaunch init --replicaset --nodes 3 --dir mdb/3_Node
* mlaunch stop --dir mdb/3_Node

* mlaunch init --replicaset --nodes 5 --dir mdb/5_Node
* mlaunch stop --dir mdb/5_Node

## Playing Time
Note: This session requires mongoDB and mtools to be installed on your system

a) 3-member Replica Set - Connection using a single IP/Hostname
  * Connecting to a replica set pointing to the IP/Hostname of the primary member
  * Bring primary node down
  * What happen to your connection?

b) 3-member Replica Set - Connection using a connection string
  * Connecting to a replica set using a connection string
  * Bring primary node down
  * What happen to your connection?

c) 3-member Replica Set w/ arbiter and writeConcern: majority
  * Bring the secondary node down
  * Insert a document into a collection using writeConcern majority

d) 3-member Replica Set w/ writeConcern: majority
  * Bring two secondary nodes down
  * Insert a document into a collection using writeConcern majority

e) 5-member Replica Set w/ delayed member
  * Bring 2 secondary nodes down (any two but the delayed member)
  * Insert a document into a collection using writeConcern majority
