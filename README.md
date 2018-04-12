# Triangle MUG - Back to Basic: Replica Sets

## Getting everybody on the same page
* Creating a 3-member Replica Set
* Member Roles
* Replica Set settings
* Changing Replica Set settings
* Connection String

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
  * Set up writeConcern to majority
  * Bring the secondary node down
  * Query a collection
  * Insert a new document into a collection
  * What happen to the write operation?

d) 3-member Replica Set w/ writeConcern: majority
  * Set up writeConcern to majority
  * Bring two secondary nodes down
  * Query a collection
  * Insert a new document into a collection
  * What happen to the write operation?

e) 5-member Replica Set w/ delayed member
  * Set up writeConcern to majority
  * Bring 2 secondary nodes down (any two but the delayed member)
  * Query a collection
  * Insert a new document into a collection
  * What happen to the write operation?
