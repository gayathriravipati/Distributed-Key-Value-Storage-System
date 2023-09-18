# Distributed-Key-Value-Storage-System
Implementation of Distributed Key-Value Storage System using Raft Consensus Algorithm

Distributed consensus is one of the fundamental problems in distributed systems. Consensus is a process where multiple servers agree on the same information, it is essential for developing fault-tolerant distributed systems. The Raft Algorithm is used to achieve consensus among multiple servers to maintain data consistency across the system.
Raft Algorithm:
The Raft protocol was created by Diego Ongaro and John Ousterhout at Stanford University, and Diego earned his Ph.D. in 2014. The goal of Raft was to provide a more understandable approach to achieving consensus, which is the process of agreeing on a single value among a group of distributed systems. Earlier Paxos Algorithm was considered very difficult to comprehend and implement. The raft was developed as a response to this challenge, and the title of Diego's paper reflects this: 'In Search of an Understandable Consensus Algorithm'.


Project Description:
Implementation of the Raft Algorithm introduced in the above research paper to insert and retrieve values based on API calls made by the client and analyze the algorithm's performance by varying parameters.
Description of terms used in the implementation:
Every server will be in one of the three states
Leader - Any request from the client flows through the Leader. All the other servers interact with the leader to maintain consistency in the log. There is utmost one leader at any point in time.
Candidate - Any server that doesn’t receive an update from the leader for a certain time turns out to be a candidate and initiates an election to request votes from the other servers.
Follower - The follower server interacts with the Leader to sync up the data. If the leader server fails, then the follower turns a candidate.
