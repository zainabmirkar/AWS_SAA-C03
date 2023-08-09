# Aurora

- postgres and mysql are only supported for Aurora
- 5X performance over mysql in rds and 3X performance of postgres on rds
- storage grows automatically from 10gb up to 128tb
- can have upto 15 replicas and relication process is faster than mysql
- self healing and auto expanding
- support for cross region
- master + upto 15 read replicas
- automatic failover for master in less than 30 seconds


### Aurora db cluster
- writer endpoint pointing to the master
- reader endpoint connection loadbalancing for all the read replicas

### Features
- restore data at any point in time without using backups
- automatic patching with 0 downtime
- push button scaling
- advanced monitoring
- routine maintenance
- backup and recovery
- automatic failover
- isolation and security
