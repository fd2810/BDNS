# Practical 5 – Java and MongoDB

## Prerequisites
- MongoDB running on `localhost:27017`
- MongoDB Java Driver JAR in classpath

## How to compile & run

```bash
javac -cp "mongo-java-driver.jar;." Insert.java
java  -cp "mongo-java-driver.jar;." Insert

# Same for Update, Retrieve, Delete
```

## Files
- `Insert.java`  – Insert a document
- `Update.java`  – Update Age of a document
- `Retrieve.java` – Display all documents
- `Delete.java`  – Delete a document by id
