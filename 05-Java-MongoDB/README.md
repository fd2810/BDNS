# Practical 5 – Java and MongoDB

## Setup Steps (CLASSPATH)

### Step 1: Download MongoDB Java Driver
1. Download the MongoDB Java Driver (`.jar` files)
2. Keep all the `.jar` files in one folder  
   Example location:
   ```
   C:\Users\YourName\Downloads\mongodb-driver
   ```

### Step 2: Add JAR to CLASSPATH
1. Copy the full path of the folder that contains the `.jar` files
2. Search **Environment Variables** in Windows
3. Click **Edit the system environment variables**
4. Click **Environment Variables...**
5. Under **System variables**:
   - If **CLASSPATH** already exists → Select it → Click **Edit**
   - If it does **not** exist → Click **New**
6. Variable name: `CLASSPATH`
7. Variable value: paste the full path of the JAR folder  
   Example:
   ```
   C:\Users\YourName\Downloads\mongodb-driver\*
   ```
   (The `*` at the end includes all jar files inside the folder)
8. Click OK on all windows

### Step 3: Start MongoDB
1. Open Command Prompt and type:
   ```bash
   mongod
   ```
2. Open another Command Prompt and type:
   ```bash
   mongo
   ```
   (or `mongosh`)

### Step 4: Compile and Run Java programs
Open Command Prompt in the folder where your `.java` files are saved and type:

```bash
javac Insert.java
java Insert

javac Update.java
java Update

javac Retrieve.java
java Retrieve

javac Delete.java
java Delete
```

### Step 5: Verify in MongoDB
```bash
use TYITDB239720
db.myCol.find().pretty()
```

---

## Files included
- `Insert.java`   → Insert a document
- `Update.java`   → Update Age of a document
- `Retrieve.java` → Display all documents
- `Delete.java`   → Delete a document by id

## Note
If you get "package com.mongodb does not exist" error, it means CLASSPATH is not set correctly. Double-check Step 2.
