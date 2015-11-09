# Distributed Systems

single data store - consistent, the building block
eventually consistent
paxos - a quorum(majority subset) must agree
master election - use slow paxos to choose a single data store to be master, use paxos to learn about masters, but talk to them directly to learn quickly

paxos a majority must agree - but not all should use odd numbers in distributed systems
a majority subset = a quorum

use paxos to find or elect the master, then talk to the master of that piece of the entire data(that shard)

read latest - time consuming but consistent


raft
leader election
log replication

higher election term wins


colocate distributed database in same app process. eg cassandra or elasticsearch node

send responses before requests(http, webrtc, video streaming etc) to improve performance
