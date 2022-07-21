# SQL Lite
Useful to store database on disk

```Python 
import sqlite3
```

### Creating a database
```Python 
conn = sqlite3.connect("database.db")
```

#### Running SQL Commands
**Creating a cursor**
```
c = conn.cursor()
```

 **Commands**
```Python 
c.execute("""
CREATE TABLE table(
	first integer
	second text
	third datetime
)
""")
```

**Commiting**
```Python
conn.commit()
```

**Closing**
```Python
conn.close()
```

#### Querys
```Python 
c.execute("SELECT * FROM table*")
```

**Viewing the query**
```Python
print(c.fetchone())
```
