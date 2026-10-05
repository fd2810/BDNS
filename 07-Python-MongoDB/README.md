# Practical 7 – Python and MongoDB

## Setup Steps (Very Important)

### Step 1: Add Python to System PATH
1. Press `Windows key` and type `%localappdata%` → press Enter
2. Open the `Programs` folder → then open the `Python` folder (e.g. Python39 or Python311)
3. Copy the full path of the folder that contains `python.exe` and the `Scripts` folder  
   Example: `C:\Users\YourName\AppData\Local\Programs\Python\Python311`
4. Search **Environment Variables** in Windows search
5. Click **Edit the system environment variables**
6. Click **Environment Variables...**
7. Under **System variables**, select **Path** → click **Edit**
8. Click **New** and paste the Python folder path
9. Also add the Scripts folder path (same path + `\Scripts`)
10. Click OK on all windows

### Step 2: Install pymongo library
Open **Command Prompt (cmd)** and type:

```bash
pip install pymongo
```

### Step 3: Start MongoDB
1. Open one Command Prompt and type:
   ```bash
   mongod
   ```
2. Open a **second** Command Prompt and type:
   ```bash
   mongo
   ```
   (or `mongosh` if you have newer MongoDB)

Now MongoDB server and shell are running.

### Step 4: Run the Python code
1. Open **Python IDLE**
2. Create a new file and paste the code (insert / update / retrieve / delete)
3. Save the file as `.py`
4. Run the file (F5 or Run → Run Module)

### Step 5: Verify output
In the Mongo shell type:

```bash
use TYITDB239720
db.MyCol.find().pretty()
```

---

## How to run individual programs

```bash
python insert.py
python update.py
python retrieve.py
python delete.py
```

## Files included
- `insert.py`   → Insert a document (interactive)
- `update.py`   → Update age of a document
- `retrieve.py` → Display all documents
- `delete.py`   → Delete a document by name
