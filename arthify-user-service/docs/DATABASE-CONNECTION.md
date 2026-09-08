# Database Connection

Target: Windows MySQL80.

Host: localhost
Port: 3306
Database: usersdb
Username: root
Password: root

PowerShell:
```powershell
$env:DB_PASSWORD="your_mysql_password"
```

Verify in MySQL CLI:
```sql
USE usersdb;
SELECT COUNT(*) FROM arthifyusers;
SELECT COUNT(*) FROM arthifyaddresses;
```

Expected pagination dataset:
100 users and 100 addresses.

Never commit the database password.
