# SQL Cheatsheet
###### Last updated Fall 2019

_Disclaimer: These are not official class notes. They're just meant to be a quick reference. Please let me know if there are any typos or mistakes._

### Creating a table

```sql
CREATE TABLE <name> AS
    SELECT <value> AS <name>, <value> AS <name> ... UNION
    SELECT <value>          , <value>           ... UNION
    ...;
```

### Simple Query

```sql
SELECT <column list>
FROM <table>;
```

### Full Query
```sql
SELECT <column list>
FROM <table list>
[WHERE] <condition> AND <condition> ...
[GROUP BY] <column list>
[HAVING] <condition> AND <condition> ...
[ORDER BY] <column> ASC/DESC, <column> ASC/DESC
[LIMIT] <amount>;
```
Notes: 

- `SELECT`: selects columns from a table, can give column name if use `AS`
- `FROM`: signals which tables to `SELECT` from
- `WHERE`: used to condition on `FROM`, combine conditions with `AND`
- `GROUP BY`: groups rows of the query on a col
- `HAVING`: is used to condition on `GROUP BY`
- `ORDER BY`: defaults to `ASC` (ascending), use `DESC` for descending


### SQL Strategy

```
FROM <table1> - which table(s) are we drawing from
WHERE <predicates> - keep only rows where <predicates> is satisfied
GROUP BY <column list> - group together rows by value of columns in <column list>
HAVING <predicates> - keep only groups having <predicates> satisfied
SELECT <column list> - select columns in <column list> to keep
ORDER BY <column list> [DESC/ASC] - order the output by value of the columns in <column list>
LIMIT <amount> - limit the output to the first <amount> rows
```

### Notes

- capitalization for keywords doesn't matter
- only need to alias tables that share column names
- joining two tables is like taking the cross product
- don't forget semicolons!

