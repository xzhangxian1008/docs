---
title: SHOW DATABASES | TiDB SQL Statement Reference
summary: An overview of the usage of SHOW DATABASES for the TiDB database.
---

# SHOW DATABASES {#show-databases}

This statement shows a list of databases that the current user has privileges to. Databases which the current user does not have access to will appear hidden from the list. The `information_schema` database always appears first in the list of databases.

`SHOW SCHEMAS` is an alias of this statement.

## Synopsis {#synopsis}

**ShowDatabasesStmt:**

![ShowDatabasesStmt](/media/sqlgram/ShowDatabasesStmt.png)

**ShowLikeOrWhereOpt:**

![ShowLikeOrWhereOpt](/media/sqlgram/ShowLikeOrWhereOpt.png)

## Examples {#examples}

```sql
mysql> SHOW DATABASES;
+--------------------+
| Database           |
+--------------------+
| INFORMATION_SCHEMA |
| PERFORMANCE_SCHEMA |
| mysql              |
| test               |
+--------------------+
4 rows in set (0.00 sec)

mysql> CREATE DATABASE mynewdb;
Query OK, 0 rows affected (0.10 sec)

mysql> SHOW DATABASES;
+--------------------+
| Database           |
+--------------------+
| INFORMATION_SCHEMA |
| PERFORMANCE_SCHEMA |
| mynewdb            |
| mysql              |
| test               |
+--------------------+
5 rows in set (0.00 sec)
```

## MySQL compatibility {#mysql-compatibility}

The `SHOW DATABASES` statement in TiDB is fully compatible with MySQL. If you find any compatibility differences, [report a bug](https://docs.pingcap.com/tidb/stable/support).

## See also {#see-also}

-   [SHOW SCHEMAS](/sql-statements/sql-statement-show-schemas.md)
-   [DROP DATABASE](/sql-statements/sql-statement-drop-database.md)
-   [CREATE DATABASE](/sql-statements/sql-statement-create-database.md)
