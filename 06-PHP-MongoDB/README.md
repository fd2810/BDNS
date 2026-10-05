# Practical 6 – PHP and MongoDB

## Setup Steps (XAMPP)

### Step 1: Download and Install XAMPP
1. Go to https://www.apachefriends.org/
2. Download the latest XAMPP for Windows
3. Install it (default location is `C:\xampp`)

### Step 2: Start Apache
1. Open **XAMPP Control Panel**
2. Click **Start** next to **Apache**
3. Make sure it turns green (running)

### Step 3: Enable MongoDB PHP Extension (Important)
1. Copy `php_mongo.dll` (or `php_mongodb.dll` for newer versions) into:
   ```
   C:\xampp\php\ext
   ```
2. Open `C:\xampp\php\php.ini` in Notepad
3. Find the line that says `;extension=php_mongo.dll` (or search for "mongo")
4. Remove the semicolon (`;`) so it becomes:
   ```
   extension=php_mongo.dll
   ```
5. Save the file and **restart Apache** from XAMPP Control Panel

### Step 4: Place your PHP files
1. Go to folder: `C:\xampp\htdocs`
2. Copy all your `.php` files here (`insert.php`, `update.php`, etc.)

### Step 5: Run the code
1. Open Chrome (or any browser)
2. Type in the address bar:
   ```
   http://localhost/insert.php
   ```
3. Press Enter
4. You will see the output on the browser

### Step 6: Verify in MongoDB
Open Mongo shell and type:
```bash
use MYDB239720
db.MyCol.find().pretty()
```

---

## Files included
- `insert.php`   → Insert a document
- `update.php`   → Update a document
- `retrieve.php` → Display all documents
- `delete.php`   → Delete a document
