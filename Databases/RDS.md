# RDS

- for databases that use sql as a query language
- allows you to create db in the cloud that are managed by AWS
  - postgres, aurora, mysql, maria db, oracle, microsoft sql server
 
### Features
- automatic scaling
- you have to set maximum storage threshhold
- automatically modify storage if the free storage is less than 10% of what has been allocated and the low storage has been lasting for more than five minutes and six hours have passed since the last modification.
- If that's the case then the storage will auto increase when you enable it. This is very helpful for applications which that have a unpredictable workload and this supports all database engines for RDS, just as MariaDB, MySQL, PostgreSQL, SQL server, and Oracle.

### Read replicas for read scalability
- create upto 15 read replicas within az, cross az or cross region
- replication is async, so reads are consistent

### read replica use case
- you have a production db that is taking a normal load
- you want to run some analytics over your data
- you will have to create a read replica to run the new workload
- the production application is unaffected
- rr are not used for update, insert and delete

#### Read replicas network cost
- within the same region, no fee
- fee applicable for cross region

### multi az disaster recovery
- sync relication
- master db in AZ A and standby db in AZ B. If there is a failure in master instnace traffic will be pointed to standby instance (one dns name automatic app failover to standby)
- no manual intervention in apps
- not used for scaling

## Note
- read replicas can be setup as multiaz for disaster recovery

### from single az to multi az
- zero downtime operation(no need to stop the az)
- internal working
  - first snapshot will be taken
  - a new db is restored using that ss in new az
  - syncronization is established within the two az
  


### RDS Custom for Oracle and Microsoft SQL Server
- managed oracle and Microsoft sql server database with os and database customization
- access to underlying database and os so you can
  - configure settings
  - install patches
  - enable native features
  - ssh
- good practice to take a snapshot before any customization


### Note
- in an rds databse you pay for storage, so if you want to use rds for 2 hrs and then stop it. what you can do is after using it take a snapshot and delete the original db this way you save money .. then you can restore it anytime










