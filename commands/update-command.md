# UPDATECOMMAND

## EXAMPLES:
```bash
UPDATE <table-name>
SET <colunm> = <new-value>
WHERE <condition>;
```
```sql
UPDATE secret_table
SET first_name = 'James'
WHERE user_id = 1;
```
```sql
UPDATE secret_table
SET code_name = 'Neo 2.0', salary = 115000
WHERE fisrt_name = 'Jack' AND last_name = 'Ryan';
```
```postgreSQL
UPDATE secret_table
SET salary = 115000
WHERE organization = 'MI6'
```
```sql
UPDATE secret_table
SET knows_kung_fu = TRUE
WHERE user_id IN (5,7,8);
```
```sql
UPDATE secret_table
SET salary = 1.1*salary;
```