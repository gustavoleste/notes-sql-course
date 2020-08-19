# INDEX COMMAND

## EXAMPLES

```sql
CREATE INDEX index_name
ON table_name (colunm_name);
```
```sql
CREATE INDEX person_first_name_idx
ON person (first_name);
```

```sql
CREATE INDEX person_first_name_last_name_idx
ON person (last_name,first_name);
```