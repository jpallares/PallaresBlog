---
title: Designing Data-Intensive Applications
bookauthor: Kleppmann, Martin
date: 2021-03-02
position: 10
quotes:
  - date: 2020-12-23
    quote: If you are designing a data system or service, a lot of tricky questions arise. How do you ensure that the data remains correct and complete, even when things go wrong internally? How do you provide consistently good performance to clients, even when parts of your system are degraded? How do you scale to handle an increase in load? What does a good API for the service look like?
  - date: 2020-12-23
    quote: Reliability The system should continue to work correctly (performing the correct function at the desired level of performance) even in the face of adversity (hardware or software faults, and even human error).
  - date: 2020-12-23
    quote: Scalability As the system grows (in data volume, traffic volume, or complexity), there should be reasonable ways of dealing with that growth.
  - date: 2020-12-23
    quote: Maintainability Over time, many different people will work on the system (engineering and operations, both maintaining current behavior and adapting the system to new use cases), and they should all be able to work on it productively.
  - date: 2020-12-27
    quote: there is a move toward systems that can tolerate the loss of entire machines, by using software fault-tolerance techniques in preference or in addition to hardware redundancy.
  - date: 2020-12-27
    quote: Latency is the duration that a request is waiting to be handled—during which it is latent, awaiting service [17].
  - date: 2020-12-27
    quote: The response time is what the client sees&#58; besides the actual time to process the request (the service time), it includes network delays and queueing delays.
  - date: 2020-12-29
    quote: since the data model has such a profound effect on what the software above it can and can’t do, it’s important to choose one that is appropriate to the application.
  - date: 2020-12-29
    quote: Most application development today is done in object-oriented programming languages, which leads to a common criticism of the SQL data model&#58; if data is stored in relational tables, an awkward translation layer is required between the objects in the application code and the database model of tables, rows, and columns.
  - date: 2020-12-29
    quote: There are many differences to consider when comparing relational databases to document databases, including their fault-tolerance properties (see Chapter 5) and handling of concurrency (see Chapter 7). In this chapter, we will concentrate only on the differences in the data model.
  - date: 2020-12-29
    quote: The database typically needs to load the entire document, even if you access only a small portion of it, which can be wasteful on large documents.
  - date: 2020-12-29
    quote: On updates to a document, the entire document usually needs to be rewritten—only modifications that don’t change the encoded size of a document can easily be performed in place [19]. For these reasons, it is generally recommended that you keep documents fairly small and avoid writes that increase the size of a document [9]. These performance limitations significantly reduce the set of situations in which document databases are useful.
  - date: 2020-12-30
    quote: Facebook maintains a single graph with many different types of vertices and edges&#58; vertices represent people, locations, events, checkins, and comments made by users; edges indicate which people are friends with each other, which checkin happened in which location, who commented on which post, who attended which event, and so on [35].
  - date: 2021-01-01
    quote: The log-structured indexes we have discussed so far are gaining acceptance, but they are not the most common type of index. The most widely used indexing
  - date: 2021-01-01
    quote: The log-structured indexes we have discussed so far are gaining acceptance, but they are not the most common type of index. The most widely used indexing structure is quite different&#58; the B-tree.
  - date: 2021-01-01
    quote: The data warehouse contains a read-only copy of the data in all the various OLTP systems in the company. Data is extracted from OLTP databases (using either a periodic data dump or a continuous stream of updates), transformed into an analysis-friendly schema, cleaned up, and then loaded into the data warehouse.
  - date: 2021-01-01
    quote: process of getting data into the warehouse is known as Extract–Transform–Load (ETL) and is illustrated in Figure 3-8.
  - date: 2021-01-01
    quote: Other columns in the fact table are foreign key references to other tables, called dimension tables. As each row in the fact table represents an event, the dimensions represent the who, what, where, when, how, and why of the event.
  - date: 2021-01-01
    quote: between sales on holidays and non-holidays. The name
  - date: 2021-01-01
    quote: The name “star schema” comes from the fact that when the table relationships are visualized, the fact table is in the middle, surrounded by its dimension tables; the connections to these tables are like the rays of a star.
  - date: 2021-01-01
    quote: The idea behind column-oriented storage is simple&#58; don’t store all the values from one row together, but store all the values from each column together instead. If each column is stored in a separate file, a query only needs to read and parse those columns that are used in that query, which can save a lot of work.
  - date: 2021-01-02
    quote: we saw that storage engines fall into two broad categories&#58; those optimized for transaction processing (OLTP), and those optimized for analytics (OLAP).
  - date: 2021-01-02
    quote: The log-structured school, which only permits appending to files and deleting obsolete files, but never updates a file that has been written.
  - date: 2021-01-02
    quote: The update-in-place school, which treats the disk as a set of fixed-size pages that can be overwritten. B-trees are the biggest example of this philosophy, being used in all major relational databases and also many nonrelational ones.
  - date: 2021-01-02
    quote: why analytic workloads are so different from OLTP&#58; when your queries require sequentially scanning across a large number of rows, indexes are much less relevant. Instead it becomes important to encode data very compactly, to minimize the amount of data that the query needs to read from disk. We discussed how column-oriented storage helps achieve this goal.
  - date: 2021-01-02
    quote: JSON’s popularity is mainly due to its built-in support in web browsers (by virtue of being a subset of JavaScript) and simplicity relative to XML.
  - date: 2021-01-02
    quote: Since the correct interpretation of data (such as numbers and binary strings) depends on information in the schema, applications that don’t use XML/JSON schemas need to potentially hardcode the appropriate
  - date: 2021-01-02
    quote: Use of XML schemas is fairly widespread, but many JSON-based tools don’t bother using schemas. Since the correct interpretation of data (such as numbers and binary strings) depends on information in the schema, applications that don’t use XML/JSON schemas need to potentially hardcode the appropriate encoding/decoding logic instead.
  - date: 2021-01-02
    quote: JSON is less verbose than XML, but both still use a lot of space compared to binary formats. This observation led to the development of a profusion of binary encodings for JSON
  - date: 2021-01-02
    quote: Apache Thrift [15] and Protocol Buffers (protobuf) [16] are binary encoding libraries that are based on the same principle. Protocol Buffers was originally developed at Google, Thrift was originally developed at Facebook, and both were made open source in 2007–08 [17].
  - date: 2021-01-04
    quote: one service makes a request to another when it requires some functionality or data from that other service. This way of building applications has traditionally been called a service-oriented architecture (SOA), more recently refined and rebranded as microservices architecture
  - date: 2021-01-04
    quote: A key design goal of a service-oriented/microservices architecture is to make the application easier to change and maintain by making services
  - date: 2021-01-04
    quote: A key design goal of a service-oriented/microservices architecture is to make the application easier to change and maintain by making services independently deployable and evolvable.
  - date: 2021-01-04
    quote: Custom RPC protocols with a binary encoding format can achieve better performance than something generic like JSON over REST. However, a RESTful API has other significant advantages&#58; it is good for experimentation and debugging (you can simply make requests to it using a web browser or the command-line tool curl, without any code generation or software installation), it is supported by all mainstream programming languages and platforms, and there is a vast ecosystem of tools available (servers, caches, load balancers, proxies, firewalls, monitoring, debugging tools, testing tools, etc.). For these reasons, REST seems to be the predominant style for public APIs. The main focus of RPC frameworks is on requests between services owned by the same organization, typically within the same datacenter.
  - date: 2021-01-04
    quote: The backward and forward compatibility properties of an RPC scheme are inherited from whatever encoding it
  - date: 2021-01-04
    quote: The backward and forward compatibility properties of an RPC scheme are inherited from whatever encoding it uses&#58;
  - date: 2021-01-04
    quote: There is no agreement on how API versioning should work (i.e., how a client can indicate which version of the API it wants to use [48]). For RESTful APIs, common approaches are to use a version number in the URL or in the HTTP Accept header.
  - date: 2021-01-04
    quote: More recently, open source implementations such as RabbitMQ, ActiveMQ, HornetQ, NATS, and Apache Kafka have become popular. We will compare them in more detail in Chapter 11.
  - date: 2021-01-04
    quote: A distributed actor framework essentially integrates a message broker and the actor programming model into a single framework.
  - date: 2021-01-04
    quote: We can conclude that with a bit of care, backward/forward compatibility and rolling upgrades are quite achievable. May your application’s evolution be rapid and your deployments be frequent.
  - date: 2021-01-05
    quote: All of the difficulty in replication lies in handling changes to replicated data, and that’s what this chapter is about. We will discuss three popular algorithms for replicating changes between nodes&#58; single-leader, multi-leader, and leaderless replication.
  - date: 2021-01-06
    quote: However, because there are so many edge cases, other replication methods are now generally preferred. Statement-based replication was used in MySQL before version 5.1. It is still sometimes used today, as it is quite compact, but by default MySQL now switches to row-based replication (discussed shortly) if there is any nondeterminism in a statement.
  - date: 2021-01-06
    quote: We can use the exact same log to build a replica on another node&#58; besides writing the log to disk, the leader also sends it across the network to its followers. When the follower processes this log, it builds a copy of the exact same data structures as found on the leader.
  - date: 2021-01-06
    quote: disadvantage is that the log describes the data on a very low level&#58; a WAL contains details of which bytes were changed in which disk blocks. This makes replication closely coupled to the storage engine. If the database changes its storage format from one version to another, it is typically not
  - date: 2021-01-06
    quote: disadvantage is that the log describes the data on a very low level&#58; a WAL contains details of which bytes were changed in which disk blocks. This makes replication closely coupled to the storage engine. If the database changes its storage format from one version to another, it is typically not possible to run different versions of the database software on the leader and the followers.
  - date: 2021-01-06
    quote: Logical (row-based) log replication An alternative is to use different log formats for replication and for the storage engine, which allows the replication log to be decoupled from the storage engine internals. This kind of replication log is called a logical log, to distinguish it from the storage engine’s (physical) data
  - date: 2021-01-06
    quote: In this situation, we need read-after-write consistency, also known as read-your-writes consistency [24]. This is a guarantee that if the user reloads the page, they will always see any updates they submitted themselves. It makes no promises about other users&#58; other users’ updates may not be visible until some later time. However, it reassures the user that their own input has been saved correctly.
  - date: 2021-01-06
    quote: When you read data, you may see an old value; monotonic reads only means that if one user makes several reads in sequence, they will not see time go backward—i.e., they will not read older data after having previously read newer data.
  - date: 2021-01-06
    quote: databases, which we will discuss in Chapter 6. If the database always applies writes in the same order, reads always see a consistent prefix, so this anomaly cannot happen. However, in many distributed databases, different partitions operate independently, so there is no global ordering of writes&#58; when a user reads from the database, they may see some parts of the database in an older state and some in a newer state.
  - date: 2021-01-06
    quote: Single-node transactions have existed for a long time. However, in the move to distributed (replicated and partitioned) databases, many systems have abandoned them, claiming that transactions are too expensive in terms of performance and availability, and asserting that eventual consistency is inevitable in a scalable system.
  - date: 2021-01-06
    quote: You need to be able to see your meetings (make read requests) and enter new meetings (make write requests) at any time, regardless of whether your device currently has an internet connection. If you make any changes while you are offline, they need to be synced with a server and your other devices when the device is next online.
  - date: 2021-01-06
    quote: As the rich history of broken calendar sync implementations demonstrates, multi-leader replication is a tricky thing to get right.
  - date: 2021-01-06
    quote: Give each write a unique ID (e.g., a timestamp, a long random number, a UUID, or a hash of the key and value), pick the write with the highest ID as the winner, and throw away the other writes. If a timestamp is used, this technique is known as last write wins (LWW). Although this approach is popular, it is dangerously prone to data loss
  - date: 2021-01-06
    quote: Operational transformation [42] is the conflict resolution algorithm behind collaborative editing applications such as Etherpad [30] and Google Docs [31]. It was designed particularly for concurrent editing of an ordered list of items, such as the list of characters that constitute
  - date: 2021-01-06
    quote: Operational transformation [42] is the conflict resolution algorithm behind collaborative editing applications such as Etherpad [30] and Google Docs [31]. It was designed particularly for concurrent editing of an ordered list of items, such as the list of characters that constitute a text document.
  - date: 2021-01-06
    quote: It once again became a fashionable architecture for databases after Amazon used it for its in-house Dynamo system [37].vi Riak, Cassandra, and Voldemort are open source datastores with leaderless replication models inspired by Dynamo, so this kind of database is also known as Dynamo-style. In some leaderless implementations, the client
  - date: 2021-01-06
    quote: Some data storage systems take a different approach, abandoning the concept of a leader and allowing any replica to directly accept writes from clients. Some of the earliest replicated data systems were leaderless [1, 44], but the idea was mostly forgotten during the era of dominance of relational databases. It once again became a fashionable architecture for databases after Amazon used it for its in-house Dynamo system [37].vi Riak, Cassandra, and Voldemort are open source datastores with leaderless replication models inspired by Dynamo, so this kind of database is also known as Dynamo-style.
  - date: 2021-01-06
    quote: More generally, if there are n replicas, every write must be confirmed by w nodes to be considered successful, and we must query at least r nodes for each read. (In our example, n = 3, w = 2, r = 2.) As long as w + r > n, we expect to get an up-to-date value when reading, because at least one of the r nodes we’re reading from must be up to date. Reads and writes that obey these r and w values are called quorum reads and writes [44].vii You can think of r and w as the minimum number of votes required for the read or write to be valid. In Dynamo-style databases, the parameters n, w, and r are typically configurable. A common choice is to make n an odd number (typically 3 or 5) and to set w = r = (n + 1) / 2 (rounded up). However, you can vary the numbers as you see fit. For example, a workload with few writes and many reads may benefit from setting w = n and r = 1. This makes reads faster, but has the disadvantage that just one failed node causes all database writes to fail.
  - date: 2021-01-07
    quote: Even if your application can tolerate stale reads, you need to be aware of the health of your replication. If it falls behind significantly, it should alert you so that you can investigate the cause (for example, a problem in the network or an overloaded node).
  - date: 2021-01-07
    quote: This is unfortunately not yet common practice, but it would be good to include staleness measurements in the standard set of metrics for databases. Eventual consistency is a deliberately vague guarantee, but for operability it’s important to be able to quantify “eventual.”
  - date: 2021-01-08
    quote: An operation A happens before another operation B if B knows about A, or depends on A, or builds upon A in some way. Whether one operation happens before another operation is the key to defining what concurrency means. In fact, we can simply say that two operations are concurrent if neither happens before the other (i.e., neither knows about the other) [54]. Thus, whenever you have two operations A and B, there are three possibilities&#58; either A happened before B, or B happened before A, or A and B are concurrent.
  - date: 2021-01-08
    quote: For defining concurrency, exact time doesn’t matter&#58; we simply call two operations concurrent if they are both unaware of each other, regardless of the physical time at which they occurred.
  - date: 2021-01-09
    quote: If the partitioning is unfair, so that some partitions have more data or queries than others, we call it skewed.
  - date: 2021-01-09
    quote: A partition with disproportionately high load is called a hot spot.
  - date: 2021-01-09
    quote: Unfortunately however, by using the hash of the key for partitioning we lose a nice property of key-range partitioning&#58; the ability to do efficient range queries.
  - date: 2021-01-09
    quote: secondary indexes are the raison d’être of search servers such as Solr and Elasticsearch.
  - date: 2021-01-09
    quote: The problem with secondary indexes is that they don’t map neatly to partitions. There are two main approaches to partitioning a database with secondary indexes&#58; document-based partitioning and term-based partitioning.
  - date: 2021-01-09
    quote: In this indexing approach, each partition is completely separate&#58; each partition maintains its own secondary indexes, covering only the documents in that partition. It doesn’t care what data is stored in other partitions. Whenever you need to write to the database—to add, remove, or update a document—you only need to deal with the partition that contains the document ID that you are writing. For that reason, a document-partitioned index is also known as a local index (as opposed to a global index, described in the next section).
  - date: 2021-01-09
    quote: if you want to search for red cars, you need to send the query to all partitions, and combine all the results
  - date: 2021-01-09
    quote: if you want to search for red cars, you need to send the query to all partitions, and combine all the results you get back.
  - date: 2021-01-09
    quote: This approach to querying a partitioned database is sometimes known as scatter/gather, and it can make read queries on secondary indexes quite expensive. Even if you query the partitions in parallel, scatter/gather is prone to tail latency amplification (see “Percentiles in Practice”). Nevertheless, it is widely used&#58;
  - date: 2021-01-09
    quote: h). We call this kind of index term-partitioned, because the term we’re looking for determines the partition of the index.
  - date: 2021-01-09
    quote: The advantage of a global (term-partitioned) index over a document-partitioned index is that it can make reads more efficient&#58; rather than doing scatter/gather over all partitions, a client only needs to make a request to the partition containing the term that it wants. However, the downside of a global index is that writes are slower and more complicated, because a write to a single document may now affect multiple partitions of the index
  - date: 2021-01-09
    quote: The process of moving load from one node in the cluster to another is called rebalancing.
  - date: 2021-01-09
    quote: the number of partitions configured at the outset is the maximum number of nodes you can have, so you need to choose it high enough to accommodate future growth. However, each partition also has management overhead, so it’s counterproductive to choose too high a number.
  - date: 2021-01-09
    quote: Dynamic partitioning is not only suitable for key range–partitioned data, but can equally well be used with hash-partitioned data. MongoDB since version 2.4 supports both key-range and hash partitioning, and it splits partitions dynamically in either case.
  - date: 2021-01-09
    quote: with a fixed number of partitions, the size of each partition is proportional to the size of the dataset. In both of these cases, the number of partitions is independent of the number of nodes.
  - date: 2021-01-09
    quote: with a fixed number of partitions, the size of each partition is proportional to the size of the dataset. In both of these cases, the number of partitions is independent of the number of nodes. A third option, used by Cassandra and Ketama, is to make the number of partitions proportional to the number of nodes—in other words, to have a fixed number of partitions per node
  - date: 2021-01-09
    quote: when you increase the number of nodes, the partitions become smaller again. Since a larger data volume generally requires a larger number of nodes to store, this approach also keeps the size of each partition fairly stable.
  - date: 2021-01-10
    quote: Many distributed data systems rely on a separate coordination service such as ZooKeeper to keep track of this cluster metadata, as illustrated in Figure 6-8. Each node registers itself in ZooKeeper, and ZooKeeper maintains the authoritative mapping of partitions to nodes.
  - date: 2021-01-10
    quote: can subscribe to this information in ZooKeeper. Whenever a partition changes ownership, or a node is added or removed, ZooKeeper notifies the routing tier so that it can keep its routing information
  - date: 2021-01-10
    quote: Whenever a partition changes ownership, or a node is added or removed, ZooKeeper notifies the routing tier so that it can keep its routing information up to date.
  - date: 2021-01-10
    quote: HBase, SolrCloud, and Kafka also use ZooKeeper to track partition assignment. MongoDB has a similar architecture, but it relies on its own config server implementation and mongos daemons as the routing tier.
  - date: 2021-01-10
    quote: datastores. However, massively parallel processing (MPP) relational database products, often used for analytics, are much more sophisticated in the types of queries they support. A typical data warehouse query contains several join, filtering, grouping, and aggregation operations. The MPP query optimizer breaks this complex query into a number of execution stages and partitions, many of which can be executed in parallel on different nodes of the database cluster.
  - date: 2021-01-10
    quote: The goal of partitioning is to spread the data and query load evenly across multiple machines, avoiding hot spots (nodes with disproportionately high load). This requires choosing a partitioning scheme that is appropriate to your data, and rebalancing the partitions when nodes are added to or removed from the cluster.
  - date: 2021-01-10
    quote: Key range partitioning, where keys are sorted, and a partition owns all the keys from some minimum up to some maximum. Sorting has the advantage that efficient range queries are possible, but there is a risk of hot spots if the application often accesses keys that are close together in the sorted order. In this approach, partitions are typically rebalanced dynamically by splitting the range into two subranges when a partition gets too big.
  - date: 2021-01-10
    quote: Hash partitioning, where a hash function is applied to each key, and a partition owns a range of hashes. This method destroys the ordering of keys, making range queries inefficient, but may distribute load more evenly. When partitioning by hash, it is common to create a fixed number of partitions in advance, to assign several partitions to each node, and to move entire partitions from one node to another when nodes are added or removed. Dynamic partitioning can also be used.
  - date: 2021-01-10
    quote: ACID, which stands for Atomicity, Consistency, Isolation, and Durability.
  - date: 2021-01-10
    quote: of ambiguity around the meaning of isolation [8]. The high-level idea is sound, but the devil is in the details. Today, when a system claims to be “ACID compliant,” it’s unclear what guarantees you can actually expect. ACID has unfortunately become mostly a marketing term.
  - date: 2021-01-10
    quote: The ability to abort a transaction on error and have all writes from that transaction discarded is the defining feature of ACID atomicity. Perhaps abortability would have been a better term than atomicity, but we will stick
  - date: 2021-01-10
    quote: The ability to abort a transaction on error and have all writes from that transaction discarded is the defining feature of ACID atomicity. Perhaps abortability would have been a better term than atomicity, but we will stick with atomicity since that’s the usual word.
  - date: 2021-01-10
    quote: database only stores it.) Atomicity, isolation, and durability are properties of the database, whereas consistency (in the ACID sense) is a property of the application. The application may rely on the database’s atomicity and isolation properties in order to achieve consistency, but it’s not up to the database alone. Thus,
  - date: 2021-01-10
    quote: Atomicity, isolation, and durability are properties of the database, whereas consistency (in the ACID sense) is a property of the application. The application may rely on the database’s atomicity and isolation properties in order to achieve consistency, but it’s not up to the database alone. Thus, the letter C doesn’t really belong in ACID.i
  - date: 2021-01-12
    quote: Isolation in the sense of ACID means that concurrently executing transactions are isolated from each other&#58; they cannot step on each other’s toes.
  - date: 2021-01-12
    quote: provide a safe place where data can be stored without fear of losing it.
  - date: 2021-01-12
    quote: snapshot isolation is readers never block writers, and writers never block readers.
  - date: 2021-01-12
    quote: saw for preventing dirty reads in Figure 7-4. The database must potentially keep several different committed versions of an object, because various in-progress transactions may need to see the state of the database at different points in time. Because it maintains several versions of an object side by side, this technique is known as multi-version concurrency control (MVCC).
  - date: 2021-01-12
    quote: The database must potentially keep several different committed versions of an object, because various in-progress transactions may need to see the state of the database at different points in time. Because it maintains several versions of an object side by side, this technique is known as multi-version concurrency control (MVCC).
  - date: 2021-01-14
    quote: The lost update problem can occur if an application reads some value from the database, modifies it, and writes back the modified value (a read-modify-write cycle). If two transactions do this concurrently, one of the modifications can be lost, because the second write does not include the first modification.
  - date: 2021-01-14
    quote: Atomic operations are usually implemented by taking an exclusive lock on the object when it is read so that no other transaction can read it until the update has been applied. This technique is sometimes known as cursor stability
  - date: 2021-01-14
    quote: database’s built-in atomic operations don’t provide the necessary functionality, is for the application to explicitly lock objects that are going to be updated.
  - date: 2021-01-14
    quote: The FOR UPDATE clause indicates that the database should take a lock on all rows returned by this query.
  - date: 2021-01-14
    quote: An alternative is to allow them to execute in parallel and, if the transaction manager detects a lost update, abort the transaction and force it to retry its read-modify-write cycle. An advantage of this approach is that
  - date: 2021-01-14
    quote: An alternative is to allow them to execute in parallel and, if the transaction manager detects a lost update, abort the transaction and force it to retry its read-modify-write cycle.
  - date: 2021-01-14
    quote: You can think of write skew as a generalization of the lost update problem. Write skew can occur if two transactions read the same objects, and then update some of those objects (different transactions may update different objects).
  - date: 2021-01-14
    quote: In the special case where different transactions update the same object, you get a dirty write or lost update anomaly (depending on the timing).
  - date: 2021-01-14
    quote: This effect, where a write in one transaction changes the result of a search query in another transaction, is called a phantom [3]. Snapshot isolation avoids phantoms in read-only queries, but in read-write transactions like the examples we discussed, phantoms can lead to particularly tricky cases of write skew.
  - date: 2021-01-15
    quote: Serializable isolation is usually regarded as the strongest isolation level. It guarantees that even
  - date: 2021-01-15
    quote: Serializable isolation is usually regarded as the strongest isolation level. It guarantees that even though transactions may execute in parallel, the end result is the same as if they had executed one at a time, serially, without any concurrency. Thus, the database guarantees that if the transactions behave correctly when run individually, they continue to be correct when run concurrently—in other words, the database prevents all possible race conditions. But if serializable isolation is so much better than the mess of weak isolation levels, then why isn’t everyone using it? To answer this question, we need to look at the options for implementing serializability, and how they perform.
  - date: 2021-01-15
    quote: Modern implementations of stored procedures have abandoned PL/SQL and use existing general-purpose programming languages instead&#58; VoltDB uses Java or Groovy, Datomic uses Java or Clojure, and Redis uses Lua.
  - date: 2021-01-15
    quote: In 2PL, writers don’t just block other writers; they also block readers and vice versa. Snapshot isolation has the mantra readers never block writers, and writers never block readers (see “Implementing snapshot isolation”), which captures this key difference between snapshot isolation and two-phase locking. On the other hand, because 2PL provides serializability, it protects against all the race conditions discussed earlier, including lost updates and write skew.
  - date: 2021-01-15
    quote: Since so many locks are in use, it can happen quite easily that transaction A is stuck waiting for transaction B to release its lock, and vice versa. This situation is called deadlock. The database automatically detects deadlocks between transactions and aborts one of them so that the others can make progress. The aborted transaction needs to be retried by the application.
  - date: 2021-01-15
    quote: Performance of two-phase locking The big downside of two-phase locking, and the reason why it hasn’t been used by everybody since the 1970s, is performance&#58;
  - date: 2021-01-16
    quote: Index-range locks are not as precise as predicate locks would be (they may lock a bigger range of objects than is strictly necessary to maintain serializability), but since they have much lower overheads, they are a good compromise.
  - date: 2021-01-16
    quote: Are serializable isolation and good performance fundamentally at odds with each other? Perhaps not&#58; an algorithm called serializable snapshot isolation (SSI) is very promising. It provides full serializability, but has only a small performance penalty compared to snapshot isolation.
  - date: 2021-01-16
    quote: Optimistic in this context means that instead of blocking if something potentially dangerous happens, transactions continue anyway, in the
  - date: 2021-01-16
    quote: Optimistic in this context means that instead of blocking if something potentially dangerous happens, transactions continue anyway, in the hope that everything will turn out all right. When a transaction wants to commit, the database checks whether anything bad happened (i.e., whether isolation was violated); if so, the transaction is aborted and has to be retried. Only transactions that executed serializably are allowed to commit.
  - date: 2021-01-16
    quote: Compared to two-phase locking, the big advantage of serializable snapshot isolation is that one transaction doesn’t need to block waiting for locks held by another transaction. Like under snapshot isolation, writers don’t block readers, and vice versa. This design principle makes query latency much more predictable and less variable. In particular, read-only queries can run on a consistent snapshot without requiring any locks, which is very appealing for read-heavy workloads.
  - date: 2021-01-16
    quote: Compared to serial execution, serializable snapshot isolation is not limited to the throughput of a single CPU core&#58; FoundationDB distributes the detection of serialization conflicts across multiple machines, allowing it to scale to very high throughput. Even though data may be partitioned across multiple machines, transactions can read and write data in multiple partitions while ensuring serializable isolation
  - date: 2021-01-17
    quote: In distributed systems, suspicion, pessimism, and paranoia pay off.
  - date: 2021-01-17
    quote: the distributed systems we focus on in this book are shared-nothing systems&#58; i.e., a bunch of machines connected by a network. The network is the only way those machines can communicate—we assume that each machine has its own memory and disk, and one machine cannot access another machine’s memory or disk (except by making requests to a service over the network).
  - date: 2021-01-17
    quote: It found that adding redundant networking gear doesn’t reduce faults as much as you might hope, since it doesn’t guard against human error (e.g., misconfigured switches), which is a major cause of outages.
  - date: 2021-01-17
    quote: Even if network faults are rare in your environment, the fact that faults can occur means that your software needs to be able to handle them. Whenever any communication happens over a network, it may fail—there is no way around it.
  - date: 2021-01-17
    quote: Some latency-sensitive applications, such as videoconferencing and Voice over IP (VoIP), use UDP rather than TCP. It’s a trade-off between reliability and variability of delays&#58; as UDP does not perform flow control and does not retransmit lost packets, it avoids some of the reasons for variable network delays (although it is still susceptible to switch queues and scheduling delays). UDP is a good choice in situations where delayed data is worthless. For example, in a VoIP phone call, there probably isn’t enough time to retransmit a lost packet before its data is due to be played over the loudspeakers.
  - date: 2021-01-17
    quote: Even better, rather than using configured constant timeouts, systems can continually measure response times and their variability (jitter), and automatically adjust timeouts according to the observed response time distribution. This can be done with a Phi Accrual failure detector [30], which is used for example in Akka and Cassandra [31]. TCP retransmission timeouts also work similarly [27].
  - date: 2021-01-17
    quote: When you make a call over the telephone network, it establishes a circuit&#58; a fixed, guaranteed amount of bandwidth is allocated for the call, along the entire route between the two callers. This circuit remains in place until the call ends
  - date: 2021-01-17
    quote: Note that a circuit in a telephone network is very different from a TCP connection&#58; a circuit is a fixed amount of reserved bandwidth which nobody else can use while the circuit is established, whereas the packets of a TCP connection opportunistically use whatever network bandwidth is available. You can give TCP a variable-sized block of data (e.g., an email or a web page), and it will try to transfer it in the shortest time possible. While a TCP connection is idle, it doesn’t use any bandwidth.
  - date: 2021-01-17
    quote: using circuits for bursty data transfers wastes network capacity and makes transfers unnecessarily slow. By contrast, TCP dynamically adapts the rate of data
  - date: 2021-01-17
    quote: using circuits for bursty data transfers wastes network capacity and makes transfers unnecessarily slow. By contrast, TCP dynamically adapts the rate of data transfer to the available network capacity.
  - date: 2021-01-17
    quote: the downside of variable delays. Variable delays in networks are not a law of nature, but simply the result of a cost/benefit trade-off.
  - date: 2021-01-17
    quote: Variable delays in networks are not a law of nature, but simply the result of a cost/benefit trade-off.
  - date: 2021-01-17
    quote: Monotonic clocks A monotonic clock is suitable for measuring a duration (time interval), such as a timeout or a service’s response time&#58;
  - date: 2021-01-17
    quote: monotonic clock is suitable for measuring a duration (time interval), such as a timeout or a service’s response time&#58;
  - date: 2021-01-17
    quote: The name comes from the fact that they are guaranteed to always move forward (whereas a time-of-day clock may jump back in time).
  - date: 2021-01-17
    quote: Monotonic Versus Time-of-Day Clocks Modern computers have at least two different kinds of clocks&#58; a time-of-day clock and a monotonic clock. Although they both measure time, it is important to distinguish the two, since they serve different purposes.
  - date: 2021-01-17
    quote: elapsed between the two checks. However, the absolute value of the clock is meaningless&#58; it might be the number of nanoseconds since the computer was started, or something similarly arbitrary.
  - date: 2021-01-17
    quote: The resolution of monotonic clocks is usually quite good&#58; on most systems they can measure time intervals in microseconds or less.
  - date: 2021-01-19
    quote: The same is true with clocks&#58; although they work quite well most of the time, robust software needs to be prepared to deal with incorrect clocks.
  - date: 2021-01-19
    quote: its quartz clock is defective or its NTP client is misconfigured, most things will seem to work fine, even though its clock gradually drifts further and further away from reality. If some piece of software is relying on an accurately synchronized clock, the result is more likely to be silent and subtle data loss than a dramatic crash [53, 54].
  - date: 2021-01-19
    quote: it’s important to be aware that the definition of “recent” depends on a local time-of-day clock, which may well be incorrect.
  - date: 2021-01-21
    quote: When writing multi-threaded code on a single machine, we have fairly good tools for making it thread-safe&#58; mutexes, semaphores, atomic counters, lock-free data structures, blocking queues, and so on. Unfortunately, these tools don’t directly translate to distributed systems, because a distributed system has no shared memory—only messages sent over an unreliable network.
  - date: 2021-01-21
    quote: we have explored the ways in which distributed systems are different from programs running on a single computer&#58; there is no shared memory, only message passing via an unreliable network with variable delays, and the systems may suffer from partial failures, unreliable clocks, and processing pauses.
  - date: 2021-01-22
    quote: Safety is often informally defined as nothing bad happens,
  - date: 2021-01-22
    quote: Safety is often informally defined as nothing bad happens, and liveness as something good eventually happens.
  - date: 2021-01-23
    quote: scalability is not the only reason for wanting to use a distributed system. Fault tolerance and low latency (by placing data geographically close to users) are equally important goals, and those things cannot be achieved with a single node.
  - date: 2021-01-23
    quote: The best way of building fault-tolerant systems is to find some general-purpose abstractions with useful guarantees, implement them once, and then let applications rely on those guarantees. This is the same approach as we used with transactions in Chapter 7&#58; by using a transaction, the application can pretend that there are no crashes (atomicity), that nobody else is concurrently accessing the database (isolation), and that storage devices are perfectly reliable (durability).
  - date: 2021-01-23
    quote: transaction isolation is primarily about avoiding race conditions due to concurrently executing transactions, whereas distributed consistency is mostly about coordinating the state of replicas in the face of delays and faults.
  - date: 2021-01-23
    quote: In a linearizable system, as soon as one client successfully completes a write, all clients reading from the database must be able to see the value just written.
  - date: 2021-01-23
    quote: It guarantees that transactions behave the same as if they had executed in some serial order (each transaction running to completion before the next transaction starts).
  - date: 2021-01-23
    quote: Linearizability Linearizability is a recency guarantee on reads and writes of a register (an individual object). It doesn’t group operations together into transactions, so it does not prevent problems such as write skew
  - date: 2021-01-23
    quote: Linearizability is a recency guarantee on reads and writes of a register (an individual object). It doesn’t group operations together into transactions, so it does not prevent problems such as write skew
  - date: 2021-01-23
    quote: A database may provide both serializability and linearizability, and this combination is known as strict serializability or strong one-copy serializability (strong-1SR)
  - date: 2021-01-24
    quote: your application requires linearizability, and some replicas are disconnected from the other replicas due to a network problem, then some replicas cannot process requests while they are disconnected&#58; they must either wait until the network problem is fixed, or return an error (either way, they become unavailable).
  - date: 2021-01-24
    quote: If your application requires linearizability, and some replicas are disconnected from the other replicas due to a network problem, then some replicas cannot process requests while they are disconnected&#58; they must either wait until the network problem is fixed, or return an error (either way, they become unavailable).
  - date: 2021-01-24
    quote: your application does not require linearizability, then it can be written in a way that each replica can process requests independently, even if it is disconnected from other replicas (e.g., multi-leader). In this case, the application can remain available in the face of a network problem, but its behavior is not linearizable.
  - date: 2021-01-24
    quote: If your application does not require linearizability, then it can be written in a way that each replica can process requests independently, even if it is disconnected from other replicas (e.g., multi-leader). In this case, the application can remain available in the face of a network problem, but its behavior is not linearizable.
  - date: 2021-01-24
    quote: applications that don’t require linearizability can be more tolerant of network problems. This insight is popularly known as the CAP theorem
  - date: 2021-01-24
    quote: The CAP theorem as formally defined [30] is of very narrow scope&#58; it only considers one consistency model (namely linearizability) and one kind of fault (network partitions,vi or nodes that are alive but disconnected from each other). It doesn’t say anything about network delays, dead nodes, or other trade-offs. Thus, although CAP has been historically influential, it has little practical value for designing systems
  - date: 2021-01-24
    quote: Linearizability is slow—and this is true all the time, not only during a network fault.
  - date: 2021-01-24
    quote: they are concurrent. This means that causality defines a partial order, not a total order&#58; some operations are ordered with respect to each other, but some are incomparable.
  - date: 2021-01-24
    quote: In a linearizable system, we have a total order of operations&#58;
  - date: 2021-01-24
    quote: causal consistency is the strongest possible consistency model that does not slow down due to network delays, and remains available in the face of network failures
  - date: 2021-01-27
    quote: it can be proved that a linearizable compare-and-set (or increment-and-get) register and total order broadcast are both equivalent to consensus [28, 67]. That is, if you can solve one of these problems, you can transform it into a solution for the others. This is quite a profound and surprising insight!
  - date: 2021-01-28
    quote: DON’T CONFUSE 2PC AND 2PL Two-phase commit (2PC) and two-phase locking (see “Two-Phase Locking (2PL)”) are two very different things. 2PC provides atomic commit in a distributed database, whereas 2PL provides serializable isolation. To avoid confusion, it’s best to think of them as entirely separate concepts and to ignore the unfortunate similarity in the names.
  - date: 2021-01-31
    quote: The validity property exists mostly to rule out trivial solutions&#58; for example, you could have an algorithm that always decides null, no matter what was proposed; this algorithm would satisfy the agreement and integrity properties, but not the validity property.
  - date: 2021-01-31
    quote: However, most implementations of consensus ensure that the safety properties—agreement, integrity, and validity—are always met, even if a majority of nodes fail or there is a severe network problem [92]. Thus, a large-scale outage can stop the system from being able to process requests, but it cannot corrupt the consensus system by causing it to make invalid decisions.
  - date: 2021-02-01
    quote: It seems that in order to elect a leader, we first need a leader. In order to solve consensus, we must first solve consensus. How do we break out of this conundrum?
  - date: 2021-02-01
    quote: Every time the current leader is thought to be dead, a vote is started among the nodes to elect a new leader. This election is given an incremented epoch number, and thus epoch numbers are totally ordered and monotonically increasing. If there is a conflict between two different leaders in two different epochs (perhaps because the previous leader actually wasn’t dead after all), then the leader with the higher epoch number prevails.
  - date: 2021-02-01
    quote: linearizability, a popular consistency model&#58; its goal is to make replicated data appear as though there were only a single copy, and to make all operations act on it
  - date: 2021-02-01
    quote: causality, which imposes an ordering on events in a system (what happened before what, based on cause and effect). Unlike linearizability, which puts all operations in a single, totally ordered timeline, causality provides us with a weaker consistency model&#58; some things can be concurrent, so the version history is like a timeline with branching and merging. Causal consistency does not have the coordination overhead of linearizability and is much less sensitive to network problems.
  - date: 2021-02-01
    quote: the example of ensuring that a username is unique and rejecting concurrent registrations for the same username. If one node is going to accept a registration, it needs to somehow know that another node isn’t concurrently in the process of registering the same name. This problem led us toward consensus.
  - date: 2021-02-18
    quote: Like a batch processing system, a stream processor consumes inputs and produces outputs (rather than responding to requests). However, a stream job operates on events shortly after they happen, whereas a batch job operates on a fixed set of input data. This difference allows stream processing systems to have lower latency than the equivalent batch systems.
  - date: 2021-02-21
    quote: Another common use for grouping is collating all the activity events for a particular user session, in order to find out the sequence of actions that the user took—a process called sessionization [37]. For example, such analysis could be used to work out whether users who were shown a new version of your website are more likely to make a purchase than those who were shown the old version (A/B testing), or to calculate whether some marketing activity is worthwhile.
  - date: 2021-02-21
    quote: genome sequences, or any other kind of data. To put it bluntly, Hadoop opened up the possibility of indiscriminately dumping data into HDFS, and only later figuring out how to process it further [53]. By contrast, MPP databases typically require careful up-front modeling of the data and query patterns before importing the data into the database’s proprietary storage format.
  - date: 2021-02-21
    quote: To put it bluntly, Hadoop opened up the possibility of indiscriminately dumping data into HDFS, and only later figuring out how to process it further [53]. By contrast, MPP databases typically require careful up-front modeling of the data and query patterns before importing the data into the database’s proprietary storage format.
  - date: 2021-02-21
    quote: The idea is similar to a data warehouse (see “Data Warehousing”)&#58; simply bringing data from various parts of a large organization together in one place is valuable, because it enables joins across datasets that were previously disparate. The careful schema design required by an MPP database slows down that centralized data collection; collecting data in its raw form, and worrying about schema design later, allows the data collection to be speeded up (a concept sometimes known as a “data lake” or “enterprise data hub” [55]).
  - date: 2021-02-21
    quote: This approach has been dubbed the sushi principle&#58; “raw data is better”
  - date: 2021-02-21
    quote: This architecture allows non-production (low-priority) computing resources to be overcommitted, because the system knows that it can reclaim the resources if necessary. Overcommitting resources in turn allows better utilization of machines and greater efficiency compared to systems that segregate production and non-production tasks.
  - date: 2021-02-22
    quote: A widely used alternative is to send messages via a message broker (also known as a message queue), which is essentially a kind of database that is optimized for handling message streams [13]. It runs as a server, with producers and consumers connecting to it as clients.
  - date: 2021-02-22
    quote: Why can we not have a hybrid, combining the durable storage approach of databases with the low-latency notification facilities of messaging? This is the idea behind log-based message brokers.
  - date: 2021-02-23
    quote: Change data capture is a mechanism for ensuring that all changes made to the system of record are also reflected in the derived data systems so that the derived
  - date: 2021-02-23
    quote: Change data capture is a mechanism for ensuring that all changes made to the system of record are also reflected in the derived data systems so that the derived systems have an accurate copy of the data.
  - date: 2021-02-24
    quote: Transaction logs record all the changes made to the database. High-speed appends are the only way to change the log. From this perspective, the contents of the database hold a caching of the latest record values in the logs. The truth is the log. The database is a cache of a subset of the log. That cached subset happens to be the latest value of each record and index value from the log.
  - date: 2021-02-26
    quote: Complex event processing Complex event processing (CEP) is an approach developed in the 1990s for analyzing event streams, especially geared toward the kind of application that requires searching for certain event patterns [65, 66]. Similarly to the way that a regular expression allows you to search for certain patterns of characters in a string, CEP allows you to specify rules to search for certain patterns of events in a stream.
  - date: 2021-02-26
    quote: CEP engines reverse these roles&#58; queries are stored long-term, and events from the input streams continuously flow past them in search of a query that matches an event pattern [68].
  - date: 2021-02-26
    quote: The boundary between CEP and stream analytics is blurry, but as a general rule, analytics tends to be less interested in finding specific event sequences and is more oriented toward aggregations and statistical metrics over a large number of events—for
  - date: 2021-02-27
    quote: If the highest aim of a captain was the preserve his ship, he would keep it in port forever.)
  - date: 2021-02-28
    quote: Faced with this profusion of alternatives, the first challenge is then to figure out the mapping between the software products and the circumstances in which they are a good fit.
  - date: 2021-02-28
    quote: If it is possible for you to funnel all user input through a single system that decides on an ordering for all writes, it becomes much easier to derive other representations of the data by processing the writes in the same order.
  - date: 2021-02-28
    quote: In the absence of widespread support for a good distributed transaction protocol, I believe that log-based derived data is the most promising approach for integrating different data systems. However, guarantees such as reading your own writes are useful, and I don’t think that it is productive to tell everyone “eventual consistency is inevitable—suck it up and learn to deal with it” (at least not without good guidance on how to deal with it).
  - date: 2021-02-28
    quote: building for scale that you don’t need is wasted effort and may lock you into an inflexible design. In effect, it is a form of premature optimization.
  - date: 2021-02-28
    quote: By themselves, TCP, database transactions, and stream processors cannot entirely rule out these duplicates. Solving the problem requires an end-to-end solution&#58; a transaction identifier that is passed all the way from the end-user client to the database.
  - date: 2021-02-28
    quote: The end-to-end argument also applies to checking the integrity of data&#58; checksums built into Ethernet, TCP, and TLS can detect corruption of packets in the network, but they cannot detect corruption due to bugs in the software at the sending and receiving ends of the network connection, or corruption on the disks where the data is stored. If you want to catch all possible sources of data corruption, you also need end-to-end checksums. A similar argument applies with encryption [55]&#58; the password on your home WiFi network protects against people snooping your WiFi traffic, but not against attackers elsewhere on the internet; TLS/SSL between your client and the server protects against network attackers, but not against compromises of the server. Only end-to-end encryption and authentication can protect against all of these things.
  - date: 2021-03-01
    quote: In slogan form&#58; violations of timeliness are “eventual consistency,” whereas violations of integrity are “perpetual inconsistency.”
  - date: 2021-03-01
    quote: in most applications, integrity is much more important than timeliness. Violations of timeliness can be annoying and confusing, but violations of integrity can be catastrophic.
  - date: 2021-03-01
    quote: reliable stream processing systems can preserve integrity without requiring distributed transactions and an atomic commit protocol, which means they can potentially achieve comparable correctness with much better performance and operational robustness.
  - date: 2021-03-01
    quote: an interesting property of the event-based dataflow systems that we have discussed in this chapter is that they decouple timeliness and integrity.
  - date: 2021-03-01
    quote: These applications do require integrity&#58; you would not want to lose a reservation, or have money disappear due to mismatched credits and debits. But they don’t require timeliness on the enforcement of the constraint&#58; if you have sold more items than you have in the warehouse, you can patch up the problem after the fact by apologizing.
  - date: 2021-03-01
    quote: these observations mean that dataflow systems can provide the data management services for many applications without requiring coordination, while still giving strong integrity guarantees. Such coordination-avoiding data systems have a lot of appeal&#58; they can achieve better performance and fault tolerance than systems that need to perform synchronous coordination
  - date: 2021-03-01
    quote: Another way of looking at coordination and constraints&#58; they reduce the number of apologies you have to make due to inconsistencies, but potentially also reduce the performance and availability of your system, and thus potentially increase the number of apologies you have to make due to outages. You cannot reduce the number of apologies to zero, but you can aim to find the best trade-off for your needs—the sweet spot where there are neither too many inconsistencies nor too many availability problems.
  - date: 2021-03-01
    quote: When services become good at predicting what content users want to see, they may end up showing people only opinions they already agree with, leading to echo chambers in which stereotypes, misinformation, and polarization can breed.
  - date: 2021-03-02
    quote: In the words of Bruce Schneier [96]&#58; Data is the pollution problem of the information age, and protecting privacy is the
  - date: 2021-03-02
    quote: In the words of Bruce Schneier [96]&#58; Data is the pollution problem of the information age, and protecting privacy is the
  - date: 2021-03-02
    quote: In the words of Bruce Schneier [96]&#58; Data is the pollution problem of the information age, and protecting privacy is the
  - date: 2021-03-02
    quote: environmental challenge. Almost all computers produce information. It stays around, festering. How we deal with it—how we contain it and how we dispose of it—is central to the health of our information economy. Just as we look back today at the early decades of the industrial age and wonder how our ancestors could have ignored pollution in their rush to build an industrial world, our grandchildren will look back at us during these early decades of the information age and judge us on how we addressed the challenge of data collection and misuse. We should try to make them proud.
  - date: 2021-03-02
    quote: We discussed how to solve this data integration problem by using batch processing and event streams to let data changes flow between different systems.
  - date: 2021-03-02
    quote: We discussed how to solve this data integration problem by using batch processing and event streams to let data changes flow between different systems. In this approach, certain systems are designated as systems of record, and other data is derived from them through transformations. In this way we can maintain indexes, materialized views, machine learning models, statistical summaries, and more. By making these derivations and transformations asynchronous and loosely coupled, a problem in one area is prevented from spreading to unrelated parts of the system, increasing the robustness and fault-tolerance of the system as a whole.
  - date: 2021-03-02
    quote: By structuring applications around dataflow and checking constraints asynchronously, we can avoid most coordination and create systems that maintain integrity but still perform well, even in geographically distributed scenarios and in the presence of faults.
---

## _{{page.bookauthor}}_

{% for quote in page.quotes reversed %}

#### {{ quote.date | date: '%B %d, %Y' }}

{{ quote.quote }}
{% endfor %}
