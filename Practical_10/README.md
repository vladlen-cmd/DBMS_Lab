# Practical 10

## Aim
Create and perform database operations using ODBC.

## Steps (Theoretical Overview)

1. Install Oracle ODBC driver on your system.
2. Configure DSN (Data Source Name) using ODBC Data Source Administrator.
3. Connect your Oracle database using ODBC-compliant applications (e.g., MS Excel, Python pyodbc, C#, Java).
4. Perform database operations like SELECT, INSERT, UPDATE, DELETE from the external application.
5. Verify operations in Oracle DB.

## Example (Using Python pyodbc)

```python
import pyodbc
conn = pyodbc.connect('DSN=Your_DSN;UID=user;PWD=password')
cursor = conn.cursor()
cursor.execute('SELECT * FROM Customer')
for row in cursor:
    print(row)
conn.close()
