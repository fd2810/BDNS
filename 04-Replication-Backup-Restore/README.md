# Practical 4 – Replication, Backup and Restore

> Note: Full commands for replication depend on your MongoDB setup (standalone vs replica set).  
> Below are the standard student-friendly steps.

## A. Create a Replica Set (Basic Steps)

1. Stop MongoDB service.
2. Start MongoDB with replica set option:

```bash
mongod --replSet rs0 --port 27017 --dbpath /data/db
```

3. Open mongo shell and initiate:

```bash
rs.initiate()
rs.status()
```

## B. Create Backup of Existing Database

```bash
# Backup a specific database
mongodump --db TYITDB239720 --out /backup/TYITDB239720

# Backup all databases
mongodump --out /backup/all
```

## C. Restore Database from Backup

```bash
# Restore a specific database
mongorestore --db TYITDB239720 /backup/TYITDB239720/TYITDB239720

# Restore all
mongorestore /backup/all
```

## Useful Commands

```bash
# Show current replica set status
rs.status()

# Add secondary member (example)
rs.add("localhost:27018")

# Check configuration
rs.conf()
```
