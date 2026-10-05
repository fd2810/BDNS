# Practical 1B – Create, Display and Drop Collection

## Commands

```bash
use Romal

# Show collections (should be empty)
show collections

# Create a new collection
db.createCollection("Practical1")

# Display collections
show collections

# Drop the collection
db.Practical1.drop()
```

## Expected Output

```
> use Romal
switched to db Romal

> show collections

> db.createCollection("Practical1")
{ "ok" : 1 }

> show collections
Practical1

> db.Practical1.drop()
true
```
