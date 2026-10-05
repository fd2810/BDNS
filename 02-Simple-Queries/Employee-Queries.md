# Practical 2 – Simple Queries with MongoDB (Employee)

## 1. Insert and Display Documents

```bash
use Employee

db.col.insertMany([
  {Name:"Smitu",  Salary:100000, Dept:"ID",        City:"Mumbai"},
  {Name:"Romal",  Salary:15000,  Dept:"IT",        City:"Thane"},
  {Name:"Sujal",  Salary:9000,   Dept:"Tester",    City:"Bandra"},
  {Name:"Manav",  Salary:30000,  Dept:"Finance",   City:"Kurla"},
  {Name:"Swathi", Salary:40000,  Dept:"Developer", City:"Pune"}
])

db.col.find()
```

## 2. Employees living in Mumbai

```bash
db.col.find({City:"Mumbai"})
```

## 3. Employee in Kurla with Salary > 19000

```bash
db.col.find({City:"Kurla", Salary:{$gt:19000}})
```

## 4. Salary greater than or equal to 10000 but less than 20000

```bash
db.col.find({Salary:{$gte:10000, $lt:20000}})
```

## 5. Employees in Thane or Mumbai with Salary > 10000

```bash
db.col.find({
  $or: [{City:"Mumbai"}, {City:"Thane"}],
  Salary: {$gt:10000}
})
```

## 6. Salary not equal to 10000 and working in Developer or Tester

```bash
db.col.find({
  $or: [{Dept:"Developer"}, {Dept:"Tester"}],
  Salary: {$ne:10000}
})
```
