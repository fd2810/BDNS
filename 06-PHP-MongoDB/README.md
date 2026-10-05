# Practical 6 – PHP and MongoDB

## Setup Steps (XAMPP)

1. Copy `php_mongo.dll` into `C:\xampp\php\ext`
2. Open `php.ini` and add / uncomment:
   ```
   extension=php_mongo.dll
   ```
3. Restart Apache from XAMPP Control Panel
4. Place all `.php` files inside `C:\xampp\htdocs\`
5. Open browser → `http://localhost/insert.php` (or respective file name)

## Files
- `insert.php`   – Insert document
- `update.php`   – Update document
- `retrieve.php` – Display documents
- `delete.php`   – Delete document
