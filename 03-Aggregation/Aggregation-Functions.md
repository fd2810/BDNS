# Practical 3 – Aggregation Functions

## Insert Sample Data

```bash
use Aggregate

db.col.insertMany([
  {Name:"Romal", Age:17, City:"Mumbai", Salary:12000},
  {Name:"Rohan", Age:22, City:"Thane",  Salary:60000},
  {Name:"Sujal", Age:19, City:"Mumbai", Salary:3000},
  {Name:"Manav", Age:47, City:"Pune",   Salary:55000},
  {Name:"Ria",   Age:34, City:"Mumbai", Salary:83000}
])

db.col.find()
```

## 1. Count (Group by City)

```bash
db.col.aggregate([
  {$group: {_id: "$City", cityCount: {$sum: 1}}}
])
```

## 2. Sum of Salary

```bash
db.col.aggregate([
  {$group: {_id: "$City", totalSalary: {$sum: "$Salary"}}}
])
```

## 3. Average Salary

```bash
db.col.aggregate([
  {$group: {_id: "$City", avgSalary: {$avg: "$Salary"}}}
])
```

## 4. Minimum Salary

```bash
db.col.aggregate([
  {$group: {_id: "$City", minSalary: {$min: "$Salary"}}}
])
```

## 5. Maximum Salary

```bash
db.col.aggregate([
  {$group: {_id: "$City", maxSalary: {$max: "$Salary"}}}
])
```

## 6. First Salary

```bash
db.col.aggregate([
  {$group: {_id: "$City", firstSalary: {$first: "$Salary"}}}
])
```

## 7. Last Salary

```bash
db.col.aggregate([
  {$group: {_id: "$City", lastSalary: {$last: "$Salary"}}}
])
```

## 8. Push (Collect all salaries)

```bash
db.col.aggregate([
  {$group: {_id: "$City", salaries: {$push: "$Salary"}}}
])
```

## 9. addToSet (Unique salaries)

```bash
db.col.aggregate([
  {$group: {_id: "$City", uniqueSalaries: {$addToSet: "$Salary"}}}
])
```
