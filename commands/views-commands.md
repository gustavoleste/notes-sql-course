# VIEWS COMMANDS

## EXAMPLES

```sql
CREATE VIEW view_name AS
SELECT colunm(s)
FROM table_name;
```
```sql
CREATE VIEW martian_public AS
SELECT martian_id, first_name, last_name, base_id, super_id
FROM martian_confidencial;
```
```sql
CREATE VIEW martian_public AS
SELECT martian_id, first_name, last_name, base_id, super_id
FROM martian_confidencial;
```
```sql
CREATE VIEW people_on_mars AS
SELECT CONCAT('m',martian_id) AS id, first_name, last_name, 'Martian' AS status
FROM martian_public
UNION
SELECT CONCAT('v',visitor_id) AS id, first_name, last_name, 'Visitor' AS status
FROM visitor;
```

```sql
CREATE VIEW base_storage AS
SELECT b.base_id, s.supply_id, s.name,
COALESCE(
	(SELECT quantity FROM inventory
	 WHERE base_id = b.base_id AND supply_id = s.supply_id),0)
	 AS quantity
FROM base AS b
CROSS JOIN supply AS s;
```