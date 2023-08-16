# ElastiCache
- it is for redis and memcached
- in memory databases with really high performance and low latency
- helps load off of db for read intensive workloads
- helps make your application stateless
- involves heavy application code changes
  
## ElatiCache Redis v/s Memcached

### Redis
- Multi AZ with with Auto Failover
- read replicas to scale reads and high availability
- data durability using AOF
- backup and restore features
- supports sets and sorted features


### Memcached
- multi node for partitioning of data (sharding)
- no high avalability (replication)
- non persistent
- no backup and restore
- multi threaded architecture
  
