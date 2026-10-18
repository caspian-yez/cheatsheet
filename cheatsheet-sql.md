SQL
===

# find rows if "column name" is NULL

```sql
SELECT * FROM "table-name" WHERE "column name" IS NULL;     -- Will find rows with NULL value
SELECT * FROM "table-name" WHERE "column name"=NULL;        -- This do not work
```
