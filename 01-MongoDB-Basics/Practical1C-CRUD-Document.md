# Practical 1C – Insert, Query, Update and Delete a Document

## Commands

```bash
use Romal

# ---------- INSERT ----------
db.Doc.insert({Name:"Romal", Age:10})

# ---------- QUERY (FIND) ----------
db.Doc.find()

# ---------- UPDATE ----------
db.Doc.update({Name:"Romal"}, {$set:{Age:20}})
db.Doc.find()

# ---------- DELETE ----------
db.Doc.remove({Name:"Romal"})
```

## Expected Output

```
> db.Doc.insert({Name:"Romal", Age:10})
WriteResult({ "nInserted" : 1 })

> db.Doc.find()
{ "_id" : ObjectId("..."), "Name" : "Romal", "Age" : 10 }

> db.Doc.update({Name:"Romal"}, {$set:{Age:20}})
WriteResult({ "nMatched" : 1, "nUpserted" : 0, "nModified" : 1 })

> db.Doc.find()
{ "_id" : ObjectId("..."), "Name" : "Romal", "Age" : 20 }

> db.Doc.remove({Name:"Romal"})
WriteResult({ "nRemoved" : 1 })
```
