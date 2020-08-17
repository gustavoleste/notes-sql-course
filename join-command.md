# JOIN COMMAND

## EXAMPLES

```sql
SELECT colunm
FROM table_name
(INNER | RIGHT | LEFT | FULL) JOIN table_name
ON condition;
```

```sql
SELECT *
FROM martian
INNER JOIN base
ON martian.base_id = base.base_id
```
```sql
SELECT martian.martian_id, base.base_id, base.base_name
FROM martian
INNER JOIN base
ON martian.base_id = base.base_id;
```
```sql
SELECT m.martian_id, b.base_id, b.base_name
FROM martian AS m
INNER JOIN base AS b
ON m.base_id = b.base_id;
```