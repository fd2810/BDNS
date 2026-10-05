# Practical 1A – Create and Drop Database

## Commands

```bash
# Show all existing databases
show dbs

# Switch to (or create) a database named Romal
use Romal

# Create a collection so the database becomes visible
db.createCollection("Practical1")

# Show databases again – Romal will now appear
show dbs

# Drop the entire database
db.dropDatabase()
```

## Expected Output

```
> show dbs
Employee     0.000GB
Romal_239720 0.000GB
admin        0.000GB
config       0.000GB
local        0.000GB

> use Romal
switched to db Romal

> db.createCollection("Practical1")
{ "ok" : 1 }

> show dbs
Employee     0.000GB
Romal        0.000GB
Romal_239720 0.000GB
admin        0.000GB
config       0.000GB
local        0.000GB

> db.dropDatabase()
{ "ok" : 1 }
```
